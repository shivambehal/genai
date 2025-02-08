<test-cases>
    <case id="simple-1">
        <english>I eat bread.</english>
        <vocabulary>
            <word>
                <french>manger</french>
                <english>to eat</english>
            </word>
            <word>
                <french>pain</french>
                <english>bread</english>
            </word>
        </vocabulary>
        <structure>[Subject] + [Verb] + [Object].</structure>
        <considerations>
            - Basic sentence with subject, verb, and object
            - Present tense form
            - Subject must be included in French
        </considerations>
    </case>
    <case id="simple-2">
        <english>The book is red.</english>
        <vocabulary>
            <word>
                <french>livre</french>
                <english>book</english>
            </word>
            <word>
                <french>rouge</french>
                <english>red</english>
            </word>
        </vocabulary>
        <structure>[Subject] + [être] + [Adjective].</structure>
        <considerations>
            - Simple descriptor sentence
            - Uses être verb
            - Adjective agreement required
        </considerations>
    </case>
</test-cases>

### 1.2 Question Sentences
```xml
<test-cases>
    <case id="question-1">
        <english>Do you have a cat?</english>
        <vocabulary>
            <word>
                <french>avoir</french>
                <english>to have</english>
            </word>
            <word>
                <french>chat</french>
                <english>cat</english>
            </word>
        </vocabulary>
        <structure>Est-ce que + [Subject] + [Verb] + [Object]?</structure>
        <considerations>
            - Basic question formation
            - Uses est-ce que
            - Article required
        </considerations>
    </case>
</test-cases>

### 1.3 Compound Sentences
```xml
<test-cases>
    <case id="compound-1">
        <english>I eat bread and drink water.</english>
        <vocabulary>
            <word>
                <french>manger</french>
                <english>to eat</english>
            </word>
            <word>
                <french>pain</french>
                <english>bread</english>
            </word>
            <word>
                <french>boire</french>
                <english>to drink</english>
            </word>
            <word>
                <french>eau</french>
                <english>water</english>
            </word>
        </vocabulary>
        <structure>[Subject] + [Verb1] + [Object1] + et + [Verb2] + [Object2].</structure>
        <considerations>
            - Compound sentence with two actions
            - Subject shared between clauses
            - Article usage with each noun
        </considerations>
    </case>
</test-cases>

## 2. Teaching Components Tests

### 2.1 Vocabulary Table Format
```xml
<vocabulary-test>
    <requirements>
        - Only show dictionary forms
        - No articles included
        - Appropriate A1 level words
        - Clear English | French format
        - No duplicate entries
    </requirements>
    <example>
        <good>
            English | French
            --------|--------
            to eat  | manger
            cat     | chat
        </good>
        <bad>
            English | French
            --------|--------
            the cat | le chat
            eating  | mangeant
        </bad>
    </example>
</vocabulary-test>

### 2.2 Sentence Structure Format
```xml
<structure-test>
    <requirements>
        - Use square brackets for components
        - No conjugations shown
        - No articles included
        - Simple A1 level patterns
        - Based on example patterns
    </requirements>
    <example>
        <good>[Subject] + [Verb] + [Object]</good>
        <bad>[The Subject] + [conjugated Verb] + [Article + Object]</bad>
    </example>
</structure-test>

## 3. State Transition Tests

### 3.1 Valid Transitions
```xml
<transition-test>
    <scenario id="setup-to-attempt">
        <initial-state>Setup</initial-state>
        <input>Je mange le pain.</input>
        <expected-state>Attempt</expected-state>
        <validation>
            - Input contains French text
            - Uses vocabulary from setup
            - Is an attempt at translation
        </validation>
    </scenario>
    <scenario id="attempt-to-clues">
        <initial-state>Attempt</initial-state>
        <input>How do I use articles?</input>
        <expected-state>Clues</expected-state>
        <validation>
            - Input is a question
            - References grammar concept
            - Related to previous attempt
        </validation>
    </scenario>
</transition-test>

## 4. Teaching Scenario Tests

### 4.1 Common Mistakes
```xml
<teaching-test>
    <scenario id="article-mistake">
        <student-attempt>Je mange pain.</student-attempt>
        <error>Missing article</error>
        <expected-guidance>
            - Acknowledge attempt
            - Hint about article usage
            - Encourage new attempt
        </expected-guidance>
    </scenario>
    <scenario id="adjective-agreement">
        <student-attempt>Le livre est vert.</student-attempt>
        <error>Adjective agreement with feminine noun</error>
        <expected-guidance>
            - Point out noun gender
            - Review adjective agreement rules
            - Encourage correction
        </expected-guidance>
    </scenario>
</teaching-test>

## 5. Validation Criteria

### 5.1 Response Scoring
```xml
<scoring-criteria>
    <category name="vocabulary-table">
        <criteria>
            - Contains all necessary words (2 points)
            - Correct table format (2 points)
            - Dictionary forms only (2 points)
            - No articles included (2 points)
            - A1 appropriate vocabulary (2 points)
        </criteria>
    </category>
    <category name="sentence-structure">
        <criteria>
            - Clear bracketed format (2 points)
            - No conjugations shown (2 points)
            - A1 appropriate level (2 points)
            - Matches example patterns (2 points)
            - No articles included (2 points)
        </criteria>
    </category>
    <category name="considerations">
        <criteria>
            - Concise bullet points (2 points)
            - Clear next steps (2 points)
            - Relevant to attempt (2 points)
            - A1 appropriate guidance (2 points)
            - No direct answers (2 points)
        </criteria>
    </category>
</scoring-criteria>

## 6. Version Control

### 6.1 Document History
```xml
<version-control>
    <version number="1.0">
        <changes>
            - Initial test documentation
            - Basic test cases added
            - State transition examples
            - Teaching scenario examples
        </changes>
        <date>2025-02-08</date>
    </version>
    <planned-improvements>
        - Add more complex sentence patterns
        - Expand teaching scenarios
        - Include cultural context tests
        - Add error recovery scenarios
    </planned-improvements>
</version-control>