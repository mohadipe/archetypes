# Maven Archetype um ein sehr einfaches Java-Maven-Project anzulegen.
    - JUnit 4.12 (via dependencyManagement)
    - Java 1.8 (target und source)
    - UTF8
    - readme.md

# Ziel
    - Schnell ein benutzbares Java-Maven-Projekt aufsetzen.
    - Mit aktueller Test-Bibliothek los legen zu können.
    - Mit aktuellem Java los legen zu können.
    - Encoding ist richtig eingestellt.

# Nicht Ziel des Projectes
    - Endlos weiter ausbauen, mit weiteren Abhängigkeiten, ...
    - kein Multi-Modul-Support.

# Verwendung
## Bauen
    - mvn clean install <- lokales Repository
    - Unter .m2 muss eine Datei: archetype-catalog.xml existieren. In dieser trägt man seine Archetypen ein.
    Beispiel:
        <?xml version="1.0" encoding="UTF-8"?>
        <archetype-catalog xsi:schemaLocation="http://maven.apache.org/plugins/maven-archetype-plugin/archetype-catalog/1.0.0 http://maven.apache.org/xsd/archetype-catalog-1.0.0.xsd"
            xmlns="http://maven.apache.org/plugins/maven-archetype-plugin/archetype-catalog/1.0.0"
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
          <archetypes>
            <archetype>
              <groupId>de.mohadipe.archetype</groupId>
              <artifactId>simple-java</artifactId>
              <version>0.0.2-SNAPSHOT</version>
              <repository></repository>
            </archetype>
          </archetypes>
        </archetype-catalog>

## Kommandozeile
    ausführen: mvn archetype:generate -DarchetypeCatalog=local -DarchetypeGroupId="de.mohadipe.archetype" -DarchetypeArtifactId="simple-java" -DarchetypeVersion="0.0.2-SNAPSHOT"
    
    Ausfüllen einiger Variablen:
    groupId: <de.mohadipe.test>
    artifactId: <test-it>
    version: <0.0.1-SNAPSHOT>
    package: <de.mohadipe.test>
    project-name: <TestIt> <- Aufpassen, muss mit Grossbuchstaben beginnen weil die initiale Klasse den gleichen Namen bekommt.
    property-file-name <test>
    junit-version: Vorgabe lassen oder ändern


