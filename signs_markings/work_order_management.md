<<<<<<< HEAD
[Data Tracker Guides](./) > [Signs & Markings](/signs_markings#signs-and-markings-data-tracker-user-guides) > [Work Order Management](work_order_management.md)

# Managing Work Orders

- [About Work Orders](#about-work-orders)
- [Find a Work Order](#find-a-work-order)
- [Create a Work Order](#create-a-work-order)
- [Edit a Work Order](#edit-a-work-order)
- [Put a Work Order ON HOLD](#put-a-work-order-on-hold)
- [My Work Orders](#my-work-orders)
- [Advanced Search](#advanced-search)

## About Work Orders

Work Orders are the process by which Signs & Markings work is requested, dispatched, and completed. The overall workflow is:

1. A user creates a new work order which specifies the location and type of work to be completed. Plans must be attached to the work order after it is created. If the work order has a REG, it must be attached to the work order after it is created. 
2. A supervisor reviews the work order and issues individual jobs to work groups.
3. Work groups complete their jobs.
4. An analyst reviews the work order and updates asset information in GIS.
5. A supervisor reviews the work order and closes it.


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

1. Visit the work orders landing page: http://transportation.austintexas.io/data-tracker/#home/work-orders-markings/markings/. 
Note: You can toggle between Signs or Markings work order views using the corresponding tabs below the "Signs & Markings | Work Orders" page header.

2. By default, the Work Order table displays **NEED TO BE ISSUED** records. Additional tabs display work orders that are filtered based on their status.

3. The search box at the top of the work orders table enables searching by keyword. Partial words are accepted.

4. To view details of a work order, click on the **Details icon** in the left-most column of the table.

## Create a Work Order

##### User Role Required: Viewer or Technician

1. Visit the Signs & Markings Data Tracker Work Orders Landing Page: http://transportation.austintexas.io/data-tracker/#home/work-orders-markings/

2. Click **New Work Order** button.

3. Complete New Work Order form:
    - **Work Type**: Choose whether this is a Signs or Markings work order | Required.
    
    - **Requester**: The business unit requesting the work. | This will be defaulted based on your account information. 
    
    - **Work Groups**: The Markings work group(s) that will complete the work. This section will only appear when requesting a Markings work order. | Required for Markings work orders.

Markings work is broken into four work groups as follows:

Long line       | Short lines		| Specialty Markings 	| Raised Pavement Markings |
:---            | :--- 				|  :--- 				|  :--- 				   |
Center lines	| Crosswalks 		| Arrows 				| Raised Pavement Markings |
Lane lines      | Stop lines 		| Legends				| 
Edge lines      | Yield lines 		| Words  				| 
Bike lane lines | School Zone line  | Cross hatches 		| 
Turn Bays       | 					| Painted Curb 			|
|				| 					| Parking T's and L's 	|
|				| 					| Delineators 			|
|				| 					| Concrete Domes 		| 
|				| 					| Rubber Speed Cushions | 
   
    - **Requester Work Order ID**: the ID of the requester's work order/plan | Required.
    
    
    - **Regulation**: | Indicate if work order has a Regulation. If "Yes", the work order will be placed on hold until REG is attached. You will enter the REG number when you attach the REG | Required.

    - **Coordination Need**: Indicate if the work order requires coordination across multiple ATD divisions or with a contractor | Required.
    
    - **Instructions and Comments**: Description of the work to be completed and any additional comments | Required.

    - **Location Type**: Select from: Intersection, Section of Road, or Specific Location and fill out the associated fields | Required.
    
  Note: When using the search field to find a street with a “N”, “S”, “E”, “W” prefix, DO NOT include the prefix in the search. Ex. For S Lamar, search “Lamar”, not “S Lamar”. 

    - **Primary Street:** The name of the primary street at which work will be completed. | Required.
    
    - **Cross Street**: The name of the cross street at which work will be completed | Required if Location Type is Intersection.
    
    - **From Street**: The name of the first cross street that intersects with the primary street at which work will be completed | Required if Location Type is Section of Road.
    
    - **To Street**: The name of the second cross street that intersects with the primary street at which work will be completed | Required if Location Type is Section of Road.

    - **Address or Block #**: The street address or block number on the primary street at which work will be completed | Required if Location Type is Specific Location.
    
    - **Area**: The region of the city in which the work will be completed (North / Central / South) | Required.
    
    - **School**: Indicate if there is a school nearby this work location | Required.

    - **Street Segment ID**: Provide 8-digit street segment ID which references the work location. A link to the Street Segment ID map is provided.
    
    - **Location Details**: Additional description of the location at which work will be completed. Use this field to explain special, unique, or complicated locations. 

4. Click the **Create Work Order** button to submit the form.
        
    - You will be redirected to the Work Order Details page and there will be a banner at the top of the page that says "This work order is on hold. See On Hold Reason for details."
    
    - An email is automatically sent to the logged-in user confirming that a work order has been created

5. Attach Plans. From the Work Order Details page, click the **Add Attachment** button and complete the form.
    - **Type**: The type of attachment (Plans / Regulation / Image / Other). | Required

    - **Description**: A description of the attachment. | Optional

    - **File**: The file to be uploaded. Click 'Browse' to locate the file. | Required

    - **Submit button**: Click to submit the attachment and return to the work order details page.

6. Attach regulation document. If a regulation # was provided when the work order was created, the work order will have a status of ON HOLD and a hold reason of **WAITING FOR REG** until the regulation document is attached. 
	- To attach a reg, click on the **Add Attachment** button:
    - Choose "Regulation" as the attachment **Type**. | Required
    - An additional field for **Regulation #**. Enter an 8-digit Regulation # (ex. 2018-0012) | Required
    - Click **Submit** | File Type: PDF

Note: You must attach Plans and Regulations as separate attachments. 

7. Verify Work Order Status. The work order should now have a status of **NEED TO BE ISSUED**. If not, check the **ON HOLD** reason to add attachments, if necessary.

8. Verify that the Jobs have been created. On the Work Order Details page,scroll down to the Jobs section. For Markings work orders, there will be one job for each work group you identified when creating the work order. For Signs work orders, there will only be one job listed as "SIGNS". Each job will have a status of **NEED TO BE ISSUED**.

9. Add additional jobs. If you need to add additional jobs to the work order, scroll down to the Jobs section and select the required work group from the Work group drop-down menu. Click **Create Work Job** to create the job. The new job will appear in the Jobs Table.

    \* *It is not possible to create jobs if the work order status is **ON HOLD**.*

## Edit a Work Order

Note: A work order can only be edited if no jobs have been issued.

1. To edit a work order, start by viewing the **Work Order Details** of the work order you wish to edit.

2. Click the **Edit Work Order** button to edit the work order.

3. Complete any changes as needed and click the **Update Work Order** button to save changes.

## Put a Work Order ON HOLD

Note: A work order can only be placed on hold if its status is **NEED TO BE ISSUED** or **ISSUED**.

1. To place a work order **ON HOLD**, start by viewing the **Work Order Details** of the work order you wish to place on hold.

2. Click the **Hold** button. 

3. From the confirmation window, select the **Hold Reason** from the drop down field:

On Hold Reason          				| Description|
:---                    				| :--- |
**WAITING FOR INVENTORY**   			| The work order can not be worked on because inventory items are not on hand. |
**WAITING FOR ROADWAY IMPROVEMENTS**    | The work order can not be worked on because the roadway is still being worked on |
**WAITING FOR PLANS**             		| The work order can not be worked on because plans are not ready|
**WAITING FOR SBO**           			| The work order can not be worked on because waiting for Street & Bridge Operations is not complete yet|
**OTHER -- SEE COMMENTS**        		| Provide a comment on why the work order is on hold in the comments section on the work order details page |

Then click the **Put On Hold** button to place the work order **ON HOLD**.

4. To remove the **ON HOLD** status, click the **Hold** button

5. From the confirmation window, click the **Remove Hold Button** to reset the work order status. 

## My Work Orders

1. You can view all of the work orders you have created by clicking the **My Work Orders** button on the Signs & Markings Work Orders Landing Page. 

Note: By default, the My Work Orders table displays **NEED TO BE ISSUED** work orders. Additional tabs display work order that are filtered based on each status and can be viewed by clicking each tab.

2.	To view the details of a work order, click the **Details icon** in the left-most column of the table.

## Advanced Search

1. Click on **Advanced Search** button from the Work Order Landing page

2. Input your search criteria and click **Search**. 

3. You can go to a work order in the results table by clicking the **Details icon** in the left-most column. 

=======
[Data Tracker Guides](./) > [Signs & Markings](/signs_markings#signs-and-markings-data-tracker-user-guides) > [Work Order Management](work_order_management.md)

# Managing Work Orders

- [About Work Orders](#about-work-orders)
- [Find a Work Order](#find-a-work-order)
- [Create a Work Order](#create-a-work-order)
- [Edit a Work Order](#edit-a-work-order)
- [Put a Work Order ON HOLD](#put-a-work-order-on-hold)
- [My Work Orders](#my-work-orders)
- [Advanced Search](#advanced-search)

## About Work Orders

Work Orders are the process by which Signs & Markings work is requested, dispatched, and completed. The overall workflow is:

1. A user creates a new work order which specifies the location and type of work to be completed. Plans must be attached to the work order after it is created. If the work order has a REG, it must be attached to the work order after it is created. 
2. A supervisor reviews the work order and issues individual jobs to work groups.
3. Work groups complete their jobs.
4. An analyst reviews the work order and updates asset information in GIS.
5. A supervisor reviews the work order and closes it.


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

1. Visit the work orders landing page: http://transportation.austintexas.io/data-tracker/#home/work-orders-markings/markings/. 
Note: You can toggle between Signs or Markings work order views using the corresponding tabs below the "Signs & Markings | Work Orders" page header.

2. By default, the Work Order table displays **NEED TO BE ISSUED** records. Additional tabs display work orders that are filtered based on their status.

3. The search box at the top of the work orders table enables searching by keyword. Partial words are accepted.

4. To view details of a work order, click on the **Details icon** in the left-most column of the table.

## Create a Work Order

##### User Role Required: Viewer or Technician

1. Visit the Signs & Markings Data Tracker Work Orders Landing Page: http://transportation.austintexas.io/data-tracker/#home/work-orders-markings/

2. Click **New Work Order** button.

3. Complete New Work Order form:
    - **Work Type**: Choose whether this is a Signs or Markings work order | Required.
    
    - **Requester**: The business unit requesting the work. | This will be defaulted based on your account information. 
    
    - **Work Groups**: The Markings work group(s) that will complete the work. This section will only appear when requesting a Markings work order. | Required for Markings work orders.

Markings work is broken into four work groups as follows:

Long line       | Short lines		| Specialty Markings 	| Raised Pavement Markings |
:---            | :--- 				|  :--- 				|  :--- 				   |
Center lines	| Crosswalks 		| Arrows 				| Raised Pavement Markings |
Lane lines      | Stop lines 		| Legends				| 
Edge lines      | Yield lines 		| Words  				| 
Bike lane lines | School Zone line  | Cross hatches 		| 
Turn Bays       | 					| Painted Curb 			|
|				| 					| Parking T's and L's 	|
|				| 					| Delineators 			|
|				| 					| Concrete Domes 		| 
|				| 					| Rubber Speed Cushions | 
   
  - **Requester Work Order ID**: the ID of the requester's work order/plan | Required.
  - **Regulation**: | Indicate if work order has a Regulation. If "Yes", the work order will be placed on hold until REG is attached. You will enter the REG number when you attach the REG | Required.
  - **Coordination Need**: Indicate if the work order requires coordination across multiple ATD divisions or with a contractor | Required.
  - **Instructions and Comments**: Description of the work to be completed and any additional comments | Required.
  - **Location Type**: Select from: Intersection, Section of Road, or Specific Location and fill out the associated fields | Required.
  
  Note: When using the search field to find a street with a “N”, “S”, “E”, “W” prefix, DO NOT include the prefix in the search. Ex. For S Lamar, search “Lamar”, not “S Lamar”. 

  - **Primary Street:** The name of the primary street at which work will be completed. | Required.
  - **Cross Street**: The name of the cross street at which work will be completed | Required if Location Type is Intersection.
  - **From Street**: The name of the first cross street that intersects with the primary street at which work will be completed | Required if Location Type is Section of Road.
  - **To Street**: The name of the second cross street that intersects with the primary street at which work will be completed | Required if Location Type is Section of Road.
  - **Address or Block #**: The street address or block number on the primary street at which work will be completed | Required if Location Type is Specific Location.  
  - **Area**: The region of the city in which the work will be completed (North / Central / South) | Required.    
  - **School**: Indicate if there is a school nearby this work location | Required.
  - **Street Segment ID**: Provide 8-digit street segment ID which references the work location. A link to the Street Segment ID map is provided.  
  - **Location Details**: Additional description of the location at which work will be completed. Use this field to explain special, unique, or complicated locations. 

4. Click the **Create Work Order** button to submit the form.
        
    - You will be redirected to the Work Order Details page and there will be a banner at the top of the page that says "This work order is on hold. See On Hold Reason for details."
    
    - An email is automatically sent to the logged-in user confirming that a work order has been created

5. Attach Plans. From the Work Order Details page, click the **Add Attachment** button and complete the form.
    - **Type**: The type of attachment (Plans / Regulation / Image / Other). | Required

    - **Description**: A description of the attachment. | Optional

    - **File**: The file to be uploaded. Click 'Browse' to locate the file. | Required

    - **Submit button**: Click to submit the attachment and return to the work order details page.

6. Attach regulation document. If a regulation # was provided when the work order was created, the work order will have a status of ON HOLD and a hold reason of **WAITING FOR REG** until the regulation document is attached. 
	- To attach a reg, click on the **Add Attachment** button:
    - Choose "Regulation" as the attachment **Type**. | Required
    - An additional field for **Regulation #**. Enter an 8-digit Regulation # (ex. 2018-0012) | Required
    - Click **Submit** | File Type: PDF

Note: You must attach Plans and Regulations as separate attachments. 

7. Verify Work Order Status. The work order should now have a status of **NEED TO BE ISSUED**. If not, check the **ON HOLD** reason to add attachments, if necessary.

8. Verify that the Jobs have been created. On the Work Order Details page,scroll down to the Jobs section. For Markings work orders, there will be one job for each work group you identified when creating the work order. For Signs work orders, there will only be one job listed as "SIGNS". Each job will have a status of **NEED TO BE ISSUED**.

9. Add additional jobs. If you need to add additional jobs to the work order, scroll down to the Jobs section and select the required work group from the Work group drop-down menu. Click **Create Work Job** to create the job. The new job will appear in the Jobs Table.

    \* *It is not possible to create jobs if the work order status is **ON HOLD**.*

## Edit a Work Order

Note: A work order can only be edited if no jobs have been issued.

1. To edit a work order, start by viewing the **Work Order Details** of the work order you wish to edit.

2. Click the **Edit Work Order** button to edit the work order.

3. Complete any changes as needed and click the **Update Work Order** button to save changes.

## Put a Work Order ON HOLD

Note: A work order can only be placed on hold if its status is **NEED TO BE ISSUED** or **ISSUED**.

1. To place a work order **ON HOLD**, start by viewing the **Work Order Details** of the work order you wish to place on hold.

2. Click the **Hold** button. 

3. From the confirmation window, select the **Hold Reason** from the drop down field:

On Hold Reason          				| Description|
:---                    				| :--- |
**WAITING FOR INVENTORY**   			| The work order can not be worked on because inventory items are not on hand. |
**WAITING FOR ROADWAY IMPROVEMENTS**    | The work order can not be worked on because the roadway is still being worked on |
**WAITING FOR PLANS**             		| The work order can not be worked on because plans are not ready|
**WAITING FOR SBO**           			| The work order can not be worked on because waiting for Street & Bridge Operations is not complete yet|
**OTHER -- SEE COMMENTS**        		| Provide a comment on why the work order is on hold in the comments section on the work order details page |

Then click the **Put On Hold** button to place the work order **ON HOLD**.

4. To remove the **ON HOLD** status, click the **Hold** button

5. From the confirmation window, click the **Remove Hold Button** to reset the work order status. 

## My Work Orders

1. You can view all of the work orders you have created by clicking the **My Work Orders** button on the Signs & Markings Work Orders Landing Page. 

Note: By default, the My Work Orders table displays **NEED TO BE ISSUED** work orders. Additional tabs display work order that are filtered based on each status and can be viewed by clicking each tab.

2.	To view the details of a work order, click the **Details icon** in the left-most column of the table.

## Advanced Search

1. Click on **Advanced Search** button from the Work Order Landing page

2. Input your search criteria and click **Search**. 

3. You can go to a work order in the results table by clicking the **Details icon** in the left-most column. 

>>>>>>> dev
