Here are some problems i faced while pushing code to git hub along with thier solution and a breif explanation!

1: **Error messege**
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/shaik-adnan1/flutter_expenses_app.git



This error is basically thrown at you beacuse, a push has already been made on the master branch and 
the commit you are trying to make is "behind".

As in the error messege you have to fetch first and
then create a pull, add the files, commit them and then push to the master branch


