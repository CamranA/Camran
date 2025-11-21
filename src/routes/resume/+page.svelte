<script lang="ts">
    import { Briefcase, MapPin, Calendar } from "@lucide/svelte";

    const jobs = [
        {
            company: "GM Financial",
            role: "Software Development Engineer III",
            duration: "Mar 2023 - Present",
            location: "Oregon Area, Remote",
            description: [
                "MyAccount application development engineer for gmfinancial.com and cadillacfinancial.com using Java, JavaScript, and AEM.",
                "MyAccount development lead for migration from AEM 6.3 to AEM Cloud",
                "Developed and implemented cadillacfinancial.ca",
            ],
            skills: [
                "Java",
                "JavaScript",
                "Git",
                "Azure DevOps",
                "HTML",
                "Adobe Experience Manager (AEM)",
                "AEM Cloud",
                "AEM Sites",
                "Maven",
                "npm",
                "Agile",
                "VS Code",
                "CSS",
                "JSON",
                "jQuery",
                "Databases",
                "Version Control",
                "Microsoft Office",
                "XML",
            ],
        },
        {
            company: "Accenture",
            role: "AEM Developer",
            duration: "May 2021 - Mar 2023",
            location: "Phoenix, Arizona Area",
            description: [
                "Development of a company public facing website using Agile Scrum methodology (Java/Javascript/AEM Sites/Git).",
                "Lead Developer for Adobe Experience Manager 6.5 Forms/Site implementation (Java/Javascript/AEM Sites/AEM Forms/Git/J2EE).",
            ],
            skills: [
                "Agile",
                "VS Code",
                "JavaScript",
                "JSON",
                "HTML",
                "Databases",
                "Azure DevOps",
                "Java",
                "Git",
                "Microsoft Office",
                "Version Control",
                "XML",
                "Adobe Experience Manager (AEM)",
                "AEM Cloud",
                "AEM Sites",
                "Maven",
                "jQuery",
                "SQL",
                "MS SQL Server",
            ],
        },
        {
            company: "Boeing",
            role: "Software Developer - Information Science",
            duration: "Jul 2019 - May 2021",
            location: "Phoenix, Arizona Area",
            description: [
                "Develop and maintain front-end web applications and server side applications for Boeing Corporate Library. (JavaScript/Java/Python)",
                "Provided leadership as Subject Matter Expert(SME) for migration from Adobe LiveCycle ES2 (J2EE) to Adobe Experience Manager Forms 6.4(JBoss/Windows Server/J2EE).",
            ],
            skills: [
                "Documentation",
                "VS Code",
                "JavaScript",
                "JSON",
                "HTML",
                "Python",
                "Databases",
                "Java",
                "Git",
                "Microsoft Office",
                "Version Control",
                "Excel",
                "XML",
                "AEM",
                "jQuery",
                "SQL",
                "MS SQL Server",
            ],
        },
        {
            company: "Boeing",
            role: "Forms Developer",
            duration: "Feb 2018 - Jul 2019",
            location: "Phoenix, Arizona Area",
            description: [
                "Develop information systems with business partners to retrieve and distribute data across the organization using JavaScript, Adobe LiveCycle Designer, Adobe LiveCycle Workbench, and SQL server databases.",
                "Create official company forms using Adobe LiveCycle Designer ES4, gathering business process requirements from customers and business partners across the Boeing Company.",
            ],
            skills: [
                "Documentation",
                "VS Code",
                "JavaScript",
                "JSON",
                "HTML",
                "Python",
                "Databases",
                "Microsoft Office",
                "Version Control",
                "Excel",
                "XML",
                "AEM",
                "jQuery",
                "SQL",
                "MS SQL Server",
            ],
        },
        {
            company: "Daimler Trucks North America",
            role: "Product Data Analyst II - Marketing Strategy",
            duration: "Oct 2015 - Oct 2016",
            location: "Portland, Oregon Area",
            description: [
                "Create Python/VBA scripts to interact with FPX Product Data Manager database and an IBM mainframe.",
                "Analyze and perform QA on weekly releases to all Freightliner/Western Star dealers using SpecPro 21 application.",
                "Maintain and update SpecPro 21 freight truck ordering application, and FPX Product Data Manager database.",
            ],
            skills: [
                "Documentation",
                "Python",
                "VBA",
                "Databases",
                "Data Analysis",
                "Microsoft Office",
                "Excel",
                "XML",
                "Visual Basic",
            ],
        },
        {
            company: "Daimler Trucks North America",
            role: "Engineering Analyst I - Engineering Operations and Systems",
            duration: "Aug 2014 - Oct 2015",
            location: "Portland, Oregon Area",
            description: [
                "Create applications and scripts using VB.NET/Python/VBA for process improvement, increasing workflow efficiency, and updating compatibility database.",
                "Audit freight truck production build schedules.",
                "Develop, maintain, and review engineering design data.",
                "Review and analyze all new and revised sales data codes for impact on database.",
                "Construct and revise compatibility rules to ensure proper truck build generation, for current product and engineering projects.",
                "Create and improve Documentation/Standard Operating Procedures",
            ],
            skills: [
                "Documentation",
                "Python",
                "VBA",
                "Databases",
                "Data Analysis",
                "Visual Studio",
                "Microsoft Office",
                "Excel",
                "Visual Basic",
            ],
        },
        {
            company: "Boeing Commercial Airplanes",
            role: "Chemical Process Management Intern",
            duration: "Jun 2011 - Jan 2012",
            location: "Portland, Oregon Area",
            description: [
                "Designed and carried out testing procedures for RO water implementation for current plating shop processes to be used in new state of the art plating shop.",
                "Reviewed P&IDs for all plating shop baths and designed database for all current alarms including maintenance frequency and all process set points within plating shops.",
                "Worked with shop personnel to test and ensure all alarms were working properly and were receiving scheduled maintenance.",
                "Assisted in safety review of all plating shop equipment including pumps, piping, chemical baths, safety systems, and detectors.",
                "Performed emissions analysis to determine the primary source of hexavalent chrome emissions for plating shop baths.",
            ],
            skills: [],
        },
    ];
</script>

<section class="max-w-4xl mx-auto my-12 px-4">
    <h1
        class="text-4xl font-black tracking-tight mb-12 text-center bg-clip-text text-transparent bg-gradient-to-r from-gray-900 to-gray-600 dark:from-white dark:to-gray-400"
    >
        Professional Experience
    </h1>

    <div class="space-y-12">
        {#each jobs as job}
            <div
                class="relative pl-8 border-l-2 border-gray-200 dark:border-gray-800"
            >
                <!-- Timeline Dot -->
                <div
                    class="absolute -left-[9px] top-0 w-4 h-4 rounded-full bg-blue-600 dark:bg-blue-500 ring-4 ring-white dark:ring-gray-950"
                ></div>

                <div
                    class="flex flex-col sm:flex-row sm:items-start sm:justify-between mb-2"
                >
                    <div>
                        <h2
                            class="text-2xl font-bold text-gray-900 dark:text-white"
                        >
                            {job.role}
                        </h2>
                        <div
                            class="flex items-center gap-2 text-lg font-medium text-blue-600 dark:text-blue-400 mt-1"
                        >
                            <Briefcase class="w-4 h-4" />
                            {job.company}
                        </div>
                    </div>
                    <div
                        class="flex flex-col sm:items-start mt-2 sm:mt-0 text-sm text-gray-500 dark:text-gray-400"
                    >
                        <div class="flex items-center gap-1.5">
                            <Calendar class="w-4 h-4" />
                            {job.duration}
                        </div>
                        <div class="flex items-center gap-1.5 mt-1">
                            <MapPin class="w-4 h-4" />
                            {job.location}
                        </div>
                    </div>
                </div>

                {#if job.description.length > 0}
                    <ul
                        class="mt-4 space-y-2 text-gray-600 dark:text-gray-300 list-disc list-outside ml-4"
                    >
                        {#each job.description as desc}
                            <li class="leading-relaxed">{desc}</li>
                        {/each}
                    </ul>
                {/if}

                {#if job.skills.length > 0}
                    <div class="mt-6 flex flex-wrap gap-2">
                        {#each job.skills as skill}
                            <span
                                class="px-2.5 py-0.5 text-xs font-medium rounded-full bg-gray-100 text-gray-800 dark:bg-gray-800 dark:text-gray-200 border border-gray-200 dark:border-gray-700"
                            >
                                {skill}
                            </span>
                        {/each}
                    </div>
                {/if}
            </div>
        {/each}
    </div>
</section>
