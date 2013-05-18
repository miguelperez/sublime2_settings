First, after installing sublime open it and install the package control.

Installation is through the Sublime Text 2 console. This is accessed via the ctrl+` shortcut. Once open, paste the following command into the console.

    import urllib2,os; pf='Package Control.sublime-package'; ipp=sublime.installed_packages_path(); os.makedirs(ipp) if not os.path.exists(ipp) else None; urllib2.install_opener(urllib2.build_opener(urllib2.ProxyHandler())); open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read()); print('Please restart Sublime Text to finish installation')

This command creates the Installed Packages folder for you (if necessary), and then downloads the Package Control.sublime-package into it.


After it is installed. Just replace the directory User inside:

    ~/Library/Application Support/Sublime Text 2/Packages
    
With the contents of this repository.
