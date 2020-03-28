<template>
  <div>
    <Header title="Clients" :logo="logo"/>

    <div class="container">
      <div v-for="(client) in server.PipelineContactList" v-bind:key="client.id">
        <b-card no-body class="mb-1" header-tag="header" align="left">
          <b-card-header class="p-1" role="tab" align="left">
            <b-button block href="#" align="left" variant="outline-default">
              <i class="fe fe-help-circle mr-2" />
              <span v-html="client.FirstName" />
              <span class="ml-1" v-html="client.LastName" />
            </b-button>
          </b-card-header>
        </b-card>
      </div>
    </div>
  </div>
</template>

<script>

import Header from './Header.vue';

export default {
  name: "Clients",
  props: {
    logo: String
  },
  components:{
      Header
  },
  data: function() {
    return {
      server: {
        PipelineContactList: [
          {
            ClientCity: "",
            ClientProvince: "",
            CompanyName: "",
            ContactGuid: "b1b16c8e-8520-4141-aee0-3ea7d5bfc257",
            ContactStatus: "Inactive",
            ContactStatusColor: "#EE2D24",
            DisplayName: "Test1ttttt Test2",
            FirstName: "Test1ttttt",
            IllustrationRequested: true,
            IllustrationUpdateId: null,
            LastName: "Test2",
            PrimaryEmailAddress: "testing@gmail.com",
            PrimaryPhoneNumber: "4164564567",
            Guid: "383aaabe-36cb-49a5-af1d-8e3949c74044",
            Id: 209898,
            SecurityPermissions: null,
            TimeZone: null
          }
        ],
        PipelineContactStatuss: ["Inactive"],
        DisplayName: "Techlicity",
        DistributorContactsContent: null,
        DistributorPortal: "Techlicity",
        DistributorPortalId: 153,
        EnrolmentOverviewContent: null,
        IntegrisContactsContent: null,
        LandingView: "Techlicity",
        LandingViewTitle: "Techlicity",
        LanguageAbbreviation: null,
        LanguageId: 0,
        LanguageName: null,
        LanguageNativeName: null,
        PrimaryProductPlatform: null,
        ProductPlatforms: null,
        ResourceLibraryContent: null,
        ResourceLibraryContentCategorys: null,
        ResourceLibraryContentList: null,
        UserEmailAddress: "farooq.kaiser@gmail.com",
        UserFullName: "Kaiser, Farooq",
        UserId: 2068,
        WelcomeContent: null,
        Guid: "7d46e6bd-1838-4f3e-865f-26ddbdbfd5b0",
        Id: 153,
        SecurityPermissions: null,
        TimeZone: null
      }
    };
  }
};
</script>