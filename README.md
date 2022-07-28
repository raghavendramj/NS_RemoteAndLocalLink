
1. To clone an already existing repo
----------------------------------------
git clone develop_url

local_develop	-------A(a.txt, b.txt, c.txt)------------------------------------>
	Working-directory ->
		added new file -> d.txt
		modified existing file -> a.txt
		git status
			-> untracked files -> d.txt -> red
			-> modified files -> a.txt -> red
	1. git add <file-names>
		Staging Area -> git add <file-names> or git add .
			git add d.txt, a.txt
			git status
			->  new file: d.txt  -> green
			->  modified:a.txt -> green
	2. git commit -m "My First Commit"
		(Local Repo)		local_develop	-------A(a.txt, b.txt, c.txt, d.txt)------------------------------------>
		(Remote Repo) 			 develop -------A(a.txt, b.txt, c.txt)------------------------------------>
	3. git push
		(Local Repo)		local_develop	-------A(a.txt, b.txt, c.txt, d.txt)------------------------------------>
		(Remote Repo) 			 develop  -------A(a.txt, b.txt, c.txt, d.txt)------------------------------------>

	git clone https://github.com/raghavendramj/NS_Github_Prac.git


2. Create a local repository and then link it with remote repository.
	---------------------------------------------------------------------
	1. create a folder ex:- mkdir ns_local_repo
	2. Go inside ex:- cd  ns_local_repo
	3. git init -> convert the folder to repository
	4. add some files,
		-> code first.txt -> my first file -> save
		-> code second.txt -> my second file -> save
	5. git status
		Untracked files:
			first.txt
			second.txt
	6. git add first.txt second.txt
	7. git status
		Changes to be committed:
		  (use "git rm --cached <file>..." to unstage)
				new file:   first.txt
				new file:   second.txt
	8. git commit -m "This is my first local commit"
	9. git push -> FAILED -> fatal: No configured push destination.
	10. Goto https://github.com/raghavendramj/ and create a repository. -> https://github.com/raghavendramj/NS_RemoteAndLocalLink.git
	11. Set the remote
			Commandd :- git remote add origin https://github.com/raghavendramj/NS_RemoteAndLocalLink.git
	12. git push --set-upstream origin master
	
