<template>
    <div class="relative z-20 overflow-auto w-[300px] p-4 bg-gray-800 shadow">
        <MenuItem link="/" :subItems="menu.dashboard" class="mb-2">
            <IconChartBar class="w-5 h-5 mr-2" />
            Dashboard
        </MenuItem>

        <MenuItem link="/empresas" :subItems="menu.companies" class="mb-2">
            <IconOfficeBuilding class="w-5 h-5 mr-2" />
            Empresas
        </MenuItem>

        <MenuItem link="/relatorios" :subItems="menu.reports">
            <IconDocumentReport class="w-5 h-5 mr-2" />
            Relatórios
        </MenuItem>
    </div>
</template>

<script>
import MenuItem from "@/Shared/Components/MenuItem";

import IconChartBar from "@/Shared/Icons/ChartBar";
import IconOfficeBuilding from "@/Shared/Icons/OfficeBuilding";
import IconDocumentReport from "@/Shared/Icons/DocumentReport";

export default {
    components: {
        MenuItem,
        IconChartBar,
        IconOfficeBuilding,
        IconDocumentReport,
    },

    data() {
        return {
            menu: {
                dashboard: [],
                companies: [
                    {
                        title: "Grupos",
                        link: "/grupos",
                    },
                    {
                        title: "Classificações",
                        link: "/classificacoes",
                    },
                    {
                        title: "Listar Empresas",
                        link: "/empresas",
                    },
                ],
                reports: [
                    {
                        title: "Empresas",
                        link: "/relatorios/empresas",
                    },
                    {
                        title: "Contatos",
                        link: "/relatorios/contatos",
                    },
                ],
            },
        };
    },
};
</script>
