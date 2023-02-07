1) willExpireAt()
  due_time is equal to  convert parse due_time
  created_at is equal to  convert parse created_at
  difference is equal to the diffrent between to due_time and created_at
  if difference is greater and equal to 90 then time is equal to due_time
  if difference is greater and equal to 24 then add 90 min in created_at in time
  else time is equal to due_time sub hours of 48

return time with format
2) createOrUpdate() UserRepository
 role
 name
 company_id
 department_id
 email
 dob_or_orgid
 phone
 mobile
 if password and id is isset then password is bcrypt

  	$model->detachAllRoles();
        $model->save();
        $model->attachRole($request['role']);

remove all roles
save date
add role


if role is CUSTOMER_ROLE_ID
if consumer_type is paid and company_id is not empty
  then
	type is equal to type where code is equal to pait limit one
	create company and deparment
	save company_id and department_id

	    $user_meta = UserMeta::firstOrCreate(['user_id' => $model->id]);
            $old_meta = $user_meta->toArray();
            $user_meta->consumer_type = $request['consumer_type'];
            $user_meta->customer_type = $request['customer_type'];
            $user_meta->username = $request['username'];
            $user_meta->post_code = $request['post_code'];
            $user_meta->address = $request['address'];
            $user_meta->city = $request['city'];
            $user_meta->town = $request['town'];
            $user_meta->country = $request['country'];
            $user_meta->reference = (isset($request['reference']) && $request['reference'] == 'yes') ? '1' : '0';
            $user_meta->additional_info = $request['additional_info'];
            $user_meta->cost_place = isset($request['cost_place']) ? $request['cost_place'] : '';
            $user_meta->fee = isset($request['fee']) ? $request['fee'] : '';
            $user_meta->time_to_charge = isset($request['time_to_charge']) ? $request['time_to_charge'] : '';
            $user_meta->time_to_pay = isset($request['time_to_pay']) ? $request['time_to_pay'] : '';
            $user_meta->charge_ob = isset($request['charge_ob']) ? $request['charge_ob'] : '';
            $user_meta->customer_id = isset($request['customer_id']) ? $request['customer_id'] : '';
            $user_meta->charge_km = isset($request['charge_km']) ? $request['charge_km'] : '';
            $user_meta->maximum_km = isset($request['maximum_km']) ? $request['maximum_km'] : '';
            $user_meta->save();

save user meta



