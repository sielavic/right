 public function isPerfomer($user_id){
        if (USER_COOKIE_ID == $user_id) {
            $permission = $this->permissions->where('id', 64)->first();
            $permission_user = collect();
            if (!empty($permission)) {
                $permission_user = $permission->permissionUsers->where('user_id', $user_id)->first();
                return true;
            } else {
                \Entity\Permission_user::addPermissionUser($user_id, 64, 1);
                return true;
            }
        }else{
               return false;
            }
    }
