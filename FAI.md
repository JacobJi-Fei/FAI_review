# FAI

## Basic AI

### AI

- Definition (What is AI)

	- Artificial Intelligence (AI) is the branch of computer science that develops machines and software with intelligence
	- 主要的 researchers 和 textbooks 定义这个领域为 the study of design of intelligent agents
where an intelligent agent is a system that perceives its environment and takes actions that maximize its chances of success.

- History of AI

	- 1943 WW2

		- Turing Test 图灵测试
		- Influenced AI , till now

	- 1956 Birth of AI

		- John McCarthy and Marvin Minsky
		- AI term coined, Dartmouth University
		- Top down approach: pre-processed to do things
		- Bottom up approach: simulate brains, learn new behaviours

	- 1970's AI winter

		- Common sense reasoning and supposedly simple tasks like face recognition would always be beyond their capability

			- Reason

				- Funding for the industry was slashed 资金不足
				- Perceptron not able to implement basic function. 感知器不能实现基本功能
				- Example：Machine translations 机翻 心有余而力不足 1950‘s

	- 1980 expert system, new hope

		- General problem solving vs. expert system

	- 1990 Bottom up approach

		- Immitate biology ,ANN

	- 1997 AI Game, Milestone

		- Deep Blue

	- 2002 First robot for the home

		- Roomba by iRobot

	- 2008 Speech recognition

		- Google

	- 2011

		- Watson won US quiz show Jeopardy

	- 2014 Turing test passed

- Turing Test

	- The test is conducted with two people and a machine 两个人一个机器
	- One person plays the role of an interrogator and is in a separate room from the machine and the other person 其中一个人作为审问者，和其他的机器和人分隔开

		- The interrogator cannot see the machine and person, he only knows the person and machine as A and B. 这人看不见机器和人， 只知道机器和人是A或者B（尼玛这不是派西维尔）
		- The interrogator’s task: to find out which candidate is the machine or human, only by asking them questions. 
审问者的任务是通过问问题找出哪个是人哪个是机器

	- The aim of the machine is to fool the interrogator into thinking that it is a person. 机器的目的是混淆审问者，让他觉得自己是人（小莫？）

		- If the machine can fool the interrogator 30% of the time, the machine is considered intelligent.

	- Suggested as a way of saying when we could consider machines to be intelligent, or at least act intelligently
	- A satisfactory operational definition of intelligence
	- The first machine to pass a Turing test

		- the chatbot "Eugene Goostman"

	- The need?

		- Natural language processing
		- Knowledge representation
		- Automated reasoning

			- to use the stored information to answer questions and to draw new conclusions. c储存信息用来回答并且总结出新的结论

		- Machine learning
		- Vision ( for Total Turing Test)
		- Motor control (total test)

			- to act upon objects as requested.按要求对物体施加作用

		- Other senses (total test)

			- such as audition, smell, touch, etc

- The Chinese Room

	- 1980 John Searle devised a thought experiment which he called the Chinese Room

		- Searle argued that the Turing test could not be used to determine if a machine can think
他认为图灵测试不能决定机器可以思考
		- Behaving intelligently was not enough to prove a computer was intelligent

	- comprise of

		- a human, who only understands English
		- a rule book, written in English
		- stack of paper

			- One stack of paper is blank
			- The other has symbols on them.

		- In computing terms

			- human - CPU
			- The rule book is the program
			- two stacks of paper are storage devices

	- the system does not understand Chinese as it just comprises a rule book and stacks of paper which do not understand Chinese.

		- 反驳图灵测试的点

			- 机器能翻译但是他还是不懂中文
			- running the right program does not necessarily generate understanding, the system only act as it understands Chinese

### Strong AI vs. Weak AI

- John Searle
- Strong AI

	- A system can have a mind and mental states

- Weak AI

	- A system can act intelligently

		- there are non-intelligent ways to achieve intelligent tasks

### Basics in Machine learning

## Problem Formulation And Search Tree 

### basics

- Search space

	- Set of all possible solutions to a problem

- Search algorithms

	- Take a problem as input
	- Return a solution to the problem

### Definitions and examples of problems 

- Problem formulation

	- Problem formulation is the process of deciding what actions and states to consider, given a goal.
	- Problem components

		- Initial State

			- The starting state of the problem, defined in a suitable manner

		- Actions(operators)

			- An action or a set of actions that moves the problem from one state to another
			- The set of all possible states reachable from a given state s by applying all legal action is known as the neighbourhood and the action(s) can be recognized as the successor function

		- Goal Test

			- A test applied to a state which returns true if we have reached a state that solves the problem 到没到终点

		- Path Cost

			- How much it costs to take a particular sequence of actions 这一系列actions 的cost 

		- A solution to a problem is an action sequence that leads from the initial state to the goal state.

	- Example

		- Romania

			- Initial State

				- Arad

			- Operator

				- Driving between cities
				- State space consists of all 20 cities in the graph

			- Goal Test

				- Is the current state Bucharest?
				- a solution is a path from the initial to the goal state

			- Path cost

				- a function of time/distance/risk/petrol

		- 8-puzzle Game

			- Initial State

				- Specifies the location of each of the eight tiles and the blank in one of the nine squares

			- Operators

				- Blank tile moves left, right, up or down

			- Goal Test

				- The current state matches a certain state

			- Path Cost

				- Each move of the blank costs 1

			- How big is the State space

				- 9?

			- Number of actions/ operators
(how they are formulated)

				- 4 possible moves could be specified for each of the 8 tiles, 4 * 8 = 32
				- 4 moves for blank square - 4 operators

		- 8-Queen

- Problem representation

	- Trees - Terminology

		- Nodes

			- Root node
			- Children/parent of nodes
			- Leaves

		- Branches
		- Average branching factor

			- Average number of branches of the nodes in the tree

		- Depth

			- Depth of a node

				- the number of edges(branches) away from the root node说白了就是到第几层了
注意： root 的位置 d = 0

			- Depth of a tree

				- The depth of a tree is the depth of the deepest node

		- Tree size

			- Nodes at d = 2的d次方
			- Nodes in a tree = 2 的d+1 次方  - 1

		- 与Problem components 对应

			- States - nodes

				- Possible states of problem, defined in some suitable manner

			- Initial State - root node

				- The starting state of the problem

			- State Space – all nodes in the tree

				- The set of all states reachable from the initial state

			- Neighborhood

				- The set of all possible states reachable from a given state
				- Branching factor: number of neighborhoods

			- Operators - branches

				- A set of actions that moves the problem from one state to another

	- Example

		- Romania
		- Tic-Tac-Toe

			- Nodes: states of problem
			- Root node: initial state of the problem
			- Branches: moves by operator
			- Branching factor: number of neighbours

	- Search Tree issues

		- Search trees grow very quickly
		- The size of the search tree is governed by the branching factor
		- Even the simple game with branching factor of 3 has a complete search tree of large number of potential nodes
		- The search tree for chess has a branching factor of about 35
		- Example

			- Claude Shannon delivered a paper in 1949 at a New York conference on how a computer could play chess.

				- Working at 200 million positions per second, Deep Blue would require 10100 years to evaluate all possible games.
				- 10的100次方 is larger than the number of atoms in the universe.

### Good Solution

- How good is a solution

	- Does out search method actually find a solution?
	- good solution

		- Path cost
		- Search Cost

			- Time and Memory

	- Does it find the optimal solution? 最佳方案

- Evaluation criteria

	- Strategies are evaluated along the following dimensions

		- Completeness

			- does it always find a solution if one exists

		- time complexity

			- number of nodes generated/expanded

		- space complexity

			- maximum number of nodes in memory

		- optimality

			- does it always find a least-cost solution

	- Time and space complexity are measured in terms of  

		- b

			- maximum branching factor of the search tree

		- d

			- depth of the least-cost solution

		- m

			- maximum depth of the state space

				- 可能到∞

### Uninformed(blind) search algorithms

- No additional information about states beyond that provided in the problem definition
- Implementation

	- Fundamental actions(operators)
	- "Expand"

		- Ask a node for its children

	- "Test" 

		- Test a node to see whether it is a goal

- General Tree Search

	- frontier - 一层一层取

- Breadth First Search (BFS)

	- Method

		- Queuing function: adds nodes to the end of the queue(FIFO)

	- Implementation

		- Frontier nodes(open nodes, leaves)

			- have been discovered
			- have not yet been processed

				- Children not yet explored; not yet tested if they are goal

		- Visited nodes( closed nodes)

			- have been discovered
			- have been processed

				- Children explored; tested if they match a goal

		- Undiscovered nodes

			- have not yet been discovered

	- Evaluating a search

		- Completeness

			- Guaranteed to find a solution if one exist?

				- yes

		- Time Complexity

			- How long does it tale to find a solution?

				- b的d次方

		- Space Complexity

			- How much memory required to perform the search?

				- b的d次方

		- Optimality

			- Find the optimal solution(one or all optimal solutions)?

				- yes

		- b: the maximum branching factor
d: is the depth of the search tree
		- Big O: notation in complexity theory

			- We use it to measure how the problem size affects the algorithm’s computational resource (time or memory).

		- Combinatorial explosion: 

			- the number of problem solutions grows exponentially with its size

- Depth First Search(DFS)

	- Method

		- Expand Root Node First
		- Explore one branch before exploring another branch
		- Queuing function: adds  nodes to the front of the queue(LIFO)
		- 简而言之，把左边那一支全找完 再找右边

	- Evaluation

		- b: a branching factor
m: maximum depth
		- Space complexity

			- DFS requires storage of O(bm) nodes ?

		- Time complexity

			- O(b的m次方）in the worst case

		- Completeness

			- An infinite branch: never terminate = > no goal state exist in that branch

				- NO

		- Optimality

			- Finds a solution: is there a better solution at a lower level

				- NO

- Uniform cost search ( UCS)

	- UCS vs. BFS

		- Optimal condition

			- BFS: Cost: same for all branches
			- UCS: Cost never decreases

		- Order of nodes explored

			- BFS: Shallower noes first
			- UCS: Lowest cost node first

	- Cost: total cost of the path from the root to node n
	-  UCS(problem) returns a solution or failure
	- Evaluation

		- Optimality

			- BFS: Only if the branch costs are the same
			- UCS: Even branch costs are different

		- Completeness

			- Systematically search the whole tree ( in the worst case)

		- Time complexity

			- b的d次方

		- Space complexity

			- b的d次方

		- When UCS = BFS

			- When all branches have the same cost
			- We are talking about the worst case scenario

		- UCS is usually better than BFS

- Blind (Uniformed) Searches

	- Simply searches the State Space

		- No preference as to which node to expand next 对下一步的扩展没有优先级

	- The different blind searches

		- Characterised by searches

			- Characterised by | the order | which expands the nodes

				- Different node ordering: shape of the frontier
				- Different shapes of the frontier: very different memory usages

	- An uninformed search

		- Has no knowledge about its domain

### Blind Search vs. Heuristic Search

- Blind Search

	- Blindly choose where to search in the search tree (瞎JB找）

		- When problems get large, not practical any mpre

- Heuristic Search

	- Explore the node:  more likely to lead to the goal state
	- Using knowledge, so called informed search
	- Greedy search, A* search

### Informed search algorithms（Heuristic Search)

- Introduction

	- Add domain-specific information to select the best path along which to continue searching 
添加特定领域信息来选接下来走哪个

		- !!!Work by deciding which is the next best code to expand to reach the goal using domain knowledge

	- Sometimes known as informed search, it is usually more efficient than blind searches
	- Heuristic Search works by deciding which is the next best node to expand 
Heuristic Search 运行通过决定哪一个是最好的下一步， 但是不能保证他选的确实就是最好的
	- A heuristic method is particularly used to rapidly come to a solution that is hoped to be close to the best possible answer, or 'optimal solution’ 快速产出-得到最好的答案
	- Heuristic function h(n) estimates the "goodness" of a node n.

h(n) = estimated cost (or distance) of minimal cost path form n to a goal state
h(n) 就是一个函数用来估计从n到终点最小cost path 的 cost 或者 distance.
	- All domain knowledge used in the search is encoded in h(n), which is computable from the current state description.
Domain knowledge 就是用在 h(n)中
	- In general, h(n) ≥ 0 for all nodes n and h(n) = 0 implies that n is a goal node

- Greedy Search

	- Use as an evaluation function f(n) = h(n) , sorting nodes by increasing values of f
	- Selects node to expand believed to be closest ("greedy") to a goal node 
	- It is only concerned with short term gains
	- It is possible to get stuck in an infinite loop unless mechanism for avoiding repeated states is in place
	- Not Complete
	- Not Optimal
	- Time complexity is O(b的d次方）

		- where d is the depth of the search tree

	- Space complexity is O (b 的 d 次方）

		- where d is the depth of the search tree

- UCS vs. Greedy Search

	- Order of nodes to explore

		- UCS: Nodes of the lowest path cost
		- Greedy search: Nodes which are the closest to the goal

	- Cost(n)

		- UCS: g(n): actual path cost thus far
		- Greedy Search: h(n): estimate cost to the goal( using heuristic)

- A* Search

	- UCS is a special case of BFS which can be applied to graphs where the costs of each branch vary
	- UCS works by expanding the lowest cost node on the fringe 通过计算最低cost node
	- Combines the cost so far and the estimated cost to the goal 结合从起点到现在的cost 和 估计之后到终点的cost

		- f(n) = g(n) + h(n)

			- g: cost from the initial state to the current state
			- h: the cost from the current state to a goal state
			- f: an evaluation of the state: estimated cost of the cheapest solution through n
			- h = 0, A* becomes UCS

				- complete & optimal*, but search undirected

					- *when cost along path never decrease

			- h too large thus dominates g

				- becomes Greedy, lose optimality

	- Optimal and complete

		- If the heuristic is admissible

			- Admissible: the heuristic must never over estimate the cost to reach the goal

				- ­h(n): a valid lower bound on cost to the goal

					- hn 是定一下下一个node 的方向，必须是h(n)逐渐变小

	- Example

		- 8-puzzle-game

			-  develop an admissible heuristic in A* that does not over estimate, to find the optimal solution

				- h1 = no. of tiles in the wrong position
				- h2 = sum of the distance of the tiles to their goal positions using the Manhattan Distance
				- INFORMEDNESS

					- h2 is much more informed
					- Domination translate to efficiency: A* using h2 will never expand more nodes than A* using h1, h2 永远不会比使用h1扩展更多的节点
					- 使用具有较高值的启发式函数，只要它不高估启发式的计算时间不是太大

	- Effective branching factor

		- Effective branching factor: average no. of branches expanded
		- Quality of a heuristic:

			- average effective branching factor

		- A good heuristic

			- The closer the estimate of the heuristic, the better
			- Lower average effective branching factor
			- Admissible

		- 选那种能得到最佳结论且expand nodes 少的

## Game Playing (Adversarial Search)

### Components of Game Search

- The initial state

	- board position, indication of those move it is

- A set of operators

	- define the legal moves that a player can make

- A terminal test

	- determines when the game is over ( terminal states)

- A utility (payoff) funcition

	- gives a numeric value for the outcome(terminal state) of a class (like chess: +1, 0, 1/2)

### Minimax

- utility function (minimax value) of a node

	- the utility (for MAX) of being in the corresponding state ( larger values are better for "MAX")

- MAX: take the best move for MAX

	- Next state: the one with the highest utility

		- i.e. the maximum of its children in the search tree

- MIN: take the best move for MIN(the worst for MAX)

	- Next state: the one with the lowest utility 

		- i.e. the minimum of its children in the search tree

- 两个玩家一个 MIN 一个 MAX ， MAX走的都是让utility 大的一步， 就是让MAX赢， MIN 走的就是让utility 小的一步，就是不让MAX赢
- Example

	- Nim

		- utility function

			- 0 =  a win for MIN
			- 1 = a win for MAX

- Efficiency of the search

	- Game trees are very big
	- vEvaluation of positions is time-consuming

- How can we reduce the number of nodes to be evaluated??

	- alpha-beta pruning based on minimax, Deep Blue
	- Better estimation of utility values (possibility of winning), i.e. heuristic, ANN, etc.

### ALPHA-BETA PRUNING

- Pruning allow us to ignore portions of the search tree that make no difference to the final choice 
忽略那些对final choice 没有影响的portions

	- Why use？

		- The number of nodes grow exponentially, nodes 的数量以指数形式增长
		- It is possible to compute the correct minimax decision without looking at every node in the game tree 不需要看树中的每一个节点就可以得出结果
		- Use the idea of pruning to eliminate large parts of the tree from consideration

- alpha-beta pruning effection

	- If this is done well then alpha-beta search can effectively double the depth of search tree that is searchable in a given time. 
树可以更深

- Two parameters

	- alpha 

		- α values are stored with each MAX node
		- the highest-value we have found so far at any choice point along the path of MAX

	- beta

		- values are stored with each MIN node
		- the lowest-value we have found so far at any choice point along the path of MIN

- If we were doing BFS, would you still be able to prune nodes in this fashion?

	- NO! Because the pruning on node D is made by evaluating the tree underneath D
	- This form of pruning relies on doing a DFS

- To maximise pruning: first expand the best children最大程度地pruning

	- cannot know which ones are really best
	- use heuristics for the “best-first” ordering
	- Heuristic evaluation function allow us to approximate the true utility of a state without doing a complete search.
用 Heuristic evaluation function 去估计一个sate 去真正利用当还没做完一个complete search

### CLASSIFICATION

- Fully observable

	- Both players have full and perfect information about the current state of the game

- Partially observable

	- Players do not have access to the full “state of the game”

		-  card games – you typically cannot see all of your opponents cards

- Deterministic

	- There is no element of chance
	- The outcome of making a sequence of moves is entirely determined by the sequence itself

- Stochastic

	-  there is some element of chance

		- E.g. Backgammon – throw dice in order to move

### How is a game represented as a search problem?

- The different states of the game are represented by nodes in the game tree, very similar to the above planning problems.

## 分支主题 4

*XMind - Trial Version*