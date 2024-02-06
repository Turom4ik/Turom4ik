class User:
    def init(self, username, email):
        self.username = username
        self.email = email

class UserManager:
    def init(self):
        self.users = []

    def add_user(self, user):
        self.users.append(user)

    def remove_user(self, user):
        self.users.remove(user)

    def get_user_by_username(self, username):
        for user in self.users:
            if user.username == username:
                return user
        return None

    def get_user_by_email(self, email):
        for user in self.users:
            if user.email == email:
                return user
        return None
