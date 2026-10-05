<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">

<title>Pharm.D (PB) R17 Marks Memo</title>

<style>

    @page {
        size: A4 portrait;
        margin: 12mm;
    }

    * {
        box-sizing: border-box;
    }

    body {
        margin: 0;
        padding: 0;
        font-family: "Times New Roman", serif;
        font-size: 11px;
        color: #000;
        background: #fff;
    }

    .memo {
        width: 100%;
        max-width: 190mm;
        margin: auto;
    }

    /* HEADER */

    .college-header {
        text-align: center;
        margin-bottom: 5px;
    }

    .college-name {
        font-size: 18px;
        font-weight: bold;
        text-transform: uppercase;
    }

    .college-address {
        font-size: 11px;
        margin-top: 2px;
    }

    .memo-title {
        text-align: center;
        font-size: 15px;
        font-weight: bold;
        margin: 8px 0;
        text-transform: uppercase;
    }

    /* STUDENT DETAILS */

    .details-table {
        width: 100%;
        border-collapse: collapse;
        margin-bottom: 8px;
    }

    .details-table td {
        padding: 3px 5px;
        vertical-align: middle;
    }

    .label {
        font-weight: bold;
        width: 17%;
    }

    .value {
        width: 33%;
    }

    /* MARKS TABLE */

    .marks-table {
        width: 100%;
        border-collapse: collapse;
        table-layout: fixed;
    }

    .marks-table th,
    .marks-table td {
        border: 1px solid #000;
        padding: 4px 3px;
        text-align: center;
        vertical-align: middle;
    }

    .marks-table th {
        font-weight: bold;
    }

    .marks-table .slno {
        width: 6%;
    }

    .marks-table .code {
        width: 14%;
    }

    .marks-table .subject {
        width: 35%;
        text-align: left;
    }

    .marks-table .marks {
        width: 9%;
    }

    .marks-table .result {
        width: 10%;
    }

    .subject-name {
        text-align: left !important;
    }

    /* TOTAL */

    .total-row {
        font-weight: bold;
    }

    .summary {
        margin-top: 5px;
        width: 100%;
        border-collapse: collapse;
    }

    .summary td {
        padding: 3px 5px;
    }

    .summary-label {
        font-weight: bold;
    }

    /* SIGNATURE */

    .signature-table {
        width: 100%;
        margin-top: 25px;
        border-collapse: collapse;
    }

    .signature-table td {
        text-align: center;
        width: 50%;
        padding-top: 25px;
        font-weight: bold;
    }

    /* INSTRUCTIONS */

    .instructions-title {
        margin-top: 15px;
        font-weight: bold;
        text-decoration: underline;
    }

    .instruction-table {
        width: 100%;
        border-collapse: collapse;
        margin-top: 4px;
    }

    .instruction-table th,
    .instruction-table td {
        border: 1px solid #000;
        padding: 4px;
        text-align: center;
    }

    .instruction-table th:first-child {
        text-align: left;
        width: 40%;
    }

    .note {
        margin-top: 6px;
        font-size: 10px;
    }

    /* PRINT */

    @media print {

        body {
            background: white;
        }

        .memo {
            width: 100%;
        }

        .no-print {
            display: none !important;
        }
    }

</style>
</head>

<body>

<div class="memo">

    <!-- COLLEGE HEADER -->

    <div class="college-header">

        <div class="college-name">
            SRI VENKATESWARA COLLEGE OF PHARMACY
        </div>

        <div class="college-address">
            RVS Nagar, Chittoor, Andhra Pradesh
        </div>

    </div>

    <div class="memo-title">
        MARKS MEMO
    </div>


    <!-- EXAMINATION / STUDENT DETAILS -->

    <table class="details-table">

        <tr>
            <td class="label">Memo No:</td>
            <td class="value" id="memoNo"></td>

            <td class="label">Sl.No:</td>
            <td class="value" id="slNo"></td>
        </tr>

        <tr>
            <td class="label">Examination:</td>
            <td colspan="3" id="examination">
                I-YEAR (R17) REGULAR EXAMINATIONS
            </td>
        </tr>

        <tr>
            <td class="label">Branch:</td>
            <td id="branch">
                POST BACCALAUREATE
            </td>

            <td class="label">Hallticket No:</td>
            <td id="hallticket">
                SACM029147
            </td>
        </tr>

        <tr>
            <td class="label">Month & Year of Exam:</td>
            <td id="examMonth">
                September 2024
            </td>

            <td class="label">Name:</td>
            <td id="studentName">
                K CHETHAN SIVA SAI
            </td>
        </tr>

    </table>


    <!-- MARKS TABLE -->

    <table class="marks-table">

        <thead>

            <tr>
                <th class="slno">Sl.<br>No.</th>
                <th class="code">Subject<br>Code</th>
                <th class="subject">Subject Title</th>
                <th class="marks">Internal</th>
                <th class="marks">External</th>
                <th class="marks">Total</th>
                <th class="result">Result</th>
            </tr>

        </thead>

        <tbody id="marksBody">
        </tbody>

        <tfoot>

            <tr class="total-row">

                <td colspan="3">
                    Subjects Registered:
                    <span id="registered">0</span>
                    &nbsp;&nbsp;

                    Appeared:
                    <span id="appeared">0</span>
                    &nbsp;&nbsp;

                    Passed:
                    <span id="passed">0</span>
                </td>

                <td id="internalTotal">0</td>
                <td id="externalTotal">0</td>
                <td id="grandTotal">0</td>
                <td></td>

            </tr>

        </tfoot>

    </table>


    <!-- DATE -->

    <table class="summary">

        <tr>
            <td>
                <span class="summary-label">Date:</span>
                <span id="date">13-12-2024</span>
            </td>
        </tr>

    </table>


    <!-- SIGNATURES -->

    <table class="signature-table">

        <tr>

            <td>
                Controller of Examination
            </td>

            <td>
                Principal
            </td>

        </tr>

    </table>


    <!-- INSTRUCTIONS -->

    <div class="instructions-title">
        INSTRUCTIONS:
    </div>


    <table class="instruction-table">

        <thead>

            <tr>

                <th>Subject Type</th>

                <th colspan="3">
                    MAXIMUM MARKS
                </th>

                <th colspan="2">
                    MINIMUM MARKS FOR PASS
                </th>

            </tr>

            <tr>

                <th></th>

                <th>Internal</th>
                <th>End Exam</th>
                <th>Total of Int. & End</th>

                <th>End Exam</th>
                <th>Total of Int. & End</th>

            </tr>

        </thead>

        <tbody>

            <tr>

                <td>THEORY SUBJECTS</td>

                <td>30</td>
                <td>70</td>
                <td>100</td>
                <td>-</td>
                <td>50</td>

            </tr>

            <tr>

                <td>PRACTICAL SUBJECTS</td>

                <td>30</td>
                <td>70</td>
                <td>100</td>
                <td>-</td>
                <td>50</td>

            </tr>

            <tr>

                <td>PROJECT</td>

                <td>--</td>
                <td>100</td>
                <td>100</td>
                <td>--</td>
                <td>50</td>

            </tr>

        </tbody>

    </table>


    <div class="note">
        <b>Note:</b>
        P: PASS &nbsp;&nbsp;
        F: FAIL &nbsp;&nbsp;
        AB: ABSENT &nbsp;&nbsp;
        MP: MALPRACTICE
    </div>

</div>


<script>

/*
==========================================================
STUDENT INFORMATION
==========================================================
*/

const student = {

    memoNo: "SVCOP/R17/2024/001",

    slNo: "01",

    examination:
        "I-YEAR (R17) REGULAR EXAMINATIONS",

    branch:
        "POST BACCALAUREATE",

    hallticket:
        "SACM029147",

    examMonth:
        "September 2024",

    studentName:
        "K CHETHAN SIVA SAI",

    date:
        "13-12-2024"

};


/*
==========================================================
SUBJECT DATA
==========================================================
*/

const subjects = [

    {
        code: "17T00401",
        title: "Pharmacotherapeutics-III",
        internal: 23,
        external: 30
    },

    {
        code: "17T00402",
        title: "Hospital Pharmacy",
        internal: 25,
        external: 21
    },

    {
        code: "17T00403",
        title: "Clinical Pharmacy",
        internal: 24,
        external: 37
    },

    {
        code: "17T00404",
        title: "Biostatistics & Research Methodology",
        internal: 25,
        external: 35
    },

    {
        code: "17T00405",
        title: "Biopharmaceutics & Pharmacokinetics",
        internal: 24,
        external: 41
    },

    {
        code: "17T00406",
        title: "Clinical Toxicology",
        internal: 21,
        external: 40
    },

    {
        code: "17T00407",
        title: "Pharmacotherapeutics I Lab",
        internal: 25,
        external: 61
    },

    {
        code: "17T00408",
        title: "Hospital Pharmacy Lab",
        internal: 24,
        external: 54
    },

    {
        code: "17T00409",
        title: "Clinical Pharmacy Lab",
        internal: 24,
        external: 51
    },

    {
        code: "17T00410",
        title: "Biopharmaceutics & Pharmacokinetics Lab",
        internal: 25,
        external: 54
    },

    {
        code: "17T00411",
        title: "Pharmacotherapeutics I & II",
        internal: 25,
        external: 13
    },

    {
        code: "17T00412",
        title: "Pharmacotherapeutics I & II Lab",
        internal: 24,
        external: 55
    }

];


/*
==========================================================
LOAD STUDENT INFORMATION
==========================================================
*/

document.getElementById("memoNo").textContent =
    student.memoNo;

document.getElementById("slNo").textContent =
    student.slNo;

document.getElementById("examination").textContent =
    student.examination;

document.getElementById("branch").textContent =
    student.branch;

document.getElementById("hallticket").textContent =
    student.hallticket;

document.getElementById("examMonth").textContent =
    student.examMonth;

document.getElementById("studentName").textContent =
    student.studentName;

document.getElementById("date").textContent =
    student.date;


/*
==========================================================
GENERATE SUBJECT TABLE
==========================================================
*/

const marksBody =
    document.getElementById("marksBody");

let internalTotal = 0;
let externalTotal = 0;
let grandTotal = 0;

let passed = 0;
let appeared = 0;


/*
PASSING RULE USED IN THE UPLOADED MEMO:

TOTAL >= 50 = PASS
TOTAL < 50  = FAIL

This follows the instruction table in the source memo.
*/

subjects.forEach((subject, index) => {

    const total =
        subject.internal + subject.external;

    let result;

    if (
        subject.internal === null ||
        subject.external === null
    ) {

        result = "AB";

    } else if (total >= 50) {

        result = "Pass";
        passed++;

    } else {

        result = "Fail";

    }

    appeared++;

    internalTotal += subject.internal || 0;
    externalTotal += subject.external || 0;
    grandTotal += total || 0;


    const row =
        document.createElement("tr");

    row.innerHTML = `

        <td>${index + 1}</td>

        <td>${subject.code}</td>

        <td class="subject-name">
            ${subject.title}
        </td>

        <td>${subject.internal}</td>

        <td>${subject.external}</td>

        <td>${total}</td>

        <td>${result}</td>

    `;

    marksBody.appendChild(row);

});


/*
==========================================================
DISPLAY TOTALS
==========================================================
*/

document.getElementById("registered").textContent =
    subjects.length;

document.getElementById("appeared").textContent =
    appeared;

document.getElementById("passed").textContent =
    passed;

document.getElementById("internalTotal").textContent =
    internalTotal;

document.getElementById("externalTotal").textContent =
    externalTotal;

document.getElementById("grandTotal").textContent =
    grandTotal;

</script>

</body>
</html>
