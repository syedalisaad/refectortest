 some small decription of some function 
1) index() function in Booking Controller
 if user_id isset then go to then getUserJobs 
 if user is customer then get all job with userMeta, avarage, kanguage and feedback those status is pending assigned and started
 if user is translator job which status is new
 if job is immediate is yes then it is emergency job otherwise it is normal job
2) show($id) function in Booking Controller
  show data by id with translatorJobRel.user	
3) store() function in Booking Controller
  if booking type is CUSTOMER_ROLE_ID 
	then from_language_id should not set
	if immediate is "no" then duration, due_date, due_time required and is not  set customer_phone_type, customer_physical_type
  	else duration is set
  customer_phone_type is set then customer_phone_type is yes otherwise no
  customer_physical_type is set then customer_physical_type ,customer_physical_type is yes then no 
  if immediate is yes then due is current time add with immediatetime, immediate, customer_phone_type is yes else  type is immediate
  else immediate is regular, due with date and time 
  is date is pass then return fail
  get gender from job_for
  get certified from job_for
  if consumer_type is rwsconsumer
  then job_type is rws
  if consumer_type is ngo
  then job_type is unpaid
  if consumer_type is paid
  then job_type is paid
  b_created_at current date and time

  if due is set
  then will_expire_at set
  and save
 
the reusability of code is so good 

   