<template>
  <div>
    <Header title="Frequently Asked Questions" :logo="logo"/>

    <div class="container">
      <div v-for="(faq,index) in server" v-bind:key="faq.id">
        <b-card no-body class="mb-1" header-tag="header" align="left">
          <b-card-header class="p-1" role="tab" align="left">
            <b-button
              block
              href="#"
              v-b-toggle="'accordion'+index"
              align="left"
              variant="outline-default"
            >
              <i class="fe fe-chevron-down mr-2" />
              <span v-html="faq.DisplayName" />
            </b-button>
          </b-card-header>
          <b-collapse :id="'accordion'+index" visible accordion="my-accordion" role="tabpanel">
            <b-card-body>
              <b-card-text v-html="faq.FullContent"></b-card-text>
            </b-card-body>
          </b-collapse>
        </b-card>
      </div>
    </div>
  </div>
</template>

<script>
import Header from './Header.vue';

export default {
  name: "FAQs",
  props: {
    logo: String
  },
  components:{
      Header
  },
  data: function() {
    return {
      server: [
        {
          Author: "",
          DatePostedLocal: "/Date(1540147727920)/",
          DatePostedUtc: "/Date(1540162127920)/",
          DisplayName:
            "Can you transfer half of IPP to Lif or Lira to reduce the tax hit that cannot be sheltered?",
          FullContent:
            "No. But to pay no tax on wind up of the PPP, you can purchase a ‘copy cat’ annuity pursuant to Income Tax Act section 147.4.  In that case, the LIRA/LIF tax hit does not take place because it is not governed by Income Tax Regulations 8517.\u003cbr /\u003e\u003cbr /\u003eThere is a \u0026quot;Maximum Transfer Value\u0026quot;of pension assets that can transfer to a LIRA/LIF on a  tax deferred basis. Please see the table on the last page of the Illustration for examples of the amount that would be taxable at different ages.",
          LastRevisedDateLocal: "/Date(1540147727920)/",
          LastRevisedDateUtc: "/Date(1540162127920)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "can-you-transfer-half-of-ipp-to-lif-or-lira ",
          ShortContent: "",
          Summary: "",
          Title:
            "Can you transfer half of IPP to Lif or Lira to reduce the tax hit that cannot be sheltered?",
          Guid: "fa1383f5-b9d4-45f4-b290-60be7a491f47",
          Id: 1216,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1540136025380)/",
          DatePostedUtc: "/Date(1540150425380)/",
          DisplayName:
            "I assume that the contributions stop when ever you start the pension?",
          FullContent:
            "Yes, no more annual current service cost contributions are permittedafter the pension is turned on.  However, as discussed above, to ensure that the plan remains fully funded, ‘special payments’ could be required by the company on a ‘go forward ‘…these come from the corp, not the employee.",
          LastRevisedDateLocal: "/Date(1540136025380)/",
          LastRevisedDateUtc: "/Date(1540150425380)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "i-assume-that-the-contributions-stop-when-ever-you-start-the-pension",
          ShortContent: "",
          Summary: "",
          Title:
            "I assume that the contributions stop when ever you start the pension?",
          Guid: "48ba5867-f621-448e-9412-78f62b539084",
          Id: 1215,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1540135891250)/",
          DatePostedUtc: "/Date(1540150291250)/",
          DisplayName:
            "Can you lower the monthly payout so money can last to 100?",
          FullContent:
            "Significant shareholders can reduce accrued benefits at retirement under section 48 of the regulations, thereby creating surplus and extending the life of the pension assets.  But as discussed above, there is no need to do this.",
          LastRevisedDateLocal: "/Date(1540135891250)/",
          LastRevisedDateUtc: "/Date(1540150291250)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "can-you-lower-the-monthly-payout-so-money-can-last-to-100",
          ShortContent: "",
          Summary: "",
          Title: "Can you lower the monthly payout so money can last to 100?",
          Guid: "9aee3b91-20c3-4096-afc2-155068f78a9c",
          Id: 1214,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1540135800500)/",
          DatePostedUtc: "/Date(1540150200500)/",
          DisplayName:
            "I noticed that the plan would be fully paid out by the age 85, this is different then most Defined Benefit Plans in the public sector, is that correct?",
          FullContent:
            "Option “A” on the last page of the illustration is misleading in the sense that it presents a sinking fund analysis where assets are growing at 5% and a full pension, indexed to inflation with terminal funding, is paid out.  In reality, the PPP would have a corporate sponsor all along, which means that deficits created by the payment of benefits and market downturns and fees, would require the company to make additional “special payments” to keep the plan fully funded.  Therefore, the money does not run out at 85 because the company backstops the promise.  If the company ceases to exist, or runs out of money, then we are forced by pension legislation to wind up the plan, and either: “B” purchase an annuity from a life insurance company that will guarantee pension payments as long as the client is alive (guarantees can also be purchased), or “C” transferred to a LIRA/LIF in which case INTEGRIS and the PPP is out of the equation.  How quickly someone depletes the funds in a LIF will depend on the minimum and maximum LIF payments selected by the client etc.",
          LastRevisedDateLocal: "/Date(1540135800500)/",
          LastRevisedDateUtc: "/Date(1540150200500)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "i-noticed-that-the-plan-would-be-fully-paid-out-by-the-age-85",
          ShortContent: "",
          Summary: "",
          Title:
            "I noticed that the plan would be fully paid out by the age 85, this is different then most Defined Benefit Plans in the public sector, is that correct?",
          Guid: "66f42dd4-3e77-48ff-818e-7c7f492052b1",
          Id: 1213,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1540135644857)/",
          DatePostedUtc: "/Date(1540150044857)/",
          DisplayName: "Is the monthly Pension guaranteed?",
          FullContent:
            "The life-only optional form of pension is payable as a lifetime pension guaranteed for 15 years. If you have a spouse, the form will be a joint and survivor pension guaranteed for 5 years reducing to 66 2/3% upon your death unless the spouse waives this entitlement. This pension is indexed in accordance with the Consumer Price Index (CPI) minus 1% unless we purchase full indexing under the Terminal Funding rules.  The word “guaranteed” can be misleading to the uninitiated because it connotes a loss once the guarantee runs out.  While this would be the case with a large pension plan with many plan members (Teachers’, OMERS, GM, HOOPP, Ford etc…) in our context there is no loss of pension dollars because a death after the guarantee period expires simply means that the left over pension fund dollars are now “surplus”.  Surplus belongs to the company and the company can pay it out to the survivors… so there is never any loss with a PPP.",
          LastRevisedDateLocal: "/Date(1540135644857)/",
          LastRevisedDateUtc: "/Date(1540150044857)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "is-the-monthly-pension-guaranteed",
          ShortContent: "",
          Summary: "",
          Title: "Is the monthly Pension guaranteed?",
          Guid: "ab513a48-7305-4c3e-8553-c7c3b9f0ac64",
          Id: 1211,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1540135533097)/",
          DatePostedUtc: "/Date(1540149933097)/",
          DisplayName:
            "Do the yearly contributions to the plan come directly from the corporation or does the client contribute ? is it monthly?",
          FullContent:
            "All annual contributions to the DB or DC account typically come from the corporation and can be set up monthly. We do have the option of asking the employee to contribute as well, which makes those contributions tax deductible in the hands of the employee instead of the corporation.  None of our clients use this option at the current time (not really tax effective because the client can’t spend the salary being redirected to the pension plan and is simply differing taxes at a higher rate).",
          LastRevisedDateLocal: "/Date(1540135533097)/",
          LastRevisedDateUtc: "/Date(1540149933097)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "do-the-yearly-contributions-to-the-plan-come-directly-from-the-corporation",
          ShortContent: "",
          Summary: "",
          Title:
            "Do the yearly contributions to the plan come directly from the corporation or does the client contribute ? is it monthly?",
          Guid: "7656d3e5-22f4-4f89-a47b-5d2ee1cf9fb8",
          Id: 1210,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1537463665453)/",
          DatePostedUtc: "/Date(1537478065453)/",
          DisplayName:
            "Can I setup a plan without all the client\u0027s T-4 slips?",
          FullContent:
            "Yes...\u003cbr /\u003e\u003cbr /\u003eAdvisors often think that if they cannot assemble all of the historical salaries of their clients they cannot establish a pension plan. This is incorrect, since nothing obliges a company to recognize past service at the time of plan establishment. This can always be done at any point in time in the future.\u003cbr /\u003e\u003cbr /\u003eAdvisors who want their clients to at least get a corporate tax deduction for current service cost/annual contributions, should consider getting the plan registered as soon as possible without recognizing past service initially.",
          LastRevisedDateLocal: "/Date(1544492916163)/",
          LastRevisedDateUtc: "/Date(1544510916163)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "can-I setup-a-plan-without-all-the-clients-T-4-slips",
          ShortContent: "",
          Summary: "",
          Title: "Can I setup a plan without all the client\u0027s T-4 slips?",
          Guid: "62d0df7b-6cf5-4261-82c7-aeb63d3c9d4f",
          Id: 1206,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1530533875603)/",
          DatePostedUtc: "/Date(1530548275603)/",
          DisplayName: "I already have an IPP, can I convert it into a PPP?",
          FullContent:
            'Yes. You can convert the IPP into a PPP\u003csup\u003e\u0026reg;\u003c/sup\u003e and gain the advantages of having a PPP\u003csup\u003e\u0026reg;\u003c/sup\u003e. It is an easy process which involves filing an amendment with the regulators and completing a few documents. If you are interested, please \u003ca href="mailto:question@integris-mgt.com"\u003econtact us\u003c/a\u003e and we can provide you with one of our publications that describes the steps in more detail.',
          LastRevisedDateLocal: "/Date(1544493905300)/",
          LastRevisedDateUtc: "/Date(1544511905300)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "i-already-have-an-ipp-can-i-covert-it-into-a-ppp",
          ShortContent: "",
          Summary: "",
          Title: "I already have an IPP, can I convert it into a PPP?",
          Guid: "02de20e7-d6df-4c7a-a898-b624a28f244b",
          Id: 1203,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName: "What are the tax benefits of the INTEGRIS PPP?",
          FullContent:
            "There are several.  From a tax benefit perspective, having available years of service (where T4 income is paid in prior years while not in a pension plan) provides the PPP member with an extra tax benefit (through his/her company) since the total cost to buy back this past service is only partially satisfied through a qualifying transfer of RRSP monies.  The other portion of funding the past service buyback is through employer contribution.  This contribution by the employer is tax-deductible.  Additional tax benefits include:  deductions for fees, deductions for paying interest on borrowings to make contributions to the pension plan, special payments, terminal funding and the GST/HST administrator rebate.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "what-are-the-tax-benefits-of-the-integris-ppp",
          ShortContent: "",
          Summary: "",
          Title: "What are the tax benefits of the INTEGRIS PPP?",
          Guid: "82c1e5ca-2d11-4b67-91fb-4ff02f2b23fc",
          Id: 73,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "My IT client was recently designated as a personal service business by the Canada Revenue Agency and now has to pay corporate income tax at 39.5%.  Can he still contribute to a PPP?",
          FullContent:
            "Yes. Companies that are considered Personal Service Businesses can set up a PPP and claim corporate tax deductions.",
          LastRevisedDateLocal: "/Date(1544493957117)/",
          LastRevisedDateUtc: "/Date(1544511957117)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "my-it-client-was-recently-designated-as-a-personal-service-business-by-the-canada-revenue-agency",
          ShortContent: "",
          Summary: "",
          Title:
            "My IT client was recently designated as a personal service business by the Canada Revenue Agency and now has to pay corporate income tax at 39.5%.  Can he still contribute to a PPP?",
          Guid: "321458a6-cf1c-403c-9f8c-bff2d7ee6b5d",
          Id: 74,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Why is a 40 year-old pension plan member allowed to contribute more each year under the INTEGRIS PPP?",
          FullContent:
            "There is increased funding each year because under a defined benefit plan, the promised pension must be funded by streams of invested pension assets made along the way.  A contribution made at age 64 only has 1 year to grow, whereas funds deposited when a member is age 20, have 45 years of compounding and can therefore be less than those made in later years.\u003cbr /\u003e\u003cbr /\u003eTo ensure that a balance is kept between funds required and time invested, the values in prescribed actuarial tables assume an increase in contributions each year.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "why-is-a-40-year-old-pension-plan-member-allowed-to-contribute-more-each-year-under-the-integris-ppp",
          ShortContent: "",
          Summary: "",
          Title:
            "Why is a 40 year-old pension plan member allowed to contribute more each year under the INTEGRIS PPP?",
          Guid: "19e085a8-17ba-45f6-9115-f41259b004ec",
          Id: 75,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Why is it possible to tax shelter more in an INTEGRIS PPP or a registered pension plan (RPP) in general than in an RRSP?",
          FullContent:
            '\u003col style="list-style-type: lower-roman;"\u003e\u003cli\u003eRRSPs do not offer defined benefits.  Defined benefits are offered in a pension plan and are based on a formula (discount rate (i.e. 2%) x years of credited service x final average earnings (or some other definition).  The income tax regulations assume that assets set aside to fund this promise will grow at 7.5% per annum.  If markets do not return that, the money still needs to be contributed, above and beyond the current service cost contributions.  Therefore, there is more money invested for retirement under a pension plan than under a RRSP. \u003c/li\u003e\u003cli\u003eActuarial principle dictates that anyone above age 40 can put more money towards retirement than if they had stayed in their RRSP, since the contributions made to a RRSP are not based on age. \u003c/li\u003e\u003cli\u003eEnhancements to pensions (indexing, early unreduced pensions, CPP bridge) cost a lot of money.  The employer makes those extra contributions to the pension fund.  Since RRSPs do not offer such ‘bells and whistles’, it does not permit making these additional contributions.  Therefore, at the end of the day, there is less money in the RRSP fund. \u003c/li\u003e\u003cli\u003eAdministration and investment management fees in a RRSP cannot be deducted from income.  Previously, it was possible to deduct them but then the Income Tax Act (Canada) was specifically amended to prohibit it.  Deductions are permitted under pension plans because the rationale is that the employer is treating these fees as a cost of doing business.  The impact of having the corporation pay with pre-tax dollars is two-fold\u003cbr /\u003ea. The true economic cost of the fees is lessened since the corporation can claim a tax refund for the fees;\u003cbr /\u003eb. The pool of invested assets grows (compounds) faster because it is not constantly being depleted by fees.\u003c/li\u003e\u003cli\u003eTo a lesser degree, the defined contribution money purchase limit is always 1 year ahead of the RRSP limit.  This is because the Income Tax Act (Canada) defines the RRSP limit to be the previous year’s money purchase limit.  Since the government updates the money purchase limit every year to keep up with inflation, there is always a slight advantage in favour of pension plans. When all of these independent causes and effects are combined, a substantial gap starts to appear between RRSPs and the INTEGRIS PPPs.\u003c/li\u003e\u003c/ol\u003e',
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "why-is-it-possible-to-tax-shelter-more-in-an-integris-ppp-or-a-registered-pension-plan-rpp-in-general-than-in-an-rrsp",
          ShortContent: "",
          Summary: "",
          Title:
            "Why is it possible to tax shelter more in an INTEGRIS PPP or a registered pension plan (RPP) in general than in an RRSP?",
          Guid: "e9692c34-b0a0-409a-93f6-b54c7a1bf022",
          Id: 76,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Is there any portion of the administration and management fees associated with the INTEGRIS PPP that is not tax-deductible?",
          FullContent:
            "No, all administration and investment management fees of the PPP are tax-deductible to the employer.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "is-there-any-portion-of-the-administration-and-management-fees-associated-with-the-integris-ppp-that-is-not-tax-deductible",
          ShortContent: "",
          Summary: "",
          Title:
            "Is there any portion of the administration and management fees associated with the INTEGRIS PPP that is not tax-deductible?",
          Guid: "44c92a96-4db2-4c3b-9ccc-a4ab588ae776",
          Id: 77,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Can a client transfer in RRSPs to buy back years of service in the INTEGRIS PPP, or does it have to be cash that buys that back? ",
          FullContent:
            "While the price of funding a buy back in the INTEGRIS PPP is settled in cash by the plan sponsor, the RRSP component (the qualifying transfer) can be settled in-kind.  The company portion of the buy back cost is settled in cash.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "can-a-client-transfer-in-rrsps-to-buy-back-years-of-service-in-the-integris-ppp,-or-does-it-have-to-be-cash-that-buys-that-back",
          ShortContent: "",
          Summary: "",
          Title:
            "Can a client transfer in RRSPs to buy back years of service in the INTEGRIS PPP, or does it have to be cash that buys that back? ",
          Guid: "9aaace41-a822-4992-a68b-2df9e312800d",
          Id: 78,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "What happens from a tax perspective when a defined benefit pension plan has surplus assets?  Is there a penalty similar to what happens under a RRSP where there is a 1% per month Canada Revenue Penalty on over-contributions?",
          FullContent:
            "If a defined benefit plan has assets representing 125% of liabilities promised under the plan, it is said to be in excess surplus. No other contributions can be made to the pension plan after that stage is reached until the assets fall below the 125% level.  The penalty for contributing to a plan that is in excess surplus is extreme: the plan becomes revocable.  If a registered pension plan is revoked, the assets in it become fully taxable.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "what-happens-from-a-tax-perspective-when-a-defined-benefit-pension-plan-has-surplus-assets--is-there-a-penalty",
          ShortContent: "",
          Summary: "",
          Title:
            "What happens from a tax perspective when a defined benefit pension plan has surplus assets?  Is there a penalty similar to what happens under a RRSP where there is a 1% per month Canada Revenue Penalty on over-contributions?",
          Guid: "0dcaf704-200e-4e07-a5c1-e4a7cf5e7646",
          Id: 79,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "What are the reasons why someone would not want an INTEGRIS PPP or instances where it really would not be the best option for a business owner? ",
          FullContent:
            'There are 2 key instances where a PPP would not be suitable for a  prospect:\u003col style="list-style-type: lower-roman;"\u003e\u003cli\u003eIndividuals who treat RRSPs as a special kind of savings account, and who plan to draw down on the money to make capital expenditures or for current consumption prior to retirement.\u003cbr /\u003e  Since mandatory contributions to the PPP (1% DC or DB) are locked-in by pension laws, individuals who must access their funds at a moment’s notice would not be accommodated.  However, any voluntary employee contributions are not locked-in, and neither are any RRSP monies rolled into the AVC subaccount.\u003c/li\u003e\u003cli\u003eIndividuals who want to invest all of their money in a single security.  If a client thinks they have found the perfect stock and want to leverage all of the funds by concentrating on that stock, they will be prohibited from doing so in a PPP.  The reason is the 10% concentration limit found in Schedule III to the Pension Benefits Standards Regulations, 1985 that generally applies to all registered pension plans, including the PPP.\u003c/li\u003e\u003c/ol\u003e',
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "what-are-the-reasons-why-someone-would-not-want-an-integris-ppp",
          ShortContent: "",
          Summary: "",
          Title:
            "What are the reasons why someone would not want an INTEGRIS PPP or instances where it really would not be the best option for a business owner? ",
          Guid: "7e846b61-9bbd-4213-a4cb-caa68065c60f",
          Id: 80,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Can the INTEGRIS PPP be transferred from one corporation to another in the event of a business acquisition?",
          FullContent:
            "Yes. Corporation XYZ sponsoring the PPP can assign the responsibility and assets of the PPP to Corporation ABC.  This is done via an Assignment and Assumption Agreement entered into between the two corporations.\u003cbr /\u003e\u003cbr /\u003eThere is no need to wind up the PPP and suffer the adverse tax consequences of transferring to a locked in account.  There is also no need for regulatory approval for such an assignment.  A plan amendment is needed to reflect the new corporate sponsor.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "can-the-integris-ppp-be-transferred-from-one-corporation-to-another-in-the-event-of-a-business-acquisition",
          ShortContent: "",
          Summary: "",
          Title:
            "Can the INTEGRIS PPP be transferred from one corporation to another in the event of a business acquisition?",
          Guid: "6c498961-fe74-4ae4-8e85-d7ab80a9d4e8",
          Id: 81,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "What happens when the pension fund is underfunded and a client does not have the ability to make special payments?",
          FullContent:
            "The corporate sponsor of the PPP can reduce its cash contributions to the PPP in three ways:\u003cbr /\u003e (a) the member elects to go to the Defined Contribution component of the plan on January 1st and the company only makes the mandatory 1% employer contribution (and continues to fund special payments over 5 years);\u003cbr /\u003e (b) if investment returns increase, a new actuarial valuation report showing that the underfunding has disappeared can be filed, thereby eliminating the special payments;\u003cbr /\u003e  (c) for significant shareholders in Ontario, a joint declaration can be filed under Pension Benefit Regulation 48 with the Superintendent to amend the plan and reduce the accrued benefits down to the level of funding available, thereby completely eliminating the underfunding.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "what-happens-when-the-pension-fund-is-underfunded-and-a-client-does-not-have-the-ability-to-make-special-payments",
          ShortContent: "",
          Summary: "",
          Title:
            "What happens when the pension fund is underfunded and a client does not have the ability to make special payments?",
          Guid: "53fea0c9-a026-4019-82b2-8af417080d91",
          Id: 82,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "A client aged 70 wants his family trust to be the beneficiary of the PPP upon his death.  What happens to the pension fund assets if the client dies and cannot maintain the corporation?",
          FullContent:
            "If the client wants this to occur, he or she must ensure that the spouse waives the entitlement to the survivor pension prior to pension commencement.\u003cbr /\u003e\u003cbr /\u003e  Moreover, when retirement begins, a 15 year guarantee period must be selected, and the family trust designated as the beneficiary under the guarantee period.\u003cbr /\u003e\u003cbr /\u003e  If death occurs after the 15-year period, the will of the individual should specify that the assets of the corporate sponsor of the PPP belong to the family trust, if that isn’t already the case.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "a-client-aged-70-wants-his-family-trust-to-be-the-beneficiary-of-the-ppp-upon-his-death",
          ShortContent: "",
          Summary: "",
          Title:
            "A client aged 70 wants his family trust to be the beneficiary of the PPP upon his death.  What happens to the pension fund assets if the client dies and cannot maintain the corporation?",
          Guid: "ab01b0c3-3920-4105-acb5-d6428f4d44e9",
          Id: 83,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "At what point does it make economic sense for a person to upgrade from an RRSP to a PPP given that a PPP has certain additional costs not found in RRSPs (actuarial \u0026 administration)?",
          FullContent:
            "In almost every case, an upgrade is beneficial from an economic point of view because, while a PPP requires that additional fees be paid to maintain the plan in operation, it is important to remember that the more generous tax deductions available under tax laws not only eliminate these fees, but provide an actual increase to the client’s overall net worth depending on the circumstances.\u003cbr /\u003e\u003cbr /\u003e  For example, if a client were to purchase past service and the additional tax-deductible contribution required of the company was $200,000 and the company paid corporate tax at 15.5%, the tax refund of $31,000 (new funds otherwise unavailable to the client) would be enough to pay all of INTEGRIS’ fees for 17 years.  Moreover, the additional tax deductions and credits offered under a PPP, would add (rather than subtract) value to the client above and beyond what is possible under a RRSP.  To this, one must also take into consideration that the client will have substantially more registered assets available at retirement.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "at-what-point-does-it-make-economic-sense-for-a-person-to-upgrade-from-an-rrsp-to-a-ppp",
          ShortContent: "",
          Summary: "",
          Title:
            "At what point does it make economic sense for a person to upgrade from an RRSP to a PPP given that a PPP has certain additional costs not found in RRSPs (actuarial \u0026 administration)?",
          Guid: "2c7d69cf-af70-46ce-ada9-89a46a2589e8",
          Id: 84,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Can my investment manager be a discretionary portfolio manager?",
          FullContent: "Yes.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "can-my-investment-manager-be-a-discretionary-portfolio-manager",
          ShortContent: "",
          Summary: "",
          Title:
            "Can my investment manager be a discretionary portfolio manager?",
          Guid: "d042dcd0-3209-4665-a47f-f7114adf0658",
          Id: 85,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Is the pension paid at retirement taxed at the highest personal tax brackets?",
          FullContent:
            "The first $2,000 of pension income received is eligible for the pension credit (reducing the taxes otherwise payable).  Moreover, spouses can use the pension income splitting rules to allocate up to 50% of the pension income to a spouse who is not in receipt of a pension, thereby potentially moving the PPP member’s tax bracket to a lower bracket and reducing the couple’s overall taxes in the process.  When pension income splitting is used, the first $4,000 of pension income can be claimed as a ‘pension amount’ credit to further reduce individual taxes.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "is-the-pension-paid-at-retirement-taxed-at-the-highest-personal-tax-brackets",
          ShortContent: "",
          Summary: "",
          Title:
            "Is the pension paid at retirement taxed at the highest personal tax brackets?",
          Guid: "c8621aa1-b54a-48be-907b-db92fea43634",
          Id: 86,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "My corporation’s year-end is Oct 31. With the view of establishing a new PPP, please advise if there are any tax consequences for the corporation in deductions for tax purposes or whether the deductions will be going forward for next year.",
          FullContent:
            "Contributions made within 120 days of the corporate year-end are deductible in the immediately preceding corporate year.  For example, if corporate year-end is October 31, 2014, then 120 days after is Feb 28. Therefore contributions must be made no later than Feb 28 for them to be deductible in 2014.  However, while a PPP may be established after the corporate year-end, it must be submitted for registration before the calendar year end.\u003cbr /\u003e\u003cbr /\u003eTo ensure a contribution is deductible within a fiscal year for a new PPP, it is recommended that the plan be implemented (i.e. submission of application made to Canada Revenue Agency) prior to the end of the fiscal year. Despite the fact that a Company has 120 days after the fiscal year-end to make the contribution and have it deducted, a PPP should be implemented before the fiscal year-end to avoid situation where Canada Revenue Agency denies the deduction by arguing that the PPP was not in effect within the fiscal year. ",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "my-corporations-year-end-is-oct-31-with-the-view-of-establishing-a-new-ppp",
          ShortContent: "",
          Summary: "",
          Title:
            "My corporation’s year-end is Oct 31. With the view of establishing a new PPP, please advise if there are any tax consequences for the corporation in deductions for tax purposes or whether the deductions will be going forward for next year.",
          Guid: "702427d2-475b-4753-81fe-8545cb4f71e6",
          Id: 87,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Is it possible to hold real estate such as physical buildings/property within a PPP?  If so, how can it be held?",
          FullContent:
            "Yes, pension plans can hold direct holdings of real estate (act as the landlord) or shares of real estate holding corporations that in turn, are the landlord of the property.  The holding companies are tax-exempt because the shareholder is a registered pension plan (ie. The INTEGRIS PPP).",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "is-it-possible-to-hold-real-estate-such-as-physical-buildings-property-within-a-ppp",
          ShortContent: "",
          Summary: "",
          Title:
            "Is it possible to hold real estate such as physical buildings/property within a PPP?  If so, how can it be held?",
          Guid: "69d8e98d-2f01-42de-8a86-f97c4b01a78b",
          Id: 88,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName: "How does terminal funding work?",
          FullContent:
            "Terminal funding is a one-time tax-deductible funding opportunity to enhance the pension plan\u0027s basic pension with ancillary benefits.  This is an additional amount that the corporation can contribute at the time you retire or terminate the PPP.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "how-does-terminal-funding-work",
          ShortContent: "",
          Summary: "",
          Title: "How does terminal funding work?",
          Guid: "a1b26a02-a935-4659-8ea9-83841f9d6476",
          Id: 89,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Can I delay my retirement to age 71 and draw a bigger pension?  Can the professional corporation keep making contributions past age 65 until age 71? ",
          FullContent:
            "Yes, if you choose to delay your retirement to age 71, your professional corporation must continue to make contributions.  The pension payable will be higher than had you retired at the normal retirement age of 65.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "can-i-delay-my-retirement-to-age-71-and-draw-a-bigger-pension",
          ShortContent: "",
          Summary: "",
          Title:
            "Can I delay my retirement to age 71 and draw a bigger pension?  Can the professional corporation keep making contributions past age 65 until age 71? ",
          Guid: "d579e593-0ab4-4a75-9a0a-5099ef43b0ad",
          Id: 90,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Is inflation indexing as well as an unreduced pension at age 55 possible? ",
          FullContent:
            "Yes, if the corporation has the cash to upgrade benefits (indexing or early unreduced pension or CPP Bridge) then a further deduction can be claimed at that time to ‘purchase’ these indexing benefits.  This process is called “terminal funding”.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "is-inflation-indexing-as-well-as-an-unreduced-pension-at-age-55-possible",
          ShortContent: "",
          Summary: "",
          Title:
            "Is inflation indexing as well as an unreduced pension at age 55 possible? ",
          Guid: "2ff348f1-3047-4878-ac0d-73c6697f42cb",
          Id: 91,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "What happens to the residual of the PPP fund?  Does it get paid out as a lump sum to the estate if both spouses die early? Or is it forfeited to CRA?",
          FullContent:
            "No, the CRA does not receive PPP assets.  If both the member and the spouse die (say a car crash after the celebratory retirement party), and no guarantee period was selected at the time of pension commencement, then the plan is said to be in surplus.  The plan has discharged its liabilities so there are no other uses for the money except as provided by the terms of the plan.  The surplus can be paid back to the sponsor company, or distributed as the company sees fit.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "what-happens-to-the-residual-of-the-ppp-fund--does-it-get-paid-out-as-a-lump-sum-to-the-estate-if-both-spouses-die-early-or-is-it-forfeited-to-cra",
          ShortContent: "",
          Summary: "",
          Title:
            "What happens to the residual of the PPP fund?  Does it get paid out as a lump sum to the estate if both spouses die early? Or is it forfeited to CRA?",
          Guid: "4f002074-9bad-49fc-ab86-f4afca75b02c",
          Id: 92,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName: "Who owns the surplus of the plan?",
          FullContent:
            "The terms of the plan state that surplus belongs to the corporate sponsor of the plan.  Since it belongs to the sponsor of the plan (the company), the owners of the company can pay it back to the company and flow it through dividends to the shareholders.  That said, when the plan is first established, it is possible for surplus to be made payable to the plan member.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "who-owns-the-surplus-of-the-plan",
          ShortContent: "",
          Summary: "",
          Title: "Who owns the surplus of the plan?",
          Guid: "8af39754-3ab9-4012-b7c5-f900c3ee9ef1",
          Id: 93,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName: "Who determines when the member can collect?",
          FullContent:
            "CRA allows retirement income to commence as early as age 55 and the latest December 31st, in the year the member turns 71. ",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "who-determines-when-the-member-can-collect",
          ShortContent: "",
          Summary: "",
          Title: "Who determines when the member can collect?",
          Guid: "37799227-3365-4aa2-a305-38e7796ae8a8",
          Id: 94,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName: "Who owns the pension plan?",
          FullContent:
            "The company or Professional Corporation sponsors the plan. The trustees hold the assets on behalf of the members and their beneficiaries.   No one truly ‘owns’ the pension plan, since it is a bundle of liabilities/promises and corresponding assets.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "who-owns-the-pension-plan",
          ShortContent: "",
          Summary: "",
          Title: "Who owns the pension plan?",
          Guid: "f7ba8367-0ee4-458b-9e76-d4b73742850c",
          Id: 95,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "What happens to my RRSP room when I contribute to a PPP?",
          FullContent:
            "Your RRSP room will be adjusted once you set up your pension plan. This adjustment is called a Pension Adjustment (PA). ",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "what-happens-to-my-rrsp-room-when-i-contribute-to-a-ppp",
          ShortContent: "",
          Summary: "",
          Title: "What happens to my RRSP room when I contribute to a PPP?",
          Guid: "d13c7672-8aac-4501-9732-8a4054be28b9",
          Id: 96,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "What are the restrictions on investments held in a PPP; are they the same as RRSPs?",
          FullContent:
            "In a PPP, no more than 10% of the portfolio can be held in any one stock.  Moreover, a pension plan cannot hold more than 30% of the voting shares of a particular entity.  Also, certain investments are considered “related party transactions” and are prohibited.  A pension plan would not be allowed to invest in the shares of the sponsor of the PPP, even if it otherwise met the other tests discussed above.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "what-are-the-restrictions-on-investments-held-in-a-ppp-are-they-the-same-as-rrsps",
          ShortContent: "",
          Summary: "",
          Title:
            "What are the restrictions on investments held in a PPP; are they the same as RRSPs?",
          Guid: "4be60ed9-1615-4e6d-a19f-e6105797bba5",
          Id: 97,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "What happens if the sponsoring company cannot afford to make the minimum annual contributions to the IPP? ",
          FullContent:
            "Under an IPP, pension contributions must normally be made each year unless pensionable service is suspended. The plan sponsor may borrow to fund the plan. Under a conventional defined benefit only IPP, if this is not an option, the plan sponsor can elect to wind up the plan and turn it into a Locked-in Retirement Account (LIRA) or purchase an annuity from the assets of the fund.  Under an INTEGRIS defined benefit/defined contribution PPP, the plan sponsor has the option to switch from the defined benefit component to the defined contribution component of the plan where only 1% of the annual salary is the required contribution to the plan. In this way, there is no need to wind up the plan and the plan can continue as it is and until the corporation has the cash flow to maximize plan contributions.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "what-happens-if-the-sponsoring-company-cannot-afford-to-make-the-minimum-annual-contributions-to-the-ipp",
          ShortContent: "",
          Summary: "",
          Title:
            "What happens if the sponsoring company cannot afford to make the minimum annual contributions to the IPP? ",
          Guid: "46075ce4-a9f7-4b85-a392-53c5501a602a",
          Id: 98,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "What happens to the IPP in the event of a marital breakdown?",
          FullContent:
            "Provincial laws require pension plan assets to be treated in a manner similar to RRSP assets, as matrimonial assets to be divided between the member and spouse.   Each province has its own matrimonial property division regime and you should consult an INTEGRIS Pension Officer to discuss your specific circumstances.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "what-happens-to-the-ipp-in-the-event-of-a-marital-breakdown",
          ShortContent: "",
          Summary: "",
          Title: "What happens to the IPP in the event of a marital breakdown?",
          Guid: "59d757ae-b5ba-4591-bfd0-3e271b5c9a2c",
          Id: 99,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Sam went through a divorce a few years back and gave most of his RRSPs to his ex-wife in order to keep his businesses intact and therefore, does not have a lot accumulated in RRSPs. If Sam were to do a past service calculation/contribution, would the fact that he gave a large portion of his RRSPs to his ex in the settlement have any bearing on the past service calculation?",
          FullContent:
            "If Sam has no RRSP assets (gave everything to his ex-wife), and also has no RRSP room  (he might have maximized his RRSP contributions when he was still married), then his ability to buy back past service would be greatly reduced.\u003cbr /\u003e\u003cbr /\u003eHis age may allow him to nonetheless exceed the current year RRSP room substantially:  at 61, he’d be able to claim an additional tax deduction for $13,817 above the current RRSP limit.\u003cbr /\u003e\u003cbr /\u003eDepending on the number of years he’s eligible to buy back, the fact that he still has some RRSPs available (albeit a fraction of what he had pre-divorce) would still enable his company to also make a tax-deductible contribution.",
          LastRevisedDateLocal: "/Date(1544493124940)/",
          LastRevisedDateUtc: "/Date(1544511124940)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "sam-went-through-a-divorce-a-few-years-back-and-gave-most-of-his-rrsps-to-his-ex-wife-in-order-to-keep-his-businesses-intact",
          ShortContent: "",
          Summary: "",
          Title:
            "Sam went through a divorce a few years back and gave most of his RRSPs to his ex-wife in order to keep his businesses intact and therefore, does not have a lot accumulated in RRSPs. If Sam were to do a past service calculation/contribution, would the fact that he gave a large portion of his RRSPs to his ex in the settlement have any bearing on the past service calculation?",
          Guid: "9c5a66a0-b079-4eaa-b5c7-1a031b9efe20",
          Id: 100,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "As with many business owners, the majority of my net worth is tied up in my businesses and a beautiful cottage. What are some of the tax benefits of the PPP?",
          FullContent:
            "\u003cul\u003e\u003cli\u003eWhen selling off a business, terminal funding is great way to extract corporate assets in a tax-efficient manner as an exit strategy.\u003c/li\u003e\u003cli\u003eBy rolling in RRSPs to do a buy back of past service, an employer member, also be able to do a tax-deductible corporate contribution.\u003c/li\u003e\u003cli\u003eIf an employer wants to tax deduct (within the corporation) the management fees until retirement, a rollover of RRSPs into the Additional Voluntary Contribution subaccount is possible. \u003c/li\u003e\u003c/ul\u003e",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "as-with-many-business-owners-the-majority-of-my-net-worth-is-tied-up-in-my-businesses-and-a-beautiful-cottage-what-are-some-of-the-tax-benefits-of-the-ppp",
          ShortContent: "",
          Summary: "",
          Title:
            "As with many business owners, the majority of my net worth is tied up in my businesses and a beautiful cottage. What are some of the tax benefits of the PPP?",
          Guid: "9d80979f-9cc6-4652-8775-a7271a2d521d",
          Id: 101,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "What are the sources of cash contributions that I can make to the AVCs subaccount?",
          FullContent:
            'There are two main sources of cash that can be made to the Additional Voluntary Contribution subaccount:\u003col style="list-style-type: lower-roman;"\u003e\u003cli\u003eRRSPs (unlocked) can be transferred in at any time;\u003c/li\u003e\u003cli\u003eEmployee voluntary contributions can be made at any time when the member has elected to participate in the Defined Contribution component of the plan and is therefore accruing a DC pension under the plan.\u003c/li\u003e\u003c/ol\u003e',
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "what-are-the-sources-of-cash-contributions-that-i-can-make-to-the-avcs-subaccount",
          ShortContent: "",
          Summary: "",
          Title:
            "What are the sources of cash contributions that I can make to the AVCs subaccount?",
          Guid: "102299b6-0f9c-4ef3-8a91-e9dc877f44d8",
          Id: 102,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "What is the benefit of transferring my RRSPs into the Defined Benefit component as a qualifying transfer when the member has selected a DB accrual? ",
          FullContent:
            "This would enable you to claim the HST credit and get creditor protection that is not available when the assets are inside an RRSP account.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "what-is-the-benefit-of-transferring-my-rrsps-into-the-defined-benefit-component-as-a-qualifying-transfer-when-the-member-has-selected-a-db-accrual",
          ShortContent: "",
          Summary: "",
          Title:
            "What is the benefit of transferring my RRSPs into the Defined Benefit component as a qualifying transfer when the member has selected a DB accrual? ",
          Guid: "a6825592-8179-4436-9dd3-2ddbc4728835",
          Id: 103,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "I have a daughter who works in my business. Is there a benefit to having her become a member of my PPP?",
          FullContent:
            "If your daughter works with you in your business, she could also become a plan member in the PPP that is set up for you and any surplus that could develop in the plan would pass to your daughter without creating any probate issues, upon your death.  ",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "i-have-a-daughter-who-works-in-my-business.-is-there-a-benefit-to-having-her-become-a-member-of-my-ppp",
          ShortContent: "",
          Summary: "",
          Title:
            "I have a daughter who works in my business. Is there a benefit to having her become a member of my PPP?",
          Guid: "a5fc94fd-d925-4939-893a-29d0d511af5f",
          Id: 104,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Is there any reason why an individual with a corporation who receives T4 income and generally maximizes his RRSP contribution from year to year should pick an RRSP over a PPP?",
          FullContent:
            'There are two situations where you would not suggest a PPP:\u003col type="a"\u003e\u003cli\u003eIf the client wants to invest all of his assets in a single security pension plans have a 10% concentration test.\u003c/li\u003e\u003cli\u003eIf the client is treating the account as a savings account to be used for current consumptions. This is not possible under a pension plan because of the locking in rules.\u003c/li\u003e\u003c/ol\u003e\u003cbr /\u003eFor anyone else it usually makes no sense to remain in an RRSP. ',
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "is-there-any-reason-why-an-individual-with-a-corporation-who-receives-t4-income-and-generally-maximizes-his-rrsp-contribution-from-year-to-year",
          ShortContent: "",
          Summary: "",
          Title:
            "Is there any reason why an individual with a corporation who receives T4 income and generally maximizes his RRSP contribution from year to year should pick an RRSP over a PPP?",
          Guid: "de9b7f84-40f7-4c79-a8ea-a123fe6279e1",
          Id: 105,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "If a PPP is collapsed, does the corporation lose its tax deductions, which were taken prior to the collapse?",
          FullContent:
            "Not if the PPP is collapsed in the normal course because the company decides to no longer sponsor it, or for any other business reasons.\u003cbr /\u003e\u003cbr /\u003ee.g. Corporation paid $100,000 into the PPP and takes its 15+% in write-offs; then the PPP is collapsed, is the 15+% in write-offs now payable?\u003cbr /\u003e\u003cbr /\u003eIn the example above, once the deduction is taken, it is permanent.  There are no other accounting or other equalization that must be taken into consideration.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "if-a-ppp-is-collapsed,-does-the-corporation-lose-its-tax-deductions,-which-were-taken-prior-to-the-collapse",
          ShortContent: "",
          Summary: "",
          Title:
            "If a PPP is collapsed, does the corporation lose its tax deductions, which were taken prior to the collapse?",
          Guid: "f48949e4-71a4-48e9-b655-1b24dae3411d",
          Id: 106,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "If there were 3 connected shareholders in a PPP, do they all get the same investment portfolio and gain on a % of shares owned in the Corporation holding the PPP?",
          FullContent:
            "We don’t encourage 3 connected shareholders to be in a single PPP, rather we encourage the company to sponsor 3 individual PPPs, one for each connected person.  In exceptional circumstances, where we agreed to have 3 connected persons join a single PPP, INTEGRIS would look to the company sponsoring the PPP for direction as to what the investment portfolio would look like.  It would be up to the company (and their own internal processes, whether based on % of shares owned or some other mechanism) to tell us how the investments are to take place.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "if-there-were-3-connected-shareholders-in-a-ppp-do-they-all-get-the-same-investment-portfolio-and-gain-on-a-percentage-of-shares",
          ShortContent: "",
          Summary: "",
          Title:
            "If there were 3 connected shareholders in a PPP, do they all get the same investment portfolio and gain on a % of shares owned in the Corporation holding the PPP?",
          Guid: "d899b5aa-2c43-4596-bd74-00bf84660338",
          Id: 107,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "On death, does each connected shareholder get to designate where their % goes if they die? In such case, they can ensure that the value of their pension is not given to related connected shareholder rather than a family member?",
          FullContent:
            "Yes, under pension law, each plan member has a right to designate a personal ‘beneficiary’ in instances of death (where the member has no spouse, since a spouse is an automatic beneficiary upon a member’s death (unless a written waiver has been used to waive away this statutory right)).  There is therefore no cross-subsidization of wealth across the estates of connected members in a single PPP.  This is a moot point when each member has his or her own PPP.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "on-death-does-each-connected-shareholder-get-to-designate-where-their-percentage-goes-if-they-die-in-such-case",
          ShortContent: "",
          Summary: "",
          Title:
            "On death, does each connected shareholder get to designate where their % goes if they die? In such case, they can ensure that the value of their pension is not given to related connected shareholder rather than a family member?",
          Guid: "7a218bfd-2030-47f7-b50a-5c9065ccb97c",
          Id: 108,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Does the INTEGRIS PPP, permit the corporation’s connected shareholders to avoid participating in the proposed Ontario PRPP?",
          FullContent:
            'Yes.  The Ministry of Finance has released a technical bulletin setting out the principles under which it would find that an existing hybrid pension plan would be considered a "Comparable Plan" and thus, exempt from the scope of the Ontario Retirement Pension Plan ("ORPP").\u003cbr /\u003e\u003cbr /\u003eBecause the defined benefit component of the PPP has an accrual rate that is 4 times higher than the minimum required for ORPP exemption purposes, the PPP qualifies as a "comparable plan".\u003cbr /\u003e\u003cbr /\u003eTechnical information on this can be found on the website of the Ontario Ministry of Finance: \u003ca href="http://www.fin.gov.on.ca/en/pension/orpp/bulletin-100815.html"\u003ehttp://www.fin.gov.on.ca/en/pension/orpp/bulletin-100815.html\u003c/a\u003e',
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "does-the-integris-ppp-permit-the-corporations-connected-shareholders-to-avoid-participating-in-the-proposed-ontario-prpp",
          ShortContent: "",
          Summary: "",
          Title:
            "Does the INTEGRIS PPP, permit the corporation’s connected shareholders to avoid participating in the proposed Ontario PRPP?",
          Guid: "a2a75e47-8fc9-4859-814f-21c2d3dd97b3",
          Id: 109,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Where a client saves under the DC component of the PPP and sets their salary at a modest level to avoid excess personal taxation, does this mean that that the client can use this model to \u0027beat\u0027 a RRSP---up to $440 contribution / year more?",
          FullContent:
            "Yes, the strategy is to use the DC model to beat the RRSP limits ($440 more this year), but more importantly to allow the corporation to tax-deduct all of the investment and administration fees from corporate income tax at the same time.  If the RRSP holder used to pay $10,000 a year in fees, none of those were tax-deductible.  With the DC plan, the RRSPs can be rolled into the AVC subaccount, and the $10,000 now becomes a new tax deduction to the company.  This has two impacts:  at 15.5% corporate tax rate, this creates a $1,500 tax refund (fresh new money in the pocket), and it means that at the end of the year, there are $10,000 (+ interest) more money compounding in a tax-deferred account than in the case of the RRSP (since those funds were withdrawn at source).",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "where-a-client-saves-under-the-dc-component-of-the-ppp-and-sets-their-salary-at-a-modest-level-to-avoid-excess-personal-taxation",
          ShortContent: "",
          Summary: "",
          Title:
            "Where a client saves under the DC component of the PPP and sets their salary at a modest level to avoid excess personal taxation, does this mean that that the client can use this model to \u0027beat\u0027 a RRSP---up to $440 contribution / year more?",
          Guid: "4997d301-b4d5-40f8-b595-bb574321e322",
          Id: 110,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            'Under the PPP, a client can roll their RRSPs into the Additional Voluntary Contribution subaccount, triggering large additional corporate tax deductions in connection with the administrative and investment management fees?  Please explain what is an AVC subaccount and expand on what are and how the additional corporate tax deductions are "large"?',
          FullContent:
            "Imagine a business owner with $500,000 in RRSPs and paying a Management Expense Ratio of 2%.  This person is paying $10,000 a year in fees, and because it is an RRSP, he/she is not allowed to claim any deductions (see paragraph 18(1)(u) of the Income Tax Act (Canada)).\u003cbr /\u003e\u003cbr /\u003eThis same business owner sets up a (modest DC-only) PPP.  The owner decides to roll all of the $500,000 in RRSPs into the Additional Voluntary Contribution subaccount found inside of the PPP.  Under paragraph 18(1)(a) of the Income Tax Act, the corporate sponsor of the PPP can now claim a tax deduction of $10,000 from its corporate income tax, in addition to whatever it contributes to the PPP on behalf of the business owner.  With a $1 M account, the deductions could reach $20,000.  This is why we call them \u0027large\u0027.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "under-the-ppp-a-client-can-roll-their-rrsps-into-the-additional-voluntary-contribution-subaccount",
          ShortContent: "",
          Summary: "",
          Title:
            'Under the PPP, a client can roll their RRSPs into the Additional Voluntary Contribution subaccount, triggering large additional corporate tax deductions in connection with the administrative and investment management fees?  Please explain what is an AVC subaccount and expand on what are and how the additional corporate tax deductions are "large"?',
          Guid: "46a2c786-57fe-4b4c-9266-0786e0f88cf8",
          Id: 111,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Can the amounts transferred from an RRSP into an AVC and all voluntary contributions made to the AVC sub-account be accessed (withdrawn) by the connected member of a PPP?What are ‘voluntary contributions’ and do they qualify for tax write-offs?",
          FullContent:
            "Yes, all contributions rolled into the AVC from RRSPs, or any voluntary employee contributions are exempt from “locking-in”. They can be withdrawn prior to retirement (unlike regular pension contributions) of the PPP.  This requires a plan amendment to eliminate the AVC subaccount.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "can-the-amounts-transferred-from-an-rrsp-into-an-avc-and-all-voluntary-contributions-made-to-the-avc-sub-account-be-accessed",
          ShortContent: "",
          Summary: "",
          Title:
            "Can the amounts transferred from an RRSP into an AVC and all voluntary contributions made to the AVC sub-account be accessed (withdrawn) by the connected member of a PPP?What are ‘voluntary contributions’ and do they qualify for tax write-offs?",
          Guid: "39892f1f-577b-4200-8ab2-af776aea38a0",
          Id: 112,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName: "How is the defined benefit calculated?",
          FullContent:
            "The defined benefit under the plan is calculated based on a formula set out in the plan. It is 2% of the average of the highest 3 consecutive years of indexed salary paid by the company multiplied by the member\u0027s years of service. The member\u0027s defined benefit is subject to a maximum pension amount set by the Canada Revenue Agency.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "how-is-the-defined-benefit-calculated",
          ShortContent: "",
          Summary: "",
          Title: "How is the defined benefit calculated?",
          Guid: "54a24f5c-11c9-48b4-b4bb-dc3186727fd3",
          Id: 113,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "If someone is paid in dividends and never in salary or T4 Income, how is pension calculated?",
          FullContent:
            "To be eligible for a PPP under which a person accrues a pension, that person must be in receipt of T4 income. A person who is paid dividends, is not eligible to have a PPP.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "if-someone-is-paid-in-dividends-and-never-in-salary-or-t4-income-how-is-pension-calculated",
          ShortContent: "",
          Summary: "",
          Title:
            "If someone is paid in dividends and never in salary or T4 Income, how is pension calculated?",
          Guid: "2de7b57a-af5a-45d5-a918-62ce43cf0b03",
          Id: 114,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Has the Canada Revenue Agency approved the INTEGRIS PPP?",
          FullContent:
            "The INTEGRIS PPP has been pre-approved by the Canada Revenue Agency. ",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "has-the-canada-revenue-agency-approved-the-integris-ppp",
          ShortContent: "",
          Summary: "",
          Title: "Has the Canada Revenue Agency approved the INTEGRIS PPP?",
          Guid: "8cc65d32-69c3-4489-9738-84b8f4829c75",
          Id: 115,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "How is the buyback of past years of service determined? What variables are used in calculating past service buyback years?",
          FullContent:
            'The buyback of past years of service for a PPP member is calculated from the date of incorporation of the company sponsoring the PPP for years during which the member was not a member of a pension plan. The cost to buyback service for a year is based on the annual income earned by the member for that year.\u003cbr /\u003e\u003cbr /\u003eThe variables used by the actuary to calculate the total cost of the buyback are as follows:\u003col type="a"\u003e\u003cli\u003eHow many years of past service are available? (Did the owner pay himself T4 income in those years?)\u003c/li\u003e\u003cli\u003eWhat level of T4 income was paid all along to the owner during those years to be bought back?\u003c/li\u003e\u003cli\u003eWhat is the current level of RRSP available to calculate the Past Service Pension Adjustment and the Qualifying Transfer?\u003c/li\u003e\u003cli\u003eWhat is the expected salary level for the owner going forward?\u003c/li\u003e\u003c/ol\u003e',
          LastRevisedDateLocal: "/Date(1540221218290)/",
          LastRevisedDateUtc: "/Date(1540235618290)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "how-is-the-buyback-of-past-years-of-service-determined-what-variables-are-used-in-calculating-past-service-buyback-years",
          ShortContent: "",
          Summary: "",
          Title:
            "How is the buyback of past years of service determined? What variables are used in calculating past service buyback years?",
          Guid: "3235a84c-b2dd-4c59-aad3-c5820b8122a5",
          Id: 116,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName: "Why does a PPP have to be a designated plan?",
          FullContent:
            'The tax-deductible contributions that can be made to an individual pension plan (or under the defined benefit component of a Personal Pension Plan) depend, in part, on whether the pension plan is considered a “\u003cstrong\u003edesignated plan\u003c/strong\u003e” or not.\u003cbr /\u003e\u003cbr /\u003eIt will be considered a “designated plan” when most of the plan members are classified as “\u003cstrong\u003especified individuals\u003c/strong\u003e”.\u003cbr /\u003e\u003cbr /\u003eTo be considered a “specified individual” one usually falls under one of two categories:\u003cul style="list-style-type: circle;"\u003e\u003cli\u003eThe member is a “\u003cstrong\u003econnected person\u003c/strong\u003e” or\u003c/li\u003e\u003cli\u003eThe member earns more than 2.5 times the Year’s Maximum Pensionable Earnings (in 2015, the YMPE is $53,600 so the income limit is $134,000.)\u003c/li\u003e\u003c/ul\u003eA “connected person”, generally, owns 10% or more of the shares of the company sponsoring the IPP or PPP.\u003cbr /\u003e\u003cbr /\u003eTherefore, someone earning $140,000 and who owns 11% of the shares would be a “specified individual” under both tests.  Someone earning $50,000 and owning 11% would also be a “specified individual” by virtue of being a connected person.  See examples below:\u003cbr /\u003e\u003cbr /\u003e\u003ctable style="width:90%;"\u003e\u003ctr\u003e\u003ctd\u003eShare Ownership\u003c/td\u003e\u003ctd\u003eSalary\u003c/td\u003e\u003ctd\u003eStatus\u003c/td\u003e\u003c/tr\u003e\u003ctr\u003e\u003ctd\u003e\u003cstrong\u003e9%\u003c/strong\u003e\u003c/td\u003e\u003ctd\u003e130,000\u003c/td\u003e\u003ctd\u003eNon Specified\u003c/td\u003e\u003c/tr\u003e\u003ctr\u003e\u003ctd\u003e\u003cstrong\u003e11%\u003c/strong\u003e\u003c/td\u003e\u003ctd\u003e130,000\u003c/td\u003e\u003ctd\u003eSpecified\u003c/td\u003e\u003c/tr\u003e\u003ctr\u003e\u003ctd\u003e\u003cstrong\u003e9%\u003c/strong\u003e\u003c/td\u003e\u003ctd\u003e134,100\u003c/td\u003e\u003ctd\u003eSpecified\u003c/td\u003e\u003c/tr\u003e\u003ctr\u003e\u003ctd\u003e\u003cstrong\u003e11%\u003c/strong\u003e\u003c/td\u003e\u003ctd\u003e70,000\u003c/td\u003e\u003ctd\u003eSpecified\u003c/td\u003e\u003c/tr\u003e\u003ctr\u003e\u003ctd\u003e\u003cstrong\u003e15%\u003c/strong\u003e\u003c/td\u003e\u003ctd\u003e140,000\u003c/td\u003e\u003ctd\u003eSpecified\u003c/td\u003e\u003c/tr\u003e\u003c/table\u003e\u003cbr /\u003e\u003cbr /\u003eUltimately, being a “designated plan” means that specific funding restrictions and actuarial assumptions must be used in calculating the maximum pension contributions made by the sponsoring company',
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "why-does-a-ppp-have-to-be-a-designated-plan",
          ShortContent: "",
          Summary: "",
          Title: "Why does a PPP have to be a designated plan?",
          Guid: "fdb1a90b-ed62-41fa-9f57-713e6fd6d58e",
          Id: 117,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "I’m not clear on how once the member has opted for the DC component of the PPP for a number of years, he can buy back past service under the DB component of the plan for those years, when he is close to retirement. Please explain.",
          FullContent:
            "So long as the PPP member who has opted for the DC component of the Plan for a number of years maintained T4 income throughout, he can do a plan conversion prior to retirement turning the DC years into DB years, and then doing the past service buy back.   If the member opted for DC because there was no money around and he didn’t want to wind up his PPP, then you are correct that by selecting a lower salary while under the DC rules, there would be less financial gains to convert to DB.  There is still some advantage, but it isn’t as pronounced.\u003cbr /\u003e\u003cbr /\u003eNote that terminal funding creates a new tax deduction for the company at retirement that doesn’t exist in the money purchase provision, even if the lifetime retirement benefits are lower than what is possible to get.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "im-not-clear-on-how-once-the-member-has-opted-for-the-dc-component-of-the-ppp-for-a-number-of-years",
          ShortContent: "",
          Summary: "",
          Title:
            "I’m not clear on how once the member has opted for the DC component of the PPP for a number of years, he can buy back past service under the DB component of the plan for those years, when he is close to retirement. Please explain.",
          Guid: "68c3ee5d-46f6-4746-95ef-e0735b6793a8",
          Id: 118,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "What types of tax slips are issued?  Who issues those tax slips?",
          FullContent: "The CRA T3P slip is prepared by INTEGRIS",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "what-types-of-tax-slips-are-issued--who-issues-those-tax-slips",
          ShortContent: "",
          Summary: "",
          Title:
            "What types of tax slips are issued?  Who issues those tax slips?",
          Guid: "9bbec3eb-f50f-4465-be51-a355feac9085",
          Id: 119,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "What happens if a client wants to transfer their PPP to another firm?   Are these accounts transferable to another firm?",
          FullContent:
            "Yes, a PPP can be transferred to another firm provided that the recipient firm agrees to and has the system, processes and mechanisms in place to administer the PPP.  If they want to take their PPP elsewhere, they can.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "what-happens-if-a-client-wants-to-transfer-their-ppp-to-another-firm",
          ShortContent: "",
          Summary: "",
          Title:
            "What happens if a client wants to transfer their PPP to another firm?   Are these accounts transferable to another firm?",
          Guid: "a2ca2be8-2c7e-4bb1-9706-c69576ec6866",
          Id: 120,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "What is the process for estates on the death of the client?",
          FullContent:
            "The death benefits arising under the PPP is administered in accordance with the terms of the plan and in accordance with the death benefit provisions under applicable legislation. Death Benefits are generally paid to spouses, beneficiaries and estates. ",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "what-is-the-process-for-estates-on-the-death-of-the-client",
          ShortContent: "",
          Summary: "",
          Title: "What is the process for estates on the death of the client?",
          Guid: "01a07e10-e5fc-4405-97c8-430065b321a6",
          Id: 121,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName: "What is the potential market size?",
          FullContent:
            "In Canada, there are about 1.2 Million Canadians who could avail themselves of the PPP and only 15,000 IPPs registered with the Canada Revenue Agency.",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "what-is-the-potential-market-size",
          ShortContent: "",
          Summary: "",
          Title: "What is the potential market size?",
          Guid: "558f3fea-30d5-43a6-a324-d937488ded8c",
          Id: 122,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1427328000000)/",
          DatePostedUtc: "/Date(1427342400000)/",
          DisplayName:
            "Please provide more information and explanation on “flexible contributions”.",
          FullContent:
            "The INTEGRIS PPP Plan design offers three subaccounts under one plan registration:  DB (IPP), DC and AVC.  Member gets to pick each year which subaccount to save under.  DB allows for maximum tax deductions (since it operates exactly like an IPP).  The flexibility comes in being able to elect to move to DC where the contribution is set at 1% of T4 income.  Additional and voluntary employee contributions are also allowed (0% to 17% of T4 income) and are deposited into the AVC subaccount. ",
          LastRevisedDateLocal: "/Date(1427328000000)/",
          LastRevisedDateUtc: "/Date(1427342400000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "please-provide-more-information-and-explanation-on-flexible-contributions",
          ShortContent: "",
          Summary: "",
          Title:
            "Please provide more information and explanation on “flexible contributions”.",
          Guid: "bc677200-2cb9-44db-a22d-c9e1c158111a",
          Id: 123,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1411257600000)/",
          DatePostedUtc: "/Date(1411272000000)/",
          DisplayName:
            "In the year that I set up my INTEGRIS PPP, can I also make a contribution to my RRSP?",
          FullContent:
            'Normally, yes… however, please note that the full RRSP contribution amount may not be available in that year if you are considered a \u003cspan style="text-decoration:underline;"\u003econnected person\u003c/span\u003e\u003csup style="font-size:smaller;vertical-align:sup;"\u003e[1]\u003c/sup\u003e. \u003ca href="https://www.integris-mgt.com/Articles/in-the-year-that-i-set-up-my-integris-ppp"\u003eClick here\u003c/a\u003e for more details.\u003cbr /\u003e\u003cbr /\u003e\u003csup style="font-size:smaller;vertical-align:sup;"\u003e[1]\u003c/sup\u003e Someone who owns 10% or more of any class of shares of the employer corporation that sponsors the Personal Pension Plan.',
          LastRevisedDateLocal: "/Date(1457961660280)/",
          LastRevisedDateUtc: "/Date(1457976060280)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "in-the-year-that-i-set-up-my-integris-ppp-can-i-also-make-a-contribution-to-my-rrsp",
          ShortContent: "",
          Summary: "",
          Title:
            "In the year that I set up my INTEGRIS PPP, can I also make a contribution to my RRSP?",
          Guid: "cc6474a7-269b-4411-b732-cb5793948f57",
          Id: 58,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1342310400000)/",
          DatePostedUtc: "/Date(1342324800000)/",
          DisplayName: "How much will this cost me?",
          FullContent:
            "There are three components to the costs: the INTEGRIS fee, the investment management fee and if you have selected a trust company to hold your assets, the trustee fee.  When combined, INTEGRIS clients pay less than holders of equity mutual fund. Moreover, our clients do not pay any hidden trailers, commissions to sales people nor deferred sales charges common to mutual funds RRSPs. The INTEGRIS fee covers all set-up, actuarial valuation and administration costs.",
          LastRevisedDateLocal: "/Date(1342310400000)/",
          LastRevisedDateUtc: "/Date(1342324800000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "how-much-will-this-cost-me",
          ShortContent: "",
          Summary: "",
          Title: "How much will this cost me?",
          Guid: "92c6a4dc-f905-4dbb-9a86-e37a8a1509af",
          Id: 14,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1342310400000)/",
          DatePostedUtc: "/Date(1342324800000)/",
          DisplayName: "Do I need to be incorporated?",
          FullContent:
            "Yes. If you haven\u0027t incorporated, INTEGRIS can provide you with a corporation for $400.",
          LastRevisedDateLocal: "/Date(1342310400000)/",
          LastRevisedDateUtc: "/Date(1342324800000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "do-i-need-to-be-incorporated",
          ShortContent: "",
          Summary: "",
          Title: "Do I need to be incorporated?",
          Guid: "b8808ee0-0ce8-4a92-ae1d-6cb6170ef826",
          Id: 15,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1342310400000)/",
          DatePostedUtc: "/Date(1342324800000)/",
          DisplayName:
            "How much can I contribute each year and claim a tax deduction?",
          FullContent:
            "From as low as 1% of salary paid by your professional corporation, all the way up to about 30% of salary (depending on your age).",
          LastRevisedDateLocal: "/Date(1342310400000)/",
          LastRevisedDateUtc: "/Date(1342324800000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route:
            "how-much-can-i-contribute-each-year-and-claim-a-tax-deduction",
          ShortContent: "",
          Summary: "",
          Title:
            "How much can I contribute each year and claim a tax deduction?",
          Guid: "8437d371-4814-43b2-99cb-7e5eb29e4cf7",
          Id: 16,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1342310400000)/",
          DatePostedUtc: "/Date(1342324800000)/",
          DisplayName: "What kinds of investments are you providing?",
          FullContent:
            "Depending on your preference: pooled funds, mutual funds, GICs, shares and bonds are available.",
          LastRevisedDateLocal: "/Date(1342310400000)/",
          LastRevisedDateUtc: "/Date(1342324800000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "what-kinds-of-investments-are-you-providing",
          ShortContent: "",
          Summary: "",
          Title: "What kinds of investments are you providing?",
          Guid: "84471cf1-00bd-41b9-bde9-ba6f956caa32",
          Id: 17,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        },
        {
          Author: "",
          DatePostedLocal: "/Date(1342310400000)/",
          DatePostedUtc: "/Date(1342324800000)/",
          DisplayName: "Does anyone else offer such a program?",
          FullContent:
            "Pension legislation is complex and cumbersome. Financial institutions prefer to act as service providers for a fee and leave the administrative burden with the client. We fill a niche in the market for busy professionals who want the tax advantages of a pension plan without the administrative obligations.",
          LastRevisedDateLocal: "/Date(1342310400000)/",
          LastRevisedDateUtc: "/Date(1342324800000)/",
          ReadMore:
            "                                                                                                                                                                                                                                                                ",
          Route: "does-anyone-else-offer-such-a-program",
          ShortContent: "",
          Summary: "",
          Title: "Does anyone else offer such a program?",
          Guid: "fc30a167-b08c-4b8e-9ddc-46803832740c",
          Id: 19,
          SecurityPermissions: null,
          TimeZone: "Eastern Standard Time"
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.btn {
  text-align: left;
  font-weight: bolder;
}
</style>
