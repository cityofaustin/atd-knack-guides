[Data Tracker Guides](./) > [Signs & Markings](/signs_markings#signs-and-markings-data-tracker-user-guides) > [Work Order Management](work_order_management.md)

# Managing Work Orders

- [About Work Orders](#about-work-orders)
- [Find a Work Order](#find-a-work-order)
- [Create a Work Order](#create-a-work-order)
- [Edit a Work Order](#edit-a-work-order)
- [Put a Work Order ON HOLD](#put-a-work-order-on-hold)

## About Work Orders

Work Orders are the process by which Signs & Markings work is requested, dispatched, and completed. The overall workflow is:

1. A user creates a new work order which specifies the location and type of work to be completed.
2. If the user is not a technician, plans must be attached to the work order after it is created.
3. A supervisor reviews the work order and issues individual jobs to work groups.
4. Work groups complete their jobs.
5. An analyst reviews the work order and updates asset information in GIS.
6. A supervisor reviews the work order and closes it.


Each work order may have one of six statuses:

Status                  | Description|
:---                    | :--- |
**NEED TO BE ISSUED**   | The work order has been created but there are jobs that are not issued. |
**ISSUED**              | All jobs have been issued. |
**ON HOLD**             | The work order is on hold. See **HOLD REASON** for details. |
**NEEDS GIS**           | All jobs have been completed and the work order is ready for GIS Q/A Review |
**FINAL REVIEW**        | All jobs and GIS Q/A Review have been completed and the work order is ready for final review. |
**CLOSED**              | Final review is complete and the work order has been closed. |

## Find a Work Order

##### User Role Required: Viewer

1. Visit the work orders landing page: http://transportation.austintexas.io/data-tracker/#home/work-jobs-markings/

2. By default, the Work Order table displays all work orders. Additional tabs display work orders that are filtered based on their status.

3. The search box at the top of the work orders table enables searching by keyword. Partial words are accepted.

4. To view a work order's details, click on the details icon in the left-most column of the table.

## Create a Work Order

##### User Role Required: Viewer or Technician

1. Work Orders Landing Page: http://transportation.austintexas.io/data-tracker/#home/work-orders-markings/

2. Click **New Work Order** button.

3. Complete New Work Order form:
    - **Work Type**: Signs or Markings | Required. Hidden if user role is Technician.
    
    - **Requester**: The business unit requesting the work.  | Required. Hidden and set to **MAINTENANCE** if user role is Technician.
    
    - **Work Groups**: The Markings work group(s) that will complete the work. | Required.
    
    - **311 SR #**: The Signs or Markings 311 service request number related to this work order. | Optional. Only displayed when requester is **MAINTENANCE**.
    
    - **Maximo ID**: | Optional. Only displayed when Work Type is Signs
    
    - **Engineering Work Order ID**: the ID of the requester's work order | Optional. Hidden if user role is Technician.
    
    - **Regulation #**: | Optional. Work order will be placed on hold until reg is attached. Hidden if user role is Technician.
    
    - **Coordination Need**: If the work requires coordination across multiple ATD divisions | Required if requester is not **MAINTENANCE** or **SBO / WHEREABOUTS**.
    
    - **Instructions and Comments**: Description of the work to be completed and any additional comments | Required.

    - **Location Type**: Select from: Intersection, Section of Road, or Specific Location | Required.
    
    - **Primary Street:** The name of the primary street at which work will be completed. | Required.
    
    - **Cross Street**: The name of the cross street at which work will be completed | Required if Location Type is Intersection.
    
    - **From Street**: The name of the first cross street that intersects with the primary street at which work will be completed | Required if Location Type is Section of Road.
    
    - **To Street**: The name of the second cross street that intersects with the primary street at which work will be completed | Required if Location Type is Section of Road.

    - **Address or Block #**: The street address or block number on the primary street at which work will be completed | Required if Location Type is Specific Location.
    
    - **Area**: The region of the city in which the work will be completed (North / Central / South) | Required.
    
    - **School Nearby**: Flag to indicate if there is a school nearby this work location | Required.
    
    - **Location Details**: Additional description of the location at which work will be completed | Optional.

4. Click the **Create Work Order** button to submit the form:
    - An email is automatically sent to the logged-in user confirming that a work order has been created
    
    - You will be redirected to the Work Order Details page
    
    - If Requester is not **MAINTENANCE,** Work Order Status will be set to **ON HOLD** with On Hold Reason of **WAITING FOR PLANS**

    - If the user that created the work order is a Technician, jobs will be issued automatically.

5. If the user that created the work order is a Technician, skip to step 10.

6. Attach Plans. From the Work Order Details page, click the **Add Attachment** button. Complete the form:
    - **Type**: The type of attachment. Select Plans to attach plans. | Required

    - **Description**: A lot of description of the attachment contents. | Optional

    - **File**: The file to be uploaded. (Click 'Browse' to locate the file). | Required

    - **Submit button**: click to submit the attachment and return the work order details page.

7. Attach regulation document. If a regulation # was provided when the work order was created, the work order will have  a status of ON HOLD and a hold reason of **WAITING FOR REG** until the regulation document is attached. To attach a reg, click on the **Add Attachment** button:
    - **Type**: The type of attachment. Select Regulation to attach a regulation document. | Required
    
    - See step 5 for additional attachment instructions.

8. Verify Work Order Status. The work order should now have a status of **NEED TO BE ISSUED**. If not, check the **WAITING FOR HOLD REASON** to add attachments if necessary.

8. Verify Jobs have been created. Scroll down to the Jobs section. There will be one jobs for each work group you identified when creating the work order. Each job will have a status of **NEW**.

10. Add additional jobs. If you need to add additional jobs to the work order, scroll down to the Jobs section, and select the required work group from the Work group drop-down menu. Click **Create Work Job** to create the job.

    \* *It is not possible to create jobs if the work order status is **ON HOLD**.*

## Edit a Work Order

##### User Role Required: Viewer

Note: A work order can only be edited if no jobs have been issued.

1. To edit a work order, start by viewing the **Work Order Details** of the work order you wish to edit.

2. Click the **Edit Work Order** button to edit the work order.

3. Complete any changes as needed and click the **Update Work Order** button to save changes.

## Put a Work Order ON HOLD

##### User Role Required: Viewer

Note: A work order can only be placed on hold if its status is **NEED TO BE ISSUED** or **ISSUED**.

1. To place a work order **ON HOLD**, start by viewing the **Work Order Details** of the work order you wish to edit.

2. Click the **Hold** button. From the confirmation window, select the **Hold Reason** and click the **Put On Hold** button to place the work order **ON HOLD**.

3. To remove the **ON HOLD** status, click the **Hold** button, then click the **Remove Hold Button** to reset the work order status. 










