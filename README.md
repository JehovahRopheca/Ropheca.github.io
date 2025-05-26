mport React, { useState } from 'react';

export default function ScholarshipForm() {
  const [form, setForm] = useState({});

  const handleChange = (e) => {
    const { name, value, files } = e.target;
    setForm((prev) => ({
      ...prev,
      [name]: files ? files[0] : value,
    }));
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    console.log('Form Submitted', form);
  };

  return (
    <div className="max-w-4xl mx-auto p-6 shadow-xl rounded-2xl bg-white mt-10">
      <h1 className="text-2xl font-bold mb-6 text-center">Scholarship Application Form</h1>
      <form onSubmit={handleSubmit} className="grid grid-cols-1 md:grid-cols-2 gap-4">

        {[
          { label: 'Full Name', name: 'name' },
          { label: 'Date of Birth', name: 'dob', type: 'date' },
          { label: 'Age', name: 'age' },
          { label: "Father's Name", name: 'fatherName' },
          { label: "Mother's Name", name: 'motherName' },
          { label: 'Church Affiliation', name: 'church' },
          { label: 'Address', name: 'address' },
          { label: 'Subjects Taken in Class 12', name: 'subjects12' },
          { label: 'Marks in Class 10', name: 'marks10' },
          { label: 'Marks in Class 12', name: 'marks12' },
          { label: 'Course Selected', name: 'course' },
          { label: 'Duration of Education (years)', name: 'years' },
          { label: 'Admission Fee (INR)', name: 'admissionFee' },
          { label: 'Total Tuition Fee (INR)', name: 'tuitionFee' }
        ].map(({ label, name, type = 'text' }) => (
          <div key={name}>
            <label className="block font-semibold mb-1">{label}</label>
            <input
              type={type}
              name={name}
              className="w-full border p-2 rounded"
              onChange={handleChange}
              required
            />
          </div>
        ))}

        <div className="md:col-span-2">
          <label className="block font-semibold mb-1">Upload 10th Marksheet</label>
          <input type="file" name="marksheet10" onChange={handleChange} required />
        </div>

        <div className="md:col-span-2">
          <label className="block font-semibold mb-1">Upload 12th Marksheet</label>
          <input type="file" name="marksheet12" onChange={handleChange} required />
        </div>

        <div className="md:col-span-2">
          <label className="block font-semibold mb-1">Church Membership Certificate</label>
          <input type="file" name="churchCert" onChange={handleChange} required />
        </div>

        <div className="md:col-span-2">
          <label className="block font-semibold mb-1">Aadhar Card</label>
          <input type="file" name="aadhar" onChange={handleChange} required />
        </div>

        <div className="md:col-span-2">
          <label className="block font-semibold mb-1">Death Certificate (if applicable)</label>
          <input type="file" name="deathCert" onChange={handleChange} />
        </div>

        <div className="md:col-span-2">
          <label className="block font-semibold mb-1">Income Certificate</label>
          <input type="file" name="incomeCert" onChange={handleChange} required />
        </div>

        <div className="md:col-span-2 text-center mt-6">
          <button type="submit" className="bg-blue-600 text-white px-6 py-2 rounded hover:bg-blue-700">
            Submit Application
          </button>
        </div>
      </form>
    </div>
  );
}
