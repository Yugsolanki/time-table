<script>
    import { onMount } from 'svelte';

    onMount(() => {
        let tableData = document.querySelectorAll('td:not(.prac');
        tableData.forEach((td, index) => {
            if (td.textContent.includes('/')) {
                let data = td.textContent.split('/');
                td.innerHTML = `<span class="theory">${data[0]}</span><br><span class="prac">/${data[1]}</span>`;
            }
        })

        let tableDataPrac = document.querySelectorAll('td.prac div div');
        tableDataPrac.forEach((td, index) => {
            let data = td.textContent.split('/');
            td.innerHTML = `${data[0]}<br>${data[1]}<br>/${data[2]}`;
        })
    })

    const header = ['Period No.', 'Time', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday'];
    const teachers = [
        {
            initials: "SB",
            name: "Sonali Bhutad",
            email: "sonali.bhutad@sakec.ac.in",
            subjectInitials: "SE",
            subject: "Software Engineering"
        },
        {
            initials: "VK",
            name: "Vaishali Kosamkar",
            email: "vaishali.kosamkar@sakec.ac.in",
            subjectInitials: "SE",
            subject: "Software Engineering"
        },
        {
            initials: "DP",
            name: "Deepti Pawar",
            email: "deepti.pawar@sakec.ac.in",
            subjectInitials: "SE",
            subject: "Software Engineering"
        },
        {
            initials: "SK",
            name: "Shipla Kalantri",
            email: "shilpa.kalantri@sakec.ac.in",
            subjectInitials: "CN",
            subject: "Computer Networks"
        },
        {
            initials: "AD",
            name: "Amol Dhumal",
            email: "amol.dhumal@sakec.ac.in",
            subjectInitials: "CN",
            subject: "Computer Networks"
        },
        {
            initials: "SSB",
            name: "Satish Bangla",
            email: "satish.bangal@sakec.ac.in",
            subjectInitials: "CN",
            subject: "Computer Networks"
        },
        {
            initials: "PV",
            name: "Pinki Vishwakarma",
            email: "pinki.vishwakarma@sakec.ac.in",
            subjectInitials: "DWM",
            subject: "Data Warehousing and Mining"
        },
        {
            initials: "TH",
            name: "Tejas Hirave",
            email: "tejas.hirve@sakec.ac.in",
            subjectInitials: "DWM",
            subject: "Data Warehousing and Mining"
        },
        {
            initials: "DPR",
            name: "divya Pritam",
            email: "divya.pritam@sakec.ac.in",
            subjectInitials: "DWM",
            subject: "Data Warehousing and Mining"
        },
        {
            initials: "GS",
            name: "Sharmila G.",
            email: "sharmila.gundapuneri@sakec.ac.in",
            subjectInitials: "PCE",
            subject: "Principles of Communication Engineering"
        },
        {
            initials: "SP",
            name: "Sanjay Patil",
            email: "sanjay.patil@sakec.ac.in",
            subjectInitials: "PCE",
            subject: "Principles of Communication Engineering"
        },
        {
            initials: "JSM",
            name: "Jagat Manral",
            email: "jagat.manral@sakec.ac.in",
            subjectInitials: "PCE",
            subject: "Principles of Communication Engineering"
        },
        {
            initials: "AJ",
            name: "Ajay Jaiswar",
            email: "ajay.jaiswar@sakec.ac.in",
            subjectInitials: "PCE",
            subject: "Principles of Communication Engineering"
        },
        {
            initials: "SSY",
            name: "Shahzia Sayyad",
            email: "shahzia.sayyad@sakec.ac.in",
            subjectInitials: "TCS",
            subject: "Theoretical Computer Science"
        },
        {
            initials: "PG",
            name: "Priyanka Ghule",
            email: "priyanka.ghule@sakec.ac.in",
            subjectInitials: "TCS",
            subject: "Theoretical Computer Science"
        },
        {
            initials: "VC",
            name: "Vaishali Chavan",
            email: "vaishali.chavan@sakec.ac.in",
            subjectInitials: "IP",
            subject: "Internet Programming"
        },
        {
            initials: "KB",
            name: "Karuna Borhade",
            email: "karuna.borhade@sakec.ac.in",
            subjectInitials: "IP",
            subject: "Internet Programming"
        },
        {
            initials: "MM",
            name: "Manimala Mahato",
            email: "manimala.mahato@sakec.ac.in",
            subjectInitials: "PGM",
            subject: "Probabilistic Graphical Models"
        },
        {
            initials: "PG",
            name: "Priyanka Ghule",
            email: "priyanka.ghule@sakec.ac.in",
            subjectInitials: "PGM",
            subject: "Probabilistic Graphical Models"
        }
    ]

</script>

<table>
    <thead>
        <tr>
            {#each header as column}
                <th>{column}</th>
            {/each}
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>09:15 - 10:15</td>
            <td>-</td>
            <td>Honours/VVH</td>
            <td>-</td>
            <td>-</td>
            <td>-</td>
        </tr>
        <tr>
            <td>2</td>
            <td>10:15 - 11:15</td>
            <td>CN/SK</td>
            <td>Honours/VVH</td>
            <td rowspan="2" class="prac">
                <div>
                    <div>A/SE/SB</div>
                    <div>B/CN/SSB</div>
                    <div>C/DWM/TH</div>
                    <div>D/PCE/JSM</div>
                </div>
            </td>
            <td>SE/VK</td>
            <td>DWM/PV</td>
        </tr>

        <tr>
            <td>3</td>
            <td>11:15 - 12:15</td>
            <td>CN/SK</td>
            <td>PCE/JSM</td>
            <td>SE/VK</td>
            <td>DWM/PV</td>
        </tr>

        <tr>
            <td>4</td>
            <td>12:15 - 01:00</td>
            <td colspan="5" class="break">Break</td>
        </tr>

        <tr>
            <td>5</td>
            <td>01:00 - 02:00</td>
            <td rowspan="2" class="prac">
                <div>
                    <div>A/DWM/DPR</div>
                    <div>B/PCE/SP</div>
                    <div>C/SE/DP</div>
                    <div>D/CN/AD</div>
                </div>
            </td>
            <td>PGM/MM</td>
            <td>TCS/SSY</td>
            <td>DWM/TH</td>
            <td rowspan="2" class="prac">
                <div>
                    <div>A/CN/SSB</div>
                    <div>B/DWM/TH</div>
                    <div>C/PCE/GS</div>
                    <div>D/SE/DP</div>
                </div>
            </td>
        </tr>

        <tr>
            <td>6</td>
            <td>02:00 - 03:00</td>
            <td>PGM/MM</td>
            <td>TCS/SSY</td>
            <td>CN/SSB</td>
        </tr>

        <tr>
            <td>7</td>
            <td>03:00 - 04:00</td>
            <td>SE/SB</td>
            <td rowspan="2" class="prac">
                <div>
                    <div>A/PCE/AJ</div>
                    <div>B/SE/VK</div>
                    <div>C/CN/AD</div>
                    <div>D/DWM/DPR</div>
                </div>
            </td>
            <td>PGM</td>
            <td>Honours</td>
            <td>PCE</td>
        </tr>

        <tr>
            <td>8</td>
            <td>04:00 - 05:00</td>
            <td>-</td>
            <td>Mini Project</td>
            <td>Honours</td>
            <td>TCS</td>
    </tbody>
</table>

<div class="teachers-container">
    <div>
        <div>SE - Software Engineering</div>
        {#each teachers as teacher}
            {#if teacher.subjectInitials == "SE"}
                <div>{teacher.initials} - {teacher.name}</div>
            {/if}
        {/each}
    </div>
    <div>
        <div>CN - Computer Networks</div>
        {#each teachers as teacher}
            {#if teacher.subjectInitials == "CN"}
                <div>{teacher.initials} - {teacher.name}</div>
            {/if}
        {/each}
    </div>
    <div>
        <div>DWM - Data Warehousing and Mining</div>
        {#each teachers as teacher}
            {#if teacher.subjectInitials == "DWM"}
                <div>{teacher.initials} - {teacher.name}</div>
            {/if}
        {/each}
    </div>
    <div>
        <div>PCE </div>
        {#each teachers as teacher}
            {#if teacher.subjectInitials == "PCE"}
                <div>{teacher.initials} - {teacher.name}</div>
            {/if}
        {/each}
    </div>
    <div>
        <div>TCS - Theoretical Computer Science</div>
        {#each teachers as teacher}
            {#if teacher.subjectInitials == "TCS"}
                <div>{teacher.initials} - {teacher.name}</div>
            {/if}
        {/each}
    </div>
    <div>
        <div>PGM - Probabilistic Graphical Models</div>
        {#each teachers as teacher}
            {#if teacher.subjectInitials == "PGM"}
                <div>{teacher.initials} - {teacher.name}</div>
            {/if}
        {/each}
    </div>
</div>