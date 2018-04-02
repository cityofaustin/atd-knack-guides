[Data Tracker Guides](./) > [Signs & Markings](/signs_markings#signs-and-markings-data-tracker-user-guides) > [Job Management](job_management.md)

# Managing Work Jobs

- [About Jobs](#about-jobs)
- [Create a Job](#create-a-job)
- [Find Jobs](#find-jobs)
- [Complete a Job](#complete-a-job)
- [Re-Open a Job](#re-open-a-job)
- [Cancel a Job](#cancel-a-job)

## About Jobs

Each work order contains one or more **jobs** which are to be completed by individual workgroups (Long Line, Short Line, Specialty Markings, etc.). A job may have one of four statuses:

Status      | Description
:---        | :--- 
**NEW**       | The job has not been issued to the workgroup.
**ISSUED**    | The job is ready to be completed by the workgroup.
**COMPLETED** | The job has been completed by workgroup and submitted for review.
**HOLD**      | The work order has been placed on hold.

## Create a Job

There are two mechanisms for creating jobs:

##### Auto-Generated Jobs
When a Markings work order is created, jobs for each of the selected workgroups are created automatically. See [Create a Work Order](create_work_order_non_tech.md) for more details.

##### Manually Create a Job
Jobs can be manually added to any work order, provided the work order is not **CLOSED** or **ON HOLD**. See [Manage Work Orders (COMING SOON)](#TODO) for more details.


## Find Jobs

**User Role Required**: Viewer

1. Visit the jobs landing page: http://transportation.austintexas.io/data-tracker/#home/work-jobs-markings/

2. By default, the Jobs table displays jobs which have been ISSUED to work groups. Each row in the table represents a single jobs that must be completed, and the jobs are grouped by the workgroup assigned to the job. Additional tabs display jobs that are NEW, COMPLETED, and on HOLD.

3. The search box at the top of the jobs table enabes searching by keyword. Partial words are accepted.

4. To view a job's details, click on the details icon in the left-most column of the table.

## Complete a Job

**User Role Required**: Technician

1. Follow the steps in [Find Jobs](#find-jobs) to find and view **Job Details**.

    The **Job Details** page displays relevant information about the job, as well as forms to submit information about work that was completed.

2. Scroll down the page to find tables for Time, Specifications, and Materials. There is a form below each table which will allow you to submit entries for each section of the job. 

    **Note**: The job entry forms will only be displayed if the job has status of **ISSUED** and if the user's role is **Technician**.

3. To add an entry for any section of the **Job Details**, complete the form fields in the section, then click the blue button to submit the form. A green confirmation message will confirm that the entry was successfully submitted, and a new row will display in that section's entry table.

    ![Add Specification](https://raw.githubusercontent.com/cityofaustin/data-tracker-guides/master/images/add_specification.png)
    *The Specifications section with a successfully-submitted entry*

4. Continue to add entries for Time, Specifications, and Materials as needed. You may remove entries from by clicking the trash bin icon under the **Remove** column of any of the job tables.

5. Once at least one entry has been submitted for each section of the work order\*, it is possible to mark the job as completed. To complete the job, click the **Complete Job** button at the top of the **Job Details** page.

6. From the confirmation window that appears, click the blue **Complete Job** button to mark the job as completed.

    *\*Note: Specifications are not required for the Raised Pavement Markings (RPM) group*

## Re-Open a Job

**User Role Required**: Technician

A completed job may be re-opened if it meets the following conditions:

- The job's status is **COMPLETED**
- The work order status is not **CLOSED** or **ON HOLD**

1. To re-open a job, click the **Re-Open Job** button at the top of the **Job Details** page.

2. From the confirmation window that appears, click the blue **Re-Open Jobs** button to re-open the job.

## Cancel a Job

**User Role Required**: Technician

A job may be cancelled if it meets the following conditions:

- No Time, Specifications, or Materials entries have been added to the job.
- The job status is **NEW** or **ISSUED**

1. To cancel a job, click the **Cancel Job** button at the top of the **Job Details** page.

2. From the confirmation window that appears, click the blue **Cancel Jobs** button to cancel the job.













