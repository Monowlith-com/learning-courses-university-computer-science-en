---
document_id: "university_computer_science_en:glossary"
series_id: "university_computer_science_en:_index"
series_part: 86
document_version: "0.1.1"
created: "2026-11-19"
updated: "2026-11-24"
title: "Glossary – Computer Science"
author: "Stephan Kühn"
document_type: "Supporting document"
project_name: "Learning Courses"
course: "computer science"
language: "en"
group: "Supporting material"
study_level: "University studies (supporting material)"
study_role: "Look up computer science terminology"
categories: ["Education/Learning Courses", "Supporting material/Computer Science"]
keywords: ["Computer Science", "Supporting material", "Look up computer science terminology"]
website: "https://monowlith.com"
github: "https://github.com/monowlith-com/learning-courses-university-computer-science-en"
license: "CC BY-NC-SA 4.0 International"
---

# Glossary – Computer Science

  Term                      Classification                                                  Key limitation
  ------------------------  --------------------------------------------------------------  -----------------------------------------------------------------------------
  Retrieval authorisation   Authorised access to relevant sources in RAG                    A semantic match or stale cache does not grant read permission
  KV cache                  Cache for key/value representations of earlier tokens           Context length, KV heads, precision and parallelism affect occupancy
  C2PA                      Signed, technically verifiable provenance claims for media      A signature does not automatically establish truthfulness
  Article 50 of the AI Act  Role-dependent transparency obligations for certain AI systems  A narrowly limited grace period for paragraph 2 is not a general postponement

  New/refined term      Brief meaning                                            Key limitation
  --------------------  -------------------------------------------------------  -----------------------------------------------------------
  O notation            Asymptotic upper bound on growth                         Not automatically a tight or measured runtime
  Θ notation            Asymptotically matching upper and lower bounds           Only for the specific cost function analysed
  Check/write race      Both participants see the same old state before writing  Only shared atomic protection prevents the duplicate effect
  External side effect  Payment, message or action outside a local database      Local `ROLLBACK` does not automatically reverse it
  0-RTT                 Early data when suitably resuming a QUIC/TLS context     May introduce replay risks for business effects

## M7-L3 – Distributed systems and system models {#S1}

  Term                      Meaning                                     Brief definition
  ------------------------  ------------------------------------------  ---------------------------------------------------------------------------------------
  Distributed system        Multiple independently operating processes  Communication, partial failures and lack of a global view shape correctness
  Happened-before           Causal ordering of events                   Local execution, send before receive, and transitivity
  Lamport clock             Logical counter time                        Causal order implies smaller timestamps; the converse does not hold
  Vector clock              Multi-component logical timestamp           Identifies causal dependence or concurrency under the model
  Network partition         Interrupted communication between groups    May prevent safe joint decisions
  Safety / Liveness         Safety / progress                           Nothing forbidden ever happens / eventual progress under certain conditions
  Timeout                   Expiry of a waiting period                  Suspected disruption, not proof of server failure
  Idempotence               Business effect safe to repeat              No unwanted additional effects for an identical request
  Linearisability           Strong consistency model                    Operations appear atomic between invocation and response, respecting real-time order
  Causal consistency        Ordering of dependent changes               Causal predecessors appear before their effects
  Eventual Consistency      Long-term convergence                       In the absence of changes and with working communication, states may become equal
  Consensus                 Distributed agreement                       Joint decision under defined failure assumptions
  Majority quorum           Majority of voting participants             Two majorities intersect; additional protocol rules are needed
  Raft                      Consensus protocol                          Leader election, replicated log and safety rules
  CAP theorem               Limit during network partitions             Under the model assumptions, not both linearisable and available everywhere
  FLP result                Impossibility result                        No guaranteed termination of deterministic asynchronous consensus with possible failure
  CRDT                      Conflict-free Replicated Data Type          Data structure for low-conflict convergence under suitable rules
  Replicated state machine  Shared log and deterministic application    Identical command sequences produce identical states from identical initial states
  Fencing Token             Protection against stale leader authority   The controlling resource rejects actions from old leadership epochs
  Backoff / Jitter          Delay and variation during retries          Limits and spreads retry traffic during disruptions

## M7-L2 – Correctness, computability and complex methods {#S2}

  Term                          Meaning                                           Brief definition
  ----------------------------  ------------------------------------------------  -----------------------------------------------------------------------------
  Specification                 Precise behavioural contract                      Defines expected inputs and outputs and prerequisites
  Precondition / Postcondition  Precondition / Postcondition                      Property required beforehand or guaranteed afterwards
  Hoare triple                  `{P} C {Q}`                                       Formal scheme for a partial correctness statement
  Partial / total correctness   Correct if terminated / correct and terminated    Termination requires additional proof
  Loop invariant                Persistently preserved assertion                  Valid at defined checkpoints of each iteration
  Termination measure           Well-founded decreasing quantity                  Justifies why a computation does not continue indefinitely
  Induction                     Proof by base case and step                       Establishes statements for all natural quantities or recursive structures
  Big O / Ω / Θ                 Upper / lower / tight asymptotic bound            Describe growth in resource requirements
  Amortised analysis            Average over a guaranteed sequence of operations  Neither an empirically measured average nor a guarantee of individual runtime
  Reduction                     Problem transformation                            Transfers solvability or hardness at a specified cost
  P / NP                        Polynomially solvable / polynomially verifiable   Formal complexity classes of decision problems
  NP-complete                   NP and NP-hard                                    Hardness under polynomial reductions; not the same as undecidable
  Computability                 Algorithmic solvability in principle              Independent of actual computer speed
  Halting problem               General termination decision                      Undecidable for arbitrary programs and inputs
  Diagonalisation               Contradiction through self-reference              Classical method of proving undecidability
  Safety / Liveness             Never an invalid state / eventual progress        Properties of formal state models
  Model Checking                Systematic state checking                         Searches executions of a formally defined model
  SAT / SMT                     Propositional / theory-based satisfiability       Formal tools for certain logical formulae

## M7-L1 – Scientific computer science {#S3}

  Term                               Meaning                                    Brief definition
  ---------------------------------  -----------------------------------------  ------------------------------------------------------------------
  Scientific model                   Simplified system description              Answers specific questions under explicit assumptions
  Hypothesis                         Testable conjecture                        Statement that can be tested through suitable observations
  Operationalisation                 Measurable definition                      Translation of an abstract concept into indicators
  Baseline                           Basis for comparison                       Defined reference variant of an experiment
  Falsifiability                     Principle of possible refutation           Certain conceivable observations contradict the hypothesis
  Confounding variable / Confounder  Alternative influence                      May distort an apparent cause-and-effect relationship
  Randomisation                      Random assignment                          Intended to reduce systematic biases in experimental design
  Blocking                           Formation of blocks                        Grouping comparable experimental conditions
  Correlation / Causation            Association / cause                        Joint variation does not automatically establish causation
  Validity                           Validity of a conclusion                   Checks whether measurement and assertion fit the research question
  Verification / Validation          Specification check / suitability check    Built correctly versus the right system being built
  Reproducibility                    Same procedure and same data               Consistent computational results under defined conditions
  Replication                        New data, comparable question              Consistent results from an independent study
  Generalisability                   Transferability                            Result holds in other situations or populations
  Percentile / p99                   Distribution threshold                     p99 denotes approximately the 99% threshold
  Confidence interval                Statistical interval estimation procedure  Defined coverage rate across many applications
  p-value                            Statistic under the null hypothesis        Not the probability that the null hypothesis is true
  Artefact                           Traceable research product                 E.g. dataset, code, measurement protocol or experimental design

## M10-L2 – Advanced data modelling and database queries {#S4}

  Term                   Meaning                                 Brief definition
  ---------------------  --------------------------------------  --------------------------------------------------------------------------
  Data modelling         Domain-specific structuring             Describing objects, relationships and rules as data
  Entity / Attribute     Object / property                       For example, a video and its title
  Cardinality            Number of allowed relationships         1:1, 1:n, n:m; also consider optionality
  Primary key            Primary Key                             Unique identifier of a table row
  Foreign key            Foreign Key                             Reference whose validity the DBMS can check
  Functional dependency  Determination rule between attributes   For example, `kanal_id` determines the channel name
  1NF / 2NF / 3NF        First, second and third normal forms    Criteria for reducing undesirable data dependencies
  Anomaly                Error due to unsuitable data structure  Insertion, update or deletion anomaly
  SQL                    Structured Query Language               Declarative language for structured data
  JOIN                   Table join                              Forms row combinations according to a condition
  INNER / LEFT JOIN      Inner / left outer join                 Only matches or all left-hand rows, respectively
  Granularity            Domain-specific level of a result row   For example, one row per video or per tag assignment
  GROUP BY / HAVING      Group / filter groups                   Form aggregations and select according to them
  NULL                   Missing data value                      Not equal to 0 or an empty string; observe three-valued logic
  COALESCE               Select first non-null value             For example, convert a missing sum to 0 where meaningful
  CTE                    Common Table Expression                 Subquery named with WITH within an SQL statement
  Window function        Window Function                         Calculates values across groups of rows without collapsing them completely
  EXPLAIN                Display of query plan                   Shows the execution path chosen or planned by the database system
  Selectivity            Effect of a filter                      Proportion of records that satisfy a condition
  Lost Update            Lost update                             Two uncoordinated changes overwrite each other
  Parameterised query    Pass values separately from SQL syntax  Basic protection against SQL injection
  Tenant                 Separate customer/user group            Requires unambiguous data assignment and permissions
  RLS                    Row-Level Security                      Database-side access control at row level
  Database migration     Structural/data change                  Planned versioning and transition of a schema
  Expand-and-Contract    Staged schema migration                 Keep new and old structures temporarily compatible

## M10-L1 – Networks and practical IT security {#S5}

  Term               Meaning                                     Brief definition
  -----------------  ------------------------------------------  ------------------------------------------------------------------------------------
  CIDR               Classless Inter-Domain Routing              Expresses IP networks through prefix length, e.g. `/27`
  VLAN               Virtual Local Area Network                  Logical separation of local network segments
  NAT                Network Address Translation                 Translates IP address information; not comprehensive security protection
  TCP / UDP / QUIC   Transport mechanisms                        Different models for connection and datagram communication
  TLS 1.3            Transport Layer Security                    Protocol for protecting the transport channel, described in RFC 9846 since July 2026
  DNSSEC             DNS Security Extensions                     Enables authenticity/integrity checks of DNS data; does not encrypt the query
  Least Privilege    Principle of minimum permissions            Each identity receives only the necessary permissions
  Default Deny       Deny by default                             Open communication paths only with defined permission
  Authentication     Establishment of identity                   Checks who or what is signing in
  Authorisation      Permission check                            Checks what the authenticated actor is actually allowed to do
  Passkey            Key-based authentication                    Can be designed to be service-bound and phishing-resistant
  OWASP Top 10:2025  Risk overview for web applications          Ten categories of frequently relevant vulnerability patterns
  Zero Trust         Access model without blanket network trust  Check resource, identity and context individually
  Incident Response  Response to security incidents              Detect, contain and resolve incidents, and restore operations
  Restore test       Recovery test                               Checks whether a backup is usable in practice

## M8-L3 – Advanced operating systems and concurrency {#S6}

  Term                  Meaning                                           Brief definition
  --------------------  ------------------------------------------------  ----------------------------------------------------------------------
  Process               Execution context of a program                    Includes a virtual address space and resources
  Thread                Thread of execution                               Sequence of instructions within a process schedulable by the scheduler
  Concurrency           Concurrency                                       Coordination of activities overlapping in time
  Parallelism           Parallelism                                       Truly simultaneous computations on multiple processing units
  Scheduler             Operating system scheduling component             Selects runnable threads for CPU cores
  Context switch        Context Switch                                    Saves the state of one execution and resumes another
  EEVDF                 Earliest Eligible Virtual Deadline First          Fair Linux scheduling approach with virtual lag and deadlines
  Virtual memory        Virtual Memory                                    Process-specific address space with translated memory addresses
  Page Fault            Page fault exception                              Signals a missing or invalid memory mapping
  Page Cache            Cache for file/page contents                      Avoids repeated slow file accesses
  Swap / Pagefile       Paging to mass storage                            Can alleviate memory shortages but cannot replace RAM
  Race Condition        Timing-dependent concurrency error                Result depends on uncoordinated accesses
  Mutex                 Mutual Exclusion                                  Lock for exclusive access to a critical section
  Semaphore             Counting synchronisation mechanism                For example, limits simultaneous resource accesses
  Atomic                Indivisibly visible operation                     For individual data changes; not a general transaction
  Deadlock              Deadlock                                          Cyclic waiting dependency without progress
  Livelock              Active obstruction of progress                    Participants react but accomplish nothing useful
  Starvation            Persistent disadvantage                           Task receives too few resources in the long run
  Priority Inheritance  Priority inheritance                              Lock holder temporarily receives the higher waiting priority
  IPC                   Interprocess Communication                        Exchange of data between independent processes
  Amdahl's law          Limit of parallel speed-up                        Serial portions limit overall speed-up
  PREEMPT_RT            Real-time-capable Linux preemption configuration  Improves timing behaviour in specific kernel paths

The terms are defined here as an introduction. Detailed explanations can be found in the corresponding lessons.

  Term                      Expanded form / meaning                                     Brief explanation
  ------------------------  ----------------------------------------------------------  --------------------------------------------------------------------------------------------------
  Formal language           Set of admissible words over an alphabet                    Precise definition of all permitted strings
  Alphabet                  Finite set of symbols                                       Building blocks of a formal language, e.g. `{0,1}`
  Regular language          Language recognisable by a finite automaton                 Typical basis of classical regular expressions
  DFA                       Deterministic Finite Automaton                              Finite automaton with a unique successor state per symbol
  NFA                       Nondeterministic Finite Automaton                           Finite automaton with multiple conceptually possible successor states
  Pushdown automaton (PDA)  Pushdown Automaton                                          State model with stack memory, e.g. for bracket nesting
  CFG                       Context-Free Grammar                                        Grammar with non-terminal symbols and derivation rules
  Lexer                     Lexical analyser                                            Groups characters into tokens
  Token                     Lexical unit                                                For example, an identifier, number or arithmetic operator
  Parser                    Syntax analyser                                             Checks a token sequence against the grammar and builds a structure
  AST                       Abstract Syntax Tree                                        Abstract syntax tree of an expression or program
  Symbol table              Directory of names and properties                           Supports scope and type checks
  IR                        Intermediate Representation                                 Intermediate representation for analysis, optimisation and target code
  Compiler                  Translator of program representations                       Produces e.g. bytecode, IR or machine code
  AOT                       Ahead-of-Time Compilation                                   Translates parts of a program before their later execution
  Halting problem           General decision problem in computability                   Not universally decidable for arbitrary programs and inputs
  Propositional logic       Logical propositions with true/false values                 Combines conditions using AND, OR, NOT and implication
  Predicate logic           Statements about objects                                    Formulates properties and relationships with variables and quantifiers
  Quantifiers               ∀ for all, ∃ there exists                                   Describe the validity of statements over sets of objects
  De Morgan's laws          Logical transformation rules                                Relate negation to AND or OR
  Set                       Collection of distinguishable elements                      Membership matters, not order or multiplicity
  Intersection              $A\cap B$                                                   Elements belonging to both A and B
  Cartesian product         $A\times B$                                                 Set of all ordered pairs from two sets
  Function                  Unique assignment for each admissible input                 Assigns exactly one output to each input
  Relation                  Subset of a Cartesian product                               Describes which ordered pairs stand in a relationship
  Equivalence relation      Reflexive, symmetric and transitive relation                Partitions the original set into equivalence classes
  Partial order             Reflexive, antisymmetric, transitive relation               Orders elements without requiring every pair to be comparable
  Induction                 Mathematical proof technique                                Base case plus transition to a successor
  Graph                     Vertices and edges                                          Represents connections, networks and dependencies
  DAG                       Directed Acyclic Graph                                      Directed graph without directed cycles
  BFS                       Breadth-First Search                                        Traverses graphs step by step according to edge distance
  DFS                       Depth-First Search                                          Follows paths through a graph and returns to alternatives
  Adjacency list            Neighbourhood representation of a graph                     Stores the neighbours of each vertex
  Combinatorics             Counting finite possibilities                               Explains permutations, combinations and selection counts
  Modulo                    Remainder of integer division                               Groups numbers by residue class, e.g. in sharding
  Invariant                 Preservation condition during execution                     Property intended to remain true across defined state transitions
  Algorithm                 Unambiguously described step-by-step procedure              Solves a specified class of tasks under stated prerequisites
  Abstraction               Deliberately simplified model                               Omits properties irrelevant to a particular question
  Computability             Decidability/solvability by algorithmic methods             Not every formal problem is algorithmically decidable for all inputs
  Computer science          Science of representing and processing information          Studies models, algorithms, systems and their limits
  ISA                       Instruction Set Architecture                                Software-visible instruction set/register contract of a processor family
  ALU                       Arithmetic Logic Unit                                       Arithmetic and logic circuit within a processor
  JIT                       Just-in-Time Compilation                                    Translates code into machine instructions during execution
  Virtual memory            Virtual Memory                                              Virtual address space and mapping onto physical memory; not synonymous with swap
  API                       Application Programming Interface                           Defined programming interface
  CPU                       Central Processing Unit                                     General-purpose main processor
  GPU                       Graphics Processing Unit                                    Processor particularly suitable for many parallel computations
  RAM                       Random Access Memory                                        Volatile working memory
  SSD                       Solid State Drive                                           Persistent flash-based mass storage
  DNS                       Domain Name System                                          Resolution of domain names into network addresses, among other functions
  TCP                       Transmission Control Protocol                               Reliable transport protocol mechanism in IP networks
  IP                        Internet Protocol                                           Addressing and forwarding network packets
  TLS                       Transport Layer Security                                    Cryptographically secured transport connection
  HTTP                      Hypertext Transfer Protocol                                 Protocol for web communication
  VPS                       Virtual Private Server                                      Rented virtual server
  VM                        Virtual Machine                                             Virtual machine with its own guest operating system
  VPC                       Virtual Private Cloud                                       Logically isolated cloud network area
  IAM                       Identity and Access Management                              Management of identities and permissions
  CDN                       Content Delivery Network                                    Distributed delivery of content
  CI/CD                     Continuous Integration / Continuous Delivery or Deployment  Automated integration and deployment of software
  IaaS                      Infrastructure as a Service                                 Rented infrastructure resources
  PaaS                      Platform as a Service                                       Managed platform for one's own applications
  SaaS                      Software as a Service                                       Use of ready-made software as an online service
  SQL                       Structured Query Language                                   Language for querying and processing relational data
  NoSQL                     Not Only SQL (common interpretation)                        Umbrella term for several non-classically relational database models
  ACID                      Atomicity, Consistency, Isolation, Durability               Fundamental transaction properties
  RPO                       Recovery Point Objective                                    Target for the maximum acceptable period of data loss
  RTO                       Recovery Time Objective                                     Target for the maximum acceptable recovery time
  SLA                       Service Level Agreement                                     Contractual service quality commitment
  SLO                       Service Level Objective                                     Internal or documented service quality target
  IaC                       Infrastructure as Code                                      Infrastructure in a verifiable machine-readable description
  MFA                       Multi-Factor Authentication                                 Sign-in using multiple independent factors
  REST                      Representational State Transfer                             Architectural style for networked applications
  NAT                       Network Address Translation                                 Translation of network addresses
  CAP                       Consistency, Availability, Partition tolerance              Statement about trade-offs during network partitions in certain distributed system models
  ROS 2                     Robot Operating System 2                                    Middleware and tool ecosystem for robotics
  Array                     Array of entries accessible by position numbers             Direct index access typically $O(1)$
  Linked list               Linked List                                                 Sequence of nodes that refer to other nodes
  Hash table                Hash Table                                                  Data structure for fast key-based access with suitable distribution
  Binary search             Binary Search                                               Halves the search range in an ordered, directly accessible structure
  Tree / Search tree        Tree / Search Tree                                          Hierarchical data structure; balanced search trees often $O(\log n)$
  Graph                     Graph                                                       Vertices and edges for representing relationships
  BFS                       Breadth-First Search                                        Breadth-first traversal of graphs layer by layer
  DFS                       Depth-First Search                                          Depth-first traversal; initially explores paths in depth
  LIFO                      Last In, First Out                                          Last inserted, first removed – stack
  FIFO                      First In, First Out                                         First inserted, first removed – queue
  Stack                     Stack                                                       Data structure following the LIFO principle
  Queue                     Queue                                                       Data structure following the FIFO principle
  Recursion                 Recursion                                                   Description of a problem through smaller instances of the same problem
  Memoisation               Memoization                                                 Caching previously calculated partial results
  Dynamic programming       Dynamic Programming                                         Reuse of solutions to overlapping subproblems
  Greedy                    Greedy method                                               Local decisions whose global optimality must be checked separately
  Big O / O notation        Asymptotic upper bound                                      Describes a growth bound for computational/memory cost
  NP-hard                   NP-hard                                                     Class of problems at least as hard as the hardest problems in NP; not synonymous with uncomputable

  Term                       Meaning                                                 Classification
  -------------------------  ------------------------------------------------------  -------------------------------------------------------------------------
  Module                     Software component with clearly defined responsibility  Makes changes and tests more manageable
  Cohesion                   Internal unity of a module                              How closely a module's tasks belong together in terms of their purpose
  Coupling                   Dependencies between software components                Less unnecessary coupling facilitates changes
  Encapsulation              Encapsulation                                           Protecting internal states behind defined operations
  Layered architecture       Layered Architecture                                    Separation of e.g. presentation, business logic and data access
  Contract                   Interface contract                                      Specified inputs/outputs and errors of an interface
  JSON                       JavaScript Object Notation                              Text format for structured data
  XML                        Extensible Markup Language                              Extensible markup language for structured data
  CSV                        Comma-Separated Values                                  Row-based table format
  State machine              State Machine                                           Model of allowed states and transitions
  Event-Driven Architecture  Event-driven architecture                               Processing reacts to reported events
  Unit test                  Component test                                          Tests a small, clearly bounded functional unit
  Integration test           Integration Test                                        Tests interaction between several components
  E2E                        End to End                                              End-to-end test of a complete user workflow
  Regression test            Regression Test                                         Checks whether changes damage existing behaviour
  Git                        Distributed version control system                      Manages traceable file versions
  Commit                     Version control entry                                   Stores a traceable set of changes
  Branch                     Development branch                                      Allows isolated variants of changes
  CI                         Continuous Integration                                  Frequent merging and automated testing of changes
  CD (Delivery)              Continuous Delivery                                     Tested software is ready for release
  CD (Deployment)            Continuous Deployment                                   Automatic production deployment of changes that pass tests
  Build                      Software build                                          Produces a usable program/package artefact from source code
  Monolith                   Application deployed as a single unit                   Can be cleanly divided into modules internally
  Microservices              Independently deployable services                       Allow independent operation but increase distributed-system complexity
  Technical debt             Technical Debt                                          Work saved today can make later changes more expensive
  Authentication             Authentication                                          Checks who a user is
  Authorisation              Authorization                                           Checks what a user is allowed to do
  Least Privilege            Principle of least privilege                            Grants only necessary permissions
  OWASP                      Open Worldwide Application Security Project             Security project with development aids and testing guides
  DBMS                       Database management system                              Software that manages a database, executes queries and checks rules
  Database schema            Schema                                                  Definition of tables, data types, relationships and integrity rules
  Primary key                Primary Key                                             Unique identifier of a record within a table
  Foreign key                Foreign Key                                             Reference to a matching unique identifier in a related table
  Referential integrity      Referential Integrity                                   Ensuring valid references between tables
  JOIN                       Joining relational tables                               Combines rows on the basis of matching relationships
  Normalisation              Normalization                                           Modelling to reduce unnecessary data repetition and update problems
  Denormalisation            Denormalization                                         Deliberate storage of derived or redundant values for particular accesses
  Index                      Database index                                          Additional structure for accelerating suitable search or sort queries
  Query Planner              Query planner                                           Chooses an execution path for a database query
  Transaction                Transaction                                             Related changes managed as a unit
  COMMIT / ROLLBACK          Confirm / undo                                          Complete or reverse a transaction
  MVCC                       Multi-Version Concurrency Control                       Version-based control of concurrent database accesses
  WAL                        Write-Ahead Log                                         Advance log that can contribute to recovery and transaction safety
  Document database          Document Database                                       Stores documents with flexible fields and substructures
  Key–value store            Key–Value Store                                         Data storage with direct mapping of keys to values
  SQLite                     Embedded relational database system                     Usually a local database file without a separate DBMS server
  PostgreSQL                 Relational client-server DBMS                           Standalone database server with extensive integrity and query functions

  Term                     Meaning                              Classification
  -----------------------  -----------------------------------  ---------------------------------------------------------------
  IPv4                     Internet Protocol Version 4          32-bit IP address family
  IPv6                     Internet Protocol Version 6          128-bit IP address family
  DNS resolver             DNS resolution service               Determines address information for names
  A / AAAA                 DNS Resource Record Types            A for IPv4 addresses, AAAA for IPv6 addresses
  Router                   Network intermediary                 Forwards packets towards other networks
  NAT                      Network Address Translation          Translates network addresses and often ports
  Port                     Logical communication endpoint       Helps associate connections with a service
  UDP                      User Datagram Protocol               Transport of datagrams without a built-in delivery guarantee
  QUIC                     UDP-based transport protocol         Basis of HTTP/3, with encrypted connections and streams
  HTTP                     Hypertext Transfer Protocol          Protocol for web requests and responses
  HTTPS                    HTTP over TLS                        HTTP connection with cryptographic transport protection
  TLS handshake            Negotiation of a TLS connection      Agrees security parameters and session keys
  RFC                      Request for Comments                 Technical document series, including internet standards
  OSI                      Open Systems Interconnection         Conceptual layered network model
  CA                       Certificate Authority                Certification authority for digital certificates
  Certificate              Digital certificate                  Associates a public key with a verified identity
  Hash function            Cryptographic verification function  Calculates a fingerprint that cannot easily be reversed
  Salt                     Random additional value              Separates password hash computations for different users
  Argon2id                 Password hashing method              Suitable for computationally expensive, salted password hashing
  Symmetric cryptography   Shared-key cryptography              Both partners use the same secret key
  Asymmetric cryptography  Public-key cryptography              Public and private keys for different procedures
  Firewall                 Network access control               Filters permitted and prohibited network traffic
  Threat model             Threat Model                         Consideration of assets, attacks and possible countermeasures
  Deny by Default          Deny by default                      Access granted only with explicit permission
  Session                  Session                              Association of multiple requests with a user or operation
  Access token             Access Token                         Proof of permission for particular accesses

The glossary explains technical terms across all course chapters. The precise meaning depends on the context of the respective lesson.

## Artificial intelligence and robotics (modules M5 and M6) {#S7}

- **AI (Artificial Intelligence):** umbrella term for methods that address tasks considered intelligent, for example pattern recognition, language processing or planning.
- **ML (Machine Learning):** methods that derive patterns or rules from data or experience instead of programming each rule individually.
- **Deep Learning:** machine learning with multi-layer neural networks.
- **Neural network:** mathematical system of weighted connections whose parameters are adjusted through learning.
- **Parameter / weight:** adjustable number in a model that influences its computation.
- **Backpropagation:** calculation of the influence of individual parameters on an error value in order to adjust weights efficiently.
- **Transformer:** influential neural architecture since 2017, using attention mechanisms to process sequences.
- **Attention:** mechanism that calculates which parts of an input are relevant to other parts during processing.
- **LLM (Large Language Model):** large language model that has learned language patterns from extensive training data; many current models generate text token by token.
- **Token:** processing unit of a language model; may represent a word, part of a word, character or special character.
- **Embedding:** numerical vector representing certain properties of text, images or other data.
- **Inference:** execution of a previously trained model to generate an output or prediction.
- **Fine-Tuning:** subsequent adaptation of a pretrained model with additional training data.
- **RAG (Retrieval-Augmented Generation):** incorporating externally retrieved information into the generation of a model response.
- **RLHF (Reinforcement Learning from Human Feedback):** training using human preference judgements as a reward signal.
- **Agent:** software system that can use a model to select or perform multiple work steps and tool calls.
- **ROS 2 (Robot Operating System 2):** middleware ecosystem for communication and structuring robotics software, not a complete classical operating system.
- **SLAM (Simultaneous Localization and Mapping):** simultaneous localisation and creation of a map of the environment.
- **Edge Computing:** processing close to the device rather than necessarily in a remote cloud.

## Additions from M1-L7 – further foundations {#S8}

  Term                  Expanded form / meaning               Brief explanation
  --------------------  ------------------------------------  --------------------------------------------------------------------------------------
  Concurrency           Concurrency                           Several tasks can make progress over overlapping periods
  Parallelism           Parallelism                           Several computations actually take place simultaneously
  Thread                Thread of execution within a process  Can share memory and resources with other threads of the same process
  Asynchrony            Asynchronous execution                Respond to lengthy operations without necessarily blocking until a result is available
  Race Condition        Race condition                        Result depends on the order of competing accesses
  Mutex                 Mutual Exclusion                      Lock for mutual exclusion when accessing shared data
  Atomic operation      Atomic Operation                      Step that appears indivisible to competing accesses
  Deadlock              Deadlock                              Tasks wait cyclically for one another and cannot progress
  Starvation            Starvation of a task                  A task does not receive a required resource for an extended period
  Livelock              Livelock                              Tasks constantly react to one another without making progress
  Formal language       Formal Language                       Set of strings that comply with specified rules
  Grammar               Grammar                               Rules for constructing valid expressions
  Parser                Syntax analyser                       Assigns tokens to a grammatical structure
  Token (compiler)      Language unit                         Recognised identifier, operator, literal or similar component
  Regex                 Regular Expression                    Pattern description for recognising and processing strings
  Distributed system    Distributed System                    Multiple independent computers/processes cooperate using messages
  Idempotence           Idempotence                           Repeated execution has no unwanted additional effect
  Logical clock         Logical Clock                         Method for describing event order without a perfect real-time clock
  Eventual Consistency  Eventual consistency                  Copies can agree after a delay under certain conditions
  Consensus algorithm   Consensus Algorithm                   Method for joint decisions by several nodes under defined assumptions
  HCI                   Human-Computer Interaction            Studies the design and use of digital systems
  WCAG                  Web Content Accessibility Guidelines  Guidelines for accessible web content
  W3C                   World Wide Web Consortium             Standards body for web technologies
  GDPR                  General Data Protection Regulation    EU legal framework for processing personal data
  Privacy by Design     Data protection by design             Consider data protection during planning and design
  ML                    Machine Learning                      Machine learning methods based on data or feedback
  Overfitting           Overfitting                           Model fits training examples but generalises poorly

## Additions from M2-L1 – servers, hosting and accessibility {#S9}

  Term                  Expanded form / meaning                          Brief explanation
  --------------------  -----------------------------------------------  --------------------------------------------------------------------------------------------
  Server (role)         Network service                                  Program that accepts and answers requests from other programs
  Client                Requesting program                               Browser or other software that uses a service
  Loopback / localhost  Own computer as a network destination            Access to a service on the same computer, often via `127.0.0.1`
  Background service    Service / Daemon                                 Program that runs without a visible window, continuously or on demand
  Shared Hosting        Shared hosting platform                          Provider operates a shared server environment with predefined functions
  VPS                   Virtual Private Server                           Virtual computer with a largely independent operating system environment
  Dedicated server      Dedicated Server                                 Physical server assigned to one customer
  Managed Hosting       Service partly managed by the provider           Contractual model with additional operational duties for the provider
  Web server            HTTP server program                              Accepts web requests and delivers content or forwards them
  Reverse Proxy         Server-side intermediary                         Accepts public requests and passes them to internal services
  Registrar             Domain registration provider                     Registers domain names for customers through the domain allocation system
  DNS hosting           Management of authoritative DNS records          Determines which DNS responses are provided for a domain
  CNAME                 Canonical Name (DNS record)                      Points to another DNS name rather than directly to an IP address
  NAT / CGNAT           Network Address Translation / Carrier-Grade NAT  Local or provider-side address translation; CGNAT can complicate direct incoming IPv4 access
  Port forwarding       Port Forwarding                                  Forwards incoming connections to an internal destination
  TLS termination       Termination of a TLS connection                  For example, decryption at the reverse proxy before internal forwarding
  Let's Encrypt         Certification authority                          Issues certificates automatically after successful verification of control over names
  ACME                  Automatic Certificate Management Environment     Standard protocol for automated certificate management
  HTTP-01 / DNS-01      ACME challenge methods                           Proof of domain control via a web path or DNS record, respectively
  Monitoring            Operational monitoring                           Observing availability, errors and resource usage
  Log                   Event log                                        Stored technical events for analysis and diagnosis

## Additions from M2-L2 – web applications and APIs {#S10}

  Term             Expanded form / meaning                 Brief explanation
  ---------------  --------------------------------------  -----------------------------------------------------------------------------------------------------------
  Static website   Prebuilt web files                      Web server delivers files without individually computed HTML output
  Dynamic website  Server-generated output                 Page is assembled using application logic and data
  SPA              Single-Page Application                 Interface updates sections dynamically after the initial page load
  Frontend         User interface                          Visible, interactive part of an application, usually in the browser on the web
  Backend          Background application logic            Checks operations and permissions, processes data and accesses services
  API              Application Programming Interface       Contract for using program functions from other programs
  Endpoint         API Endpoint                            Defined address and operation of a web interface
  JSON             JavaScript Object Notation              Text-based format for structured data
  REST             Representational State Transfer         Architectural style involving resources, a uniform interface and stateless requests, among other principles
  Idempotence      Same intended effect on repetition      Protection against unexpected multiple effects
  Webhook          Event notification via HTTP             Service A actively notifies service B of events
  Background job   Background Job                          Task that runs independently of an open browser request
  Queue            Queue                                   Holds jobs ready for subsequent processing
  Worker           Worker process                          Retrieves and processes tasks from a queue
  Scheduler        Scheduler                               Starts operations according to timing rules
  WebSocket        WebSocket protocol                      Longer-lived, bidirectional browser-server connection
  SSE              Server-Sent Events                      Continuous messages from the server to the browser via HTTP
  Polling          Regular status enquiry                  Client repeatedly checks for a result
  Session cookie   Session identifier in a browser cookie  Associates requests with a login session
  RBAC             Role-Based Access Control               Access permissions are organised through roles
  Multi-Tenancy    Multi-tenancy                           Several separate customer organisations use a service
  Stateful         Stateful                                Component maintains state required for later steps
  Stateless        Stateless                               Processing individual requests does not depend on prior request context stored exclusively locally
  BOLA             Broken Object Level Authorization       Vulnerability caused by missing object-level access checks
  Backpressure     Backlog control                         Slow recipients or workers should not be overloaded indefinitely with data

## Additions from M2-L3 – hosting and cloud deployment models {#S11}

  Term                   Expanded form / meaning                                Brief explanation
  ---------------------  -----------------------------------------------------  ----------------------------------------------------------------------------------------------
  On-Premises            Operation at one's own site                            Own hardware and predominantly own operations
  Colocation / Housing   Housing own servers in a third-party data centre       Provider supplies site services; customer usually manages the server
  Shared Hosting         Shared web hosting                                     Several customers use a managed web server environment
  Managed Hosting        Managed hosting                                        Contractually agreed operational tasks are additionally performed by the provider
  Unmanaged Hosting      Hosting without extensive administration               Customer usually manages the guest operating system and application
  Dedicated server       Physical Dedicated Server                              Rented physical computer, typically exclusive to one customer
  Public Cloud           Publicly offered cloud infrastructure                  Available to many organisations as a service; data need not be public
  Private Cloud          Exclusive cloud infrastructure for an organisation     Cloud operation for one organisation, hosted locally or externally
  Hybrid Cloud           Combination of connected, distinct cloud environments  Connects e.g. private and public clouds for joint use
  Community Cloud        Shared cloud for a defined group of organisations      Organisationally shared infrastructure with similar requirements
  Multicloud             Use of several cloud providers                         Not a classical NIST deployment model
  NIST                   National Institute of Standards and Technology         US institute, source of the classical cloud definition
  CaaS                   Containers as a Service                                Managed execution environment for containers
  FaaS                   Function as a Service                                  Event-driven execution of deployed functions
  Serverless             Server management hidden by the platform               Servers exist, but customers do not operate them themselves
  Managed Database       Managed database                                       Provider takes over parts of database operation, not automatically responsibility for the data
  Shared Responsibility  Shared responsibility model                            Tasks are divided between provider and customer according to the service model
  Vendor Lock-in         Dependence on provider                                 Proprietary technology or processes make switching platforms costly
  Cold Start             Start of a previously unready execution environment    May cause additional latency in event-driven functions
  Resource pool          Resource Pooling                                       Infrastructure is allocated to several customers as needed
  Elasticity             Elasticity                                             Capacity can be adjusted to changing demand

## Additions from M2-L4 – virtualisation and containers {#S12}

  Term                    Expanded form / meaning                             Brief explanation
  ----------------------  --------------------------------------------------  -------------------------------------------------------------------------------
  Virtualisation          Abstraction of physical computing resources         Enables several logically separate environments on the same hardware
  Hypervisor              Virtualisation software or layer                    Provides and manages virtual machines on physical resources
  Guest operating system  Guest Operating System                              Separate operating system within a virtual machine
  Host                    Underlying execution environment                    Physical computer or system providing VMs or containers
  vCPU                    virtual Central Processing Unit                     Virtual processor unit; not necessarily an exclusive physical core
  Virtual switch          Virtual Switch                                      Software-based network switching between virtual interfaces
  KVM                     Kernel-based Virtual Machine                        Virtualisation technology in the Linux kernel
  Kernel                  Operating system kernel                             Responsible for processes, memory and device access, among other duties
  Container               Isolated application process or group of processes  Runs with a defined filesystem, network context and resource limits
  Namespace               Linux namespace                                     Isolates the view of processes, networking, user identifiers and other elements
  cgroups                 Control Groups                                      Linux mechanism for organising and limiting resources
  Container image         Packaged runtime template                           Contains code, libraries, files and startup information
  Registry                Image registry service                              Stores and distributes container images
  Image layer             Layer of a container image                          Reusable set of filesystem changes
  Image digest            Content-based identifier                            Binds an image to a specific package version
  OCI                     Open Container Initiative                           Open standards for container images, runtime and distribution
  Docker Engine           Docker runtime and management software              Creates and operates containers on a host
  Docker Compose          Multi-container management tool                     Describes several services, networks and volumes together
  Volume                  Persistent mounted storage area                     Stores data outside the short-lived container layer
  Bind Mount              Mounting a host path                                Connects a container to files and directories on the host
  Kubernetes / K8s        Container platform for state management             Manages application instances across one or more nodes
  Control Plane           Control layer                                       Manages the desired state of a Kubernetes cluster
  Node                    Cluster node                                        Physical or virtual computer that runs pods
  Pod                     Smallest Kubernetes deployment unit                 Contains one or more closely coupled containers
  Deployment              Kubernetes resource for application instances       Defines and manages e.g. replicas and updates
  Kubernetes Service      Stable network abstraction                          Makes changing pod instances accessible via a defined address
  Orchestration           Coordinated operation of many instances             Automates placement, replacement, updates and scaling
  Desired state           Desired State                                       Declarative description of how many and which instances should run
  Rootless Mode           Operation without a privileged root daemon          Reduces certain risks in container management

## Additions from M2-L5 – cloud networks and scaling {#S13}

  Term                    Expanded form / meaning                Brief explanation
  ----------------------  -------------------------------------  ----------------------------------------------------------------------------------
  Region                  Geographic group of cloud locations    Provider-defined location area with resources and zones
  AZ                      Availability Zone                      Operational and failure domain within a cloud region (provider details vary)
  VPC                     Virtual Private Cloud                  Logically isolated virtual cloud network with routes and rules
  Subnet                  Subnetwork                             Defined IP address range within a network
  Gateway                 Network node for transitions           Connects one network to other networks
  Load Balancer           Load distributor                       Distributes requests across multiple reachable instances
  Health Check            Availability/function check            Checks whether a target server can process requests
  Connection Draining     Allowing active connections to finish  Removes an instance from new requests without immediately terminating ongoing ones
  CDN                     Content Delivery Network               Geographically distributed delivery network for suitable content
  Origin server           Origin server                          Original source of delivered content
  Cache                   Cache                                  Keeps reusable content or results available
  Cache-Hit / Cache-Miss  Hit / missing entry                    Content is present in the cache or must be retrieved again
  Cache invalidation      Invalidating cached data               Specifically invalidates outdated entries
  Scale Up                Vertical scaling                       Equip an existing instance with more resources
  Scale Out               Horizontal scaling                     Start additional instances performing the same task
  Stateless               Stateless                              Does not require state from earlier requests stored exclusively locally
  Sticky Session          Bind session to instance               Attempts to direct the same user to the same server each time
  Session store           Shared session store                   Stores server-side session information outside an individual web process
  Autoscaling             Automatic scaling                      Adjusts resources/instances according to rules or measurements
  HPA                     Horizontal Pod Autoscaler              Kubernetes controller for adjusting the number of running pods
  Rate Limit              Rate limiting                          Limits requests or actions per time interval
  Queue                   Queue                                  Buffers jobs until they are processed
  Worker                  Job processor                          Background process that processes tasks
  Backpressure            Backpressure / overload control        Limits inflow when downstream processing cannot keep up
  Idempotence             Effect safety on repetition            Multiple executions do not produce multiple unwanted effects
  Throughput              Throughput                             Number of processed tasks per unit of time
  Latency                 Latency                                Time until a single result or response
  Observability           Observability                          Trace system state through metrics, logs and traces

## Additions from M3-L1 – a database on one server {#S14}

  Term                    Expanded form / meaning              Brief explanation
  ----------------------  -----------------------------------  ------------------------------------------------------------------------------------
  Data page / data block  Page / Block                         Physical unit in which a database system organises multiple records or index entries
  Sequential Scan         Sequential table scan                Examines table rows without selective index access
  B-Tree                  Balanced Tree, balanced search tree  Common index structure for search, range and sort queries
  Selectivity             Selectivity                          Proportion of records that satisfy a search condition
  Query planner           Query Planner / Optimizer            Chooses an execution path based on statistics and cost estimates
  EXPLAIN                 PostgreSQL analysis tool             Shows the planned database query path
  EXPLAIN ANALYZE         PostgreSQL execution analysis        Executes the query and reports measurements; write queries may change data
  Buffer Pool             Database page buffer                 Keeps frequently required data blocks in RAM
  Cache-Hit / Cache-Miss  Buffer hit / missing entry           Required data block is in memory or must be loaded
  I/O                     Input/Output                         Input/output, e.g. reading and writing storage blocks
  Write-Ahead Log (WAL)   Advance log for changes              Supports transaction durability and recovery after certain crashes
  Connection Pool         Connection pool                      Reusable supply of a limited number of database connections
  MVCC                    Multi-Version Concurrency Control    Regulates concurrent transactions through different visible data versions
  Snapshot                Consistent view of data              Data version a read operation may observe according to isolation rules
  VACUUM                  PostgreSQL clean-up                  Removes or manages obsolete data versions and storage space
  Hotspot                 Highly contended data area           Row or resource accessed by many operations that interfere with one another
  SQL injection           Injecting SQL through inputs         Attack in which uncontrolled inputs are interpreted as database commands
  Parameterised query     Parameterized Query                  Separates query structure from entered values
  Database latency        Query Latency                        Response time of an individual database query
  Database throughput     Query Throughput                     Database queries processed per unit of time

## Additions from M3-L2 – replication and high availability {#S15}

  Term                      Expanded form / meaning             Brief explanation
  ------------------------  ----------------------------------  -----------------------------------------------------------------------------
  Replication               Replication                         Transfers data or changes from a database to additional nodes
  Primary / primary server  Write-leading instance              Handles changes in the simple primary/standby model
  Standby                   Following database node             Can take over or serve reads with suitable configuration
  Physical replication      Physical Replication                Keeping a PostgreSQL instance up to date through WAL/storage changes
  Logical replication       Logical Replication                 Transmission of changes to selected data objects according to a logical model
  Streaming Replication     Continuous WAL transfer             Changes are passed incrementally to a standby
  Log Shipping              Transfer of archived WAL files      Transfers log segments to other database nodes
  HA / high availability    High Availability                   Goal of keeping operational interruptions low during certain failures
  Synchronous replication   Synchronous Replication             Commit waits for a defined acknowledgement from selected standbys
  Asynchronous replication  Asynchronous Replication            Primary does not wait for replica acknowledgement on commit
  Replication Lag           Replication lag                     Delay in receiving or applying changes
  Read Replica              Read replica                        Additional node for suitable read queries
  Read-Your-Writes          Consistency after one's own write   See one's own acknowledged changes on the next read
  Failover                  Unplanned role change               Replacement takes over after the primary server fails
  Switchover                Planned role change                 Prepared switch, e.g. for maintenance
  Promotion                 Promotion to primary                A standby receives the leading write role
  Split-Brain               Split leadership                    Two systems accept conflicting writes without coordination
  Fencing                   Technical isolation                 Prevents an old primary from continuing to write
  STONITH                   Shoot The Other Node In The Head    Technique for deliberately shutting down/resetting a problematic node
  Quorum                    Required number of votes            Minimum number of acknowledgements for a decision
  RPO                       Recovery Point Objective            Target for the maximum acceptable period of data loss
  RTO                       Recovery Time Objective             Target for the maximum acceptable recovery duration
  Failure Domain            Failure domain                      Part of infrastructure with a potentially shared cause of failure
  Replication Slot          PostgreSQL replication reservation  Can retain required WAL files; creates storage risks without monitoring

## Additions from M3-L3 – partitioning and sharding {#S16}

  Term                      Expanded form / meaning         Brief explanation
  ------------------------  ------------------------------  ---------------------------------------------------------------------------
  Table partitioning        Table Partitioning              Divides a logical table into physical parts, including within an instance
  Horizontal partitioning   Horizontal Partitioning         Distributes table rows across separate subsets
  Vertical partitioning     Vertical Partitioning           Separates table columns or data areas
  Sharding                  Distribution of data subsets    Assigns data to multiple independently managed database units/nodes
  Shard                     Data subset                     Independently managed subset of a distributed database
  Shard Key                 Distribution key                Determines which shard should hold a record
  Range Sharding            Range-based distribution        Distributes data according to contiguous key ranges
  Hash Sharding             Hash-based distribution         Uses a hash function to distribute records
  Lookup Sharding           Directory-based distribution    A directory assigns keys to a shard
  Partition Pruning         Skipping irrelevant partitions  Query plan skips sections that cannot contain matching rows
  Shard router              Request distributor             Routes requests to suitable nodes using a key or metadata
  Co-Location               Grouping related data           Records frequently required together reside on the same shard
  Cross-shard JOIN          Distributed table join          JOIN must consider data from more than one shard
  Fan-out / Scatter-Gather  Distributing and collecting     Query goes to multiple shards; results are combined
  Rebalancing               Redistribution                  Moves shards/sections when load changes or nodes are added
  Hotspot (sharding)        Overloaded data subset          One shard generates disproportionate load
  2PC                       Two-Phase Commit                Two-phase procedure for coordinated commitment of a distributed transaction
  Citus                     PostgreSQL extension            Provides additional functions for distributed tables and shards

## Additions from M3-L4 – Distributed SQL, NoSQL and consistency {#S17}

  Term                  Expanded form / meaning                                          Brief explanation
  --------------------  ---------------------------------------------------------------  --------------------------------------------------------------------------------------------------
  RDBMS                 Relational Database Management System                            Relational database management system with tables, keys and transactions
  NoSQL                 Collective term for systems that are not primarily relational    Encompasses various data models and consistency mechanisms
  Document database     Document Database                                                Stores related data in documents
  Key-value store       Key-value store                                                  Maps unique keys to values
  Distributed SQL       Distributed SQL database architecture                            Provides SQL across multiple coordinated database nodes
  Consensus algorithm   Consensus Algorithm                                              Gets multiple nodes to agree on specific state changes
  Raft                  Consensus protocol                                               Manages a replicated, ordered change log through elected leadership and majorities
  Quorum                Subset able to make a decision                                   Required number of participating nodes for a decision
  RAC                   Real Application Clusters                                        Oracle architecture with multiple database instances and shared storage
  Shared Everything     Shared resources                                                 Cluster instances access shared data and storage
  Shared Nothing        Independent resources                                            Nodes/shards have their own data storage resources
  Shard Director        Shard connection router                                          Oracle component for routing requests by data location
  YSQL                  Yugabyte SQL                                                     PostgreSQL-like SQL interface of YugabyteDB
  Tablet                Data area of a distributed database                              Smaller managed data unit, e.g. in YugabyteDB
  Serializable          Serialisable                                                     Transactions produce a result as in an admissible serial execution
  Linearisability       Linearizability                                                  Operations appear as atomic individual steps according to real-time order
  Eventual Consistency  Eventually achieved consistency                                  Replicas converge when new changes cease and communication works
  Causal Consistency    Causal consistency                                               Dependent operations become visible in causally appropriate order
  Read Your Writes      See one's own changes                                            Subsequent accesses by a user recognise previously acknowledged own changes
  Monotonic Reads       Non-regressing read view                                         A sequence of reads does not fall back to older, superseded states
  CAP                   Consistency, Availability, Partition Tolerance                   Fundamental trade-off during network partitions between strict consistency and strong availability
  Network partition     Network Partition                                                Temporary communication failure between parts of a distributed system
  PACELC                Partition, Availability, Consistency; Else Latency, Consistency  Additional consideration of latency/consistency even without a partition
  Lost Update           Lost change                                                      Later write unintentionally overwrites a concurrent change
  Write Skew            Write anomaly across several records                             Two individually valid changes jointly violate a business rule
  Lock                  Lock                                                             Coordinates competing concurrent data accesses
  Retry                 Retry attempt                                                    Another attempt at a failed or ambiguously acknowledged operation
  Idempotence           Repeatable effect without duplication                            The same operation may arrive again without duplicating the business effect
  At-least-once         At least once                                                    Delivery model in which messages may arrive more than once
  Transactional Outbox  Transactional outbox                                             Business data and dispatch job are stored together in one local transaction
  Dual Write            Double write operation                                           Business change and event dispatch occur separately and can diverge
  2PC                   Two-Phase Commit                                                 Coordinated preparation and decision in distributed transactions
  Saga                  Chain of local transactions                                      Coordinates distributed business workflows, including possible compensations
  Compensation          Compensating Transaction                                         Business-level corrective action after previously committed sub-operations
  Inbox pattern         Processing log for incoming messages                             Stores identifiers of processed events to prevent duplicate effects

## Additions from M3-L6 – data durability and recovery {#S18}

  Term                    Expanded form / meaning                         Brief explanation
  ----------------------  ----------------------------------------------  ----------------------------------------------------------------------------------------
  Backup                  Independent data backup                         Retained data for subsequent recovery
  Logical backup          Logical Backup                                  Exports data and structure in a reimportable form
  Physical backup         Physical Backup                                 Backs up database files or the physical cluster state
  Base backup             Base Backup                                     Starting state for recovery and, where applicable, WAL replay
  Full backup             Full Backup                                     Contains the complete required initial data set
  Incremental backup      Incremental Backup                              Backs up specified changes since an earlier backup state
  Differential backup     Differential Backup                             Backs up changes since a defined full backup
  Storage snapshot        Storage Snapshot                                Image of storage at a point in time; not to be confused with an MVCC read snapshot
  Crash-consistent        Crash-consistent                                Data view comparable to an abrupt system termination; database recovery may be necessary
  Application-consistent  Application-consistent                          Backup takes account of the consistency requirements of the application involved
  PITR                    Point-in-Time Recovery                          Database recovery up to a selected earlier point in time
  WAL archive             Write-Ahead Log Archive                         Retained change logs for suitable physical recovery
  Offsite backup          Geographically/technically separate copy        Protection against common failures at the primary site
  Immutable Backup        Immutable backup                                Cannot readily be deleted or overwritten during a protection period
  Offline backup          Disconnected backup                             Not permanently connected to the running system
  Restore                 Recovery                                        Make data or systems usable again from backed-up data
  Restore test            Recovery test                                   Checks whether a backup is actually reusable
  Backup retention        Retention period                                Rule governing backup history and deletion of old backups
  Backup manifest         Backup file inventory/verification information  Documents associated backup files and enables integrity checks
  3-2-1 rule              Backup mnemonic                                 Three copies, two media/system types, one separate copy
  Job / background job    Background Job                                  Bounded work, potentially processed later, with identifier and status
  Queue / Job Queue       Queue                                           Buffer for tasks not yet executed
  Worker                  Worker process                                  Process that accepts and executes a job
  Scheduler               Scheduler                                       Decides on execution time or resource allocation
  Message Broker          Message broker                                  Relays messages between sending and receiving programs
  Producer / Consumer     Producer / consumer                             Message sender and message recipient
  Pub/Sub                 Publish/Subscribe                               Distributes events to multiple independent subscribers
  Event Bus               Event bus                                       Relays events according to types or rules
  Event Streaming         Event stream processing                         Continuous processing of sequences of messages or events
  DAG                     Directed Acyclic Graph                          Directed acyclic graph for dependencies between work steps
  Concurrency             Concurrency                                     Several tasks make progress over overlapping periods
  Parallelism             Parallelism                                     Several computational steps actually take place simultaneously
  Batch Processing        Batch processing                                Process collected jobs or data in batches
  Streaming               Stream processing                               Process continuously arriving data
  Hard Real-Time          Hard real-time                                  Binding response deadline that must not be missed
  ACK                     Acknowledgement                                 Acknowledgement of receipt or processing in messaging systems
  Retry / Backoff         Retry / increasing delay                        Error handling with a limited number of further attempts
  DLQ                     Dead-Letter Queue                               Holding queue for messages that repeatedly cannot be processed
  Backpressure            Backpressure                                    Protection against overload by limiting further inflow
  SQS                     Simple Queue Service                            Managed queue service from Amazon Web Services
  GPU worker              Worker with graphics processor                  Performs suitable parallel computing or AI tasks
  Model inference         Inference                                       Execution of a previously trained model on new inputs

## Additions from M4-L2 – deployment and reliability {#S19}

  Term                          Expanded form / meaning            Brief explanation
  ----------------------------  ---------------------------------  ----------------------------------------------------------------------------------
  Deployment                    Deployment                         Installation and activation of a specific software version in an environment
  Artefact / build artefact     Generated software package         Tested, identifiable result of a build process
  Staging                       Pre-production environment         Test environment before a software release to production
  Infrastructure as Code / IaC  Infrastructure as code             Versionable definition and automated management of infrastructure
  State (IaC)                   Infrastructure state information   Maps managed resources to their configurations; requires protection
  Observability                 Observability                      Understand relationships within the system from emitted signals
  Monitoring                    System monitoring                  Observation of defined metrics and states
  Log                           Event log                          Time-associated record of an event
  Metric                        Quantitative measurement           Time series for e.g. response time, error rate or resource usage
  Trace                         Execution trace                    Relationship between several processing steps of a request
  Span                          Individual step of a trace         Time interval of a traceable operation
  OpenTelemetry                 Open telemetry standard and tools  Captures and exports logs, metrics and traces; not a standalone monitoring backend
  Alerting                      Alerting                           Notification of relevant operational events
  Liveness Probe                Liveness check                     Checks whether restarting a blocked process may be appropriate
  Readiness Probe               Readiness check                    Checks whether an instance should currently receive user traffic
  Startup Probe                 Startup check                      Protects slow-starting services from premature restarts
  Rolling Update                Gradual update                     New instances replace old ones progressively
  Blue-Green Deployment         Switch between two environments    New version is tested separately before public switchover
  Canary Release                Staged release                     Initially only a subset of users receives the new version
  Feature Flag                  Feature switch                     Activates a program function without a new software release
  Rollback                      Reversion to an earlier version    Reverses a software change, not necessarily its effects on data
  Database migration            Schema or data transition          Adapts stored structures to new software versions
  Expand and Contract           Expand first, remove later         Pattern for compatible gradual database changes
  SLI                           Service Level Indicator            Metric for the quality of a service
  SLO                           Service Level Objective            Defined target for an SLI
  Error Budget                  Error budget                       Calculated tolerance for deviation accounted for in the SLO
  SRE                           Site Reliability Engineering       Technical methods and organisational practice for reliable operation
  Single Point of Failure       Single point of failure            Its failure can affect the entire service
  Availability Zone             Availability zone                  Infrastructure failure domain within a cloud region

## Additions from M4-L3 – security, data protection and responsibility {#S20}

  Term                             Expanded form / meaning                   Brief explanation
  -------------------------------  ----------------------------------------  ----------------------------------------------------------------------------------------------
  Confidentiality                  Confidentiality                           Protection against unauthorised viewing of information
  Integrity                        Integrity                                 Protection against unnoticed or unauthorised alteration of data
  Threat model                     Threat Modeling                           Systematic consideration of assets, attackers and vulnerabilities
  Authentication                   Authentication                            Proof of identity
  Authorisation                    Authorization                             Verification of the action permitted on a resource
  IAM                              Identity and Access Management            Management of identities and access permissions
  Least Privilege                  Principle of least privilege              Grants only the permissions actually needed
  RBAC                             Role-Based Access Control                 Role-based access control
  ABAC                             Attribute-Based Access Control            Access decision based on attributes and rules
  MFA                              Multi-Factor Authentication               Sign-in using multiple independent factors
  FIDO2 / WebAuthn                 Standards for strong web authentication   Basis of many passkey methods
  Passkey                          Key-based sign-in                         Authentication with a cryptographic key instead of a reusable website password
  Password hash                    One-way verification value of a password  Must be produced with suitable slow password hashing methods
  Salt                             Random additional value                   Prevents identical passwords from automatically producing identical verification values
  Argon2id                         Memory-intensive password hash function   Makes large-scale guessing of stolen password verification values more difficult
  Session                          Session                                   Recognisable, time-limited user context
  CSRF                             Cross-Site Request Forgery                Unwanted actions via external web content in the context of a login
  Secret                           Confidential access value                 E.g. API key, database password or private key
  Secret Manager                   Tool for managing secrets                 Limits and logs access to confidential values
  Key rotation                     Replacement of a secret/key               Limits the effects and lifetime of access values
  Encryption at Rest               Encryption of stored data                 Protection of certain stored data against unauthorised access
  Rate Limit                       Request limiting                          Limits how frequently an interface may be used
  SSRF                             Server-Side Request Forgery               Abuse of server-side network requests to unintended destinations
  GDPR                             General Data Protection Regulation        European rules for processing personal data
  Controller                       Data Controller                           Determines the purposes and essential means of processing
  Processor                        Data Processor                            Processes data on behalf of another party and in accordance with applicable instructions
  Data processing agreement (AVV)  Data processing agreement                 Contractual basis for processing on behalf of a controller under Article 28 GDPR
  Privacy by Design                Data protection by design                 Consider data protection already in the system design
  Privacy by Default               Privacy-friendly default settings         Process only necessary data by default
  Pseudonymisation                 Replacement of direct identifiers         Makes attribution more difficult without reliably excluding a link to a person
  EEA                              European Economic Area                    EU states plus Iceland, Liechtenstein and Norway
  Adequacy decision                Adequacy Decision                         European Commission decision on an adequate level of data protection in a third country
  SCC                              Standard Contractual Clauses              EU standard contractual clauses for certain data transfers
  Personal data breach             Personal Data Breach                      Security breach involving loss, alteration, disclosure or unauthorised access to personal data

## Additions from M4-L4 – understanding costs {#S21}

  Term            Expanded form / meaning                     Brief explanation
  --------------  ------------------------------------------  --------------------------------------------------------------------------------------
  Fixed costs     Recurring base costs                        Costs incurred during the period considered even without individual new jobs
  Variable costs  Usage-dependent costs                       Increase with the amount of service used or data volume
  Marginal costs  Additional cost of one more unit            How much one further successfully delivered service costs in addition
  Egress          Outgoing data traffic                       Data transfer out of a cloud service or defined network area
  GB-month        Gigabytes multiplied by retention duration  Unit of measurement for stored data over a period
  GB-second       Gigabytes multiplied by execution time      Common quantity in billing for functions based on memory and time
  Cloud budget    Planned spending target                     Calculated value for warnings or, if separately supported, technical spending limits
  Spend Cap       Technical spending limit                    Can block further usage in supported services; not a universal feature of every budget
  Cost alert      Budget warning                              Notifies of a threshold; does not automatically limit spending
  TCO             Total Cost of Ownership                     Total costs over a usage period including operation and additional effort
  FinOps          Financial Operations                        Jointly analyse the costs and business value of technology
  Unit Economics  Costs per meaningful unit of service        For example, per successful analysis or usable AI result
  Cost driver     Dominant cause of expenditure               For example, GPU runtime, large files or database capacity
  Utilisation     Ratio of usage to capacity                  Influences cost per completed job
  Vendor Lock-in  Dependence on provider                      Effort and risks involved in switching from proprietary platform services

## Additions from M4-L5 – own software and cloud offerings {#S22}

  Term                 Expanded form / meaning                       Brief explanation
  -------------------  --------------------------------------------  ---------------------------------------------------------------------------------------------------------------------
  SaaS product         Software as a Service                         Application used as a service with ongoing operator responsibility
  API-as-a-Service     Programming interface as a service            Machine-readable function for external customer programs
  Managed Automations  Managed automation                            Take over recurring workflows, including setup and operation
  Tenant               Individual customer area                      Logical assignment of users, data, permissions and costs
  Tenant isolation     Tenant Isolation                              Protection against unauthorised access between customer areas
  Onboarding           Introduction of a new customer                Technical creation of an account, permissions and, where applicable, billing
  MVP                  Minimum Viable Product                        Smallest usable version that makes the central benefit testable
  Freemium             Free basic service, paid extension            Business model with limited free access and paid features
  Metered Billing      Usage-based billing                           Billing based on measured requests, jobs or consumption units
  Credit model         Prepaid Credits                               Usage budget paid in advance and consumed later
  AGPLv3               GNU Affero General Public License, Version 3  Open-source licence with special conditions for network interaction with modified programs
  OSS                  One Stop Shop (EU VAT)                        Simplified procedure for certain cross-border VAT cases; not to be confused with Open Source Software in this context
  B2B / B2C            Business to Business / Business to Consumer   Offering for businesses / private customers
  Customer benefit     Value Proposition                             Practical advantage of an offering recognisable to its target group
  Churn rate           Churn Rate                                    Proportion of customers who leave during a period
  Unit costs           Unit Economics                                Costs and revenues of a meaningfully defined unit of service

## Additions from M5-L1 – history of artificial intelligence {#S23}

  Term               Expanded form / meaning                           Brief explanation
  -----------------  ------------------------------------------------  ------------------------------------------------------------------------------------------------------------------------------
  AI                 Artificial Intelligence                           Research and application field for systems with abilities such as pattern recognition, problem-solving and language processing
  Symbolic AI        Rule- and symbol-based AI                         Explicitly represents knowledge and inference rules and processes them through logic or search
  ML                 Machine Learning                                  Methods deriving patterns and decision functions from example data
  Deep Learning      Deep learning                                     Machine learning with typically multi-layer neural networks
  Generative AI      Content-generating models                         Generate text, images, audio or other new outputs based on learned patterns
  LLM                Large Language Model                              Model trained on extensive language/token data for processing and generating language
  Perceptron         Early trainable neuron model                      Combines input features with adjustable weights and makes a decision
  XOR                Exclusive OR                                      Logical operation that is true when exactly one input is true; classical example of the limits of simple linear models
  Expert system      Rule-based domain system                          Combines an explicit knowledge base with an inference engine
  Inference engine   Rule / Inference Engine                           Evaluates rules and facts to derive conclusions
  AI winter          Decline in funding and expectations               Historical periods of disappointed promises, without a complete halt to research
  Backpropagation    Backward propagation of derivative information    Method for calculating the contribution of model parameters to training error
  GPU                Graphics Processing Unit                          Parallel computing processor, often used to train and run neural networks
  AlexNet            Deep image classification architecture (2012)     Well-known milestone for large image datasets and GPU-based deep learning
  Transformer        Attention-based network architecture (2017)       Basis of many modern language and multimodal models
  Attention          Attention weighting                               Mathematical weighting of relationships between elements of an input sequence
  Token              Model-dependent text unit                         E.g. part of a word or sequence of punctuation marks; processed numerically
  Pretraining        Pretraining                                       Extensive initial learning phase, often before adaptation to specific tasks
  Few-Shot Learning  Learning/adapting with a few examples in context  A model recognises a task pattern from a few input examples without necessarily changing its weights

## Additions from M5-L2 – what is a neural network? {#S24}

  Term                Expanded form / meaning                Brief explanation
  ------------------  -------------------------------------  -------------------------------------------------------------------------------------
  Artificial neuron   Mathematical computational unit        Calculates a weighted input sum, bias and, where applicable, an activation function
  Feature             Input feature                          Numerical value that serves as input or an internal representation for a model
  Weight              Trainable model parameter              Determines the contribution of an input to a neuron's computation
  Bias                Trainable offset                       Changes the base value of a computational unit independently of current inputs
  ReLU                Rectified Linear Unit                  Activation function max(0, z); negative values become zero
  Hidden Layer        Hidden layer                           Internal processing stage between model input and model output
  Forward Pass        Forward pass                           Calculation of an output with the current model parameters
  Loss Function       Loss function                          Measures the error between output and learning target according to a specified rule
  Gradient            Rates of change of the loss function   Derivatives of the error with respect to all trainable parameters
  Gradient Descent    Gradient descent                       Changes model parameters towards a locally smaller error
  Backpropagation     Backward computation of gradients      Efficiently computes derivatives through a network using the chain rule
  Learning rate       Learning Rate                          Factor controlling step size during weight updates
  SGD                 Stochastic Gradient Descent            Gradient method with stochastically selected examples or mini-batches
  Batch / Mini-Batch  Data batch for one computational step  Small group of training examples for joint gradient computation
  Epoch               Epoch                                  One complete pass through the designated training data set
  Hyperparameter      Setting of the learning method         E.g. learning rate, batch size or number of layers; not trained directly like weights
  Generalisation      Transferability to new cases           Ability to handle previously unseen examples meaningfully
  Overfitting         Overfitting                            Low training error but weaker performance on new data
  Underfitting        Underfitting                           Model inadequately captures even the basic training patterns
  Data Leakage        Data leakage in evaluation             Impermissible information from evaluation or future data influences development
  Dropout             Training regularisation                Temporarily masks activations to limit overfitting
  CNN                 Convolutional Neural Network           Network with convolutional layers and shared filter weights, e.g. for image data
  RNN                 Recurrent Neural Network               Network with internal state for stepwise processing of sequences
  LSTM                Long Short-Term Memory                 Recurrent network architecture with special mechanisms for state and information flow
  VRAM                Video Random Access Memory             Memory on a graphics card, relevant to model parameters and intermediate values

## Additions from M5-L3 – how machines learn {#S25}

  Term                         Expanded form / meaning                     Brief explanation
  ---------------------------  ------------------------------------------  ---------------------------------------------------------------------------------------
  Supervised Learning          Supervised learning                         Learns from inputs with known target values or labels
  Unsupervised Learning        Unsupervised learning                       Looks for structures in data without predefined target labels
  Self-Supervised Learning     Self-supervised learning                    Derives prediction targets from the existing data themselves
  Reinforcement Learning (RL)  Reinforcement learning                      Learns an action policy based on rewards from an environment
  Transfer Learning            Transfer of learned capabilities            Uses previously trained parameters or representations for a new task
  Fine-Tuning                  Fine-tuning                                 Further trains an existing model for a narrower purpose
  Label                        Target annotation / target value            Desired output for a training example in supervised learning
  Classification               Category prediction                         Assigns a new example to one or more categories
  Regression (ML)              Prediction of continuous target values      Estimates e.g. price, temperature or consumption
  Clustering                   Grouping                                    Finds data points with similar features and assigns them to groups
  k-Means                      Clustering method                           Repeatedly assigns points to k group centres and updates the centres
  Masked Language Modeling     Prediction of masked text units             Self-supervised learning objective with masked tokens
  Policy                       Action strategy                             Rule or model that selects actions for observations
  Reward / Return              Reward / cumulative reward                  Evaluates action steps or their overall sequence in reinforcement learning
  Reward Hacking               Optimising past the intended goal           An agent improves a reward value without meaningfully achieving the actual objective
  Embedding                    Numerical vector of a representation        Model-dependent numerical representation of text, images or other content
  One-Hot Encoding             Encoding with one active position           Vector with one position for each possible category
  Precision                    Precision                                   Proportion of actually positive cases among all predicted positives
  Recall                       Recall                                      Proportion of detected positive cases among all actual positives
  Accuracy                     Overall accuracy                            Proportion of correct predictions among all examples; often misleading for rare classes
  F1 score                     Harmonic mean of precision and recall       Combined classification score for precision and recall
  Confusion matrix             Confusion matrix                            Shows correct and incorrect positive and negative decisions
  Benchmark                    Standardised comparison test                Measures defined model performance under specified test conditions
  Distribution Shift           Distribution shift                          New data differ statistically from training or test data
  Training-Serving-Skew        Discrepancy between training and operation  Actual inputs are collected or processed differently from training data
  Data Poisoning               Manipulation of training data               Attackers attempt to influence model behaviour using crafted data

## Additions from M6-L1 – from language processing to transformers and LLMs {#S26}

  Term                              Expanded form / meaning                                   Brief explanation
  --------------------------------  --------------------------------------------------------  ----------------------------------------------------------------------------------------------
  NLP                               Natural Language Processing                               Computer science methods for processing natural language
  n-gram                            Sequence of n units                                       Classical statistical modelling of neighbouring words or tokens
  Bigram / trigram                  Word/token sequence of length 2 or 3                      Limited context in classical n-gram models
  Smoothing                         Smoothing probabilities                                   Among other things, prevents zero probabilities for unseen cases
  Subword tokenisation              Division into parts of words                              Uses word parts instead of only whole words as token units
  BPE                               Byte Pair Encoding                                        Method for progressively merging frequent character or byte sequences
  SentencePiece                     Model and implementation family for subword tokenisation  Can train tokenisers directly on raw text
  RNN                               Recurrent Neural Network                                  Recurrent network that carries state from one sequence step to the next
  BPTT                              Backpropagation Through Time                              Backward computation of gradients through recurrent networks unrolled in time
  LSTM                              Long Short-Term Memory                                    Recurrent architecture with gates to control information flow
  Seq2Seq                           Sequence-to-Sequence                                      Architecture for transforming one sequence into another sequence
  Encoder                           Input processing and representation                       Transforms input into internal states; depending on architecture, with bidirectional attention
  Decoder                           Output-generating part of a network                       Generates outputs step by step; depending on architecture, with access to the encoder
  Attention                         Attention weighting                                       Weights contributions from other positions to a vector representation
  Self-Attention                    Attention within the same sequence                        Query, key and value come from representations of the same sequence
  Cross-Attention                   Attention across two sequences/sources                    E.g. decoder queries over encoder keys and values
  Query / Key / Value (Q/K/V)       Query / key / content vectors                             Trained projections for comparing and mixing information
  Dot product                       Dot Product                                               Multiplies vector components pairwise and sums them
  Softmax                           Normalisation of comparison scores                        Converts scores into non-negative weights whose sum is 1
  Scaled Dot-Product Attention      Scaled dot-product attention                              Forms softmax weights from $Q\cdot K^{\mathrm T}$ divided by $\sqrt{d_k}$ and mixes values
  Multi-Head Attention              Multi-head attention                                      Several separately projected attention computations are combined
  Positional Encoding               Positional encoding                                       Adds ordering information to token representations
  Feedforward layer                 Feedforward subnetwork                                    Further processes representations position by position after attention
  Residual Connection               Residual connection/path                                  Adds an input across a sub-block
  Layer Normalization               Layer normalisation                                       Normalises values to stabilise training
  Causal Mask                       Causal attention mask                                     Prevents access to future target positions in the autoregressive model
  Autoregressive                    Next step from previous steps                             Generates token by token using the preceding sequence
  Encoder-only                      Encoder-only transformer                                  Often used for representation, classification and information extraction
  Decoder-only                      Decoder-only transformer                                  Often used for causal text generation, e.g. GPT models
  Encoder-Decoder                   Combined transformer architecture                         Processes input with an encoder and generates output with a decoder
  BERT                              Bidirectional Encoder Representations from Transformers   Well-known bidirectional encoder model with self-supervised pretraining
  GPT                               Generative Pre-trained Transformer                        Family of autoregressive pretrained language models
  T5                                Text-to-Text Transfer Transformer                         Encoder-decoder approach that formulates language tasks as text-to-text tasks
  VRAM                              Video Random Access Memory                                Graphics memory for model weights and temporary computational values
  RAG                               Retrieval-Augmented Generation                            Supplements generation with externally retrieved document passages
  Chat template                     Conversation template for a model                         Encodes roles and messages in the input form expected by the model
  Token IDs                         Numerical token identifiers                               Assign discrete units to a tokeniser vocabulary
  Context window                    Context Window                                            Maximum token context that can be considered during model processing
  Inference                         Inference                                                 Running a previously trained model without ordinarily changing its weights
  Prefill                           Precomputation phase of inference                         Processes the supplied input sequence before autoregressive output
  Decoding (LLM)                    Stepwise text generation                                  Generation of further tokens depending on the previous sequence
  Logit                             Unnormalised model output value                           Score for a possible next token before softmax and sampling
  Greedy Decoding                   Greedy token selection                                    Selects the candidate with the highest selection probability at each step
  Sampling                          Weighted random selection                                 Draws the next token from a probability distribution
  Temperature (LLM)                 Temperature                                               Scales logits and changes the concentration of selection probabilities
  Top-p / Nucleus Sampling          Selection by cumulative probability                       Considers the smallest candidate set covering at least threshold p
  Top-k                             Selection from k candidates                               Limits token selection to the k most likely continuations
  KV cache                          Key-value cache                                           Caches attention states from previous positions for more efficient decoding
  Prefix Caching                    Prefix caching                                            Allows previously computed input prefixes to be reused under suitable conditions
  TTFT                              Time to First Token                                       Time until the first output token of a request
  Quantisation (LLM)                Reduced precision of numerical representation             Saves memory for model weights, among other things; may affect quality and speed
  Hallucination (LLM)               Factually unsupported or false model generation           Plausible-looking output that is not reliably grounded in facts
  Streaming (LLM)                   Incremental transmission                                  Displays the output already generated before the entire text is complete
  Base model                        Pretrained language model                                 Has learned general text patterns but need not follow instructions reliably
  Assistant model / Instruct Model  Post-trained dialogue- and task-oriented language model   Has been adapted towards desired instruction-following and response behaviour
  Post-Training                     Further training after general pretraining                Depending on the method, includes SFT, preference optimisation and further learning objectives
  Fine-Tuning                       Fine-tuning a pretrained model                            Further adaptation of weights or adapters using additional data
  SFT                               Supervised Fine-Tuning                                    Supervised fine-tuning using examples of desired outputs
  Instruction Tuning                Instruction-oriented post-training                        Often carried out as SFT on instruction-response data
  Preference data                   Comparative data for desirable responses                  Mark preferred and rejected model responses
  RLHF                              Reinforcement Learning from Human Feedback                Reinforcement learning in which human preferences influence the training objective
  Reward Model                      Reward model                                              Estimates an assessment based on human or other preference data
  PPO                               Proximal Policy Optimization                              Family of optimisation methods for reinforcement learning, including classical RLHF variants
  KL divergence                     Kullback–Leibler divergence                               Describes a directed discrepancy between probability distributions
  Reward Hacking                    Exploiting weaknesses in a reward metric                  High measured values can be achieved without actual gains in usefulness
  DPO                               Direct Preference Optimization                            Optimises preference pairs without a separate reward model/RL step in the basic method
  PEFT                              Parameter-Efficient Fine-Tuning                           Trains only a small subset of additional or selected parameters
  LoRA                              Low-Rank Adaptation                                       Trains smaller correction matrices while base matrices are frozen
  QLoRA                             Quantized Low-Rank Adaptation                             Combines quantised frozen base weights with LoRA adapters
  Data Contamination                Contamination of test data                                Test tasks are already known from training data or closely resemble them
  LLM-as-a-Judge                    Language model as evaluator                               Automatic evaluation of other responses; itself susceptible to errors and bias
  Red Teaming                       Targeted investigation of possible vulnerabilities        Examines misbehaviour, misuse opportunities and safety limits
  Guardrails                        Additional safety and control mechanisms                  E.g. access checks, schema, resource and approval rules
  Model Card                        Model card                                                Documents intended use, test methods, known limitations and risks
  Catastrophic Forgetting           Catastrophic forgetting                                   Additional training can impair existing model capabilities

## M6-L4 – Knowledge, tools and agents, and course structure {#S27}

  Term                       Explanation                                                   Significance
  -------------------------  ------------------------------------------------------------  ---------------------------------------------------------------------------
  RAG pipeline               Retrieval-Augmented Generation with retrieval and generation  External information as context without changing model weights
  Chunking                   Dividing documents into smaller text segments                 Allows targeted retrieval of relevant passages
  Embedding                  Numerical representation of text or other content             Basis of many semantic search systems
  Vector search              Similarity search in a vector space                           Finds semantically close representations, not automatically true statements
  Hybrid search              Combining full-text and vector search                         Combines exact terms and semantic proximity
  Reranking                  Reordering search results                                     Can improve relevance of the retrieved candidates
  Tool Calling               Structured request for a tool call                            Model proposes a call; application checks and executes it
  Agentic workflow           Multi-step workflow with model-controlled step selection      Connects model, tools, state and stopping rules
  Orchestrator               Coordinating application software                             Manages search, model calls, permissions and feedback
  Prompt Injection           Inserting instructions into inputs or external data           Security risk, especially with documents and tool results
  Excessive Agency           Excessive tool permissions or autonomy                        Increases consequences of erroneous or manipulated model actions
  Bachelor's elective topic  Optional advanced unit at bachelor's level                    Independent elective lessons in M8–M10
  Master's elective topic    Optional advanced unit at master's level                      Focus on formal models, trade-offs and research methods
  Master's core area F       Reserved later advanced computer science section              Not yet a developed or accredited master's programme

## M6-L5 – Multimodal AI: images, video and audio {#S28}

  Term                         Explanation                                                 Significance
  ---------------------------  ----------------------------------------------------------  -----------------------------------------------------------------------
  Modality                     Data form such as text, image, video or audio               Multimodal systems process several data forms
  Image patch                  Small rectangular portion of an image                       Common input unit for vision transformers
  Vision-language model (VLM)  Model for joint processing of visual content and language   Image questions, image descriptions, document analysis
  CLIP                         Contrastive Language–Image Pre-training                     Image and text representations are aligned using matching pairs
  Shared embedding space       Comparable numerical feature space for multiple data types  Enables search across images and similarity comparisons
  Diffusion model              Generative model with gradual denoising                     Image, video and also audio generation
  Latent space                 Learned numerical feature space                             Can organise computationally expensive generation more compactly
  Autoencoder                  Encoder with matching decoder for reconstruction            Often used for image compression in generative systems
  VAE                          Variational Autoencoder                                     Probabilistic autoencoder family, used in some latent image methods
  Conditioning                 Guiding generation using additional inputs                  E.g. text, sketches or reference images
  Inpainting                   Regenerating a selected image region                        Controlled image editing
  Outpainting                  Extending an image beyond its previous boundaries           Scene extension
  Frame                        Individual image in a video sequence                        Temporal consistency arises from relationships between frames
  Temporal consistency         Preservation of meaningful relationships over time          Important for character identity, movement and scene logic
  Sample / sampling rate       Digital measurement / measurements per second               Basis of digital audio signals
  Spectrogram                  Representation of frequency components over time            Common intermediate representation for audio AI
  ASR                          Automatic Speech Recognition                                Conversion of spoken language into text
  TTS                          Text-to-Speech                                              Conversion of text into spoken language
  Vocoder                      Generates audio waveforms from acoustic features            Part of certain speech synthesis architectures
  Prosody                      Stress, rhythm, melody and pauses in speech                 Important for the naturalness of synthetic voices
  C2PA / Content Credentials   Standards and technical provenance information for media    Support verifiable provenance but do not establish the truth of content
  Muxing                       Combining multiple media tracks into a container            Part of the video/audio production pipeline

## M6-L6 – AI infrastructure and distributed computing {#S29}

  Term                   Explanation                                                                        Significance
  ---------------------  ---------------------------------------------------------------------------------  -------------------------------------------------------------------
  Inference              Application of a previously trained model without ordinarily changing its weights  Basis for chat, image analysis and many AI services
  Training checkpoint    Saved training state including weights and other states depending on the method    Resumption after errors or interruptions
  Memory bandwidth       Amount of data transferable per unit of time between memory and computing units    Can limit model speed
  Memory-bound           Computation limited predominantly by data transfer/memory access                   More compute units alone make little difference
  Compute-bound          Computation limited predominantly by the actual arithmetic operations              Different acceleration strategies from those for memory bottlenecks
  Quantisation           Reduced numerical precision when storing/processing model values                   Can save memory and may affect quality depending on the method
  TPOT                   Time per Output Token                                                              Mean time per further generated token
  Continuous Batching    Dynamic grouping of active model requests                                          Better inference server utilisation under suitable load
  PagedAttention         Block-oriented management of attention KV cache memory                             Enables more efficient cache management in suitable engines
  Task parallelism       Distribute independent computing jobs across several workers                       Straightforward expansion of parallel job processing
  Data parallelism (AI)  Complete model copies process different training data                              Gradients are synchronised; the model must fit in each copy
  DDP                    Distributed Data Parallel                                                          PyTorch method for synchronised data parallelism
  Model parallelism      Distribute model parameters or computational steps across devices                  Helps with large models; requires communication
  Tensor parallelism     Split tensor operations across several devices                                     Partial results may require synchronisation
  Pipeline parallelism   Distribute successive model layers across several devices                          Intermediate results are passed onward
  FSDP                   Fully Sharded Data Parallelism                                                     Sharded model and training states in distributed computing
  AllReduce              Combine and distribute aggregated values among participants                        E.g. gradient synchronisation
  NCCL                   NVIDIA Collective Communications Library                                           Communication library for supported NVIDIA GPU groups
  Expert Parallelism     Distribution of experts in mixture-of-experts models                               Requires suitable routing and load planning
  Device Plugin          Extension of a cluster controller for using specialised hardware                   Allows Kubernetes to schedule GPUs
  Serving replica        Independent running instance of a model/serving system                             Processes requests independently; requires its own resources

## M6-L7 – Robotics: from language model to acting machine {#S30}

  Term                       Explanation                                                        Significance
  -------------------------  -----------------------------------------------------------------  ---------------------------------------------------------------------
  Robot                      Programmable physical system with sensors and actuators            Perceives the environment and acts mechanically upon it
  Actuator                   Component that produces movement or an effect                      Motor, gripper or valve
  Encoder                    Sensor for measuring rotation angle/movement                       Feedback for motor and position control
  IMU                        Inertial Measurement Unit                                          Measures acceleration and rotational movement, among other quantities
  LiDAR                      Light Detection and Ranging                                        Optical distance measurement for environmental perception
  Control loop               Feedback control comprising setpoint, actual value and controller  Corrects deviations during movement
  PID controller             Proportional-integral-derivative controller                        Classical control method with several correction components
  Real-time                  Time deadlines as part of correct system function                  Important for predictable control and response
  Pose                       Position and orientation of an object or robot                     Basis for localisation and grasp planning
  Sensor data fusion         Combination of multiple measurement sources into a state estimate  Reduces certain measurement uncertainties
  SLAM                       Simultaneous Localization and Mapping                              Simultaneous self-localisation and mapping
  Odometry drift             Accumulation of position errors from motion measurements           Makes supplementary localisation methods necessary
  Path planning              Search for a navigable/followable route                            Basis of mobile navigation
  Kinematics                 Geometric relationships between joints and body positions          Converts between joint angles and target poses
  End effector               Tool at the end of a robot manipulator                             For example, a gripper
  ROS 2                      Robot Operating System 2                                           Software framework for robotics components and their communication
  Node                       Individual ROS 2 component                                         Sensor, planning or control as a logical unit
  Topic                      Continuous message stream in ROS 2                                 Sensor data and status via publish/subscribe
  Service                    Short request/response operation in ROS 2                          Status query or individual computation
  Action                     Longer-running task with feedback and result                       For example, navigation to a destination
  QoS                        Quality of Service                                                 Configurable message transmission properties
  Nav2                       Navigation2                                                        ROS 2-based toolkit for mobile navigation
  MoveIt 2                   Framework for robotic manipulation                                 Kinematics, motion planning and collision checking
  ros2_control               ROS 2 hardware/controller framework                                Connects controllers and drives
  Behavior Tree              Behaviour tree for coordinated subtasks                            Structures navigation and error-handling workflows
  Edge Computing (robotics)  Computing power directly on the machine                            Enables low-latency processing independent of the network
  VLA                        Vision-Language-Action                                             Research approach to models spanning images, language and actions
  Functional safety          Safety functions and error handling based on risk assessment       Must be considered independently of the quality of an LLM response
  OTA update                 Over-the-Air Update                                                Remote update of device software
  Telemetry                  Transmitted operational and state measurements                     Monitoring and maintenance of robots and fleets

## M9-L1 – User interfaces, accessibility and software ergonomics {#S31}

  Term                      Explanation                                                         Significance
  ------------------------  ------------------------------------------------------------------  -------------------------------------------------------------
  UI                        User Interface                                                      Controls for interacting with a system
  UX                        User Experience                                                     Includes expectations and actual experience of use
  HCI                       Human–Computer Interaction                                          Research field of human–computer interaction
  Usability                 Usability                                                           Effective, efficient and satisfactory use in a context
  Accessibility             Accessibility                                                       Access for people with different abilities and circumstances
  Information architecture  Systematic organisation of content and navigation                   Makes finding and categorising information easier
  Mental model              Understanding of how a system works                                 Determines expectations and interaction behaviour
  Affordance                Perceptible action possibility of an element                        Helps identify interactions
  Progressive Disclosure    Gradual disclosure of more complex functions                        Reduces initial information load
  Design system             Shared design rules and components                                  Supports consistency and maintenance
  WCAG                      Web Content Accessibility Guidelines                                W3C guidelines with testable success criteria
  W3C                       World Wide Web Consortium                                           Standards body for web technologies
  ARIA                      Accessible Rich Internet Applications                               Semantic roles and states for assistive technology
  Screen reader             Software that conveys structured content through audio or Braille   Requires accessible names, roles and states
  Keyboard focus            Element currently addressed by keyboard                             Must be visible and reachable in a meaningful way
  Contrast ratio            Ratio of the relative luminances of two colours                     Helps assess readability
  Responsive Design         Layout adaptation to devices and display areas                      Works on mobile and large screens
  Usability test            Observed completion of specific tasks                               Identifies successes, problems and user experiences
  Heuristic evaluation      Expert review against design rules                                  Supplements but does not replace user testing
  EAA                       European Accessibility Act                                          EU legal framework for certain accessible products/services
  BFSG                      Accessibility Strengthening Act (Barrierefreiheitsstärkungsgesetz)  German legal framework implementing relevant EAA requirements
  Percentage points         Absolute difference between two percentages                         90 % − 60 % = 30 percentage points

## M9-L2 – Data analysis, visualisation and statistical thinking {#S32}

  Term                    Explanation                                                         Significance
  ----------------------  ------------------------------------------------------------------  -------------------------------------------------------------
  Unit of observation     What a data row represents                                          Do not confuse a person, job, file or measurement event
  Data cleaning           Traceable handling of data problems                                 Check units, duplicates and missing values
  NULL / missing value    No information available                                            Do not equate with the numerical value zero
  Descriptive statistics  Description of observed data                                        Location, frequency and dispersion
  Arithmetic mean         Sum of values divided by their number                               Sensitive to large extreme values
  Median                  Central value of a sorted sequence                                  More robust to individual outliers
  Mode                    Most frequently observed value                                      Also meaningful for categories
  Quartile                Cut point in a sorted distribution of values                        Specify the quantile convention
  IQR                     Interquartile range                                                 Difference between the upper and lower quartiles
  Variance                Mean squared distance from the mean                                 Distinguish population and sample formulae
  Standard deviation      Square root of the variance                                         Dispersion in the original unit
  Weighted mean           Mean with different weights for individual cases                    Account for group sizes correctly
  Population              All units relevant to the question                                  Target set of statistical statements
  Sample                  Examined subset of the population                                   Selection determines evidential strength
  Selection bias          Systematic bias in selection                                        More data alone do not remedy bias
  Sampling error          Fluctuations due to selection of a subset                           Distinguish from measurement and non-sampling error
  Standard error          Dispersion of an estimator across hypothetical samples              Basis of uncertainty intervals
  Confidence interval     Estimation interval using a procedure with a defined coverage rate  Not a probability judgement about the already fixed parameter
  Base rate               Frequency of an event in the initial set                            Important for evaluating rare alerts
  Correlation             Statistical association of two quantities                           Not proof of causation
  Causation               Cause-and-effect relationship                                       Requires appropriate study designs
  Simpson's paradox       Reversal in the direction of group comparisons upon aggregation     Check group composition
  Time series             Measurements in chronological order                                 Consider trends, seasonality and measurement windows
  Histogram               Distribution of numerical values in intervals                       Bin widths affect the representation
  Scatter plot            Representation of pairs of two measured quantities                  Identify relationships and outliers
  p-value                 Model-relative surprisingness of the data under a null hypothesis   Not a measure of the probability that the hypothesis is true
  A/B test                Planned comparison of two variants                                  Define assignment, target metric and duration in advance
  Data Leakage            Impermissible information flow in training and evaluation           Prevents credible model testing
  Data Drift              Change in input distribution over time                              Quality and monitoring may be affected
  Concept Drift           Change in the relationship between inputs and target                Model may become outdated even with unchanged metrics

## M9-L3 – Embedded systems, sensors and microcontrollers {#S33}

  Term             Expanded form / meaning                        Brief explanation
  ---------------  ---------------------------------------------  ------------------------------------------------------------
  Embedded System  Embedded system                                Computer with a specific task within a technical device
  MCU              Microcontroller Unit                           Chip with processor, memory and device interfaces
  SoC              System on a Chip                               Multiple computing and peripheral components on one chip
  GPIO             General-Purpose Input/Output                   Configurable digital input/output
  ADC              Analog-to-Digital Converter                    Converts analogue voltages into digital values
  Quantisation     Mapping continuous values onto digital levels  Resolution does not guarantee accuracy
  PWM              Pulse Width Modulation                         Controls the duty cycle of digital pulses
  Duty cycle       Duty Cycle                                     Proportion of on-time in a PWM period
  UART             Universal Asynchronous Receiver-Transmitter    Serial asynchronous transmission
  I²C              Inter-Integrated Circuit                       Two-wire bus with addressed participants
  SPI              Serial Peripheral Interface                    Serial peripheral interface with clock and data lines
  CAN              Controller Area Network                        Message-oriented fieldbus for machines and vehicles
  Interrupt        Hardware/software interrupt request            Invokes a suitable handler to process an event
  NVIC             Nested Vectored Interrupt Controller           Interrupt control in many Arm Cortex-M processors
  DMA              Direct Memory Access                           Data transfer by hardware without the CPU copying every byte
  RTOS             Real-Time Operating System                     Operating system for time-critical embedded tasks
  Deadline         Real-time deadline                             Time by which a result must be available
  Jitter           Variation in delay                             Timing irregularity of repeated events
  Watchdog         Execution monitoring                           Can detect failed program execution and initiate a restart
  Brownout         Undervoltage event                             Supply voltage falls below the permitted operating point
  OTA              Over-the-Air Update                            Transfer of new firmware via a connection
  IoT              Internet of Things                             Networked devices with sensors or actuators
  Sensor fusion    Combined evaluation of multiple sensors        Improves state estimation under suitable assumptions
  IMU              Inertial Measurement Unit                      Sensor package for acceleration and rotational movement

## Terminology from M7-L4 – architecture, data protection and risk {#S34}

  Term                         Brief definition                                                                            Important limitation
  ---------------------------  ------------------------------------------------------------------------------------------  --------------------------------------------------------------------
  Architecture decision / ADR  Documented choice with context, alternatives and consequences                               Not a substitute for subsequent reassessment
  Quality requirement          Measurable or otherwise testable quality criterion of a system                              “Fast” alone is not measurable
  Trust Boundary               Transition between areas with different security assumptions                                An internal network location does not automatically justify trust
  STRIDE                       Classification of technical threats into six groups                                         Not exhaustive for privacy and organisational risks
  Threat Modeling              Systematic examination of assets, threats and possible safeguards                           No guarantee of anticipating all attacks
  Least Privilege              Grant only required access permissions                                                      Requires maintenance as tasks change
  Zero Trust                   No implicit granting of trust based solely on location or network zone                      Neither a single product nor an all-purpose guarantee
  Row-Level Security (RLS)     Database policies limiting access to individual table rows                                  Owners and privileged roles may be exempt
  RPO                          Recovery Point Objective – intended maximum tolerated data loss expressed as a time window  Do not confuse with recovery duration
  RTO                          Recovery Time Objective – target time until service resumes                                 Without a restore test, a target is not yet a proven commitment
  Data minimisation            Process data only to the extent necessary for the purpose                                   Legal basis and purpose limitation remain subject to separate checks
  Sensitivity analysis         Check how a decision changes with different assumptions                                     Does not remedy poorly chosen criteria
  Pareto dominance             Alternative is at least as good in all criteria and better in one                           Without clear criteria there is no meaningful comparison
  Defense in Depth             Combine multiple independent security measures                                              One layer must not conceal failures in others

## Terminology from M7-L5 – scientific evaluation of AI systems {#S35}

  Term              Brief definition                                                          Limit of inference
  ----------------  ------------------------------------------------------------------------  ---------------------------------------------------------
  Evaluation        Systematic assessment against defined goals and data                      One metric does not capture all properties
  Benchmark         Standardised comparison tasks with evaluation                             Not automatically representative of every use case
  Population        Set of all cases to which a statement is intended to apply                Not identical to the observed sample
  Ground Truth      Label or result used as a reference                                       May itself be inaccurate or disputed
  Confusion matrix  Table of true/false positive and negative cases                           Only with respect to a defined positive class
  Accuracy          Proportion of all correctly classified cases                              Can be misleading for rare target classes
  Precision         TP divided by all predicted positive cases                                Not the same as recall
  Recall            Proportion of detected actually positive cases                            Not the same as precision
  F1-Score          Harmonic mean of precision and recall                                     Does not directly include TN or error costs
  Base rate         Frequency of a class in the target population                             Affects interpretability of precision
  Calibration       Agreement of estimated probabilities with frequencies                     Linguistic confidence is not calibration
  Generalisation    Performance on relevant, unseen cases                                     Must be tested for the target distribution
  Data Leakage      Impermissible flow of information between data and evaluation             Artificially good test results are possible
  Concept Drift     Change in the relationship between input data and target                  Not the same as just a change in class frequency
  OOD               Out-of-Distribution – markedly atypical inputs                            Success on test data does not guarantee OOD performance
  Slice analysis    Separate error analysis of domain-relevant subgroups                      Small groups increase uncertainty
  LLM-as-a-Judge    Language model evaluates generated results                                Check judgement bias, reference and rubric
  RAG evaluation    Separate checks of document retrieval, evidence and response              Good retrieval does not necessarily mean a correct answer
  Model Card        Standardised documentation of model purpose, performance and limitations  Not certification or a universal guarantee
  AI RMF            NIST framework for AI risk management                                     Voluntary guidance, not a model quality seal

## Terminology from M7-L6 – cross-system synthesis and research methods {#S36}

  Term                               Brief definition                                                                            Important limitation
  ---------------------------------  ------------------------------------------------------------------------------------------  --------------------------------------------------------------
  Cross-system synthesis             Connecting insights across multiple technical areas                                         Good individual results do not guarantee a good overall system
  Design Science                     Research through design and evaluation of purposeful artefacts                              Ordinary programming is not automatically research
  Research question                  Precisely delimited question that can be investigated methodically                          “Better” without a criterion is not testable
  Hypothesis                         Testable assumption with possible refuting findings                                         Not an already proven fact
  Deductive proof                    Logical derivation from axioms and prerequisites                                            Holds within the underlying model
  Empirical measurement              Observation of actual system processes                                                      Depends on measurement method, sample and context
  Design of experiments / DoE        Rules for comparable, evaluable investigations                                              Uncontrolled confounders can create apparent differences
  Confounder / confounding variable  Influence that varies systematically with the change being studied                          Can distort causal conclusions
  Randomisation                      Random assignment or random ordering in experimental design                                 Does not replace an appropriate sample
  Blocking                           Comparison within experimental groups that are as similar as possible                       Poorly chosen groups may obscure differences
  End-to-End                         Consideration of the complete chain of effects up to the user outcome                       Component values are not automatically overall values
  Tail Latency                       Slow tail regions of a runtime distribution                                                 Mean conceals problematic outliers
  SLI                                Service Level Indicator: measured quality metric of a service                               Meaningful only with a precise measurement definition
  SLO                                Service Level Objective: agreed target value for an SLI                                     A target is not proof of actual fulfilment
  Pareto dominance                   A variant is no worse in any criterion and better in at least one                           Determine criteria and hard constraints first
  Decision matrix                    Transparent weighing of multiple criteria and weights                                       Subjective scores are not objective facts
  Sensitivity analysis               Examines decisions under changed assumptions                                                Cannot rescue a flawed research question
  TCO                                Total Cost of Ownership: total costs over the period considered                             A monthly cloud price is not a complete TCO
  Reproducibility                    According to the National Academies: consistent computation with the same data and methods  Term is used differently across disciplines
  Replication                        New investigation of the same question with its own data                                    Same result not guaranteed for every population
  Generalisability                   Transferability of insights to other contexts                                               Must be justified additionally
  Research artefact                  Verifiable component of an investigation (code, data, procedure)                            Rights may limit the ability to publish
  FAIR                               Findable, Accessible, Interoperable, Reusable                                               Accessible does not necessarily mean public
  ADR                                Architecture Decision Record: documented architecture decision                              Documentation does not replace reassessment when changes occur

## M8-L4 – Algorithms and data structures in depth {#S37}

| Term | Meaning | Important |
| --- | --- | --- |
| AVL tree | Binary search tree with height difference of at most one at each node | Rotation preserves key order |
| Balance factor | Height of the left subtree minus height of the right subtree | Only -1, 0 or 1 in an AVL tree |
| Red-black tree | Search tree with colour and black-height invariants | Logarithmic height bound |
| Black height | Number of black nodes on a path under a specified counting convention | Equal on all paths from the same starting node |
| Rotation | Local restructuring of a search tree | Inorder sequence is preserved |
| Min-heap | Complete binary tree with each parent's key no greater than its children's keys | Minimum at the root, not fully sorted |
| Priority queue | Abstract data type for selection by priority | Can be implemented with a heap |

Further study: [M8-L4](../M8-L4.md).
