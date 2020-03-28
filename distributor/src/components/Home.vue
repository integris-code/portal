<template>
  <div class="main-content">
    <Header
      :logo="logo"
    >Welcome to the INTEGRIS Distributor Portal. Here is where you can get PPP Illustration quotes for your clients and prospects,marketing materials, brochures, fact sheets, Compliance Manuals,and other documents to help you understand and market the PPP.If you have any questions, or should you have any suggestions asto how we can improve on the information provided here, pleasedo not hesitate to contact your representatives or email us atquestion@integris-mgt.com.</Header>

    <div>
      <!-- CONTENT -->
      <div class="container">
        <div class="row mt-n7">
          <div class="col-12 col-lg-6">
            <!-- Card -->

            <div class="card">
              <div class="card-header bg-light">Forms</div>
              <div class="card-body">
                <div class="card p-4 border-warning font-weight-bolder">
                  <p>
                    Integris recommends that these forms be opened with Adobe
                    Acrobat Reader or Adobe Acrobat DC. Please DO NOT use the
                    built in PDF reader from your browser.
                  </p>
                  <a
                    href="https://get.adobe.com/reader/"
                    class="btn btn-outline-secondary"
                  >Get Adobe Acrobat Reader</a>
                </div>
                <div class="list-group list-group-flush my-n3">
                  <div class="list-group-item">
                    <div class="row align-items-center">
                      <div class="col ml-n2">Illustration Request Form</div>
                      <div class="col-auto">
                        <a
                          target="_blank"
                          href="#"
                          v-on:click="illustrationUpload"
                          class="btn btn-sm btn-outline-primary mr-2"
                        >
                          <i class="fe fe-upload-cloud"></i> Upload
                        </a>
                        <a
                          target="_blank"
                          :href="forms.illustration.download"
                          class="btn btn-sm btn-outline-primary"
                        >
                          <i class="fe fe-download"></i> Download
                        </a>
                      </div>
                    </div>
                    <!-- / .row -->
                  </div>
                  <div class="list-group-item">
                    <div class="row align-items-center">
                      <div class="col ml-n2">Setup Request Form</div>
                      <div class="col-auto">
                        <a
                          target="_blank"
                          href="#"
                          v-on:click="setupUpload"
                          class="btn btn-sm btn-outline-primary mr-2"
                        >
                          <i class="fe fe-upload-cloud"></i> Upload
                        </a>
                        <a
                          target="_blank"
                          :href="forms.setup.download"
                          class="btn btn-sm btn-outline-primary"
                        >
                          <i class="fe fe-download"></i> Download
                        </a>
                      </div>
                    </div>
                    <!-- / .row -->
                  </div>
                </div>
              </div>
            </div>

            <div class="card">
              <div class="card-header bg-light">Current Fee Schedules</div>
              <div class="card-body">
                <div class="list-group list-group-flush my-n3 pl-4">
                  <div class="list-group-item" v-for="fee in fees" v-bind:key="fee.title">
                    <div class="row align-items-center">
                      <div class="col ml-n2">{{fee.title}}</div>
                      <div class="col-auto">
                        <a
                          target="_blank"
                          :href="fee.link.en"
                          class="btn btn-sm btn-outline-primary mr-2"
                        >English</a>
                        <a
                          target="_blank"
                          :href="fee.link.fr"
                          class="btn btn-sm btn-outline-primary"
                        >French</a>
                      </div>
                    </div>
                    <!-- / .row -->
                  </div>
                </div>
              </div>
            </div>

            <div class="card">
              <div class="card-header bg-light">Resource Library</div>
              <div class="card-body">
                <div class="list-group list-group-flush my-n3">
                  <div
                    class="list-group-item"
                    v-for="resource in server.ResourceLibraryContentList"
                    v-bind:key="resource.DistributorPortalDocumentGuid"
                  >
                    <div class="align-items-center">
                      <a
                        :href="'/Distributors/'+server.LandingView+'/Document/'+resource.DistributorPortalDocumentGuid"
                        target="_blank"
                      >{{resource.DistributorPortalDocumentDescription}}</a>
                    </div>
                    <!-- / .row -->
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="col-12 col-lg-6">
            <!-- Card -->
            <div class="card">
              <div class="card-header bg-light">Marketing Documents</div>
              <div class="card-body">
                <div class="list-group list-group-flush my-n3 pl-4">
                  <div
                    class="list-group-item"
                    v-for="marketingDoc in marketing"
                    v-bind:key="marketingDoc.title"
                  >
                    <div class="row align-items-center">
                      <div class="col ml-n2">{{marketingDoc.title}}</div>
                      <div class="col-auto">
                        <a
                          target="_blank"
                          :href="marketingDoc.link.english"
                          class="btn btn-sm btn-outline-primary mr-2"
                        >English</a>
                        <a
                          target="_blank"
                          :href="marketingDoc.link.french"
                          class="btn btn-sm btn-outline-primary"
                        >French</a>
                      </div>
                    </div>
                    <!-- / .row -->
                  </div>
                </div>
              </div>
            </div>

            <!-- Card -->
            <div class="card">
              <div class="card-header bg-light">Ontario Registered Pension Plans Compliance Manuals</div>
              <div class="card-body row">
                <div class="col-6" v-for="manual in manuals" v-bind:key="manual.link">
                  <a :href="manual.link" class="btn btn-block btn-outline-primary">
                    <i class="fe fe-book"></i>
                    {{manual.title}}
                  </a>
                </div>
              </div>
            </div>

            <!-- Card -->
            <div class="card card-inactive">
              <div class="card-header bg-light">Distributor Contacts</div>
              <div class="card-body" v-html="server.DistributorContactsContent"></div>
            </div>
            <!-- Card -->
            <div class="card card-inactive">
              <div class="card-header bg-light">Integris Contacts</div>
              <div class="card-body">
                <!-- Title -->
                <h3>Business Development &amp; Sales Support</h3>

                <!-- Text -->
                Adrian Reynolds
                <br />SVP, Business Development
                <br />
                <a href="mailto:adrian.reynolds@integris-mgt.com">adrian.reynolds@integris-mgt.com</a>
                <br />647-956-1605
                <br />
                <br />Jean-Pierre A. Laporte
                <br />Chief
                Executive Officer
                <br />
                <a href="mailto:jp.laporte@integris-mgt.com">jp.laporte@integris-mgt.com</a>
                <br />647-956-1601
                <br />
                <br />
                <h3 class>Onboarding &amp; Client Experience</h3>Gail Frye
                <br />Manager – Onboarding &amp; Client Experience
                <br />
                <a href="mailto:gail.frye@integris-mgt.com">gail.frye@integris-mgt.com</a>
                <br />647-956-1608
              </div>
            </div>
          </div>
        </div>
        <!-- / .row -->

        <!-- / .row -->
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./Header.vue";

export default {
  name: "Home",
  props: {
    logo: String
  },
  components: {
    Header
  },
  mounted: function() {
    document.title = this.server.LandingViewTitle;
    this.loadManuals();
    this.loadForms();
    this.loadFees();
  },
  methods: {
    loadFees: function() {
      var geoTarget = function(productPlatformId) {
        switch (productPlatformId) {
          case 1:
            return "ia";
          case 2:
            return "t3";
          case 3:
            return "tc";
          case 4:
            return "dfs";
          case 5:
            return "al";
          default:
            return "all";
        }
      };

      this.server.ProductPlatforms.forEach(platform => {
        this.fees.push({
          title: platform.Text,
          link: {
            en: "/go/fs" + geoTarget(platform.Value) + "en",
            fr: "/go/fs" + geoTarget(platform.Value) + "fr"
          }
        });
      });
    },
    illustrationUpload: function() {
      window.open(
        this.forms.illustration.upload,
        "_blank",
        "location=no,height=420,width=420,scrollbars=no,status=yes"
      );
    },
    setupUpload: function() {
      window.open(
        this.forms.setup.upload,
        "_blank",
        "location=no,height=420,width=420,scrollbars=no,status=yes"
      );
    },
    loadForms: function() {
      this.forms.illustration.download =
        "/Distributors/" +
        this.server.LandingView +
        "/ClientRM/DownloadIllustrationRequestEForm?version=EF";

      this.forms.illustration.upload =
        "/Distributors/" +
        this.server.LandingView +
        "/ClientRM/UploadIllustrationRequestEForm/";

      this.forms.setup.download =
        "/Distributors/" +
        this.server.LandingView +
        "/ClientRM/DownloadPppSetupRequestEForm?version=EF";
      this.forms.setup.upload =
        "/Distributors/" +
        this.server.LandingView +
        "/ClientRM/UploadPppSetupRequestEForm/";
    },
    loadManuals: function() {
      this.server.ProductPlatforms.forEach(element => {
        if (
          this.server.PrimaryProductPlatform != null &&
          (element.Value == 2 || element.Value == 3)
        ) {
          this.manuals.push({
            title: "Establishing a New PPP",
            link: "https://www.integris-mgt.com/go/tcm"
          });
          this.manuals.push({
            title: "Ongoing Administration",
            link: "https://www.integris-mgt.com/go/tma"
          });
        } else if (
          this.server.PrimaryProductPlatform != null &&
          (element.Value == 1 || element.Value == 5)
        ) {
          this.manuals.push({
            title: "Establishing a New PPP",
            link: "https://www.integris-mgt.com/go/cmo"
          });
          this.manuals.push({
            title: "Ongoing Administration",
            link: "https://www.integris-mgt.com/go/cma"
          });
        } else if (
          this.server.PrimaryProductPlatform != null &&
          element.Value == 4
        ) {
          this.manuals.push({
            title: "PPP Administration Guide",
            link: "publish/Desjardin PPP administration employer guide.pdf"
          });
        }
      });
    }
  },
  data: function() {
    return {
      manuals: [],
      forms: {
        illustration: {},
        setup: {}
      },
      marketing: [
        {
          title: "Understanding the PPP",
          link: {
            english:
              "ClientRM/DownloadPppClientInformationSheet?language=E",
            french:
              "ClientRM/DownloadPppClientInformationSheet?language=F"
          }
        },
        {
          title: "15 reasons why you should consider a PPP® Brochure",
          link: {
            english:
              "ClientRM/DownloadPppClientInformationSheet?language=E",
            french:
              "ClientRM/DownloadPppClientInformationSheet?language=F"
          }
        }
      ],
      fees: [],
      server: {
        DisplayName: "Desjardins Insurance",
        DistributorContactsContent:
          'David Hinca<br />Senior Business Development Manager - Ontario<br /><a href="mailto:david.hinca@dfs.ca">david.hinca@dfs.ca</a><br />416-926-2789<br /><br />Olivier Lapierre<br />Directeur développement des affaires - Québec<br /><a href="olapierre@dsf.ca">olapierre@dsf.ca</a><br />418-838-4202<br />',
        DistributorPortal: "Desjardins Insurance",
        DistributorPortalId: 101,
        EnrolmentOverviewContent:
          " <h2>Fee Schedules</h2>Insurance (Desjardins): <a href=\"javascript:window.open(window.location.href + '/Document/274f6010-77f3-41af-a40f-fbad6b113b3a','_blank');\">English</a> | <a href=\"javascript:window.open(window.location.href + '/Document/caa6b229-4e72-408f-8e47-c9e094870aa5','_blank');\">French</a><br />",

        IntegrisContactsContent:
          '<span style="font-weight: bold;">Business Development & Sales Support</span><br /><br />Adrian Reynolds<br />SVP, Business Development<br /><a href="mailto:adrian.reynolds@integris-mgt.com">adrian.reynolds@integris-mgt.com</a><br />647-956-1605<br /><br />Jean-Pierre A. Laporte<br />Chief Executive Officer<br /><a href="mailto:jp.laporte@integris-mgt.com">jp.laporte@integris-mgt.com</a><br />647-956-1601<br /><br /><span style="font-weight: bold;">Onboarding & Client Experience</span><br /><br />Gail Frye<br />Manager – Onboarding & Client Experience<br /><a href="mailto:gail.frye@integris-mgt.com">gail.frye@integris-mgt.com</a><br />647-956-1608<br />',
        LandingView: "DesjardinsInsurance",
        LandingViewTitle: "Desjardins Insurance",
        LanguageAbbreviation: "en",
        LanguageId: 1,
        LanguageName: "English",
        LanguageNativeName: "English",
        LogoImageType: "png",
        LogoImgSrc:
          'src="data:image/png;base64,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"',

        PrimaryProductPlatform: {
          Text: "Insurance (Desjardins)",
          Value: 4
        },
        ProductPlatforms: [
          {
            Text: "Insurance (Desjardins)",
            Value: 4
          }
        ],
        ResourceLibraryContent:
          "The resource library lists/contains information and documents relevant to you.",
        ResourceLibraryContentCategorys: [
          {
            Text: "Brochures/Marketing Materials",
            Value: 1
          },
          {
            Text: "Enrolment/On-boarding Documents",
            Value: 3
          },
          {
            Text: "Fact Sheets",
            Value: 2
          },
          {
            Text: "iA Resource Documents",
            Value: 5
          }
        ],
        ResourceLibraryContentList: [
          {
            DisplayFileSizeString: "72.4kB",
            DistributorPortalDocumentCategorys: "|Fact Sheets|",
            DistributorPortalDocumentDescription:
              "Fact Sheet No. 15 - PPP Contributions",
            DistributorPortalDocumentFilename:
              "Fact Sheet No. 15 - PPP Contributions.pdf",
            DistributorPortalDocumentGuid:
              "A74FA1C8-6391-4215-899C-7B5333E847EC",
            DistributorPortalDocumentId: 55,
            DistributorPortalDocumentSize: 74167,
            DistributorPortalDocumentTitle:
              "Fact Sheet No. 15 - PPP Contributions",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "128.1kB",
            DistributorPortalDocumentCategorys: "|Fact Sheets|",
            DistributorPortalDocumentDescription:
              "Fact Sheet No. 01 - Understanding Wealth",
            DistributorPortalDocumentFilename:
              "Fact Sheet No. 01 - Understanding Wealth.pdf",
            DistributorPortalDocumentGuid:
              "299F23F9-5238-4A20-8CA1-46AB3B8723BB",
            DistributorPortalDocumentId: 64,
            DistributorPortalDocumentSize: 131138,
            DistributorPortalDocumentTitle:
              "Fact Sheet No. 01 - Understanding Wealth",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "45.5kB",
            DistributorPortalDocumentCategorys: "|Fact Sheets|",
            DistributorPortalDocumentDescription:
              "Fact Sheet No. 02 - Personal Service Businesses",
            DistributorPortalDocumentFilename:
              "Fact Sheet No. 02 - Personal Service Businesses.pdf",
            DistributorPortalDocumentGuid:
              "68D8E15B-08B4-4F98-AD5E-CD92A29DEFDF",
            DistributorPortalDocumentId: 65,
            DistributorPortalDocumentSize: 46630,
            DistributorPortalDocumentTitle:
              "Fact Sheet No. 02 - Personal Service Businesses",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "49.1kB",
            DistributorPortalDocumentCategorys: "|Fact Sheets|",
            DistributorPortalDocumentDescription:
              "Fact Sheet No. 03 - Creditor Protection",
            DistributorPortalDocumentFilename:
              "Fact Sheet No. 03 - Creditor Protection.pdf",
            DistributorPortalDocumentGuid:
              "0C7C8ACF-EA70-4CDA-B88C-75B68A7A6695",
            DistributorPortalDocumentId: 66,
            DistributorPortalDocumentSize: 50278,
            DistributorPortalDocumentTitle:
              "Fact Sheet No. 03 - Creditor Protection",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "52.3kB",
            DistributorPortalDocumentCategorys: "|Fact Sheets|",
            DistributorPortalDocumentDescription:
              "Fact Sheet No. 04 - Why Pay for Fiduciary Oversight",
            DistributorPortalDocumentFilename:
              "Fact Sheet No. 04 - Why Pay for Fiduciary Oversight.pdf",
            DistributorPortalDocumentGuid:
              "54D638CC-7B61-4309-82DD-7A90ACE54976",
            DistributorPortalDocumentId: 67,
            DistributorPortalDocumentSize: 53543,
            DistributorPortalDocumentTitle:
              "Fact Sheet No. 04 - Why Pay for Fiduciary Oversight",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "60.8kB",
            DistributorPortalDocumentCategorys: "|Fact Sheets|",
            DistributorPortalDocumentDescription:
              "Fact Sheet No. 05 - HST Credit What's That",
            DistributorPortalDocumentFilename:
              "Fact Sheet No. 05 - HST Credit What's That.pdf",
            DistributorPortalDocumentGuid:
              "A681CA50-7527-4851-9E13-C299956F021E",
            DistributorPortalDocumentId: 68,
            DistributorPortalDocumentSize: 62214,
            DistributorPortalDocumentTitle:
              "Fact Sheet No. 05 - HST Credit What's That",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "55.9kB",
            DistributorPortalDocumentCategorys: "|Fact Sheets|",
            DistributorPortalDocumentDescription:
              "Fact Sheet No. 06 - Terminal Funding",
            DistributorPortalDocumentFilename:
              "Fact Sheet No. 06 - Terminal Funding.pdf",
            DistributorPortalDocumentGuid:
              "38F08931-A3DA-4C15-AC76-AB261A5A4A1A",
            DistributorPortalDocumentId: 69,
            DistributorPortalDocumentSize: 57258,
            DistributorPortalDocumentTitle:
              "Fact Sheet No. 06 - Terminal Funding",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "47.1kB",
            DistributorPortalDocumentCategorys: "|Fact Sheets|",
            DistributorPortalDocumentDescription:
              "Fact Sheet No. 07 - Buying Past Service",
            DistributorPortalDocumentFilename:
              "Fact Sheet No. 07 - Buying Past Service.pdf",
            DistributorPortalDocumentGuid:
              "0C2CFDA3-DB2E-4CD2-9770-30D23792895F",
            DistributorPortalDocumentId: 70,
            DistributorPortalDocumentSize: 48193,
            DistributorPortalDocumentTitle:
              "Fact Sheet No. 07 - Buying Past Service",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "74.6kB",
            DistributorPortalDocumentCategorys: "|Fact Sheets|",
            DistributorPortalDocumentDescription:
              "Fact Sheet No. 08 - Dividends or Salary",
            DistributorPortalDocumentFilename:
              "Fact Sheet No. 08 - Dividends or Salary.pdf",
            DistributorPortalDocumentGuid:
              "684655DE-CA1E-4F27-B4FE-EA39C0E8498C",
            DistributorPortalDocumentId: 71,
            DistributorPortalDocumentSize: 76399,
            DistributorPortalDocumentTitle:
              "Fact Sheet No. 08 - Dividends or Salary",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "57.6kB",
            DistributorPortalDocumentCategorys: "|Fact Sheets|",
            DistributorPortalDocumentDescription:
              "Fact Sheet No. 09 - Opportunity Cost",
            DistributorPortalDocumentFilename:
              "Fact Sheet No. 09 - Opportunity Cost.pdf",
            DistributorPortalDocumentGuid:
              "FE177B51-7FFA-4CB6-8092-F75B351F6A53",
            DistributorPortalDocumentId: 72,
            DistributorPortalDocumentSize: 58942,
            DistributorPortalDocumentTitle:
              "Fact Sheet No. 09 - Opportunity Cost",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "58.0kB",
            DistributorPortalDocumentCategorys: "|Fact Sheets|",
            DistributorPortalDocumentDescription:
              "Fact Sheet No. 10 - Connected Persons and Tax Deductions",
            DistributorPortalDocumentFilename:
              "Fact Sheet No. 10 - Connected Persons and Tax Deductions.pdf",
            DistributorPortalDocumentGuid:
              "378376AE-4CDB-4669-B2A3-984B3167BFAA",
            DistributorPortalDocumentId: 73,
            DistributorPortalDocumentSize: 59371,
            DistributorPortalDocumentTitle:
              "Fact Sheet No. 10 - Connected Persons and Tax Deductions",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "57.4kB",
            DistributorPortalDocumentCategorys: "|Fact Sheets|",
            DistributorPortalDocumentDescription:
              "Fact Sheet No. 12 - Understanding AVCs",
            DistributorPortalDocumentFilename:
              "Fact Sheet No. 12 - Understanding AVCs.pdf",
            DistributorPortalDocumentGuid:
              "FD2AA7D0-E67B-42A1-9773-2149257F0AC8",
            DistributorPortalDocumentId: 74,
            DistributorPortalDocumentSize: 58744,
            DistributorPortalDocumentTitle:
              "Fact Sheet No. 12 - Understanding AVCs",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "112.6kB",
            DistributorPortalDocumentCategorys: "|Fact Sheets|",
            DistributorPortalDocumentDescription:
              "Fact Sheet No. 13 - Plan Set Up",
            DistributorPortalDocumentFilename:
              "Fact Sheet No. 13 - Plan Set Up.pdf",
            DistributorPortalDocumentGuid:
              "EC3C59FF-25A9-4018-9FD4-9DF464498358",
            DistributorPortalDocumentId: 75,
            DistributorPortalDocumentSize: 115255,
            DistributorPortalDocumentTitle: "Fact Sheet No. 13 - Plan Set Up",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "75.6kB",
            DistributorPortalDocumentCategorys: "|Fact Sheets|",
            DistributorPortalDocumentDescription:
              "Fact Sheet No. 16 - Moving An IPP To An INTEGRIS PPP",
            DistributorPortalDocumentFilename:
              "Fact Sheet No. 16 - Moving An IPP To An INTEGRIS PPP.pdf",
            DistributorPortalDocumentGuid:
              "B54C6AD4-26B7-418D-86E9-A1E72F67D20A",
            DistributorPortalDocumentId: 77,
            DistributorPortalDocumentSize: 77408,
            DistributorPortalDocumentTitle:
              "Fact Sheet No. 16 - Moving An IPP To An INTEGRIS PPP",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "95.1kB",
            DistributorPortalDocumentCategorys: "|Fact Sheets|",
            DistributorPortalDocumentDescription:
              "Fact Sheet No. 14 - For Accountants",
            DistributorPortalDocumentFilename:
              "Fact Sheet No. 14 For Accountants - 2016.pdf",
            DistributorPortalDocumentGuid:
              "B88D0393-8E89-47E3-837B-A535E45D0E4C",
            DistributorPortalDocumentId: 110,
            DistributorPortalDocumentSize: 97349,
            DistributorPortalDocumentTitle:
              "Fact Sheet No. 14 - For Accountants",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "28.1kB",
            DistributorPortalDocumentCategorys: "||",
            DistributorPortalDocumentDescription:
              "INTEGRIS Bulk Illustration Request Data Capture Form",
            DistributorPortalDocumentFilename:
              "INTEGRIS Bulk Illustration Request Data Capture Form.xlsx",
            DistributorPortalDocumentGuid:
              "ba298576-c860-42a3-bc72-8b6643679612",
            DistributorPortalDocumentId: 202,
            DistributorPortalDocumentSize: 28733,
            DistributorPortalDocumentTitle:
              "INTEGRIS Bulk Illustration Request Data Capture Form",
            DistributorPortalDocumentType:
              "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "913.0kB",
            DistributorPortalDocumentCategorys:
              "|Brochures/Marketing Materials|",
            DistributorPortalDocumentDescription:
              "Desjardins Personal Pension Plan Brochure",
            DistributorPortalDocumentFilename:
              "Desjardins Personal Pension Plan Brochure.pdf",
            DistributorPortalDocumentGuid:
              "18ff6ee3-cdd4-4223-92d0-5437d2fe9fe5",
            DistributorPortalDocumentId: 204,
            DistributorPortalDocumentSize: 934948,
            DistributorPortalDocumentTitle:
              "Desjardins Personal Pension Plan Brochure",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "366.1kB",
            DistributorPortalDocumentCategorys: "||",
            DistributorPortalDocumentDescription:
              "FeeScheduleV15-001-20190101E",
            DistributorPortalDocumentFilename:
              "FeeScheduleV15-001-20190101E.pdf",
            DistributorPortalDocumentGuid:
              "274f6010-77f3-41af-a40f-fbad6b113b3a",
            DistributorPortalDocumentId: 212,
            DistributorPortalDocumentSize: 374857,
            DistributorPortalDocumentTitle:
              "Fee Schedule – Insurance (Desjardins) - English",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          },
          {
            DisplayFileSizeString: "368.3kB",
            DistributorPortalDocumentCategorys: "||",
            DistributorPortalDocumentDescription:
              "FeeScheduleV15-001-20190101F",
            DistributorPortalDocumentFilename:
              "FeeScheduleV15-001-20190101F.pdf",
            DistributorPortalDocumentGuid:
              "caa6b229-4e72-408f-8e47-c9e094870aa5",
            DistributorPortalDocumentId: 213,
            DistributorPortalDocumentSize: 377174,
            DistributorPortalDocumentTitle:
              "Fee Schedule – Insurance (Desjardins) - French",
            DistributorPortalDocumentType: "application/pdf",
            DistributorPortalId: 101
          }
        ],
        UserEmailAddress: "subhas@techlicity.com",
        UserFullName: "Fagu, 918FirstName",
        UserId: 2026,
        WelcomeContent:
          "Welcome to the INTEGRIS Distributor Portal for Desjardins Insurance. Here you will find a wealth of information on INTEGRIS Personal Pension Plans. It you have any questions, please do not hesitate to contact us via the Distributor or Integris Contact info.",
        YesNo: [
          {
            Text: "No",
            Value: false
          },
          {
            Text: "Yes",
            Value: true
          }
        ],
        Guid: "ff608d7f-dfc7-4102-b9a0-af5a8c4c80e3",
        Id: 101,
        SecurityPermissions: null,
        TimeZone: null
      }
    };
  }
};
</script>