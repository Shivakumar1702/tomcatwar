job("java-maven-build-DSL"){
    
    scm{
        github('Shivakumar1702/tomcatwar', 'master')
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