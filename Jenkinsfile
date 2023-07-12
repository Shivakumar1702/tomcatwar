job("java-maven-build-DSL"){
    
    scm{
        github('https://github.com/Shivakumar1702/tomcatwar.git', 'master')
    }
    triggers{
        scm('* * * * *')
    }
    steps{
        maven('clean package', 'myartifact/pom.xml')
    }
    publishers{
        archiveArtifacts '**/*.war'
    }

    
}