
## Follow the instruction. 

Skip to content
 
java codi

Pull requests
Issues
Marketplace
Explore
 @Ranjanas25 Sign out
0
0 665 Ranjusun/pmd
forked from pmd/pmd
 Code  Pull requests 0  Projects 0  Wiki  Insights  Settings
pmd/pom.xml
08950c9  7 days ago
@Thunderforge Thunderforge Upgrading JCommander from 1.48 to 1.72
@adangel @jsotuyod @Thunderforge @oowekyala @sergeygorbaty @rsoesemann @MatiasComercio @vickenty @daleanson @bric3 @AustinShalit
     
1175 lines (1133 sloc)  47 KB
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>
    <groupId>net.sourceforge.pmd</groupId>
    <artifactId>pmd</artifactId>
    <version>6.10.0-SNAPSHOT</version>
    <packaging>pom</packaging>
    <name>PMD</name>

    <description>
PMD is a source code analyzer. It finds common programming flaws like unused variables, empty catch blocks, unnecessary object creation, and so forth. It supports Java, JavaScript, Salesforce.com Apex, PLSQL, Salesforce.com Visualforce, Apache Velocity, XML, XSL.

Additionally it includes CPD, the copy-paste-detector. CPD finds duplicated code in Java, C, C++, C#, Groovy, PHP, Ruby, Fortran, JavaScript, PLSQL, Apache Velocity, Scala, Objective C, Matlab, Python, Go, Swift and Salesforce.com Apex.
    </description>

    <url>https://pmd.github.io/</url>
    <ciManagement>
        <url>https://travis-ci.org/pmd/pmd</url>
    </ciManagement>
    <inceptionYear>2002</inceptionYear>
    <licenses>
        <license>
            <name>BSD-style</name>
            <url>http://pmd.sourceforge.net/license.html</url>
            <distribution>repo</distribution>
        </license>
    </licenses>
    <mailingLists>
        <mailingList>
            <name>PMD development</name>
            <subscribe>https://lists.sourceforge.net/lists/listinfo/pmd-devel</subscribe>
            <unsubscribe>https://lists.sourceforge.net/lists/listinfo/pmd-devel</unsubscribe>
            <archive>https://sourceforge.net/p/pmd/mailman/pmd-devel</archive>
        </mailingList>
        <mailingList>
            <name>PMD commits</name>
            <subscribe>https://lists.sourceforge.net/lists/listinfo/pmd-commits</subscribe>
            <unsubscribe>https://lists.sourceforge.net/lists/listinfo/pmd-commits</unsubscribe>
            <archive>https://sourceforge.net/p/pmd/mailman/pmd-commits</archive>
        </mailingList>
    </mailingLists>
    <developers>
        <developer>
            <id>tomcopeland</id>
            <name>Tom Copeland</name>
            <email>tom@infoether.com</email>
            <organization>InfoEther</organization>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>dpeugh</id>
            <name>David Dixon-Peugh</name>
            <email>ddp@apache.org</email>
            <organization>Lockheed Martin Corporation</organization>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>olemartin</id>
            <name>Ole-Martin Mork</name>
            <email>olemartin@users.sourceforge.net</email>
            <organization>Bekk Consulting</organization>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>mikkey</id>
            <name>Miguel Griffa</name>
            <email>mikkey@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>phherlin</id>
            <name>Philippe Herlin</name>
            <email>phherlin@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>jigerjava</id>
            <name>Jiger Patel</name>
            <email>jigerjava@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>kubacki</id>
            <name>Radim Kubacki</name>
            <email>kubacki@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>tomslot</id>
            <name>Tomasz Slota</name>
            <email>tomslot@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>ezust</id>
            <name>Alan Ezust</name>
            <email>ezust@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>nascif</id>
            <name>Nascif Abousalh Neto</name>
            <email>nascif@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>allancaplan</id>
            <name>Allan Caplan</name>
            <email>allancaplan@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>holobender</id>
            <name>Sven Jacob</name>
            <email>holobender@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>wfzelle</id>
            <name>Wouter Zelle</name>
            <email>wfzelle@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>hooperbloob</id>
            <name>Brian Remedios</name>
            <email>hooperbloob@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>xlv</id>
            <name>Xavier Le Vourch</name>
            <email>xlv@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>rgustav</id>
            <name>Ryan Gustafson</name>
            <email>rgustav@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>bluejohn</id>
            <name>Johan Nagels</name>
            <email>bluejohn@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>tkleiber</id>
            <name>Torsten Kleiber</name>
            <url>http://develishdevelopment.wordpress.com</url>
            <email>tkleiber@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>rpelisse</id>
            <name>Romain Pelisse</name>
            <email>rpelisse@users.sourceforge.net</email>
            <url>http://belaran.eu/</url>
            <organization>Atos Origin</organization>
            <organizationUrl>https://osc-service.si.fr.atosorigin.com/</organizationUrl>
            <roles>
                <role>Developer</role>
            </roles>
            <timezone>+1</timezone>
            <properties>
                <picUrl>http://belaran.eu/wordpress/wp-content/uploads/2008/05/RomainPELISSE.jpg</picUrl>
            </properties>
        </developer>
        <developer>
            <id>adangel</id>
            <name>Andreas Dangel</name>
            <email>adangel@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
            <timezone>+1</timezone>
        </developer>
        <developer>
            <id>acanda</id>
            <name>Philip Graf</name>
            <email>acanda@users.sourceforge.net</email>
            <roles>
                <role>Developer</role>
            </roles>
        </developer>
        <developer>
            <id>jsotuyod</id>
            <name>Juan Martín Sotuyo Dodero</name>
            <email>juansotuyo@gmail.com</email>
            <roles>
                <role>Developer</role>
            </roles>
            <timezone>-3</timezone>
        </developer>
    </developers>
    <scm>
        <connection>scm:git:git://github.com/pmd/pmd.git</connection>
        <developerConnection>scm:git:ssh://git@github.com/pmd/pmd.git</developerConnection>
        <url>https://github.com/pmd/pmd</url>
        <tag>HEAD</tag>
    </scm>
    <distributionManagement>
        <snapshotRepository>
            <id>ossrh</id>
            <url>https://oss.sonatype.org/content/repositories/snapshots</url>
        </snapshotRepository>
        <repository>
            <id>ossrh</id>
            <url>https://oss.sonatype.org/service/local/staging/deploy/maven2/</url>
        </repository>
    </distributionManagement>
    <organization>
        <name>PMD</name>
        <url>https://pmd.github.io/</url>
    </organization>
    <issueManagement>
        <url>https://github.com/pmd/pmd/issues</url>
    </issueManagement>

    <properties>
        <java.version>7</java.version>
        <!-- Workaround for https://youtrack.jetbrains.com/issue/IDEA-188690 -->
        <maven.compiler.source>1.${java.version}</maven.compiler.source>
        <maven.compiler.target>1.${java.version}</maven.compiler.target>

        <maven.compiler.test.source>1.8</maven.compiler.test.source>
        <maven.compiler.test.target>1.8</maven.compiler.test.target>


        <kotlin.compiler.jvmTarget>${maven.compiler.test.target}</kotlin.compiler.jvmTarget>
        <kotlin.version>1.2.61</kotlin.version>


        <javacc.version>5.0</javacc.version>
        <surefire.version>2.22.0</surefire.version>
        <checkstyle.version>3.0.0</checkstyle.version>
        <pmd.plugin.version>3.11.0</pmd.plugin.version>
        <ant.version>1.10.1</ant.version>
        <javadoc.plugin.version>3.0.1</javadoc.plugin.version>
        <antlr.version>4.7</antlr.version>

        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
        <project.reporting.outputEncoding>UTF-8</project.reporting.outputEncoding>
        <pmd.website.baseurl>https://pmd.github.io/pmd</pmd.website.baseurl>

        <argLine>-Xmx512m -Dfile.encoding=${project.build.sourceEncoding}</argLine>

        <pmd.build-tools.version>1.2</pmd.build-tools.version>

    </properties>

    <build>
        <pluginManagement>
            <plugins>
                <plugin>
                    <groupId>org.antlr</groupId>
                    <artifactId>antlr4-maven-plugin</artifactId>
                    <version>${antlr.version}</version>
                    <configuration>
                        <inputEncoding>${project.build.sourceEncoding}</inputEncoding>
                    </configuration>
                    <executions>
                        <execution>
                            <id>antlr</id>
                            <goals>
                                <goal>antlr4</goal>
                            </goals>
                        </execution>
                    </executions>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-antrun-plugin</artifactId>
                    <version>1.8</version>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-assembly-plugin</artifactId>
                    <version>3.1.0</version>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-dependency-plugin</artifactId>
                    <version>3.1.1</version>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-release-plugin</artifactId>
                    <version>2.5.3</version>
                    <configuration>
                        <releaseProfiles>pmd-release</releaseProfiles>
                        <pushChanges>true</pushChanges>
                        <localCheckout>true</localCheckout>
                        <autoVersionSubmodules>true</autoVersionSubmodules>
                        <tagNameFormat>pmd_releases/@{project.version}</tagNameFormat>
                        <goals>deploy</goals>
                    </configuration>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-clean-plugin</artifactId>
                    <version>3.1.0</version>
                </plugin>

                <!-- Kotlin compiler for test-compile -->
                <!-- The kotlin plugin has to run before the java plugin-->
                <plugin>
                    <artifactId>kotlin-maven-plugin</artifactId>
                    <groupId>org.jetbrains.kotlin</groupId>
                    <version>${kotlin.version}</version>
                    <executions>
                        <execution>
                            <id>kotlin-test-compile</id>
                            <goals>
                                <goal>test-compile</goal>
                            </goals>
                            <phase>process-test-sources</phase>
                            <configuration>
                                <sourceDirs>
                                    <sourceDir>${project.basedir}/src/test/kotlin</sourceDir>
                                    <sourceDir>${project.basedir}/src/test/java</sourceDir>
                                </sourceDirs>
                            </configuration>
                        </execution>
                    </executions>
                </plugin>

                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-compiler-plugin</artifactId>
                    <version>3.7.0</version>
                    <configuration>
                        <release>${java.version}</release>
                    </configuration>
                    <executions>
                        <!-- Replacing default-compile as it is treated specially by maven -->
                        <execution>
                            <id>default-compile</id>
                            <phase>none</phase>
                        </execution>
                        <!-- Replacing default-testCompile as it is treated specially by maven -->
                        <execution>
                            <id>default-testCompile</id>
                            <phase>none</phase>
                        </execution>
                        <execution>
                            <id>java-compile</id>
                            <phase>compile</phase>
                            <goals>
                                <goal>compile</goal>
                            </goals>
                        </execution>
                        <execution>
                            <id>java-test-compile</id>
                            <phase>test-compile</phase>
                            <goals>
                                <goal>testCompile</goal>
                            </goals>
                            <configuration>
                                <source>${maven.compiler.test.source}</source>
                                <target>${maven.compiler.test.target}</target>
                            </configuration>
                        </execution>
                    </executions>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-deploy-plugin</artifactId>
                    <version>2.8.2</version>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-install-plugin</artifactId>
                    <version>2.5.2</version>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-jar-plugin</artifactId>
                    <version>3.1.0</version>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-resources-plugin</artifactId>
                    <version>3.1.0</version>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-shade-plugin</artifactId>
                    <version>3.1.1</version>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-surefire-plugin</artifactId>
                    <version>${surefire.version}</version>
                    <configuration>
                        <forkMode>once</forkMode>
                        <runOrder>alphabetical</runOrder>
                        <testSourceDirectory>${project.basedir}/src/test/java</testSourceDirectory>
                        <testSourceDirectory>${project.basedir}/src/test/kotlin</testSourceDirectory>
                    </configuration>
                    <dependencies>
                        <!-- Junit 5 = Platform + Jupiter (5) + Vintage (3 & 4)-->

                        <!-- Junit platform -->
                        <!-- Needed to use kotlintest -->
                        <dependency>
                            <groupId>org.junit.platform</groupId>
                            <artifactId>junit-platform-surefire-provider</artifactId>
                            <version>1.2.0</version>
                        </dependency>

                        <!-- Junit 3 & 4 engine -->
                        <dependency>
                            <groupId>org.junit.vintage</groupId>
                            <artifactId>junit-vintage-engine</artifactId>
                            <version>5.3.0-M1</version>
                        </dependency>
                    </dependencies>
                </plugin>
                <plugin>
                    <groupId>org.codehaus.mojo</groupId>
                    <artifactId>build-helper-maven-plugin</artifactId>
                    <version>3.0.0</version>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-source-plugin</artifactId>
                    <version>3.0.1</version>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-javadoc-plugin</artifactId>
                    <version>${javadoc.plugin.version}</version>
                    <configuration>
                        <quiet>true</quiet>
                        <doclint>none</doclint>
                        <additionalJOptions>
                            <additionalJOption>-html5</additionalJOption>
                        </additionalJOptions>
                        <additionalDependencies>
                            <!-- TODO: this is only needed to make javadoc happy -->
                            <additionalDependency>
                                <groupId>org.apache.ant</groupId>
                                <artifactId>ant</artifactId>
                                <version>${ant.version}</version>
                            </additionalDependency>
                        </additionalDependencies>
                    </configuration>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-checkstyle-plugin</artifactId>
                    <version>${checkstyle.version}</version>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-enforcer-plugin</artifactId>
                    <version>3.0.0-M2</version>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-pmd-plugin</artifactId>
                    <version>${pmd.plugin.version}</version>
                    <executions>
                        <execution>
                            <phase>verify</phase>
                            <goals>
                                <goal>check</goal>
                                <goal>cpd</goal>
                            </goals>
                        </execution>
                    </executions>
                    <configuration>
                        <linkXRef>true</linkXRef>
                        <minimumTokens>100</minimumTokens>
                        <targetJdk>1.${java.version}</targetJdk>
                        <rulesets>
                            <ruleset>/net/sourceforge/pmd/pmd-dogfood-config.xml</ruleset>
                        </rulesets>
                        <excludeRoots>
                            <excludeRoot>target/generated-sources/javacc</excludeRoot>
                            <excludeRoot>target/generated-sources/antlr4</excludeRoot>
                        </excludeRoots>
                        <skipPmdError>false</skipPmdError>
                        <failurePriority>2</failurePriority>
                        <failOnViolation>true</failOnViolation>
                        <printFailingErrors>true</printFailingErrors>
                    </configuration>
                    <dependencies>
                        <!-- Note: we can't use a property for the version here due to https://issues.apache.org/jira/browse/MRELEASE-932 -->
                        <dependency>
                            <groupId>net.sourceforge.pmd</groupId>
                            <artifactId>pmd-core</artifactId>
                            <version>6.9.0</version>
                        </dependency>
                        <dependency>
                            <groupId>net.sourceforge.pmd</groupId>
                            <artifactId>pmd-java</artifactId>
                            <version>6.9.0</version>
                        </dependency>
                        <!-- This contains the dogfood ruleset -->
                        <dependency>
                            <groupId>net.sourceforge.pmd</groupId>
                            <artifactId>pmd-build-tools-config</artifactId>
                            <version>${pmd.build-tools.version}</version>
                        </dependency>
                    </dependencies>
                </plugin>
                <plugin>
                    <groupId>org.codehaus.mojo</groupId>
                    <artifactId>versions-maven-plugin</artifactId>
                    <version>2.5</version>
                </plugin>
                <plugin>
                    <groupId>org.sonatype.plugins</groupId>
                    <artifactId>nexus-staging-maven-plugin</artifactId>
                    <version>1.6.8</version>
                </plugin>
                <plugin>
                      <groupId>org.jacoco</groupId>
                      <artifactId>jacoco-maven-plugin</artifactId>
                      <version>0.8.2</version>
                </plugin>
                <!--This plugin's configuration is used to store Eclipse
                    m2e settings only. It has no influence on the Maven build itself. -->
                <plugin>
                    <groupId>org.eclipse.m2e</groupId>
                    <artifactId>lifecycle-mapping</artifactId>
                    <version>1.0.0</version>
                    <configuration>
                        <lifecycleMappingMetadata>
                            <pluginExecutions>
                                <pluginExecution>
                                    <pluginExecutionFilter>
                                        <groupId>org.apache.maven.plugins</groupId>
                                        <artifactId>maven-antrun-plugin</artifactId>
                                        <versionRange>[1.7,)</versionRange>
                                        <goals>
                                            <goal>run</goal>
                                        </goals>
                                    </pluginExecutionFilter>
                                    <action>
                                        <execute>
                                            <runOnIncremental>false</runOnIncremental>
                                            <runOnConfiguration>true</runOnConfiguration>
                                        </execute>
                                    </action>
                                </pluginExecution>
                            </pluginExecutions>
                        </lifecycleMappingMetadata>
                    </configuration>
                </plugin>
            </plugins>
        </pluginManagement>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-enforcer-plugin</artifactId>
                <executions>
                    <execution>
                        <id>enforce-versions</id>
                        <goals>
                            <goal>enforce</goal>
                        </goals>
                        <configuration>
                            <rules>
                                <requireJavaVersion>
                                    <version>[10,)</version>
                                </requireJavaVersion>
                            </rules>
                        </configuration>
                    </execution>
                </executions>
            </plugin>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-antrun-plugin</artifactId>
                <inherited>true</inherited>
                <executions>
                    <execution>
                        <id>pmd-clean</id>
                        <phase>clean</phase>
                        <configuration>
                            <target>
                                <echo>PMD specific tasks: cleaning generated xdocs</echo>
                                <delete quiet="true">
                                    <fileset dir="${src.xdocs.dir}/rules" includes="**/*.xml" />
                                    <fileset dir="${src.xdocs.dir}/" includes="mergedruleset.xml" />
                                </delete>
                            </target>
                        </configuration>
                        <goals>
                            <goal>run</goal>
                        </goals>
                    </execution>
                </executions>
            </plugin>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-pmd-plugin</artifactId>
                <!-- configuration is in plugin management section -->
            </plugin>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-checkstyle-plugin</artifactId>
                <executions>
                    <execution>
                        <id>checkstyle-check</id>
                        <phase>verify</phase>
                        <goals>
                          <goal>check</goal>
                        </goals>
                    </execution>
                </executions>
                <dependencies>
                    <dependency>
                        <groupId>com.puppycrawl.tools</groupId>
                        <artifactId>checkstyle</artifactId>
                        <version>8.8</version>
                    </dependency>
                    <dependency>
                        <groupId>net.sourceforge.pmd</groupId>
                        <artifactId>pmd-build-tools-config</artifactId>
                        <version>${pmd.build-tools.version}</version>
                    </dependency>
                </dependencies>
                <configuration>
                    <configLocation>/net/sourceforge/pmd/pmd-checkstyle-config.xml</configLocation>
                    <suppressionsLocation>/net/sourceforge/pmd/pmd-checkstyle-suppressions.xml</suppressionsLocation>
                    <includeTestSourceDirectory>true</includeTestSourceDirectory>
                    <sourceDirectories>
                        <sourceDirectory>${project.build.sourceDirectory}</sourceDirectory>
                    </sourceDirectories>
                </configuration>
            </plugin>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-javadoc-plugin</artifactId>
                <executions>
                    <execution>
                        <id>attach-javadocs</id>
                        <goals>
                            <goal>jar</goal>
                        </goals>
                    </execution>
                </executions>
            </plugin>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-source-plugin</artifactId>
                <executions>
                    <execution>
                        <id>attach-sources</id>
                        <goals>
                            <goal>jar</goal>
                        </goals>
                    </execution>
                </executions>
            </plugin>
            <plugin>
                <groupId>org.sonatype.plugins</groupId>
                <artifactId>nexus-staging-maven-plugin</artifactId>
                <extensions>true</extensions>
                <configuration>
                    <serverId>ossrh</serverId>
                    <nexusUrl>https://oss.sonatype.org/</nexusUrl>
                    <!-- if autoReleaseAfterClose is true, then the artifacts will be
                         automatically promoted to maven central -->
                    <autoReleaseAfterClose>true</autoReleaseAfterClose>
                </configuration>
            </plugin>
        </plugins>
    </build>

    <reporting>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-jxr-plugin</artifactId>
                <version>2.5</version>
            </plugin>

            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-javadoc-plugin</artifactId>
                <version>${javadoc.plugin.version}</version>
                <reportSets>
                    <reportSet>
                        <reports>
                            <report>javadoc</report>
                            <report>test-javadoc</report>
                            <report>aggregate</report>
                            <report>test-aggregate</report>
                        </reports>
                    </reportSet>
                </reportSets>
            </plugin>

            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-pmd-plugin</artifactId>
                <version>${pmd.plugin.version}</version>
                <!-- configuration is in plugin management section -->
            </plugin>

            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-checkstyle-plugin</artifactId>
                <version>${checkstyle.version}</version>
                <configuration>
                    <configLocation>/net/sourceforge/pmd/pmd-checkstyle-config.xml</configLocation>
                    <suppressionsLocation>/net/sourceforge/pmd/pmd-checkstyle-suppressions.xml</suppressionsLocation>
                    <includeTestSourceDirectory>true</includeTestSourceDirectory>
                    <sourceDirectories>
                        <sourceDirectory>${project.build.sourceDirectory}</sourceDirectory>
                    </sourceDirectories>
                </configuration>
                <reportSets>
                    <reportSet>
                        <reports>
                            <report>checkstyle</report>
                        </reports>
                    </reportSet>
                </reportSets>
            </plugin>

            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-project-info-reports-plugin</artifactId>
                <version>2.9</version>
                <reportSets>
                    <reportSet>
                        <reports>
                            <report>summary</report>
                            <report>dependencies</report>
                            <report>dependency-convergence</report>
                            <report>dependency-info</report>
                            <report>dependency-management</report>
                            <report>modules</report>
                            <report>plugin-management</report>
                            <report>plugins</report>
                            <report>project-team</report>
                            <report>mailing-list</report>
                            <report>cim</report>
                            <report>issue-tracking</report>
                            <report>license</report>
                            <report>scm</report>
                        </reports>
                    </reportSet>
                </reportSets>
            </plugin>

            <plugin>
                <groupId>org.codehaus.mojo</groupId>
                <artifactId>versions-maven-plugin</artifactId>
                <reportSets>
                    <reportSet>
                        <reports>
                            <report>dependency-updates-report</report>
                            <report>plugin-updates-report</report>
                            <report>property-updates-report</report>
                        </reports>
                    </reportSet>
                </reportSets>
            </plugin>
        </plugins>
    </reporting>

    <dependencyManagement>
        <dependencies>
            <dependency>
                <groupId>org.antlr</groupId>
                <artifactId>antlr4-runtime</artifactId>
                <version>${antlr.version}</version>
            </dependency>
            <dependency>
                <groupId>org.apache.ant</groupId>
                <artifactId>ant</artifactId>
                <version>${ant.version}</version>
            </dependency>
            <dependency>
                <groupId>org.apache.ant</groupId>
                <artifactId>ant-testutil</artifactId>
                <version>${ant.version}</version>
            </dependency>
            <dependency>
                <groupId>jaxen</groupId>
                <artifactId>jaxen</artifactId>
                <version>1.1.6</version>
                <exclusions>
                    <exclusion>
                        <artifactId>xercesImpl</artifactId>
                        <groupId>xerces</groupId>
                    </exclusion>
                    <exclusion>
                        <artifactId>xalan</artifactId>
                        <groupId>xalan</groupId>
                    </exclusion>
                    <exclusion>
                        <artifactId>icu4j</artifactId>
                        <groupId>com.ibm.icu</groupId>
                    </exclusion>
                </exclusions>
            </dependency>
            <dependency>
              <groupId>com.beust</groupId>
              <artifactId>jcommander</artifactId>
              <version>1.72</version>
            </dependency>
            <dependency>
                <groupId>org.ow2.asm</groupId>
                <artifactId>asm</artifactId>
                <version>6.2.1</version>
            </dependency>
            <dependency>
                <groupId>net.sourceforge.pmd</groupId>
                <artifactId>pmd-core</artifactId>
                <version>${project.version}</version>
            </dependency>
            <dependency>
                <groupId>net.sourceforge.pmd</groupId>
                <artifactId>pmd-test</artifactId>
                <version>${project.version}</version>
            </dependency>
            <dependency>
                <groupId>net.sourceforge.saxon</groupId>
                <artifactId>saxon</artifactId>
                <version>9.1.0.8</version>
            </dependency>
            <dependency>
                <groupId>net.sourceforge.saxon</groupId>
                <artifactId>saxon</artifactId>
                <version>9.1.0.8</version>
                <classifier>dom</classifier>
            </dependency>
            <dependency>
                <groupId>org.mozilla</groupId>
                <artifactId>rhino</artifactId>
                <version>1.7.7.2</version>
            </dependency>
            <dependency>
                <groupId>junit</groupId>
                <artifactId>junit</artifactId>
                <version>4.12</version>
            </dependency>
            <dependency>
                <groupId>org.hamcrest</groupId>
                <artifactId>hamcrest-library</artifactId>
                <version>1.3</version>
            </dependency>
            <dependency>
                <groupId>pl.pragmatists</groupId>
                <artifactId>JUnitParams</artifactId>
                <version>1.1.1</version>
            </dependency>
            <dependency>
                <groupId>net.java.dev.javacc</groupId>
                <artifactId>javacc</artifactId>
                <version>${javacc.version}</version>
            </dependency>
            <dependency>
                <groupId>commons-io</groupId>
                <artifactId>commons-io</artifactId>
                <version>2.6</version>
            </dependency>
            <dependency>
                <groupId>org.mockito</groupId>
                <artifactId>mockito-all</artifactId>
                <version>1.10.19</version>
            </dependency>
            <dependency>
                <groupId>org.apache.commons</groupId>
                <artifactId>commons-lang3</artifactId>
                <version>3.8.1</version>
            </dependency>
            <dependency>
                <groupId>org.slf4j</groupId>
                <artifactId>slf4j-api</artifactId>
                <version>1.7.25</version>
            </dependency>
            <dependency>
                <groupId>com.github.tomakehurst</groupId>
                <artifactId>wiremock</artifactId>
                <version>1.57</version>
                <exclusions>
                    <exclusion>
                        <artifactId>commons-lang</artifactId>
                        <groupId>commons-lang</groupId>
                    </exclusion>
                </exclusions>
            </dependency>
            <dependency>
                <groupId>org.codehaus.groovy</groupId>
                <artifactId>groovy</artifactId>
                <version>2.4.7</version>
            </dependency>
            <dependency>
                <groupId>com.github.stefanbirkner</groupId>
                <artifactId>system-rules</artifactId>
                <version>1.8.0</version>
            </dependency>

            <!-- TEST DEPENDENCIES -->


            <dependency>
                <groupId>net.sourceforge.pmd</groupId>
                <artifactId>pmd-lang-test</artifactId>
                <version>${project.version}</version>
                <scope>test</scope>
            </dependency>

            <!-- Kotlin -->

            <dependency>
                <groupId>org.jetbrains.kotlin</groupId>
                <artifactId>kotlin-stdlib</artifactId>
                <version>${kotlin.version}</version>
                <scope>test</scope>
            </dependency>

            <dependency>
                <groupId>org.jetbrains.kotlin</groupId>
                <artifactId>kotlin-stdlib-jdk8</artifactId>
                <version>${kotlin.version}</version>
                <scope>test</scope>
            </dependency>

            <dependency>
                <groupId>org.jetbrains.kotlin</groupId>
                <artifactId>kotlin-test-junit</artifactId>
                <version>${kotlin.version}</version>
                <scope>test</scope>
            </dependency>

            <dependency>
                <groupId>io.kotlintest</groupId>
                <artifactId>kotlintest-runner-junit5</artifactId>
                <version>3.1.8</version>
                <scope>test</scope>
            </dependency>

        </dependencies>
    </dependencyManagement>

    <repositories>
        <repository>
            <id>sonatype-nexus-snapshots</id>
            <name>Sonatype Nexus Snapshots</name>
            <url>https://oss.sonatype.org/content/repositories/snapshots</url>
            <releases>
                <enabled>false</enabled>
            </releases>
            <snapshots>
                <enabled>true</enabled>
            </snapshots>
        </repository>
        <repository>
            <id>central</id>
            <name>Central Repository</name>
            <url>https://repo.maven.apache.org/maven2</url>
            <snapshots>
                <enabled>false</enabled>
            </snapshots>
        </repository>
    </repositories>
    <pluginRepositories>
        <pluginRepository>
            <id>central</id>
            <name>Central Repository</name>
            <url>https://repo.maven.apache.org/maven2</url>
            <releases>
                <updatePolicy>never</updatePolicy>
            </releases>
            <snapshots>
                <enabled>false</enabled>
            </snapshots>
        </pluginRepository>
        <pluginRepository>
            <id>sonatype-nexus-plugin-snapshots</id>
            <name>Sonatype Nexus Snapshots</name>
            <url>https://oss.sonatype.org/content/repositories/snapshots</url>
            <releases>
                <enabled>false</enabled>
            </releases>
            <snapshots>
                <enabled>true</enabled>
            </snapshots>
        </pluginRepository>
    </pluginRepositories>

    <profiles>
        <profile>
            <id>pmd-release</id>
            <properties>
                <pmd.website.baseurl>https://pmd.github.io/pmd-${project.version}</pmd.website.baseurl>
            </properties>
            <build>
                <plugins>
                    <plugin>
                        <groupId>org.apache.maven.plugins</groupId>
                        <artifactId>maven-gpg-plugin</artifactId>
                        <version>1.6</version>
                        <executions>
                            <execution>
                                <id>sign-artifacts</id>
                                <phase>verify</phase>
                                <goals>
                                    <goal>sign</goal>
                                </goals>
                            </execution>
                        </executions>
                    </plugin>
                </plugins>
            </build>
        </profile>

        <profile>
            <id>doclint</id>
            <build>
                <pluginManagement>
                    <plugins>
                        <plugin>
                            <groupId>org.apache.maven.plugins</groupId>
                            <artifactId>maven-javadoc-plugin</artifactId>
                            <configuration>
                                <doclint>all</doclint>
                            </configuration>
                        </plugin>
                    </plugins>
                </pluginManagement>
            </build>
        </profile>

        <profile>
            <id>coveralls</id>
            <build>
                <plugins>
                    <plugin>
                      <groupId>org.jacoco</groupId>
                      <artifactId>jacoco-maven-plugin</artifactId>
                      <executions>
                          <execution>
                              <id>default-prepare-agent</id>
                              <goals>
                                  <goal>prepare-agent</goal>
                              </goals>
                          </execution>
                      </executions>
                    </plugin>
                    <plugin>
                        <groupId>org.eluder.coveralls</groupId>
                        <artifactId>coveralls-maven-plugin</artifactId>
                        <version>4.3.0</version>
                        <dependencies>
                            <!--
                                coveralls maven plugin needs javax.xml.bind api
                                See also https://github.com/trautonen/coveralls-maven-plugin/issues/112
                            -->
                            <dependency>
                                <groupId>javax.xml.bind</groupId>
                                <artifactId>jaxb-api</artifactId>
                                <version>2.3.0</version>
                            </dependency>
                        </dependencies>
                    </plugin>
                </plugins>
            </build>
        </profile>

        <profile>
            <id>sonar</id>
            <properties>
                <sonar.host.url>https://sonarcloud.io</sonar.host.url>
            </properties>
            <build>
                <pluginManagement>
                    <plugins>
                        <plugin>
                            <groupId>org.sonarsource.scanner.maven</groupId>
                            <artifactId>sonar-maven-plugin</artifactId>
                            <version>3.4.1.1168</version>
                        </plugin>
                    </plugins>
                </pluginManagement>
                <plugins>
                    <plugin>
                      <groupId>org.jacoco</groupId>
                      <artifactId>jacoco-maven-plugin</artifactId>
                      <executions>
                          <execution>
                              <id>default-prepare-agent</id>
                              <goals>
                                  <goal>prepare-agent</goal>
                              </goals>
                          </execution>
                      </executions>
                    </plugin>
                </plugins>
            </build>
        </profile>
    </profiles>

    <modules>
        <module>pmd-core</module>
        <module>pmd-cpp</module>
        <module>pmd-cs</module>
        <module>pmd-dist</module>
        <module>pmd-fortran</module>
        <module>pmd-go</module>
        <module>pmd-groovy</module>
        <module>pmd-java</module>
        <module>pmd-javascript</module>
        <module>pmd-jsp</module>
        <module>pmd-matlab</module>
        <module>pmd-objectivec</module>
        <module>pmd-perl</module>
        <module>pmd-php</module>
        <module>pmd-plsql</module>
        <module>pmd-python</module>
        <module>pmd-ruby</module>
        <module>pmd-scala</module>
        <module>pmd-swift</module>
        <module>pmd-test</module>
        <module>pmd-visualforce</module>
        <module>pmd-vm</module>
        <module>pmd-xml</module>

        <!-- java8 modules -->
        <module>pmd-apex-jorje</module>
        <module>pmd-apex</module>
        <module>pmd-java8</module>
        <module>pmd-ui</module>
        <module>pmd-doc</module>
        <module>pmd-lang-test</module>
    </modules>
</project>
© 2018 GitHub, Inc.
Terms
Privacy
Security
Status
Help
Contact GitHub
Pricing
API
Training
Blog
About
Press h to open a hovercard with more details.
