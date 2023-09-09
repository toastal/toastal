toastal does **not** support GitHub as a code forge platform
============================================================

   Choosing proprietary tools and services for your free software project ultimately sends a message to downstream developers and users of your project that freedom of all users—developers included—is not a priority.
   
   -- Matt Lee, https://www.linuxjournal.com/content/opinion-github-vs-gitlab

.. role:: strike

* Git should be decentralized, not requiring a specific platform. While there are some enhancements to the process, there should not be a barrier beyond email if a user does not wish to share data with GitHub (alternatively, decentralized authentication). Due to this, many projects are stuck on GitHub through vendor lock-in. As a user, I *must* fork your project on GitHub to submit a merge request & I *must* have an account to raise or comment on issues. Worse is some communities, like Elm & Nix have tied their user identity in the community to this closed system.
* GitHub is trying to make code unnecessarily ‘social’ which doesn’t need to exist. We don’t need targeted advertising for other projects or anxiety about how colorful status progress bars are. Plug: I have created a `uBlock Origin list <https://git.sr.ht/~toastal/github-less-social>`_ to help declutter your page.
* GitHub is owned by Microsoft—the same company that used `embrace, extend, extinguish (EEE) <https://en.wikipedia.org/wiki/Embrace,_extend,_and_extinguish>`_ in the past to ruin software as a whole. Microsoft is trying to further monopolize with Azure, Codespaces, Visual Studio (regular & Code), npm, Sponsors, & trying to steal mindshare from free software with Windows Subsystem Linux (WSL) & your org with Teams. Over time, they have been pushing for tighter & tighter integrations, & we can assume eventually they will see no need to afford any interop & more proprietary extensions will be added. This is what happens under capitalism and publicly traded companies are legally obligated to make profits for the shareholders & have no allegience to helping the users if it does not help profit.
* GitHub is closed source. While Git is open & many of the projects on GitHub are, GitHub is not. If you have a problem, you can’t just send up a fix nor can you fork & self-host the project. Putting your business’s data on it assures no protections.
* The API of GitHub is `not very stable <https://github.com/MichaelMure/git-bug/issues/749#issuecomment-1072991272>`_. So while you can tool your way around simple things like email, it is not as simple with GitHub.
* Search results are gated. When you search a project on Microsoft GitHub & looking to use the “Code” section, when you are not authenticated you will get a ``?`` results & clicking “Code” will bring you too a login. Users may not search code without a Microsoft account.
* GitHub’s Copilot should not be supported & it’s controversially either spitting out code that violates :ac:`GPL` or as one lawyer said all outputs are derivative & *must* be in the public domain (so your code may have future legal issues), it copies bugs, & isn’t there to help more than you help train it. :strike:`As it is meant to be paid in the future, right now, *you* the user are training it & not getting paid for your service despite the stated future being that it will be` It is now a product sold back to you. While lessening the barrier to entry for programming could be good, training on all of our open code behind a closed platform, closed data, & capital-hungry entity to sell isn’t in the spirit of open source or free software. Currently the project `is under litigation <https://githubcopilotlitigation.com>`_.
* The $500k donation :ac:`PR` stunt is an attempt to get more folks to buy into their payment platform (which will take an additional 10% cut beyond an other transaction fees). Naturally this was paid out only to folks that signed up for their payment service in an attempt to bring others in on :ac:`FOMO` & further monopolize the source code platform.
* GitHub has a terrible landing page experience. Does your :ac:`CI` build status badges in your README *really* help me understand the how/what/why of your project, or are you bloating the README because GitHub doesn’t give you more flexible ways to mark up your projects? GitLab has badges as a project setting. SourceHut lets you upload arbiritrary (sanitized) HTML to the landing page. As an Hacker News user eloquently phrased it, the README has become a RENDERME & thus GitHub has ruined the README. A lot of the recent *good* ideas coming into GitHub have been borrowed from its competitors (Mermaid docs, integrated :ac:`CI`/:ac`CD`). Now they want `to break Markdown standards further <https://github.com/orgs/github-community/discussions/16925>`_ despite existing proposals to CommonMark with more GitHub-flavored nonsense because they are a bully & no longer feel they need to cooperate.

We’ve seen most :ac:`GPL`, :ac:`GNU`, & privacy-oriented projects move to alternatives because they want to respect their users and the spirit of open source. I hope to see your projects move to one of the alternatives soon too.

What can I as a user do today?
------------------------------

* Use an alternative Git code forge

  Git-supporting Code Forge Alternatives
   `SourceHut <https://sr.ht/>`_
      self-hostable AGPL service where using their hosted basics are free (including mailing lists & an :ac:`IRC` bouncer), but :ac:`CI` is paid, however it is not :ac:`VC`\-funded nor does it have investors or shareholders to appease
	`GNU Savannah <https://savannah.gnu.org/>`_
		for :ac:`FLOSS` software where your projects need to be approved as such
	`Forgejo <https://forgejo.org/>`_
		self-hosted, :ac:`FLOSS` GitHub clone essentially
	`Codeberg <https://codeberg.org/>`_
		Forgejo hosted by a German non-profit
	`cgit <https://git.zx2c4.com/cgit/about/>`_
		tiny, self-hosted :ac:`GPL` Git :ac:`UI`
	`GitLab <https://gitlab.com/>`_
		free, open-core, Ruby-based forge support with full build pipeline & self-hostable community edition (however are :ac:`VC`\-funded & is publicly traded so they have investors to appease, so we’ll see about the future)
* Try an alternative to Git
	Some other :ac:`VCS` options
		`darcs <http://darcs.net>`_
			“Darcs is a free and open source, cross-platform version control system, […] with a very different approach: focus on changes rather than snapshots. Darcs offers a freer way of working, and a simpler user interface.”
* Ask your code communities & workplace to switch to an alternative code forge or officially back a mirror on an alternative. If that cannot be done, ask your code communities & workplace to at least allow additions to its larger ecosystem from these alternatives (plugins, packages, etc.) as well as posting a public mailing address to email code patches.
* Oppose all attempts to standardize, endorse, or weigh anything in GitHub’s specific favor (like shorthands for packages)
* Make sure educational institutions aren’t requiring students to sign up for proprietary accounts. It’s bad enough that the next generation continues to be trained in Adobe Suite & Microsoft Office instead of :ac:`FLOSS` options, but now Git & other :ac:`VCS` are in the same boat where fundamentals can be learned that don’t require a proprietary service (and universites in particular have the resources to self-host at least cgit). If you are doing a workshop, bootcamp, or other smaller beginner-related activity, this rule should still apply.

Then why are you even here?
---------------------------

I back open source ethos & its projects with a lot them are here haplessly. I care more about that ethos than my self-held stance on where the code is hosted, but we need to get more code off this platform. You can’t have any migration conversations without contributing to projects in good faith. To a lot of folks GitHub is seen as a default & alternatives were never considered.

Also let’s glare at GitHub for stripping out ``<abbr>`` tags from rendered documents such as this even though these tags would help accessibility.

Where can I find your code now?
-------------------------------

SourceHut (primary)
	https://sr.ht/~toastal/
darcs hub
	https://hub.darcs.net/toastal/
Codeberg
	https://codeberg.org/toastal/
GitLab
	https://gitlab.com/toastal
