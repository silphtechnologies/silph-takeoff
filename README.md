# SILPH Takeoff

Open-source software for project take-off tracking. Start with an idea quotation, end with an invoice!

- Based onto SSO most common login provider (Google, Apple, GitHub at first);
- Fully implemented out-of-the-box, ready to deploy onto GCP environments;
- Sprint tracking, date reminding, alert missing. Based onto `mailgun` service;
- Angular PWA for smarter use as native app or as web app;
- Role segregation for project and organization;
- Integrated with Stripe&copy; dashboard for payment collection;
- Based for Premium Tier features

[TOCM]

#DB Description
Database is based onto a relational one with a basic-but-strong logic behind:

+ Root objects are `Organization`s that has many relations with `Project` and `User` (that univoquely belongs to only one `Organization`); also have many relations with `User` for admin recognition;

------------
+ Every `Project` has a partecipation into several many to many relationships that have to indicate admin, managers, editors and viewers; also have an array of `WorkedHours`that indicates **daily amount of worked hour per project**

------------
+ Every `User` has a status payment boolean flag setted when paid for premium plan;


#License
SILPH Takeoff is MIT licensed
