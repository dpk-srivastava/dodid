dodid
=====

import java.awt.Point;
import java.math.BigInteger;

import java.text.DateFormat;

import java.text.SimpleDateFormat;

import java.util.ArrayList;

import java.util.Arrays;

import java.util.Collection;

import java.util.Collections;

import java.util.Comparator;

import java.util.Date;

import java.util.Deque;

  import java.util.HashMap;

import java.util.HashSet;

import java.util.Iterator;

import java.util.LinkedHashMap;

import java.util.LinkedList;

import java.util.List;

import java.util.Map;

import java.util.Map.Entry;

import java.util.PriorityQueue;

import java.util.Properties;

import java.util.Queue;

import java.util.Scanner;

import java.util.Set;

import java.util.Stack;

import java.util.TreeMap;
import java.util.concurrent.Callable;

import java.util.concurrent.ExecutionException;

import java.util.concurrent.ExecutorService;

import java.util.concurrent.Executors;

import java.util.concurrent.Future;

import java.util.concurrent.atomic.AtomicInteger;



import javax.mail.Message;

import javax.mail.MessagingException;

import javax.mail.Session;

import javax.mail.Transport;

import javax.mail.internet.InternetAddress;

import javax.mail.internet.MimeMessage;

import org.apache.commons.lang3.ArrayUtils;

class Box implements Comparable<Box> {

	Integer x;

	Integer y;

	Integer z;



	Integer area;

	public Box(Integer x, Integer y, Integer z) {

		this.x = x;

		this.y = y;

		this.z = z;

		area = y * z;

	}



	@Override

	public int compareTo(Box box) {

		return box.area - this.area;

	}

}


class Interval {

	Integer x;



	Integer y;



	public Interval(Integer x, Integer y) {

		this.x = x;

		this.y = y;

	}



	public Interval() {

		this.x = null;

		this.y = null;

	}

}

class Graph {

	int v;



	LinkedList<Integer> adj[];



	public Graph(int v){

		this.v=v;

		adj = new LinkedList[v];

		for (int i = 0; i < v; i++)

			adj[i] = new LinkedList<Integer>();

	}



	public void addEdge(int v, int w) {

		adj[v].add(w);

	}

}

 
 class Sum {

	public int S;



	public Sum(int s) {

		this.S = s;

	}



}

 class LinkedSet {

	int val;

	LinkedSet next;

	LinkedSet prev;

	LinkedSet head;



	LinkedSet right;



	LinkedSet random;

	

	public LinkedSet(final int val)

	{

		this.val=val;

		this.prev=null;

		this.next=null;

	}

	

	LinkedSet push(LinkedSet head_ref, int data) {

		/*

		 * 1 & 2: Allocate the Node & Put in the data

		 */

		LinkedSet new_node = new LinkedSet(data);



		/* 3. Make next of new Node as head */

		new_node.next = head_ref;



		/* 4. Move the head to point to new Node */

		head_ref = new_node;



		/* 5. return to link it back */

		return head_ref;

	}



	public void insert(final LinkedSet linkSet)

	{

		if(this.head==null)

		{

			this.head=linkSet;

			this.head.prev=null;

			this.head.next=null;

		}

		else

		{

			LinkedSet temp=this.head;

			while(temp.next!=null)

			{

				temp=temp.next;

			}

			temp.next=linkSet;

			linkSet.prev=temp;

		}

	}



	public int size(LinkedSet node) {

		int count = 0;

		while (node != null) {

			node = node.next;

			count++;

		}

		return count;

	}

}

 class TreeNode implements Comparable<TreeNode> {

	int val;



	Character value;

	TreeNode right;



	TreeNode left;



	TreeNode root;



	TreeNode random;



	String st;



	int hd;



	public TreeNode(final int val) {

		this.val = val;

	}



	public TreeNode(final String st) {

		this.st = st;

	}



	public TreeNode(final Character value) {

		this.value = value;

	}



	public TreeNode(final Character value, final int val, final TreeNode left, final TreeNode right) {

		this.val = val;

		this.value = value;

		this.left = left;

		this.right = right;

	}



	public TreeNode insertBST(final TreeNode node, TreeNode root) {

		if (root == null) {

			root = node;

			this.root=root;

		}

 else if (root.val < node.val) {

			if (root.right != null)

				this.insertBST(node, root.right);

			else

				root.right = node;

		}

		else {

			if (root.left != null)

				this.insertBST(node, root.left);

			else

				root.left = node;

		}

		return root;

	}



	public TreeNode insertBT(final TreeNode node, TreeNode root) {

		if (root == null) {

			root = node;

			return root;

		}

		this.insertBT(node, root.left);

		if (root.left == null) {

			root.left = node;

			return root;

		} else if (root.right == null) {

			root.right = node;

			return root;

		}



		this.insertBT(node, root.right);

		return root;

	}



	@Override

	public int compareTo(final TreeNode that) {

		return (this.val - that.val) * -1;

	}

}

 class Lottery {

	public static final String prize = "64000";



	private static long num = 0;



	public Lottery() {

		num++;

	}



	public static long num() {

		return num;

	}

}

 public class TestPractice extends Lottery {



	private final String name;



	TestPractice(String name) {

		this.name = name;

	}



	private String name() {

		return name;

	}



	private void reproduce() {

		new TestPractice("reproduce") {

			void printName() {

				System.out.println(name());

			}

		}.printName();

	}



	public static final String prize = "200";



	static final int SIZE = 5;



	Map<Integer, LinkedSet> LRUCache = new HashMap<Integer, LinkedSet>();



	LinkedSet cacheNodes = new LinkedSet(-999);



	LinkedSet head = null;



	TreeNode root = null;



	TreeNode prev = null;



	static int count = 0;

	TreeNode clonedRoot = null;



	LinkedSet rear = null;



	public TestPractice() {

		name = "";



	}



	public static void main(final String[] args) {





		System.out.println((String)null);

		try {

			TestPractice prac = new TestPractice();

			prac.writeLogs("", "");

			prac.executeFuturetask();

			TreeNode root = new TreeNode(5);

			root.left = new TreeNode(2);

			root.right = new TreeNode(12);

			root.left.left = new TreeNode(1);

			root.left.right = new TreeNode(3);

			root.right.left = new TreeNode(9);

			root.right.right = new TreeNode(21);

			root.right.left.left = new TreeNode(19);

			root.right.right.right = new TreeNode(25);



			System.out.println(prac.findDistanceBetweenNode(root.right.right, root.right.right.right, root));



			prac.findMaxProduct(new int[] {

					1, -2, -3, 0, 7, -8, -2

			});



			prac.findMaxFlippingZeroes(new int[] {

					0, 0, 0, 1, 0, 1

			});

			prac.alternateElementsMaxSum(new int[] {

					5, 5, 10, 100, 10, 5

			});



			prac.nge(new int[] {

					11, 13, 21, 3

			});

			prac.printJumpingNumbers(101);

			prac.printMatrixSpiral(new int[][] {

					{

							1, 2, 3, 4

					}, {

							5, 6, 7, 8

					}, {

							9, 10, 11, 12

					},

		           {13, 14, 15, 16}

			}, 6);

  			prac.searchAnElementRotatedArray(3);

			LinkedSet node1111 = new LinkedSet(-5);

			node1111.next = new LinkedSet(0);

			node1111.next.next = new LinkedSet(1);

			node1111.next.next.next = new LinkedSet(-2);

			node1111.next.next.next.next = new LinkedSet(3);

			node1111.next.next.next.next.next = new LinkedSet(4);

			node1111.next.next.next.next.next.next = new LinkedSet(5);

			node1111.next.next.next.next.next.next.next = new LinkedSet(-5);



			Lottery creature = null;

			for (int i = 0; i < 100; i++)

				creature = new Lottery();

			reverseBitsNumber(4);

			System.out.println(creature.num());

			new TestPractice("main").reproduce();

			System.out.println(TestPractice.prize);



			prac.slidingMax(new int[] {

					12, 1, 78, 90, 57, 89, 56

			}, 3);

			prac.sortLinkedList(node1111.next);

			prac.test();

			prac.testCode();

			prac.findHeightOfTrees(new int[] {

					2, 3, 4, 5

			});



			Scanner ssss = new Scanner(System.in);



			Graph fgg = new Graph(4);

			for (int i = 0; i < 3; i++) {

				String valu = ssss.nextLine(); // Reading input from STDIN

				int p = Integer.parseInt(valu.split(" ")[0]);

				int q = Integer.parseInt(valu.split(" ")[1]);

				fgg.addEdge(p, q);

			}

			for (int i = 1; i <= 4; i++) {

				findMissingEdges(fgg, new boolean[5], i);

			}

			System.out.print(count);

			Double valse = 47.01D;

			valse = valse + 0.01d;

			valse.floatValue();

			TreeNode vBST = new TreeNode(3);

			vBST.left = new TreeNode(2);

			vBST.right = new TreeNode(5);

			vBST.left.left = new TreeNode(1);

			vBST.left.right = new TreeNode(7);



			LinkedSet node = new LinkedSet(-5);

			node.next = new LinkedSet(-5);

			node.next.next = new LinkedSet(5);

			node.next.next.next = new LinkedSet(4);

			node.next.next.next.next = new LinkedSet(3);

			node.next.next.next.next.next = new LinkedSet(-2);

			node.next.next.next.next.next.next = new LinkedSet(1);

			node.next.next.next.next.next.next.next = new LinkedSet(1);



			System.out.println(prac.findValidBST(vBST));



			prac.findMax(new int[] {

					1, 20, 3

			}, 3);



			prac.LIS(new int[] {

					3, 10, 2, 1, 20

			});



			LRUCache ca = new LRUCache(4);

			ca.refer(1);

			ca.refer(2);

			ca.refer(3);

			ca.refer(1);

			ca.refer(4);

			ca.refer(5);

			ca.display();



			Graph g1 = new Graph(5);

			g1.addEdge(1, 0);

			g1.addEdge(0, 2);

			g1.addEdge(2, 0);

			g1.addEdge(0, 3);

			g1.addEdge(3, 4);

			Graph g22 = new Graph(3);

			g22.addEdge(0, 1);

			g22.addEdge(1, 2);



			System.out.println(prac.findCycle(g1, new boolean[5]));



			int mat[][] = {

					{

							1, 2, 3

					}, {

							4, 5, 6

					}, {

							7, 8, 9

					}

			};

			prac.printMatrixDiagonally(mat);

			Scanner s1 = new Scanner(System.in);

			String lines = s1.nextLine(); // Reading input from STDIN

			int n1 = Integer.parseInt(lines.split(" ")[0]);

			int k1 = Integer.parseInt(lines.split(" ")[1]);

			int[] arv = new int[n1];

			lines = s1.nextLine();

			for (int i = 0; i < n1; i++) {

				arv[i] = Integer.parseInt(lines.split(" ")[i]);

			}

			prac.findMinimumArr(arv, k1);



			int vals[] = new int[] {

					60, 100, 120

			};

			int wts[] = new int[] {

					10, 20, 30

			};

			int Ws = 50;

			prac.knapsack(vals, wts, Ws);

			prac.findRevisionPages(new int[] {

					2, 9, 4, 6, 18

			}, 3);



			LinkedSet L = new LinkedSet(0);



			L.head = L.push(L.head, 30);

			L.head = L.push(L.head, 8);

			L.head = L.push(L.head, 7);

			L.head = L.push(L.head, 5);



			L.head.right = L.push(L.head.right, 20);

			L.head.right = L.push(L.head.right, 10);



			L.head.right.right = L.push(L.head.right.right, 50);

			L.head.right.right = L.push(L.head.right.right, 22);

			L.head.right.right = L.push(L.head.right.right, 19);



			L.head.right.right.right = L.push(L.head.right.right.right, 45);

			L.head.right.right.right = L.push(L.head.right.right.right, 40);

			L.head.right.right.right = L.push(L.head.right.right.right, 35);

			L.head.right.right.right = L.push(L.head.right.right.right, 20);



			// flatten the list

			L.head = prac.flattenLinkedList(L.head);



			prac.getFormattedDate(new Date().toString());

			prac.findMaxAreaHistogram(new Integer[] {

					6, 2, 5, 4, 5, 1, 6

			});

			

			TreeNode kthBST = new TreeNode(20);

			kthBST.left = new TreeNode(8);

			kthBST.right = new TreeNode(22);

			kthBST.left.left = new TreeNode(4);

			kthBST.left.right = new TreeNode(12);

			kthBST.left.right.left = new TreeNode(10);

			kthBST.left.right.right = new TreeNode(14);

			prac.findKthElementBST(kthBST, 6, new ArrayList<TreeNode>());

    			prac.findLongestIncreasingSubsequence(new int[] {

					10, 22, 9, 33, 21, 50, 41, 60

			});

			prac.findmaximumInsertionsforPalindrome("geeks", "skeeg");



			prac.maximumSumRectangle(new int[][] {

					{

							1, 2, -1, -4, -20

					}, {

							-8, -3, 4, 2, 1

					}, {

							3, 8, 10, 1, 3

					}, {

							-4, -1, 1, 7, -6

					}

			});



			Box[] boxes = new Box[4];

			boxes[0] = new Box(4, 6, 7);

			boxes[1] = new Box(1, 2, 3);

			boxes[2] = new Box(4, 5, 6);

			boxes[3] = new Box(10, 12, 32);



			System.out.println(prac.maxBoxStacking(Arrays.asList(boxes)));



			Interval arr[] = new Interval[] {

					new Interval(5, 24), new Interval(27, 40), new Interval(50, 60), new Interval(15, 25),

			};



			System.out.println(prac.longestPairSubSequence(Arrays.asList(arr)));



			System.out.println(prac.eggDroppingProblem(2, 36));



			TreeNode diag = new TreeNode(8);

			diag.left = new TreeNode(3);

			diag.right = new TreeNode(10);

			diag.left.left = new TreeNode(1);

			diag.left.right = new TreeNode(6);

			diag.right.right = new TreeNode(14);

			diag.right.right.left = new TreeNode(13);

			diag.left.right.left = new TreeNode(4);

			diag.left.right.right = new TreeNode(7);



			Map<Integer, List<Integer>> diagMap = prac.diagonalTraversalOfTree(diag,

					new HashMap<Integer, List<Integer>>(), 0);

			for (int k : diagMap.keySet()) {

				System.out.println(Arrays.asList(diagMap.get(k).toArray()));

			}

			LinkedSet loop = new LinkedSet(50);

			loop.next = new LinkedSet(20);

			loop.next.next = new LinkedSet(15);

			loop.next.next.next = new LinkedSet(4);

			loop.next.next.next.next = new LinkedSet(10);



			// Creating a loop for testing

			loop.next.next.next.next.next = loop.next.next;



			prac.detectLoopInLinkedList(loop);



			Graph graph = new Graph(4);

			graph.addEdge(0, 1);

			graph.addEdge(0, 2);

			graph.addEdge(1, 2);

			graph.addEdge(2, 0);

			graph.addEdge(2, 3);

			graph.addEdge(3, 3);

			prac.detectCycleInADirectedGraph(graph, 4);



			Graph g2 = new Graph(3);

			g2.addEdge(0, 1);

			g2.addEdge(1, 2);

			prac.detectCycleInUndirectedGraph(g2, 5);



			LinkedSet rightNode=new LinkedSet(12);

			rightNode.next=new LinkedSet(15);

			rightNode.next.next = new LinkedSet(15);

			rightNode.next.next.next = new LinkedSet(15);

			rightNode.next.next.next.next=new LinkedSet(5);

			rightNode.next.next.next.next.next = new LinkedSet(15);

			rightNode.next.next.next.next.next.next=new LinkedSet(2);

			rightNode.next.next.next.next.next.next.next=new LinkedSet(3);

			

			prac.deleteAllOccurences(rightNode, 12);



			prac.deleteNodesWithRightGreaterValue(rightNode);

			prac.countPossibleDecodings("1234".toCharArray(), 4);



			prac.findNDigitNumbersWithSum(2, 5);

			prac.convert_to_words("1110".toCharArray());



			int pre[] = {

					10, 30, 20, 5, 15

			};

			char preLN[] = {

					'N', 'N', 'L', 'L', 'L'

			};

			TreeNode temp = prac.createTree(pre, preLN, new Sum(0), null);

			prac.printInorder(temp);

			int[] parentIndices = {

					-1, 0, 0, 1, 1, 3, 5

			};

			prac.createBinaryTreefromParentIndices(parentIndices);

			int[] ropes = {

					4, 3, 2, 6

			};

			prac.connectMinSumRopes(ropes);



			int[] comb = {

					2, 4, 6, 8

			};

			List<List<Integer>> finalAr = new ArrayList<List<Integer>>();

			prac.combinationalSum(finalAr, new ArrayList<Integer>(), comb, 0, 8);

			prac.root = null;

			TreeNode tree = new TreeNode(1);

			tree.left = new TreeNode(2);

			tree.right = new TreeNode(3);

			tree.left.left = new TreeNode(4);

			tree.left.right = new TreeNode(5);

			tree.random = tree.left.right;

			tree.left.left.random = tree;

			tree.left.right.random = tree.right;



			prac.cloneBinaryTreeLeftRight(tree, new HashMap<TreeNode, TreeNode>());



			LinkedSet Randomlist = new LinkedSet(5);

			Randomlist.next = new LinkedSet(4);

			Randomlist.next.next = new LinkedSet(3);

			Randomlist.next.next.next = new LinkedSet(2);

			Randomlist.next.next.next.next = new LinkedSet(1);



			// Setting up random references.

			Randomlist.random = Randomlist.next.next;

			Randomlist.next.random = Randomlist.next.next.next;

			Randomlist.next.next.random = Randomlist.next.next.next.next;

			Randomlist.next.next.next.random = Randomlist.next.next.next.next.next;

			Randomlist.next.next.next.next.random = Randomlist.next;



			LinkedSet cloneList = prac.cloneLinkedList(Randomlist);

			prac.printLinkedList(cloneList);



			TreeNode bottomView = new TreeNode(20);

			bottomView.left = new TreeNode(8);

			bottomView.right = new TreeNode(22);

			bottomView.left.left = new TreeNode(5);

			bottomView.left.right = new TreeNode(3);

			bottomView.left.right.left = new TreeNode(10);

			bottomView.left.right.right = new TreeNode(14);

			bottomView.right.right = new TreeNode(25);





			TreeMap<Integer, Integer> map = prac.showBottomViewTree(bottomView, new TreeMap<Integer, Integer>(),

					new LinkedList<TreeNode>());

			System.out.println(Arrays.asList(map.values().toArray()));



			int[][] board = new int[][] {

					{

							3, 0, 6, 5, 0, 8, 4, 0, 0

					}, {

							5, 2, 0, 0, 0, 0, 0, 0, 0

					}, {

							0, 8, 7, 0, 0, 0, 0, 3, 1

					}, {

							0, 0, 3, 0, 1, 0, 0, 8, 0

					}, {

							9, 0, 0, 8, 6, 3, 0, 0, 5

					}, {

							0, 5, 0, 0, 9, 0, 6, 0, 0

					}, {

							1, 3, 0, 0, 0, 0, 2, 5, 0

					}, {

							0, 0, 0, 0, 0, 0, 0, 7, 4

					}, {

							0, 0, 5, 2, 0, 6, 3, 0, 0

					}

			};

			if (!prac.sudoku(board, 9)) {

				System.out.println("No Solution");

			}



			int[][] hamiltonianCycle= {{0, 1, 0, 1, 0}, 

                    {1, 0, 1, 1, 1}, 

                    {0, 1, 0, 0, 1}, 

                    {1, 1, 0, 0, 0}, 

                    {0, 1, 1, 0, 0}, 

                   }; 

			int[] path = new int[hamiltonianCycle.length];

			for (int i = 0; i < hamiltonianCycle.length; i++) {

				path[i] = -1;

			}

			path[0] = 0;

			if (prac.findHamiltonianCycle(hamiltonianCycle, path, 1)) {

				Arrays.toString(path);

			}

			

			TreeNode addTree = new TreeNode(50);

			addTree.left = new TreeNode(30);

			addTree.right = new TreeNode(70);

			addTree.left.left = new TreeNode(20);

			addTree.left.right = new TreeNode(40);

			addTree.right.left = new TreeNode(60);

			addTree.right.right = new TreeNode(80);



			prac.addAllValues(addTree, new Sum(0));



			int[] trap = {

					0, 1, 0, 2, 1, 0, 1, 3, 2, 1, 2, 1

			};

			prac.trappingRainWaterAr(trap);



			int[][] celebrity = {

					{

							0, 0, 1, 0

					}, {

							0, 0, 1, 0

					}, {

							0, 0, 0, 0

					}, {

							0, 0, 1, 0

					}

			};

			prac.celebrityProblem(celebrity);



			int[] bstArr = {

					1, 2, 3

			};

			TreeNode bstNode = prac.createBSTWithSortedArray(bstArr, 0, bstArr.length - 1);

			prac.printLeafNodes(bstNode);

			LinkedSet sortAbsList = new LinkedSet(0);

			sortAbsList.next = new LinkedSet(1);

			sortAbsList.next.next = new LinkedSet(-2);

			sortAbsList.next.next.next = new LinkedSet(3);

			sortAbsList.next.next.next.next = new LinkedSet(4);

			sortAbsList.next.next.next.next.next = new LinkedSet(5);

			sortAbsList.next.next.next.next.next.next = new LinkedSet(-5);

			prac.sortLinkedListWithAbsValues(sortAbsList);



			int slindingArr[] = {

					12, 1, 78, 90, 57, 89, 56

			};

			prac.SlidingWindowMaximum(slindingArr, 3);

			TreeNode serializeTree = new TreeNode(20);

			serializeTree.left = new TreeNode(8);

			serializeTree.right = new TreeNode(22);

			serializeTree.left.left = new TreeNode(4);

			serializeTree.left.right = new TreeNode(12);

			serializeTree.left.right.left = new TreeNode(10);

			serializeTree.left.right.right = new TreeNode(14);



			prac.serializeDeseralizeTree(serializeTree);



			prac.solve("bbbabcaabb");



			prac.findSubIndex("ababa", "ab");



			int[] primeSubs = {

					9, 4, 9, 1, 5

			};

			prac.solve(primeSubs);

			TreeNode sumNode = new TreeNode(10);

			sumNode.left = new TreeNode(8);

			sumNode.right = new TreeNode(2);

			sumNode.left.left = new TreeNode(3);

			sumNode.left.right = new TreeNode(5);

			sumNode.right.left = new TreeNode(2);

			

			System.out.println(prac.rootToLeafPath(sumNode, 14, 0));

  			prac.reverseSentence("i like this program very much");



			TreeNode revnode = new TreeNode(1);

			revnode.left = new TreeNode(2);

			revnode.right = new TreeNode(3);

			revnode.left.left = new TreeNode(4);

			revnode.left.right = new TreeNode(5);

			prac.reverseReverseOrderTraversal(revnode);

			

			int[] replaceElemRight = {

					16, 17, 4, 3, 5, 2

			};

			prac.replaceMaxElementOntheRight(replaceElemRight);



			LinkedSet removeList = new LinkedSet(1);

			removeList.next = new LinkedSet(2);

			removeList.next.next = new LinkedSet(3);

			removeList.next.next.next = new LinkedSet(4);

			removeList.next.next.next.next = new LinkedSet(5);

			removeList.next.next.next.next.next = new LinkedSet(6);

			removeList.next.next.next.next.next.next = new LinkedSet(7);

			removeList.next.next.next.next.next.next.next = new LinkedSet(8);

			prac.printLinkedList(prac.removeEveryKthNode(removeList, 1));

			prac.queueOperations(new Stack<Integer>());

			System.out.println(prac.rearrangeCharacters("aacbcbc"));



			prac.printAllPermutations("ABC");



			TreeNode commonNodeA = new TreeNode(5);

			commonNodeA.left = new TreeNode(1);

			commonNodeA.right = new TreeNode(10);

			commonNodeA.left.left = new TreeNode(0);

			commonNodeA.left.right = new TreeNode(4);

			commonNodeA.right.right = new TreeNode(3);

			commonNodeA.right.left = new TreeNode(7);

			commonNodeA.right.left.right = new TreeNode(9);



			TreeNode commonNodeB = new TreeNode(10);

			commonNodeB.left = new TreeNode(7);

			commonNodeB.right = new TreeNode(20);

			commonNodeB.left.left = new TreeNode(4);

			commonNodeB.left.right = new TreeNode(9);

			prac.findCommonNodes(commonNodeA, commonNodeB);



			List<Integer> jumpList = prac.jumpingNumbers(40);

			for (int i : jumpList) {

				System.out.println(i + " ");

			}

			LinkedSet nodeSwap = new LinkedSet(1);

			nodeSwap.next = new LinkedSet(2);

			nodeSwap.next.next = new LinkedSet(3);

			nodeSwap.next.next.next = new LinkedSet(4);

			nodeSwap.next.next.next.next = new LinkedSet(5);

			System.out.println(prac.swapAdjacentElements(nodeSwap));

			int[][] numpaths = {

					{

							1, 2, 3

					}, {

							4, 6, 5

					}, {

							3, 2, 1

					}

			};

			System.out.println(prac.getNumberOfPaths(numpaths, 2, 2, 12, new int[3][3][13]));

			prac.getMinimumCoinChangeProblem(3, 5);

			int ngeArr[] = {

					13, 7, 6, 12

			};

			prac.nextGreaterElement(ngeArr);



			int rotArr[][] = {

					{

							2, 1, 0, 2, 1

					}, {

							1, 0, 1, 2, 1

					}, {

							1, 0, 0, 2, 1

					}

			};

			System.out.println(prac.checkAllRottenOranges(rotArr));

			System.out.println(prac.printSquaresOfCharactersremovingK("abbccc", 4));



			LinkedSet nodeA = new LinkedSet(15);

			nodeA.next = new LinkedSet(10);

			nodeA.next.next = new LinkedSet(5);

			LinkedSet nodeB = new LinkedSet(20);

			nodeB.next = new LinkedSet(3);

			nodeB.next.next = new LinkedSet(2);

			prac.printLinkedList(prac.mergeTwoSortedLists(nodeA, nodeB));



			System.out.println(removeSpecial("abc$"));

			int arrr1[] = {

					2, 3, 7, 10, 12, 15, 30, 34

			};

			int arrr2[] = {

					1, 5, 7, 8, 10, 15, 16, 19

			};

			System.out.println(prac.findMaxSumCommonPoints(arrr1, arrr2));



			int[] altArr = {

					5, 5, 10, 40, 50, 35

			};



			System.out.println(prac.findMaxAlternateSum(altArr));



			int[] maxRotations = {

					10, 1, 2, 3, 4, 5, 6, 7, 8, 9

			};



			System.out.println(prac.maxSumRotationsar(maxRotations));



			int[] maxSumLen = {

					4, 5, 7, 1, 2, 9, 8, 4, 3, 1

			};



			System.out.println(prac.findMaxLenNonOverlappingSubArr(maxSumLen, 4));

			int[] maxProd1 = {

					1, -2, -3, 0, 7, -8, -2

			};

			System.out.println(prac.maxProductSubarray(maxProd1));

			TreeNode LCAnode = new TreeNode(26);

			LCAnode.left = new TreeNode(10);

			LCAnode.right = new TreeNode(7);

			LCAnode.left.left = new TreeNode(4);

			LCAnode.left.right = new TreeNode(6);

			LCAnode.right.right = new TreeNode(3);

			LCAnode.right.left = new TreeNode(8);



			System.out.println(prac.findLeastCommonAncestor(LCAnode, 6, 8));



			int[] minMaxArray = {

					-1, -2, -3, 4, 10

			};

			prac.maximizeArrandIndexDiff(minMaxArray);



			int[] flipSubArr = {

					0, 0, 0, 1, 0, 1

			};

			System.out.println(prac.flipSubArray(flipSubArr));

			prac.maxSubStringWithoutRepeatingChars("GEEKSFORGEEKS");



			int[] sum0Arr = {

					1, 0, 0, 1, 0, 1, 1

			};

			prac.largestArrayWithEqualZeroesOnes(sum0Arr);

			int[] stackUsingQueue = {

					1, 2, 4, 6, 10, 12, 14

			};

			Queue<Integer> queue = new LinkedList<Integer>();

			for (int b : stackUsingQueue)

				queue = prac.implementStackUsingQueueInsert(queue, b);

			LinkedSet llist = new LinkedSet(10);

			llist.next = new LinkedSet(40);

			llist.next.next = new LinkedSet(53);

			llist.next.next.next = new LinkedSet(30);

			llist.next.next.next.next = new LinkedSet(67);

			llist.next.next.next.next.next = new LinkedSet(12);

			llist.next.next.next.next.next.next = new LinkedSet(89);



			System.out.println(prac.sortLinkedListAscendingDescending(llist));



			System.out.println(prac.findNextSparseNumber(38));

			int[] floorArray = {

					1, 2, 4, 6, 10, 12, 14

			};

			System.out.println(prac.floorValueInArray(floorArray, 7));

			int[] zeroFlips = {

					1, 0, 0, 1, 1, 0, 1, 0, 1, 1

			};

			System.out.println(prac.findMaximumWindowOf1(zeroFlips, 2));

			int[] missingTwoNum = {

					4, 2, 4, 5, 2, 3, 3, 1

			};

			System.out.println(Arrays.toString(prac.findTwoMissingNumbers(missingTwoNum)));



			Integer[] minEleArr = {

					1, 1, 0, -1, -2

			};

			System.out.println(prac.findSmallestPositiveNumber(minEleArr));



			int minMaxArr[] = {

					1, 3, 50, 10, 9, 7, 6

			};

			System.out.println(prac.findElementFistIncreasingThenDecreasing(minMaxArr));



			int[] maxLen = {

					15, -2, 2, -8, 1, 7, 10, 23

			};

			System.out.println(prac.findLengthOfLargestSubArray(maxLen));

			int[] minArr = {

					8, 4, 20, 3, 10, 30, 5, 35, 40, 50

			};

			System.out.println(prac.findNextGreaterElement(minArr));

			int subArr[] = {

					15, 2, 4, 8, 9, 5, 10, 23

			};

			int[] negativeSubArr = {

					1, 4, 20, 3, 10, 5

			};

			System.out.println(prac.findNegativeSubArrayWithGivenSum(negativeSubArr, -10));

			System.out.println(prac.findPositiveSubArrayWithGivenSum(subArr, 23));



			System.out.println(prac.findMagicNumber(5));

			System.out.println(prac.findNextGreaterNumber(534976));



			int[] coins = {

					9, 6, 5, 1

			};

			System.out.println(prac.minCoinChange(coins, 11));

			int[] miniArr = {

					2, 3, 4, 5, 6, 7, 8, 1

			};

			System.out.println(prac.findMinimumElementInSortedArray(miniArr));



			int[] maxProd = {

					10, 3, 5, 6, 20

			};

			System.out.println(prac.findMaximumProductTriplet(maxProd));



			System.out.println(prac.excelNumberToWord(705));

			System.out.println(prac.findIndexWithBalancedBrackets("))"));

			System.out.println(prac.findEqualPointInBracketsString("(())))("));

    			int[] subseqArr = {

					4, 3, 2, 1

			};

			System.out.println(prac.findSortedSubSequence(subseqArr, 3));



			int peakArr[] = {

					1, 3, 20, 4, 1, 0

			};

			System.out.println(prac.findPeakElement(peakArr, 0, peakArr.length - 1));

			System.out.println(prac.extractMaxNumericValue("100klh564abc365bg"));



			TreeNode charNode = new TreeNode("+");

			charNode.left = new TreeNode("*");

			charNode.right = new TreeNode("-");

			charNode.left.left = new TreeNode("5");

			charNode.left.right = new TreeNode("4");

			charNode.right.left = new TreeNode("100");

			charNode.right.right = new TreeNode("20");

			System.out.println(prac.evaluateExpressionTree(charNode));

			

			int arr1[] = {

					1, 2, 3, 4, 7, 9

			};

			int arr2[] = {

					0, 1, 2, 1, 1, 4

			};

			prac.findNumberOfWaysOfArrayIndexLessThanIstArrayValues(arr1, arr2);



			System.out.println(prac.palindromicPartitioning("ababbbabbababa"));

			String seq = "GEEKSFORGEEKS";

			int increasingSubseq[] = new int[] {

					1, 101, 2, 3, 100, 4, 5

			};

			System.out.println(prac.maximumIncreasingSumSubSequence(increasingSubseq));

			System.out.println(prac.longestPalindromicSubsequence(seq));

			int val[] = new int[] {

					60, 100, 120

			};

			int wt[] = new int[] {

					10, 20, 30

			};

			int W = 50;

			System.out.println(prac.knapSackProblem(val, wt, W));



			int[] countArr = {

					1, 20, 6, 4, 5

			};

			System.out.println(prac.countInversion(countArr));



			System.out.println(prac.countDigitsWithSameFirstLast(5, 40));



			Point[] points = new Point[6];

			points[0] = new Point(-1, 1);

			points[1] = new Point(0, 0);

			points[2] = new Point(1, 1);

			points[3] = new Point(2, 2);

			points[4] = new Point(3, 3);

			points[5] = new Point(3, 4);

			System.out.println(prac.countMaximumPointsOnSameLine(points));

			System.out.println(prac.convertRomanToNumber("IV"));

			Integer[] zigZagAr = {

					4, 3, 7, 8, 6, 2, 1

			};

			System.out.println(Arrays.toString(prac.convertToZigZag(zigZagAr)));

			System.out.println(prac.knightTourProblem(8));

			System.out.println(prac.circularRobot("GLGLGLG"));



			int[] dupElementsK = {

					1, 2, 3, 4, 4

			};

			System.out.println(prac.duplicateElementsDistanceK(dupElementsK, 3));



			System.out.println(prac.balancedParanthesis("[(])"));

			Graph g = new Graph(4);



			g.addEdge(0, 1);

			g.addEdge(0, 2);

			g.addEdge(1, 2);

			g.addEdge(2, 0);

			g.addEdge(2, 3);

			g.addEdge(3, 3);

			prac.BFS(g, 2);



			int[] prodArr = {

					10, 3, 5, 6, 2

			};

			System.out.println(Arrays.toString(prac.productOfArray(prodArr)));

			prac.printAllPermutations("abc".toCharArray(), 0, 2);

			System.out.println(prac.countTilePlacing(4));

			int[] rotated = {

					3, 4, 5, 1, 2

			};

			System.out.println(prac.findArrayType(rotated));

			System.out.println(prac.findSquareRoot(4));



			int[] rearrange = {

					-1, 2, -3, 4, 5, 6, -7, 8, 9

			};

			System.out.println(Arrays.toString(prac.reverseAnArrayByPos(rearrange, 4)));

			prac.rearrangePositiveNegative(rearrange);

			prac.implementQueueWithLinkedList();



			System.out.println(prac.findFirstOne(18));

			TreeNode node11 = new TreeNode(10);

			node11.left = new TreeNode(8);

			node11.left.left = new TreeNode(3);

			node11.left.right = new TreeNode(5);

			node11.right = new TreeNode(2);

			node11.right.left = new TreeNode(2);

			LinkedSet leafNode = null;

			leafNode = prac.extractLeavesTree(node11, leafNode);



			prac.root = prac.traverseBT(node11);



			prac.levelOrderTraversal(node11);

			List<Integer> listNodes = new ArrayList<Integer>();

			prac.findAllNonLeaf(node11, listNodes);

			listNodes = new ArrayList<Integer>();

			listNodes.add(node11.val);

			prac.findAllNonSibling(node11, listNodes);

			listNodes = new ArrayList<Integer>();

			List<List<Integer>> finalList = new ArrayList<List<Integer>>();

			prac.findAllLeafPaths(node11, finalList, listNodes);

			

			

			System.out.println(prac.findtwoPrimeNumbers(9990));



			int[] triangles = {

					10, 21, 22, 100, 101, 200, 300

			};

			System.out.println(prac.findNumberOfTriangles(triangles));



			int[] fourSum = {

					1, 5, 1, 0, 6, 0

			};

			System.out.println(prac.findSumOfFourElementsExits(fourSum, 7));

			int[] occurence = {

					1, 3, 5, 5, 5, 5, 7, 123, 125

			};

			System.out.println(prac.findFistLastOccurence(occurence, 7));



			int[] fillArr = {

					0, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 1, 0

			};

			System.out.println(prac.fillArrayWith1(fillArr));

			int[] equilibirumAr = {

					-7, 1, 5, 2, -4, 3, 0

			};

			System.out.println(prac.findEquilibiriumIndex(equilibirumAr));

			int[] countAr = {

					1, 1, 2, 2, 2, 2, 3

			};

			System.out.println(prac.countAllPossiblePaths(3, 3));

			System.out.println(prac.countNoOfOccurences(countAr, 2));

			System.out.println(prac.countDDigitNumbersWith0(4));

			System.out.println(prac.countNumberOfDigitsFlipped(10, 20));

			System.out.println(prac.checkIfNoExpressedXPowY(27));



			TreeNode node1 = new TreeNode(26);

			node1.left = new TreeNode(10);

			node1.right = new TreeNode(3);

			node1.left.left = new TreeNode(4);

			node1.left.right = new TreeNode(6);

			node1.right.right = new TreeNode(3);

			

			TreeNode node2 = new TreeNode(26);

			node2.left = new TreeNode(3);

			node2.right = new TreeNode(10);

			node2.left.left = new TreeNode(3);

			node2.right.left = new TreeNode(5);

			node2.right.right = new TreeNode(4);



          System.out.println(prac.checkIfMirrorTree(node1, node2));

          prac.sumTree(node11);



          System.out.println(prac.validateSumTree(node1));

        System.out.println(prac.checkIfAllBitsSet(5));

        System.out.println(prac.buildLowestNumber(4325043, 3));

        System.out.println(prac.checkIfStringRotated("geeks", "eksle"));

        Integer[] smallArr = {

            1, 3, 0, 2, 5

        };

        System.out.println(prac.checkNearestElements(smallArr));

        smallArr = new Integer[] {

            0, 20, 9, 40

        };

        System.out.println(prac.pairWithGivenProduct(smallArr, 0));



        Integer[] array = {

            1, 2, 3, 4, 5

        };

        int[][] booleanArray = {

            {

                1, 0

            }, {

                0, 0

            }

        };

        System.out.println(prac.rotateArray(array, 2));

        prac.printMatrix(prac.booleanMatrix(booleanArray));



        System.out.println(prac.firstNegativeInteger(array, 2));

        System.out.println(prac.replace0with5(10120));





        prac.findSumOfFactorials(array, 1);

        List<Interval> intervals = new ArrayList<Interval>();

        intervals.add(new Interval(6, 8));

        intervals.add(new Interval(1, 9));

        intervals.add(new Interval(2, 4));

        intervals.add(new Interval(4, 7));

        prac.mergeOverlappingIntervals(intervals);

        int[] ar={-2,-3,4,-1,-2,1,5,-3};

        prac.largestSumContigousArray(ar);

        prac.printPattern(11);

        System.out.println(prac.encodeHoffMan("abcdffe"));

        int[] a4 = {

            1, 11, 2, 10, 4, 5, 2, 1

        };



        int[][] islands = {

            {

                1, 1, 0, 0, 0

            }, {

                0, 1, 0, 0, 1

            }, {

                1, 0, 0, 1, 1

            }, {

                0, 0, 0, 0, 0

            }, {

                1, 0, 1, 0, 1

            }

        };

        System.out.println(prac.countNoOfIslands(islands));

        List<String> list = new ArrayList<String>();

        list.add("abc");

        list.add("abc");

        list.add("abc");

        list.add("cde");

        list.add("cde");

        list.add("cde");

        list.add("cde");

        list.add("def");

        list.add("def");

        list.add("fgh");

        prac.kFrequentlyUsedWords(list, 3);

        prac.longestCommonSubsequence("AGGTAB", "GXTXAYB");

        prac.lengthOfLongestSubsequence(a4);

        System.out.println(prac.getMaximumAngle("12:30"));

        System.out.println(prac.findAdjacentElements(a4, 4));

        System.out.println(prac.countNoOfSteps(2));

        System.out.println(prac.findPossibleWays("(1 1)(3 3)"));

        System.out.println(prac.runLengthCoding("aaaaabccc"));

        LinkedSet link = null;

        /*

         * new LinkedSet(5); link.insert(link); link.insert(new LinkedSet(6)); link.insert(new LinkedSet(3));

         * link.insert(new LinkedSet(8));

         */



        LinkedSet link1 = new LinkedSet(8);

        link1.insert(link1);

        link1.insert(new LinkedSet(4));

        link1.insert(new LinkedSet(2));

        link1.insert(new LinkedSet(9));

        link1.insert(new LinkedSet(7));



        TreeNode node111 = new TreeNode(1);

        node111.left = new TreeNode(2);

        node111.right = new TreeNode(3);

        node111.left.left = new TreeNode(4);

        node111.left.right = new TreeNode(5);



        TreeNode root1 = new TreeNode(20);

        root1.left = new TreeNode(8);

        root1.right = new TreeNode(22);

        root1.left.left = new TreeNode(4);

        root1.left.right = new TreeNode(12);

        root1.left.right.left = new TreeNode(10);

        root1.left.right.right = new TreeNode(14);

        root1.right.right = new TreeNode(25);

        /*

         * node.right.left = new TreeNode(6); node.right.right = new TreeNode(7); node.right.right.left = new

         * TreeNode(8);

         */

        prac.printAllBoundaryNodes(root1);

        prac.getMaximumParentSum(node111);

        prac.printRightViewTree(root);

        List ans = new ArrayList();

        prac.findDiamterOfTree(node111, ans);

        System.out.println(ans.get(0));

        prac.printLinkedList(prac.addingTwoLinkedList(link, link1));

        prac.printLinkedList(prac.sumOfLinkLists(link, link1));





        prac.printLinkedList(link != null ? link.head : link);

        prac.pairSumCountLinkList(link != null ? link.head : link, 10);

        // prac.rotateLinkedList(link.head, 4);

        int[] ar12 = {

            5, 1, 3, 2, 8

        };

        prac.removeWhiteSpace("A  A   Williams");

        prac.orderLinkedListArray(link != null ? link.head : link, ar12);





        System.out.println(prac.handlePostfixNotation("2 3 1 * + 9 -"));

        System.out.println(prac.convertPostfixtoInfix("a b * c +"));

        System.out.println(Arrays.toString(prac.allAnagrams("abc").toArray()));

        Integer[] ar1={0,1,0,2,2,1,1,0,1,2,1,0};

        System.out.println(Arrays.toString(prac.segregate012(ar1)));

        int[] ar2 = {

            2, 0, 2

        };

        System.out.println(prac.trappingRainWater(ar2));

        List<Point> tuppleList = new ArrayList<Point>();

        tuppleList.add(new Point(-2, 4));

        tuppleList.add(new Point(0, -2));

        tuppleList.add(new Point(-1, 0));

        tuppleList.add(new Point(0, 0));

        tuppleList.add(new Point(-2, -3));

        tuppleList.add(new Point(3, 2));

        tuppleList = prac.kClosestTuples(tuppleList, 2);

        for (Point p : tuppleList) {

          System.out.println("(" + p.x + "," + p.y + ")");

        }

        int M[][] = {

            {

                0, 0, 1, 1, 1

            }, {

                1, 1, 1, 1, 1

            }, {

                0, 1, 1, 1, 1

            }, {

                0, 1, 1, 1, 1

            }, {

                1, 1, 1, 1, 1

            }

        };

        prac.printMatrixInSpiral(M);

        prac.printMatrix(prac.rotateMatrixAnticlockWise(M));

        prac.printMatrix(prac.rotateMatrixClockWise(M));

        System.out.println(prac.getMaximumMatrixSize(M));

        System.out.println(prac.validateParanthesis("(v)())()"));

        Stack<String> st = prac.nQueenProblem(8);

        while (!st.isEmpty()) {

          System.out.println(st.pop());

        }

        int[] ar3 = {

            1, 6, 3, 4, 5

        };

        System.out.println(prac.findMaxima(ar3));

        list = prac.chunkedPalindrome("geeksforgeeks");

        for (String s : list) {

          System.out.println(s);

        }

      } catch (Exception e) {

        // TODO Auto-generated catch block

        e.printStackTrace();

      }

    }
    
    	public void printLinkedList(LinkedSet temp) {

		while (temp != null) {

			System.out.print(temp.val + "-->");

			temp = temp.next;

		}

		System.out.println("null");

	}



	public String runLengthCoding(final String s) {

		Map<Character, Integer> map = new LinkedHashMap<Character, Integer>();

		int c = 0;

		String finalString = "";

		for (int i = 0; i < s.length(); i++) {

			if (s.charAt(i) != ' ') {

				if (map.get(s.charAt(i)) == null) {

					map.put(s.charAt(i), 1);

				}

				else {

					c = map.get(s.charAt(i));

					map.put(s.charAt(i), c + 1);

				}

			}

		}

		Iterator<Entry<Character, Integer>> it = map.entrySet().iterator();

		while (it.hasNext()) {

			Entry<Character, Integer> entry = it.next();

			finalString = finalString + entry.getKey() + entry.getValue();

		}

		return finalString;

	}



	public void pairSumCountLinkList(LinkedSet linkSet, final int sum) {

		if (linkSet == null)

			return;

		Set<Integer> set = new HashSet<Integer>();

		while (linkSet.next != null) {

			set.add(linkSet.val);

			linkSet = linkSet.next;

			if (set.contains(sum - linkSet.val)) {

				System.out.println(linkSet.val + " + " + (sum - linkSet.val));

			}

		}

	}



	public void rotateLinkedList(LinkedSet linkedSet, final int n) {

		int count = 0;

		LinkedSet temp = linkedSet.head;

		LinkedSet curr = null;

		while (linkedSet.next != null) {

			++count;

			if (count == n) {

				curr = linkedSet;

			}

			linkedSet = linkedSet.next;

		}

		if (n < 0 || count < n) {

			System.out.println("Please provide valid value to rotate");

		}

		linkedSet.next = temp;

		temp.prev = linkedSet;

		curr.prev.next = null;

		curr.prev = null;

		linkedSet.head = curr;

		this.printLinkedList(linkedSet.head);

	}

	public void orderLinkedListArray(LinkedSet linkedSet, final int[] ar) {

		Map<Integer, Integer> map = new HashMap<Integer, Integer>();

		LinkedSet newSet = null;

		int count = 0;

		while (linkedSet != null) {

			if (map.get(linkedSet.val) == null)

				map.put(linkedSet.val, 1);

			else {

				count = map.get(linkedSet.val);

				map.put(linkedSet.val, ++count);

			}

			linkedSet = linkedSet.next;

		}



		for (int i = 0; i < ar.length; i++) {

			if (map.get(ar[i]) != null) {

				count = map.get(ar[i]);

				while (count != 0) {



					newSet = new LinkedSet(ar[i]);

					newSet.insert(newSet);

					if (i == 0)

						newSet.head = newSet;

					count--;

				}

			}

		}

		this.printLinkedList(newSet != null ? newSet.head : newSet);

	}



	public void removeWhiteSpace(final String s) {

		String newS = s.trim().replaceAll("\\s+", " ");

		System.out.println(newS);

	}



	public LinkedSet sumOfLinkLists(final LinkedSet linkSet1, final LinkedSet linkSet2) {

		int l1 = this.lengthOfLinkedSet(linkSet1);

		int l2 = this.lengthOfLinkedSet(linkSet2);

		LinkedSet linkedSet = null, head = null;

		LinkedSet temp = null;

		int sum = 0, carry = 0;

		LinkedSet temp1 = this.reverseLinkList(linkSet1), temp2 = this.reverseLinkList(linkSet2);

		if (l2 > l1) {

			temp = temp1;

			temp1 = temp2;

			temp2 = temp;

			temp = null;

		}

		while (temp1 != null && temp2 != null) {

			sum = temp1.val + temp2.val + carry;

			carry = sum >= 10 ? 1 : 0;

			sum = (sum >= 10 ? (sum % 10) : sum);

			temp = new LinkedSet(sum);

			if (head == null) {

				linkedSet = temp;

				head = temp;

			} else {

				linkedSet.next = temp;

				linkedSet = linkedSet.next;

			}

			temp1 = temp1.next;

			temp2 = temp2.next;

		}

		while (temp1 != null) {

			sum = temp1.val + carry;

			carry = sum > 10 ? 1 : 0;

			sum = (sum > 10 ? (sum % 10) : sum);

			temp = new LinkedSet(sum);

			if (head == null) {

				head = temp;

				linkedSet = temp;

			} else {

				linkedSet.next = temp;

				linkedSet = temp;

			}

			temp1 = temp1.next;

		}

		if (carry == 1) {

			temp = new LinkedSet(carry);

			linkedSet.next = temp;

		}

		return this.reverseLinkList(head);

	}



	public int lengthOfLinkedSet(LinkedSet linkedSet){

		int count=0;

		while(linkedSet!=null){

			count++;

			linkedSet = linkedSet.next;

		}

		return count;

	}



	public LinkedSet reverseLinkList(LinkedSet linkedSet) {
	
		LinkedSet prev = null;

		LinkedSet curr = linkedSet;

		while (linkedSet != null) {

			linkedSet = linkedSet.next;

			curr.next = prev;

			prev = curr;

			curr = linkedSet;
	
		}

		return prev;

	}

	public int handlePostfixNotation(final String s) throws Exception

	{

		String[] tokens = s.split(" ");

		Stack<Integer> postFixStack=new Stack<Integer>();

		int len=tokens.length;

		if(ArrayUtils.removeElement(tokens, " ").length<len){

			throw new Exception();

		}

		for(int i=0;i<tokens.length;i++){

			if(i<=1 && (tokens[i]=="+" || tokens[i]=="-" ||tokens[i]=="*" ||tokens[i]=="-"))

			{

				throw new Exception();

			}

			else if(tokens[i].charAt(0)>=48 && tokens[i].charAt(0)<=57){

				postFixStack.push(Integer.parseInt(tokens[i]));

			}

			else {

				int num1=postFixStack.pop();

				int num2=postFixStack.pop();

				postFixStack.push(this.evaluateExpression(num2,num1,tokens[i]));

				}

		}

		if (postFixStack.size() == 1)

			return postFixStack.pop();

		else

			throw new Exception();

	}



	public int evaluateExpression(final int num1, final int num2, final String token) throws Exception {

		switch (token) {

			case "+":

				return num1 + num2;

			case "-":

				return num1 - num2;

			case "*":

				return num1 * num2;

			case "/":

				return num1 / num2;

			default:

				throw new Exception();

		}

	}



	public Integer[] segregate012(final Integer[] ar) {

		int low = 0;

		int mid = 0;

		int high = ar.length - 1;

		while (mid <= high) {

			switch (ar[mid]) {

				case 0:

					this.swapArray(low, mid, ar);

					low++;

					mid++;

					break;

				case 1:

					mid++;

					break;

				case 2:

					this.swapArray(mid, high, ar);

					mid++;

					high--;

					break;

			}

		}

		return ar;

	}



	public void swapArray(final int low, final int high, final Integer[] ar) {

		int temp = ar[low];

		ar[low] = ar[high];

		ar[high] = temp;

	}



	public String convertPostfixtoInfix(final String s) throws Exception {

		String[] tokens = s.split(" ");

		String infix = "";

		int count = 0;

		boolean isEmpty = false;

		Stack<String> stack = new Stack<String>();

		for (int i = 0; i < tokens.length; i++) {

			if (i > 1 && (tokens[i].trim().equals("+") || tokens[i].trim().equals("-") || tokens[i].trim().equals("*") || tokens[i].trim().equals("/"))) {

				if (count == 0) {

				String num1 = stack.pop();

				String num2 = stack.pop();

					infix = "("+num2 + tokens[i] + num1+")";

					count++;

					isEmpty = stack.isEmpty();

				} else {

					String num1 = stack.pop();

					if (isEmpty)

						infix = "(" + infix + tokens[i] + num1 + ")";

					else

						infix = "(" + num1 + tokens[i] + infix + ")";

				}

			} else if (tokens[i].charAt(0) >= 48 || tokens[i].charAt(0) <= 57)

				stack.push(tokens[i]);

			else

				throw new Exception();

		}

		return infix;

	}



	public List<String> allAnagrams(final String s) {

		int low=0;

		int high=s.length()-1;

		List<String> list=new ArrayList<String>();

		this.permuteString(s, low, high, list);

		return list;

	}



	public void permuteString(String s, final int low, final int high, final List<String> list)

	{

		int i=0;

		if(low==high)

		{

			list.add(s);

		} else {

			for (i = low; i <= high; i++) {

				s = this.swap(s, i, low);

				this.permuteString(s, low + 1, high, list);

				s = this.swap(s, i, low);

			}

		}

	}



	public String swap(final String s, final int low, final int high) {

		StringBuffer st = new StringBuffer(s);

		st.setCharAt(low, s.charAt(high));

		st.setCharAt(high, s.charAt(low));

		return st.toString();

	}



	public int findPossibleWays(final String s) {

		// Assuming the input pattern is fixed

		int sourceX = Integer.parseInt(s.charAt(1) + "");

		int sourceY = Integer.parseInt(s.charAt(3) + "");

		int destX = Integer.parseInt(s.charAt(6) + "");

		int destY = Integer.parseInt(s.charAt(8) + "");

		return this.countNoOfWays(sourceX, sourceY, destX, destY);

	}



	public int countNoOfWays(final int sourceX, final int sourceY, final int destX, final int destY) {

		if (destX == sourceX && destY == sourceY)

			return 1;

		else if (destX < sourceX || destY < sourceY)

			return 0;

		else

			return this.countNoOfWays(sourceX + 1, sourceY, destX, destY)

					+ this.countNoOfWays(sourceX, sourceY + 1, destX, destY);

	}



	public int countNoOfWaysDP(final int sourceX, final int sourceY, final int destX, final int destY) {

		int[][] dp = new int[destX - sourceX + 1][destY - sourceY + 1];

		int i = 0, j = 0;

		for (i = 0; i <= dp.length; i++) {

			for (j = 0; j <= dp[0].length; j++) {

				if (i == j) {

					dp[i][j]=1;

				}

				else if(i>j){

					dp[i][j]=0;

				}

				else

					dp[i][j] = dp[i + 1][j] + dp[i][j + 1];

			}

		}

		return dp[i][j];

	}



	public int trappingRainWater(final int[] ar) {

		int[] maxArr = new int[ar.length];

		int[] minArr = new int[ar.length];

		int temp = ar[0];

		int sum = 0;

		for (int i = 0; i < ar.length; i++) {

			if (temp < ar[i])

				temp = ar[i];

			maxArr[i] = temp;

		}

		temp = ar[0];

		for (int i = ar.length - 1; i >= 0; i--) {

			if (temp < ar[i])

				temp = ar[i];

			minArr[i] = temp;

		}

		for (int i = 0; i < ar.length; i++) {

			sum = sum + (Math.min(minArr[i], maxArr[i]) - ar[i]);

		}

		return sum;



	}



	public void printRightViewTree(final TreeNode root) {

		if (root == null)

			return;

		System.out.println(root.val);

		this.printRightViewTree(root.right != null ? root.right : root.left);

	}



	public int findDiamterOfTree(final TreeNode node, final List<Integer> ans) {

		if (node == null) {

			return 0;

		}

		int lhieght = this.findDiamterOfTree(node.left, ans);

		int rHieght = this.findDiamterOfTree(node.right, ans);

		if(ans.size()>0)

		ans.set(0, Math.max(ans.get(0), lhieght + rHieght + 1));

		else

			ans.add(lhieght + rHieght + 1);

		return 1 + Math.max(lhieght, rHieght);

	}



	public List<Point> kClosestTuples(final List<Point> tuppleList, int k) {

		if (k == 0 || tuppleList == null || tuppleList.isEmpty())

			return null;

		List<Point> newList = new ArrayList<Point>();

		Map<Double, Point> pointMap = new TreeMap<Double, Point>();

		int x = Integer.MIN_VALUE;

		int y = Integer.MIN_VALUE;

		for (Point p : tuppleList) {

			x = p.x;

			y = p.y;

			Double d = Math.sqrt((x * x) + (y * y));

			pointMap.put(d, p);

		}

		Iterator<Map.Entry<Double, Point>> it = pointMap.entrySet().iterator();

		while (k > 0 && it.hasNext()) {

			Map.Entry<Double, Point> entry = it.next();

			newList.add(entry.getValue());

			k--;

		}

		return newList;

	}



	public int getMaximumMatrixSize(final int[][] ar){

		int max=Integer.MIN_VALUE;

		int newAr[][] = {

				{

						0, 0, 0, 0, 0

				}, {

						0, 0, 0, 0, 0

				}, {

						0, 0, 0, 0, 0

				}, {

						0, 0, 0, 0, 0

				}, {

						0, 0, 0, 0, 0

				}

		};

		for(int i=0;i<newAr.length;i++){

			for (int j = 0; j < newAr[i].length; j++) {

				if(i==0||j==0)

					newAr[i][j]=ar[i][j];

					else{

					newAr[i][j] = ar[i][j] + Math.min(Math.min(newAr[i - 1][j], newAr[i - 1][j - 1]), newAr[i][j - 1]);

					}

				if (max < newAr[i][j])

					max = newAr[i][j];

				this.printMatrix(newAr);

				}



			}

		return max;

		}	
		
		
  public void printMatrix(final int[][] ar) {

		for (int i = 0; i < ar.length; i++) {

			System.out.println("\n");

			for (int j = 0; j < ar[i].length; j++) {

				System.out.print(ar[i][j] + " ");

			}

		}

		System.out.println("\n");

	}



	public boolean validateParanthesis(final String s) {

		Stack<Character> st = new Stack<Character>();

		for (int i = 0; i < s.length(); i++) {

			if (s.charAt(i) == '(' || s.charAt(i) == '{' || s.charAt(i) == '[') {

				st.push(s.charAt(i));

			} else if (!st.isEmpty() && ((s.charAt(i) == '}' && st.peek() == '{')

					|| (s.charAt(i) == ')' && st.peek() == '(') || (s.charAt(i) == ']' && st.peek() == '['))) {

				st.pop();

			}

			else if(s.charAt(i) == '}' || s.charAt(i) == ')' || s.charAt(i) == ']')

				return false;

		}

		return st.isEmpty();

	}



	public Stack<String> nQueenProblem(final int n) {

		Stack<String> positions = new Stack<String>();

		this.placeQueen(0, positions, n);

		return positions;

	}



	public boolean placeQueen(final int column, final Stack<String> positions, final int n) {

		if (column >= n)

			return true;

		int row = 0;

		while (row < n) {

			positions.add(row + "," + column);

			if (this.isSafe(row, column, positions, n) && this.placeQueen(column + 1, positions, n)) {

				return true;

			}

			positions.pop();

			row++;

		}

		return false;

	}



	public boolean isSafe(final int row, final int col, final Stack<String> positions, final int n) {

		for (String st : positions) {

			int addedRow = Integer.parseInt(st.split(",")[0]);

			int addedCol = Integer.parseInt(st.split(",")[1]);

			if (row == addedRow && col == addedCol) {

				continue;

			}

			if ((Math.abs(row - addedRow) == Math.abs(col - addedCol)) || row == addedRow || col == addedCol) {

				return false;

			}

		}

		return true;

	}



	public List<String> chunkedPalindrome(final String st) {

		int i = 0;

		int j = st.length() - 1;

		String s = "";

		String comb = "";

		List<String> list = new ArrayList<String>();

		while (i <= j) {

			s = s + st.charAt(i);

			comb = st.charAt(j) + comb;

			if (i == j)

				break;

			if (s.equals(comb)) {

				list.add(comb);

				s = "";

				comb = "";

			}

			i++;

			j--;

		}

		if (comb.length() > 0 && s.length() > 0)

			if (i == j)

			list.add(s.substring(0, s.length() - 1) + comb);

			else

				list.add(s + comb);

		return list;

	}



	public int findMaxima(final int[] ar) {

		int begin = 0;

		int last = ar.length - 1;

		int mid = 0;

		while (begin <= last) {

			if (ar[begin] <= ar[last])

				return ar[begin];

			mid = (begin + last) / 2;

			if (ar[mid] > ar[mid + 1] && ar[mid] > ar[mid - 1])

				return ar[mid];

			else if (ar[mid] >= ar[begin]) {

				begin = mid + 1;

			} else if (ar[mid] <= ar[last])

				last = mid - 1;

		}

		return -1;

	}



	public int countNoOfSteps(final int n) {

		int[] steps = new int[n + 1];

		steps[0] = 1;

		steps[1] = 1;

		for (int i = 2; i <= n; i++) {

			steps[i] = steps[i - 1] + steps[i - 2];

		}

		return steps[n];

	}



	public int findAdjacentElements(final int[] a, final int x) {

		int diff = 0;

		int i = 0;

		while (i < a.length) {

			if (a[i] == x)

				return i + 1;

			diff = Math.abs(a[i] - x);

			i = i + diff;

		}

		return -1;

	}	
	
	public int getMaximumAngle(final String s) {

		String[] split = s.split(":");

		int hours = Integer.parseInt(split[0]);

		int minutes = Integer.parseInt(split[1]);



		int degreeInMinutes = 6 * minutes;

		int degreeinHours = (int)((60 * hours + minutes) * (0.5));

		int degree = Math.abs(degreeinHours - degreeInMinutes);



		return Math.max(360 - degree, degree);



	}



	public TreeNode getMaximumParentSum(final TreeNode root) {

		if (root == null)

			return null;

		if (root.left != null && root.right != null)

			root.val = root.left.val + root.right.val;

		else if (root.left != null)

			root.val = root.left.val;

		else if (root.right != null)

			root.val = root.right.val;

		this.getMaximumParentSum(root.left);

		this.getMaximumParentSum(root.right);

		return root;



	}



	public int[][] rotateMatrixAnticlockWise(final int[][] mat) {

		System.out.println("Print Matrix AntiClockWise");

		int rows = mat.length;

		int cols = mat[0].length;

		int[][] transpMat = this.findTransposeMatrix(mat);



		for (int i = rows - 1; rows - 1 - i <= i; i--) {

			for (int j = 0; j < cols; j++) {

				int temp = transpMat[i][j];

				transpMat[i][j] = transpMat[rows - 1 - i][j];

				transpMat[rows - 1 - i][j] = temp;

			}

		}

		return transpMat;

	}

	/*

	 * 1 2 3 4 5 6 7 8 2 3 6 7 8 7 4 3 4 8 7 3 3 7 6 4 2 6 3 7 1 5 2 8

	 */



	public int[][] rotateMatrixClockWise(final int[][] mat) {

		System.out.println("Print Matrix ClockWise");

		int rows = mat.length;

		int cols = mat[0].length;

		int[][] transpMat = this.findTransposeMatrix(mat);



		for (int i = 0; i < rows; i++) {

			for (int j = cols - 1; cols - 1 - j <= j; j--) {

				int temp = transpMat[i][j];

				transpMat[i][j] = transpMat[i][cols - 1 - j];

				transpMat[i][cols - 1 - j] = temp;

			}

		}

		this.printMatrix(transpMat);

		return transpMat;

	}



	public int[][] findTransposeMatrix(final int[][] mat) {

		this.printMatrix(mat);

		int rows = mat.length;

		int cols = mat[0].length;

		for (int i = 0; i < rows; i++) {

			for (int j = i; j < cols; j++) {

				int temp = mat[i][j];

				mat[i][j] = mat[j][i];

				mat[j][i] = temp;

			}

		}

		this.printMatrix(mat);

		return mat;

	}



	public void printMatrixInSpiral(final int[][] mat) {

		this.printMatrix(mat);

		int left=0;

		int right = mat[0].length - 1;

		int top=0;

		int bottom = mat.length - 1;

		int dir = 0;

		while (top <= bottom && left <= right) {

			if (dir == 0) {

				System.out.println("------------------------------");

				for (int i = left; i <= right; i++) {

					System.out.print(mat[top][i] + " ");

				}

				dir++;

				top++;

			}

			else if (dir == 1) {

				System.out.println("------------------------------");

				for (int i = top; i <= bottom; i++) {

					System.out.print(mat[i][right] + " ");

				}

				dir++;

				right--;

			} else if (dir == 2) {

				System.out.println("------------------------------");

				for (int i = right; i >= left; i--) {

					System.out.print(mat[bottom][i] + " ");

				}

				dir++;

				bottom--;

			} else if (dir == 3) {

				System.out.println("------------------------------");

				for (int i = bottom; i >= top; i--) {

					System.out.print(mat[i][left] + " ");

				}

				dir = 0;

				left++;

			}

		}

	}



	public int lengthOfLongestSubsequence(final int a[]) {

		if (a.length <= 1) {

			return 1;

		}

		int max = 0;

		int maxDec = 0;

		int[] incSub = new int[a.length];

		int[] decSub = new int[a.length];

		for (int i = 0; i < a.length; i++) {

			incSub[i] = 1;

			decSub[i] = 1;

		}

		for (int i = 1; i < a.length; i++) {

			for (int j = 0; j < i; j++) {

				if (a[i] > a[j] && incSub[i] < incSub[j] + 1) {

					incSub[i] = incSub[j] + 1;

				}

			}

			maxDec = this.longestDecreasingSubsequence(a, i + 1);

			max = Math.max(max, maxDec + incSub[i]);

		}

		

		/*

		 * for (int i = 1; i < a.length; i++) { for (int j = 0; j < i; j++) { if (a[i] < a[j] && decSub[i] < decSub[j] +

		 * 1) { decSub[i] = decSub[j] + 1; } } }

		 */



		/*

		 * for (int i = 0; i < a.length - 1; i++) { if (maxDec < decSub[i]) maxDec = decSub[i]; max = Math.max(max,

		 * incSub[i] + decSub[a.length - 1 - i] - maxDec + 1); }

		 */

		return max;

	}



	public int longestIncreasingSubsequence(final int[] a) {

		if (a.length <= 1) {

			return 1;

		}

		int max = 0;

		int[] incSub = new int[a.length];

		for (int i = 0; i < a.length; i++) {

			incSub[i] = 1;

		}

		for (int i = 1; i < a.length; i++) {

			for (int j = 0; j < i; j++) {

				if (a[i] > a[j] && incSub[i] < incSub[j] + 1) {

					incSub[i] = incSub[j] + 1;

				}

			}

		}

		for (int i = 0; i < a.length - 1; i++) {

			max = Math.max(max, incSub[i]);

		}

		return max;

	}

	public int longestDecreasingSubsequence(final int[] a, final int k) {

		if (a.length <= 1) {

			return 1;

		}

		int max = 0;

		int[] decSub = new int[a.length];

		for (int i = 0; i < a.length; i++) {

			decSub[i] = 1;

		}

		for (int i = k; i < a.length; i++) {

			for (int j = k - 1; j < i; j++) {

				if (a[i] < a[j] && decSub[i] < decSub[j] + 1) {

					decSub[i] = decSub[j] + 1;

				}

			}

		}

		for (int i = k; i < a.length - 1; i++) {

			max = Math.max(max, decSub[i]);

		}

		return max;

	}



	public int longestCommonSubsequence(final String s1, final String s2) {

		int[][] sequence = new int[s1.length() + 1][s2.length() + 1];

		for (int i = 0; i <= s1.length(); i++) {

			for (int j = 0; j <= s2.length(); j++) {

				if (i == 0 || j == 0)

					sequence[i][j] = 0;

				else if (s1.charAt(i - 1) == s2.charAt(j - 1))

				sequence[i][j]=1+sequence[i-1][j-1];

			else

					sequence[i][j] = Math.max(sequence[i - 1][j], sequence[i][j - 1]);

		}

	}

		return sequence[s1.length()][s2.length()];

	}



	class Pair

	{

		String num;

		int count;



		public Pair(final String num, final int count) {

			this.num = num;

			this.count = count;

		 }



	}



	public List<String> kFrequentlyUsedWords(final List<String> st, final int k) {

		Map<String,Integer> map=new HashMap<String,Integer>();

		for(String s:st){

			if(map.containsKey(s)){

				map.put(s, map.get(s)+1);

			}

			else{

				map.put(s, 1);

			}

		}

		

		PriorityQueue<Pair> pq = new PriorityQueue<Pair>(k, new Comparator<Pair>() {

			@Override

			public int compare(final Pair a,final Pair b){

				return a.count-b.count;

			}

		});



		for (String s : map.keySet()) {

			Pair p = new Pair(s, map.get(s));

			pq.add(p);

			if (pq.size() > k)

				pq.poll();

		}



		List<String> list = new ArrayList<String>();

		for (Pair p : pq) {

			list.add(p.num);

		}



		Collections.reverse(list);

		return list;

	}



	public String encodeHoffMan(final String st) {

		Map<Character, Integer> map = new HashMap<Character, Integer>();

		for (int i = 0; i < st.length(); i++) {

			if(map.containsKey(st.charAt(i))){

				map.put(st.charAt(i), map.get(st.charAt(i)) + 1);

			}

			else{

				map.put(st.charAt(i), 1);

			}

		}

		Stack<TreeNode> stack = new Stack<TreeNode>();

		for (Character c : map.keySet()) {

			stack.add(new TreeNode(c, map.get(c), null, null));

		}

		Collections.sort(stack);

		while (stack.size() != 1) {

			TreeNode left = stack.pop();

			TreeNode right = stack.pop();

			TreeNode newNode = new TreeNode('\0', left.val + right.val, left, right);

			stack.push(newNode);

			Collections.sort(stack);

		}

		Map<Character, String> lookupTable = new HashMap<Character, String>();

		TreeNode node = stack.pop();

		this.generateCode(node, "", lookupTable);

		String s = "";

		for (Character c : lookupTable.keySet()) {

			s = s + lookupTable.get(c);

		}

		return s;

	}



	public void generateCode(final TreeNode node, final String st,

			final Map<Character, String> lookupTable) {

		if (node.left == null && node.right == null) {

			lookupTable.put(node.value, st);

		}

		else {

			this.generateCode(node.left, st + "0", lookupTable);

			this.generateCode(node.right, st + "1", lookupTable);

		}

	}



	public int countNoOfIslands(final int[][] ar) {

		int rows = ar.length;

		int cols = ar[0].length;

		int count = 0;

		boolean[][] visited = new boolean[rows][cols];

		for (int i = 0; i < rows; i++) {

			for (int j = 0; j < cols; j++) {

				if (ar[i][j] == 1 && !visited[i][j]) {

					this.dfs(ar, i, j, visited);

					count++;

				}

			}

		}

		return count;

	}



	public void dfs(final int[][] ar, final int i, final int j, final boolean[][] visited) {

		int[] X = {

				-1, -1, -1, 0, 0, 1, 1, 1

		};

		int[] Y = {

				-1, 0, 1, -1, 1, -1, 0, 1

		};



		visited[i][j] = true;

		for (int k = 0; k < 8; k++) {

			if (this.isSafe(ar, i + X[k], j + Y[k], visited))

				this.dfs(ar, i + X[k], j + Y[k], visited);

		}

	}



	public boolean isSafe(final int[][] ar, final int i, final int j, final boolean[][] visited) {

		if (i >= 0 && j >= 0 && i < ar.length && j < ar[0].length && ar[i][j] == 1 && !visited[i][j]) {

			return true;

		}

		return false;

	}



	public void LRUCacheImplementation() {



	}



	public void set(final int key, final LinkedSet node) {

		if (this.LRUCache.containsKey(key)) {

			this.removeNode(this.LRUCache.get(key));

			this.addFirstNode(key, node);

		} else {

			this.addFirstNode(key, node);

			}

	}



	public LinkedSet getNode(final int key) {

		LinkedSet node = this.LRUCache.get(key);

		this.removeNode(node);

		this.addFirstNode(key, node);

		return this.LRUCache.get(key);

		}



	public void addFirstNode(final int key, final LinkedSet node) {

		this.head.prev = node;

		node.next = this.head;

		this.head = node;

		this.LRUCache.put(key, node);

	}



	public void removeNode(final LinkedSet node) {

		LinkedSet temp = this.head;

		int size = temp.size(temp);

		if (size == SIZE) {

			while (temp.next.next != null) {

				temp = temp.next;

			}

			LinkedSet removedNode = temp.next;

			this.LRUCache.remove(removedNode.val);

			temp.next = null;

		}

		else{

			while (temp.next != node) {

				temp = temp.next;

			}

			if (node != null) {

				temp.next = node.next;

				if (node.next != null)

					node.next.prev = temp;

			} else

				temp.next = null;

		}



	}

	public void printPattern(int count) {

		int i = 0;

		while (i < count) {

			System.out.println("\n");

			for (int j = count; j >= i + 1; j = j - 2) {

				System.out.print(j + " ");

			}

			i = i + 2;

		}

	}



	public int largestSumContigousArray(int[] a) {

		int max = Integer.MIN_VALUE;

		int sum = 0;

		for (int i = 0; i < a.length; i++) {

			sum = sum + a[i];

			max = Math.max(sum, max);

			if (sum < 0)

				sum = 0;

		}

		return max;

	}



	public void printAllBoundaryNodes(TreeNode root) {

		if (root == null)

			return;

		System.out.println(root.val);

		printLeftNodes(root.left);

		printLeafNodes(root);

		printRightNodes(root.right);

	}



	public void printLeftNodes(TreeNode root) {

		if (root == null || (root.left == null && root.right == null))

			return;

		System.out.println(root.val + ",");

		printLeftNodes(root.left);

	}



	public void printLeafNodes(TreeNode root) {

		if (root == null)

			return;

		if (root.left == null && root.right == null)

			System.out.println(root.val + ",");

		printLeafNodes(root.left);

		printLeafNodes(root.right);

	}



	public void printRightNodes(TreeNode root) {

		if (root == null || (root.left == null && root.right == null))

			return;

		printRightNodes(root.right);

		System.out.println(root.val + ",");

	}



	public Object[] mergeOverlappingIntervals(List<Interval> intervals) {

		Collections.sort(intervals, new Comparator<Interval>() {



			@Override

			public int compare(Interval interval1, Interval interval2) {

				return Integer.compare(interval1.x, interval2.x);

			}



		});

		Stack<Interval> st = new Stack<Interval>();

		for (Interval p : intervals) {

			if(!st.isEmpty()){

				Interval temp = st.peek();

				if (temp.y > p.x) {

					temp.x=Math.min(temp.x, p.x);

					temp.y=Math.max(temp.y, p.y);

					st.pop();

					st.push(temp);

				}

			}

			else

				st.push(p);

		}

		

		return st.toArray();

	}

	
	public void orderOfPeopleHieghts(int[] ar, int k) {



	}



	public int findSumOfFactorials(Integer[] ar, int k) {

		if (k == 0 || ar.length < k) {

			return -1;

		}

		Map<Integer[], Integer> map = new HashMap<Integer[], Integer>();

		Integer[] subArray = null;

		int sum = 0;

		for (int i = 0; i < ar.length; i++) {

			subArray = new Integer[k];

			sum = 0;

			for (int count = 0; count < k; count++) {

				subArray[count] = ar[i + count];

				sum = sum + (ar[i + count] % 998244353);

			}

			map.put(subArray, sum);

		}

		int gcd = 0;

		int finalSum = 0;

		for (Integer[] key : map.keySet()) {

			gcd = findGCD(key);

			finalSum = finalSum + ((gcd * map.get(key)) % 998244353);

		}

		return finalSum;

	}



	public int findGCD(Integer[] arr) {

		int result = arr[0];

		for (int i = 1; i < arr.length; i++)

			result = gcd(arr[i], result);

		return result;

	}



	public int gcd(int a, int b) {

		if (a == 0)

			return (b % 998244353);

		return gcd(b % a, a);

	}



	public Object[] firstNegativeInteger(Integer[] array, int k) {

		List<Integer> list = new ArrayList<Integer>();

		Queue<Integer> queue = new LinkedList<Integer>();

		PriorityQueue<Integer> pq = new PriorityQueue<>(k, new Comparator<Integer>() {



			@Override

			public int compare(Integer arg0, Integer arg1) {

				return Integer.compare(arg0, arg1);

			}



		});

		for (int i : array) {

			queue.add(i);

			if (queue.size() == k) {

				pq.addAll(queue);

				int temp = pq.poll();

				queue.poll();

				pq.clear();

				if(temp<0)

					list.add(temp);

				else

					list.add(0);

			}

		}

		return list.toArray();

	}



	public void djikstraAlgo(int[][] ar, int start) {



	}



	public boolean checkIfStringRotated(String str1, String str2) {

		if (str1.length() != str2.length())

			return false;

		int i = 0;

		int j = 0;

		int count = 0;

		while (i != str1.length() && j != str2.length()) {

			if (str1.charAt(i) == str2.charAt(j)) {

				i++;

				j++;

			} else {

				i++;

				count++;

			}

		}

		i = 0;

		while (i <= count) {

			if (j <= str2.length() - 1) {

				if (str1.charAt(i) == str2.charAt(j)) {

					j++;

				} else

					return false;

			}

			else if(i!=count)

				return false;

			i++;

		}

		return true;

	}



	public Integer[] checkNearestElements(Integer[] ar) {

		Stack<Integer> st = null;

		Integer[] newar = new Integer[ar.length];

		for (int i = 0; i < ar.length; i++) {

			if (i == 0)

				newar[i] = Integer.MIN_VALUE;

			else {

				st = new Stack<Integer>();

				for (int j = 0; j < i; j++) {

				if (ar[j] < ar[i]) {

					st.push(ar[j]);

				}

			}

				if (!st.isEmpty())

					newar[i] = st.pop();

				else

					newar[i] = Integer.MIN_VALUE;

			}

		}

		return newar;

	}

		public boolean pairWithGivenProduct(Integer[] ar, int x) {

		Set<Long> set = new HashSet<Long>();

		for (int i = 0; i < ar.length; i++) {

			if (ar[i] == 0) {

				set.add(Long.valueOf(0));

				continue;

			}

			long temp = x / ar[i];

			if (set.contains(temp)) {

				return true;

			}

			set.add(Long.valueOf(ar[i]));

		}

		return false;

	}



	public int replace0with5(int a) {

		int temp = a;

		StringBuffer b = new StringBuffer("");

		int digit = 0;

		while (a != 0) {

			digit = a % 10;

			if (digit == 0) {

				digit = 5;

			}

			b = b.append(digit);

			a = a / 10;

		}

		b = b.reverse();

		if (Long.valueOf(b.toString()) > Integer.MAX_VALUE) {

			return temp;

		}

		return Integer.parseInt(b.toString());

	}



	public int[][] booleanMatrix(int[][] a) {

		Set<Point> set = new HashSet<Point>();

		for (int i = 0; i < a.length; i++) {

			for (int j = 0; j < a[i].length; j++) {

				if (a[i][j] == 1) {

					set.add(new Point(i, j));

				}

			}

		}

		for (Point point : set) {

			int row = point.x;

			int col = point.y;

			for (int i = 0; i < a.length; i++) {

				a[i][col] = 1;

			}

			for (int i = 0; i < a[0].length; i++) {

				a[row][i] = 1;

			}

		}

		return a;

	}



	public Integer[] rotateArray(Integer[] a, int x) {

		int temp = 0;

		int len = a.length;

		int currindex = 0;

		int newIndex = 0;

		int newVal = a[newIndex];

		for (int i = 0; i < len; i++) {

			currindex = newIndex;

			newIndex = (currindex - (x % len) + len) % len;

			temp = a[newIndex];

			a[newIndex] = newVal;

			newVal = temp;

		}

		return a;

	}



	public int buildLowestNumber(int a, int n) {

		String s = String.valueOf(a);

		String finalVal = "";

		if (n >= s.length()) {

			return Integer.parseInt(s);

		}

		int minIndex = 0;

		int max = Integer.MAX_VALUE;

		int index = 0;

		int counter = 0;

		String temp = "";

		while (temp.length() < n) {

			max = Integer.MAX_VALUE;

			n = n - minIndex;

			temp = s.substring(minIndex == 0 ? minIndex : minIndex + 1, s.length());

			for (int i = 0; i <= n; i++) {

				if (i < temp.length() && Integer.parseInt(temp.charAt(i) + "") < max) {

					max = Integer.parseInt(temp.charAt(i) + "");

					index = i;

				}

				counter++;

			}

			minIndex = index;

			counter = index;

			finalVal = finalVal + max;

		}

		return Integer.parseInt(finalVal);

	}



	public boolean checkIfAllBitsSet(int n) {

		while (n != 0) {

			if ((n & 1) == 0) {

				return false;

			}

			n = n >> 1;

		}

		return true;

	}



	public boolean validateSumTree(TreeNode node) {

		if (node == null) {

			return true;

		}



		int sum = 0;

		if (node.left != null) {

			sum = sum + getSubtreeSum(node.left);

		}

		if (node.right != null) {

			sum = sum + getSubtreeSum(node.right);

		}

		else if(node.left==null && node.right==null)

			sum=node.val;



		if (node.val == sum && validateSumTree(node.left) && validateSumTree(node.right)) {

			return true;

		}

		return false;



	}



	public int getSubtreeSum(TreeNode node) {

		if (node == null)

			return 0;

		int sum = 0;

		sum = sum + node.val + getSubtreeSum(node.left) + getSubtreeSum(node.right);

		return sum;

	}



	public boolean checkIfNoExpressedXPowY(int n) {

		for (int i = 2; i <= Math.sqrt(n); i++) {

			int p = i;

			while (p <= n) {

				p = p * i;

				if (p == n)

					return true;

			}

		}



		return false;

	}



	public boolean checkIfMirrorTree(TreeNode node1, TreeNode node2) {

		if (node1 == null && node2 == null)

			return true;

		else if (node1 != null && node2 == null)

			return false;

		else if (node1 == null && node2 != null)

			return false;

		else if (node1.val != node2.val) {

			return false;

		}

		if (node1.val == node2.val && checkIfMirrorTree(node1.left, node2.right)

				&& checkIfMirrorTree(node1.right, node2.left)) {

			return true;

		}

		return false;

	}



	public int countDDigitNumbersWith0(int d) {

		int count = 0;

		count = (int)(Math.pow(10, d - 1) - Math.pow(9, d - 1)) * 9;

		return count;

	}



	public int countNumberOfDigitsFlipped(Integer d1, Integer d2) {

		int n=d1^d2;

		 int count = 0; 

	        while (n != 0) { 

	            count += n & 1; 

	            n >>= 1; 

	        } 

		return count;

		/*

		 * String b1 = Integer.toBinaryString(d1); String b2 = Integer.toBinaryString(d2); int i = 0; if (b2.length() >

		 * b1.length()) { String temp = b1; b1 = b2; b2 = temp; } while (b1.length() != b2.length()) { b2 = "0" + b2; }

		 * int count = 0; while (i < b2.length()) { if (b1.charAt(i) != b2.charAt(i)) { count++; } i++; } return count;

		 */

	}


		public int countNoOfOccurences(int[] ar, int x) {

		int count = 0;

		int low = 0;

		int high = ar.length - 1;

		int mid = 0;

		int f = 0;

		while (low <= high) {

			mid = (low + high) / 2;

			if (ar[mid] == x) {

				f = 1;

				break;

			}

			if (ar[mid] < x) {

				low = mid + 1;

			}

			if (ar[mid] > x) {

				high = mid - 1;

			}

		}

		if (f == 1) {

			int i = mid;

			while (i >= 0 && ar[i] == x) {

				count++;

				i--;

			}

			i = mid;

			while (i < ar.length && ar[i] == x) {

				count++;

				i++;

			}

			return count - 1;

		}

		return count;

	}



	// public int countAllCombDibBy3(Integer[] arr) {

	// int[] c = new int[] {

	// 0, 0, 0

	// };

	// for (int i = 0; i < arr.length; i++)

	// c[arr[i] % 3]++;

	// }



	public int countAllPossiblePaths(int m, int n) {

		int[][] ar = new int[m][n];

		for (int i = 0; i < m; i++) {

			for (int j = 0; j < n; j++) {

				if (i == 0 || j == 0)

					ar[i][j] = 1;

				else{

					ar[i][j]=ar[i - 1][j]+ar[i][j-1]; 

				}

			}

		}

		return ar[m-1][n-1];

	}



	public int countTripletsSmallerSum(List<Integer> arr,int sum){

		Collections.sort(arr);

		int finalSum=0;

		List<Integer> list=new ArrayList<Integer>();

		for(int i=0;i<arr.size();i++){

			finalSum=finalSum+arr.get(i);

			if(finalSum<sum && list.size()<3){

				list.add(arr.get(i));

			}

		//	else if()

		}

		return 0;

	}



	public int findEquilibiriumIndex(int[] ar) {

		int sum = 0;

		int leftSum = 0;

		for (int i = 0; i < ar.length; i++) {

			sum = sum + ar[i];

		}

		for (int i = 0; i < ar.length; i++) {

			sum = sum - ar[i];



			if (leftSum == sum)

				return i;

			leftSum = leftSum + ar[i];

		}

		return -1;

	}



	public int fillArrayWith1(int[] ar) {

		int last1Index = 0;

		int last0Index = 0;

		int len = 0;

		int flag = -1;

		while (flag != 1) {

			last1Index = 0;

			last0Index = 0;

			len++;

			flag = 1;

			for (int i = 0; i < ar.length; i++) {

				if (ar[i] == 1) {

					last1Index = i;

				}

				if (ar[i] == 0) {

					last0Index = i;

					flag = 0;

				}

				if (Math.abs(last0Index - last1Index) == 1) {

					ar[last0Index] = 1;

					last0Index = -1;

				}

			}

		}

		return len - 1;

	}



	public String findFistLastOccurence(int[] ar, int x) {

		String res = "";

		int low = 0;

		int high = ar.length - 1;

		if (ar.length <= 2) {

			for (int i = 0; i < ar.length; i++) {

				if (ar[i] == x) {

					res = res + i;

				}

			}

			return res;

		}



		while (low <= high) {

			int mid = (low + high) / 2;

			if (ar[mid] == x && x > ar[mid - 1]) {

				res = res + mid + " ";

				break;

			} else if (ar[mid] < x) {

				low = mid + 1;

			} else

				high = mid - 1;

		}

		low = 0;

		high = ar.length - 1;

		while (low <= high) {

			int mid = (low + high) / 2;

			if (ar[mid] == x && x < ar[mid + 1]) {

				res = res + mid;

				break;

			} else if (ar[mid] > x) {

				high = mid - 1;

			} else

				low = mid + 1;

		}

		return res;

	}



	public String findSumOfFourElementsExits(int ar[], int sum) {

		Map<Integer, String> map = new HashMap<Integer, String>();

		int tempSum = 0;

		for (int i = 0; i < ar.length; i++) {

			for (int j = i + 1; j < ar.length; j++) {

				tempSum = ar[i] + ar[j];

				if(map.containsKey(sum-tempSum)){

					String[] st = map.get(sum - tempSum).split(" ");

					if (Integer.parseInt(st[0]) != i && Integer.parseInt(st[1]) != j) {

						return st[0] + " " + st[1] + " " + i + " " + j;

					}

				}

				else {

					map.put(tempSum, i + " " + j);

				}

			}

		}

		return "";

	}

			public int findMinDifference(int[] ar) {

		Arrays.sort(ar);

		int diff=Integer.MAX_VALUE;

		for(int i=0;i<ar.length-1;i++){

			if(diff>Math.abs(ar[i]-ar[i+1])){

				diff = Math.abs(ar[i] - ar[i + 1]);

			}

		}

		return diff;

	}



	public int findNumberOfTriangles(int[] ar) {

		int count = 0;

		Arrays.sort(ar);

		int n=ar.length;

		for(int i=0;i<n-2;i++){

			int k=i+2;

			for(int j=i+1;j<n;j++){

				while(k<n && ar[i]+ar[j]>ar[k])

				{

					k++;

				}

				count += k - j - 1;

			}

		}



		return count;

	}



	public String findtwoPrimeNumbers(int val) {

		Map<Integer,Integer> map = new HashMap<Integer,Integer>();

		if (val <= 2) {

			return "";

		}

		for (int i = 2; i < val; i++) {

			if(isPrime(i)){

				if (map.containsKey(val - i)) {

					return map.get(val - i) + " " + i;

				}

				else{

					map.put(i, i);

				}

			}

		}

		return "";

	}



	public boolean isPrime(int val) {

		for (int i = 2; i <= Math.sqrt(val); i++) {

			if (val % i == 0)

				return false;

		}

		return true;

	}



	public List<List<Integer>> findAllLeafPaths(TreeNode node, List<List<Integer>> finalList, List<Integer> list) {

		if (node == null) {

			return finalList;

		}

		else{

		list.add(node.val);

			if (node.left == null && node.right == null) {

				finalList.add(new ArrayList<Integer>(list));

			}

		findAllLeafPaths(node.left, finalList, list);

		findAllLeafPaths(node.right, finalList, list);

			list.remove(list.size() - 1);

		return finalList;

		}

	}



	public void levelOrderTraversal(TreeNode node) {

		int hieght = hieghtOfTree(node);

		for (int i = 0; i < hieght; i++) {

			System.out.println("\n");

			System.out.println("Level " + (i + 1));

			levelOrder(node, i);

		}

	}



	public void levelOrder(TreeNode node, int level) {

		if (node == null)

			return;

		if (level == 0) {

			System.out.print(node.val + "=>");

		}

		else {

		levelOrder(node.left, level - 1);

		levelOrder(node.right, level - 1);

		}

	}



	public int hieghtOfTree(TreeNode node) {

		if (node == null)

			return 0;

		return 1 + Math.max(hieghtOfTree(node.left), hieghtOfTree(node.right));

	}



	public int findNonAdjacentSum(int[] ar) {

		int inc = ar[0];

		int exc = 0;

		int exclNew = 0;

		for (int i = 1; i < ar.length; i++) {

			exclNew = Math.max(exc, inc);

			inc = exc + ar[i];

			exc = exclNew;

		}

		return Math.max(exc, inc);

	}



	public int findFirstOne(int n) {

		int count = 1;

		int m = 1;

		while ((n & m) == 0) {

			m = m << 1;

			count++;

		}

		return count;

	}



	public List<Integer> findAllNonLeaf(TreeNode root, List<Integer> list) {

		if (root == null || (root.left == null && root.right == null))

			return list;

		list.add(root.val);

		findAllNonLeaf(root.left, list);

		findAllNonLeaf(root.right, list);

		return list;

	}

	

	public List<Integer> findAllNonSibling(TreeNode root, List<Integer> list) {

		if (root == null)

			return list;

		if (root.left != null && root.right == null)

			list.add(root.left.val);

		if ((root.left == null && root.right != null))

			list.add(root.right.val);

		findAllNonSibling(root.left, list);

		findAllNonSibling(root.right, list);

		return list;

	}



	public void implementQueueWithLinkedList() {

		LinkedSet root=enqueue(10);

		root = enqueue(20);

		root = enqueue(30);

		root = dequeue();

		root = dequeue();

	}



	public LinkedSet enqueue(int val) {

		LinkedSet node = null;

		if (this.head == null) {

			node=new LinkedSet(val);

			this.head = node;

			this.rear = node;

		}

		else

		{

			node = this.head;

			LinkedSet temp=new LinkedSet(val);

			temp.next = node;

			node.prev = temp;

			this.head = temp;

		}

		return this.head;

	}

		public LinkedSet dequeue() {

		LinkedSet node = null;

		if (this.rear == null || this.rear == this.head) {

			return null;

		} else {

			node = this.rear;

			LinkedSet temp = node.prev;

			temp.next = null;

			node.prev = null;

			this.rear = temp;

		}

		return this.head;

	}



	public void rearrangePositiveNegative(int[] ar) {

		int i = -1;

		int temp = 0;

		for (int j = 0; j < ar.length; j++) {

			if (ar[j] < 0) {

				i++;

				temp = ar[j];

				ar[j] = ar[i];

				ar[i] = temp;

			}

		}

		int pos = i + 1;

		for (int j = 0; j < pos; j += 2) {

			temp = ar[j];

			ar[j] = ar[pos];

			ar[pos] = temp;

			pos++;

		}

	}



	public int[] reverseAnArrayByPos(int[] ar, int k) {

		int temp = 0;

		for (int i = 0; i < k / 2; i++) {

			temp = ar[i];

			ar[i] = ar[k - i - 1];

			ar[k - i - 1] = temp;

		}

		return ar;

	}



	public int findSquareRoot(int x) {

		int result = 0;

		int i = 0;

		while (result <= x) {

			i++;

			result = i * i;

		}

		return i - 1;

	}



	public int countTilePlacing(int n) {

		if (n == 0)

			return 0;

		if (n == 1 || n == 2) {

			return n;

		}

		return countTilePlacing(n - 1) + countTilePlacing(n - 2);

	}



	public String findArrayType(int[] ar) {

		int i=0;

		int n=ar.length;

		while (i < n - 1 && ar[i] < ar[i + 1])

			i++;

		if(i==n-1){

			return "Ascending with Max Value "+ar[i];

		}

		

		if(i==0){

			while (i < n - 1 && ar[i] > ar[i + 1])

				i++;

			if(i==n-1){

				return "Descending with Max Value "+ar[0];

			}



			if(ar[0]<ar[i+1]){

				 return "Descending rotated with" + 

			                " maximum element = " + Math.max(ar[0], ar[i+1]); 

			}

			else{

				 return "Ascending rotated with" + 

		                " maximum element = " + Math.max(ar[0], ar[i+1]); 

			}

		}

		 if (i < n -1 && ar[0] > ar[i+1]) 

		    { 

			return "Ascending rotated with maximum element =  " + Math.max(ar[i], ar[0]);

		    } 

		  

		return "Descending rotated with maximum element =  " + Math.max(ar[i], ar[0]);

	}



	public void printAllPermutations(char[] s, int low, int high) {

		if (low == high)

			System.out.println(s);

		else {

			for (int i = low; i <= high; i++) {

				char temp = s[i];

				s[i] = s[low];

				s[low] = temp;

				printAllPermutations(s, low + 1, high);

				temp = s[i];

				s[i] = s[low];

				s[low] = temp;

			}

		}

	}



	public int[] productOfArray(int[] ar){

		int n=ar.length;

		int[] prodLeft=new int[n];

		int[] prodRight=new int[n];

		prodLeft[0]=1;

		prodRight[n-1]=1;

		for (int i = 1; i < n; i++) {

			prodLeft[i] = prodLeft[i - 1] * ar[i - 1];

		}

		for (int i = n - 2; i >= 0; i--) {

			prodRight[i] = prodRight[i + 1] * ar[i + 1];

		}

		for (int i = 0; i < n; i++) {

			ar[i] = prodLeft[i] * prodRight[i];

		}

		return ar;

	}



	public LinkedSet addingTwoLinkedList(LinkedSet l1, LinkedSet l2) {

		l1 = reverseLinkedSet(l1);

		l2 = reverseLinkedSet(l2);

		int carry = 0;

		int sum = 0;

		LinkedSet finalList = null;

		LinkedSet listHead = null;

		while (l1 != null && l2 != null) {

			sum = l1.val + l2.val + carry;

			carry = 0;

			if (sum > 9) {

				carry = sum / 10;

				sum = sum % 10;

			}

			if (finalList == null) {

				finalList = new LinkedSet(sum);

				listHead = finalList;

			} else {

				finalList.next = new LinkedSet(sum);

				finalList = finalList.next;

			}

			l1 = l1.next;

			l2 = l2.next;

		}

		while (l1 != null) {

			sum = l1.val + carry;

			carry = 0;

			if (sum > 9) {

				carry = sum / 10;

				sum = sum % 10;

			}

			if (finalList == null) {

				finalList = new LinkedSet(sum);

				listHead = finalList;

			} else {

				finalList.next = new LinkedSet(sum);

				finalList = finalList.next;

			}

			l1 = l1.next;

		}

		while (l2 != null) {

			sum = l2.val + carry;

			carry = 0;

			if (sum > 9) {

				carry = sum / 10;

				sum = sum % 10;

			}

			if (finalList == null) {

				finalList = new LinkedSet(sum);

				listHead = finalList;

			} else {

				finalList.next = new LinkedSet(sum);

				finalList = finalList.next;

			}

			l2 = l2.next;

		}

		return listHead;

	}



	public LinkedSet reverseLinkedSet(LinkedSet l) {

		LinkedSet curr = l;

		LinkedSet prev = null;

		while (l != null) {

			l = l.next;

			curr.next = prev;

			prev = curr;

			curr = l;

		}

		return prev;

	}



	public TreeNode insertBST(TreeNode root, int val) {

		if (root == null) {

			root = new TreeNode(val);

			return root;

		}

		else if (root.val > val) {

			root.left = insertBST(root.left, val);

		} else {

			root.right = insertBST(root.right, val);

		}

		return root;

	}

		public TreeNode searchBST(TreeNode root, int val) {

		if (root == null)

			return null;

		if (root.val == val) {

			return root;

		} else if (root.val > val)

			return searchBST(root.left, val);

		else {

			return searchBST(root.right, val);

		}

	}



	public TreeNode traverseBT(TreeNode root) {

		if (root == null) {

			return null;

		}

		this.root = insertBST(this.root, root.val);

		traverseBT(root.left);

		traverseBT(root.right);

		return this.root;

	}



	public void BFS(Graph g, int s) {

		boolean[] visited = new boolean[g.v];

		Queue<Integer> queue = new LinkedList<Integer>();

		queue.add(s);

		visited[s] = true;

		while (!queue.isEmpty()) {

			s = queue.poll();

			System.out.print(s + ",");

			for (Integer e : g.adj[s]) {

				if (!visited[e]) {

					visited[e] = true;

					queue.add(e);

				}

			}



		}

	}



	public boolean balancedParanthesis(String s) {

		Stack<Character> st = new Stack<Character>();

		for (int i = 0; i < s.length(); i++) {

			Character c = s.charAt(i);

			if (c == '(' || c == '{' || c == '[') {

				st.push(c);

			} else if (!st.isEmpty() && (c == ')' && st.peek() == '(') || (c == '}' && st.peek() == '{')

					|| (c == ']' && st.peek() == '[')) {

				st.pop();

			}

			else if(s.charAt(i) == '}' || s.charAt(i) == ')' || s.charAt(i) == ']')

				return false;

		}

		return st.isEmpty();

	}



	public boolean duplicateElementsDistanceK(int ar[], int k) {

		Map<Integer, Integer> map = new HashMap<Integer, Integer>();

		for (int i = 0; i < ar.length; i++) {

			if (map.containsKey(ar[i])) {

				int index = map.get(ar[i]);

				if (i - index <= k) {

					return true;

				}

			} else {

				map.put(ar[i], i);

			}

		}

		return false;

	}



	public boolean circularRobot(String s) {

		int x = 0;

		int y = 0;

		int dir = 0;

		for (int i = 0; i < s.length(); i++) {

			char move = s.charAt(i);

			if (move == 'L') {

				dir = (dir - 1 + 4) % 4;

			} else if (move == 'R') {

				dir = (dir + 1) % 4;

			} else {

				if (dir == 0) {

					y++;

				} else if (dir == 1) {

					x++;

				} else if (dir == 2) {

					y--;

				} else

					x--;

			}

		}

		return x == 0 && y == 0;

	}



	public boolean knightTourProblem(int n) {

		int[][] tour = new int[n][n];

		for (int i = 0; i < n; i++) {

			for (int j = 0; j < n; j++) {

				tour[i][j] = -1;

			}

		}

		boolean poss = checkTour(0, 0, 0, tour);

		printMatrix(tour);

		return poss;

	}



	public boolean checkTour(int x, int y, int move, int[][] tour) {

		int[] xMove = {

				2, 1, -1, -2, -2, -1, 1, 2

		};

		int[] yMove = {

				1, 2, 2, 1, -1, -2, -2, -1

		};

		int n = tour.length;

		if (move == n * n) {

			return true;

		}



		for (int i = 0; i < tour.length; i++) {

			int nextX = x + xMove[i];

			int nextY = y + yMove[i];

			if (isSafe(x, y, n, tour)) {

				tour[x][y] = move + 1;

				if (checkTour(nextX, nextY, move + 1, tour))

					return true;

				else

					tour[x][y] = -1;

			}

		}



		return false;



	}



	public boolean isSafe(int x, int y, int n, int[][] tour) {

		return x >= 0 && y >= 0 && x < n && y < n && tour[x][y] == -1;

	}



	public LinkedSet extractLeavesTree(TreeNode root, LinkedSet node) {

		if (root == null)

			return node;

		if (root.left == null && root.right == null) {

			if (node == null) {

				node = new LinkedSet(root.val);

				node.head = node;

			} else {

				LinkedSet temp = new LinkedSet(root.val);

				node.next = temp;

				temp.prev = node;

				node = temp;

			}

		}

		node = extractLeavesTree(root.left, node);

		node = extractLeavesTree(root.right, node);

		return node;

	}



	public int sumTree(TreeNode node) {

		if (node == null)

			return 0;

		int oldData = node.val;

		node.val = sumTree(node.left) + sumTree(node.right);

		return node.val + oldData;

	}

		public Integer[] convertToZigZag(Integer[] ar) {

		boolean flag = true;

		int n = ar.length;

		for (int i = 0; i < n - 2; i++) {

			if (flag) {

				if (ar[i] > ar[i + 1])

					swapArray(i, i + 1, ar);

			}

			else{

				if (ar[i] < ar[i + 1])

					swapArray(i+1, i, ar);

			}

			flag = !flag;

		}

		return ar;

	}



	public int convertRomanToNumber(String s) {

		Map<Character, Integer> map = new HashMap<Character, Integer>();

		map.put('I', 1);

		map.put('V', 5);

		map.put('X', 10);

		map.put('L', 50);

		map.put('C', 100);

		map.put('D', 500);

		map.put('M', 1000);

		int sum = 0;

		for (int i = 0; i < s.length(); i++) {

			int m = map.get(s.charAt(i));

			if(i+1<s.length()){

			int n = map.get(s.charAt(i + 1));

			

			if (m < n) {

				sum = sum + n - m;

				i++;

			} else

				sum = sum + m;

		}

		else

		{

			sum=sum+m;

				i++;

		}

	}

		return sum;

	}



	public int countMaximumPointsOnSameLine(Point[] points) {

		double slope = 0D;

		double xDiff = 0D;

		double yDiff = 0D;

		int countMax = 0;

		boolean addFlag = true;

		Map<Double, Integer> map = new HashMap<Double, Integer>();

		Map<Double, List<Point>> pointMap = new HashMap<Double, List<Point>>();

		for (int i = 0; i < points.length; i++) {

			for (int j = i + 1; j < points.length; j++) {

				addFlag = true;

				xDiff = (long)points[i].x - points[j].x;

				yDiff = (long)points[i].y - points[j].y;

				slope = yDiff / xDiff;

				if (map.get(slope) != null) {

					List<Point> list = pointMap.get(slope);

					for (Point point : list) {

						if ((point.x == points[j].x && point.y == points[j].y)) {

							addFlag = false;

							break;

						}

					}

					if (addFlag) {

					map.put(slope, map.get(slope) + 1);

						list.add(points[j]);

						pointMap.put(slope, list);

					}



				} else {

					map.put(slope, 2);

					List<Point> list = new ArrayList<Point>();

					list.add(points[i]);

					list.add(points[j]);

					pointMap.put(slope, list);

				}

				countMax = Math.max(countMax, map.get(slope));

			}

		}

		return countMax;

	}



	public int countNumberOfSteps(int n) {

		int[] count = new int[n];

		count[0] = 1;

		count[1] = 1;

		count[2] = 2;

		for (int i = 3; i <= n; i++) {

			count[i] = count[i - 3] + count[i - 2] + count[i - 1];

		}

		return count[n];

	}



	public int countDigitsWithSameFirstLast(int start, int end) {

		return countSameDigitsFrom1(end) - countSameDigitsFrom1(start - 1);

	}



	public int countSameDigitsFrom1(int x) {

		if (x < 10) {

			return x;

		}

		int res = x / 10;

		res = res + 9;

		int firstDigit = getFirstDigit(x);

		int lastDigit = x % 10;

		if (firstDigit > lastDigit) {

			res--;

		}

		return res;



	}



	public int getFirstDigit(int x) {

		while (x >= 10) {

			x = x / 10;

		}

		return x;

	}



	public int countInversion(int[] arr) {

		int[] temp = new int[arr.length];

		return mergeSort(arr, 0, arr.length - 1, temp);

	}



	public int mergeSort(int[] arr, int left, int right, int[] temp) {

		int mid = 0;

		int invCount = 0;

		if (left < right) {

			mid = (left + right) / 2;

			invCount = mergeSort(arr, left, mid, temp);

			invCount += mergeSort(arr, mid + 1, right, temp);

			invCount += merge(arr, left, mid + 1, right, temp);

		}

		return invCount;

	}



	public int merge(int[] arr, int left, int mid, int right, int[] temp) {

		int i, j, k;

		int inv_count = 0;

		i = left;

		j = mid;

		k = left;

		while (i <= mid - 1 && j <= right) {

			if (arr[i] <= arr[j]) {

				temp[k++] = arr[i++];

			} else {

				temp[k++] = arr[j++];

				inv_count = inv_count + mid - i;

			}

		}

		while (i <= mid - 1)

			temp[k++] = arr[i++];



		while (j <= right)

			temp[k++] = arr[j++];



		for (i = left; i <= right; i++)

			arr[i] = temp[i];

		return inv_count;

	}



	public void dfs(Graph g, boolean[] visited, int v) {

		visited[v] = true;

		System.out.println(v + " ");

		Iterator<Integer> it = g.adj[v].iterator();

		while (it.hasNext()) {

			int n = it.next();

			if (!visited[v])

				dfs(g, visited, n);

		}

	}

	
	public int diameterOfBinaryTree(TreeNode root) {

		if (root == null)

			return 0;

		int leftHieght = hieghtOfTree(root.left);

		int rightHieght = hieghtOfTree(root.right);

		int leftNodeDiameter = diameterOfBinaryTree(root.left);

		int righntNodeDiameter = diameterOfBinaryTree(root.right);

		return Math.max(Math.max(leftNodeDiameter, righntNodeDiameter), 1 + leftHieght + rightHieght);

	}



	public int knapSackProblem(int[] value, int[] weight, int maxWeight) {

		int[][] knapsack = new int[value.length + 1][maxWeight + 1];

		for (int i = 0; i <= value.length; i++) {

			for (int j = 0; j <= maxWeight; j++) {

				if (i == 0 || j == 0) {

					knapsack[i][j] = 0;

				} else if (weight[i - 1] <= j) {

					knapsack[i][j] = Math.max(value[i - 1] + knapsack[i - 1][j - weight[i - 1]],

							knapsack[i - 1][j]);

				}

				else{

					knapsack[i][j]=knapsack[i-1][j];

				}

			}

		}

		return knapsack[value.length][maxWeight];

	}



	public int[][] longestPalindromicSubsequence(String st) {

		int[][] subsequence = new int[st.length()][st.length()];

		for (int i = 0; i < st.length(); i++) {

			subsequence[i][i] = 1;

		}



		for (int i = 2; i <= st.length(); i++) {

			for (int j = 0; j < st.length() - i + 1; j++) {

				int k = i + j - 1;

				if (st.charAt(k) == st.charAt(j) && i == 2)

					subsequence[j][k] = 2;

				if (st.charAt(j) == st.charAt(k)) {

					subsequence[j][k] = subsequence[j + 1][k - 1] + 2;

				} else {

					subsequence[j][k] = Math.max(subsequence[j + 1][k], subsequence[j][k - 1]);

				}

			}

		}

		return subsequence;

	}



	public int longestCommonSubSequence(String s1, String s2) {

		int[][] subsequence = new int[s1.length() + 1][s2.length() + 1];

		for (int i = 0; i < s1.length(); i++) {

			subsequence[i][0] = 0;

		}

		for (int i = 0; i < s2.length(); i++) {

			subsequence[0][i] = 0;

		}



		for (int i = 0; i < s1.length(); i++) {

			for (int j = 0; j < s2.length(); j++) {

				if (s1.charAt(i - 1) == s2.charAt(j - 1)) {

					subsequence[i][j] = subsequence[i - 1][j - 1] + 1;

				} else {

					subsequence[i][j] = Math.max(subsequence[i - 1][j], subsequence[i][j - 1]);

				}

			}

		}

		return subsequence[s1.length()][s2.length()];

	}



	public int maximumIncreasingSumSubSequence(int[] ar) {

		int i = 0;

		int j = 0;

		int max = 0;

		int msis[] = new int[ar.length];

		for (i = 0; i < ar.length; i++) {

			msis[i] = ar[i];

		}



		for (i = 1; i < ar.length; i++) {

			for (j = 0; j < i; j++) {

				if (ar[i] > ar[j] && msis[i] < ar[i] + msis[j]) {

					msis[i] = ar[i] + msis[j];

				}

			}

		}

		for (i = 0; i < ar.length; i++)

			if (max < msis[i])

				max = msis[i];

		return max;

	}



	public int palindromicPartitioning(String st){

		boolean[][] palinSequence = new boolean[st.length()][st.length()];

		for (int i = 0; i < st.length(); i++) {

			palinSequence[i][i] = true;

		}

		for (int l = 2; l < st.length(); l++) {

			for (int i = 0; i < st.length() - l + 1; i++) {

				int j = i + l - 1;

				if (l == 2) {

					palinSequence[i][j] = st.charAt(i) == st.charAt(j);

				} else {

					palinSequence[i][j] = st.charAt(i) == st.charAt(j) && palinSequence[i + 1][j - 1];

				}

			}

		}

		int[] cuts=new int[st.length()];

		int temp = Integer.MAX_VALUE;

		for(int i=0;i<st.length();i++){

			if (palinSequence[0][i]) {

				cuts[i] = 0;

			} else {

				temp = Integer.MAX_VALUE;

				for (int j = 0; j < i; j++) {

					if (palinSequence[j + 1][i] && temp > cuts[j] + 1)

						temp = cuts[j] + 1;

				}

				cuts[i] = temp;

			}

		}



		return cuts[st.length() - 1];

	}


	public void findNumberOfWaysOfArrayIndexLessThanIstArrayValues(int[] arr1, int arr2[]) {

		Arrays.sort(arr2);

		for (int i = 0; i < arr1.length; i++) {

			int index = searchBinary(arr2, arr1[i]);

			System.out.println(index + 1 + " ");

		}

	}



	public int searchBinary(int[] arr, int x) {

		int low = 0;

		int high = arr.length - 1;

		while (low <= high) {

			int mid = (low + high) / 2;

			if (arr[mid] <= x) {

				low = mid + 1;

			} else {

				high = mid - 1;

			}

		}

		return high;

	}



	public int evaluateExpressionTree(TreeNode root) {

		if (root == null) {

			return 0;

		}

		if (root.left == null && root.right == null) {

			return Integer.parseInt(root.st);

		}

		int leftVal = evaluateExpressionTree(root.left);

		int rightVal = evaluateExpressionTree(root.right);

		if (root.st == "+")

			return leftVal + rightVal;

		if (root.st == "-")

			return leftVal - rightVal;

		if (root.st == "*")

			return leftVal * rightVal;

		return leftVal / rightVal;



	}



	public int extractMaxNumericValue(String st) {

		int res = 0;

		int num = 0;

		for (int i = 0; i < st.length(); i++) {

			if (Character.isDigit(st.charAt(i))) {

				num = num * 10 + (st.charAt(i) - '0');

			} else {

				res = Math.max(res, num);

				num = 0;

			}

		}

		return res;

	}



	public int findPeakElement(int[] arr, int low, int high) {

		int mid = 0;

		int n = arr.length;

		while (low <= high) {

			mid = (low + high) / 2;

			if ((mid == 0 || arr[mid - 1] < arr[mid]) && (mid == n - 1 || arr[mid] > arr[mid + 1])) {

				return arr[mid];

			} else if (mid > 0 && arr[mid] < arr[mid + 1]) {

				findPeakElement(arr, low, mid - 1);

			} else {

				findPeakElement(arr, mid + 1, high);

			}

		}

		return -1;

	}



	public int[] findSortedSubSequence(int[] arr, int size) {

		Queue<Integer> queue = new LinkedList<Integer>();

		for (int ele : arr) {

			if (!queue.isEmpty() && queue.peek() > ele) {

				if (queue.size() == size)

					queue.poll();

				queue.add(ele);

			} else

				queue.add(ele);

		}

		arr = new int[size];

		int i = 0;

		arr[0] = Integer.MIN_VALUE;

		for(int val:queue){

			if (i == 0) {

				arr[i] = val;

				i++;

			}

			else if (arr[i - 1] < val) {

				arr[i] = val;

				i++;

			}

			if (i == size)

				break;

		}

		return arr;

	}



	public int findEqualPointInBracketsString(String st) {

		Stack<Character> stack = new Stack<Character>();

		int f = 0;

		int i = 0;

		for (i = 0; i < st.length(); i++) {

			if (st.charAt(i) == '(' || st.charAt(i) == '{' || st.charAt(i) == '[') {

				stack.push(st.charAt(i));

				f = 1;

			} else if ((!stack.isEmpty()) && ((stack.peek() == '(' && st.charAt(i) == ')')

					|| (stack.peek() == '{' && st.charAt(i) == '}') || (stack.peek() == '[' && st.charAt(i) == ']'))) {

				stack.pop();

			}

			else if(st.charAt(i) == ')' || st.charAt(i) == '}' || st.charAt(i) == ']'){

				f=1;

				continue;

			}

			if (f == 1 && stack.isEmpty()) {

				return i;

			}

		}

		if (f == 1 && stack.isEmpty()) {

			return i;

		}

		return -1;

	}



	public int findIndexWithBalancedBrackets(String st) {

		int[] open = new int[st.length() + 1];

		int[] close = new int[st.length() + 1];

		close[st.length()] = 0;

		open[0] = 0;

		if (st.charAt(0) == '(') {

			open[1] = 1;

		}

		if (st.charAt(st.length() - 1) == ')') {

			close[st.length() - 1] = 1;

		}

		for (int i = 1; i < st.length(); i++) {

			if (st.charAt(i) == '(') {

				open[i + 1] = open[i] + 1;

			} else

				open[i + 1] = open[i];

		}

		for (int i = st.length() - 2; i >= 0; i--) {

			if (st.charAt(i) == ')') {

				close[i] = close[i + 1] + 1;

			} else

				close[i] = close[i + 1];

		}

		if (close[0] == 0) {

			return 0;

		}

		if (open[st.length()] == 0)

			return st.length();

		for (int i = 0; i < st.length(); i++) {

			if (open[i] == close[i]) {

				return i;

			}

		}

		return -1;

	}


	public String excelNumberToWord(int num) {

		int res = 0;

		String st = "";

		while (num > 0) {

			res = num % 26;

			if (res == 0) {

				st = "Z" + st;

				num = (num / 26) - 1;

			} else {

				st = (char)((res - 1) + 'A') + st;

				num = num / 26;

			}

		}

		return st;

	}



	public int findHieghtOfSpecialBinaryTree(TreeNode root){

		if(root==null)

			return 0;

		if(isLeaf(root)){

			return 1;

		}

		return 1 + Math.max(findHieghtOfSpecialBinaryTree(root.left), findHieghtOfSpecialBinaryTree(root.right));

	}



	public boolean isLeaf(TreeNode root) {

		return root.left != null && root.left.right == root && root.right != null && root.right.left == root;

	}



	public int findMaximumProductTriplet(int[] ar) {

		int maxA = Integer.MIN_VALUE;

		int maxB = Integer.MIN_VALUE;

		int maxC = Integer.MIN_VALUE;

		int minB = Integer.MAX_VALUE;

		int minC = Integer.MAX_VALUE;

		for (int i = 0; i < ar.length; i++) {

			if (ar[i] > maxA) {

				maxC = maxB;

				maxB = maxA;

				maxA = ar[i];

			} else if (ar[i] > maxB) {

				maxC = maxB;

				maxB = ar[i];

			} else if (minC < ar[i]) {

				maxC = ar[i];

			}

			if (minB > ar[i]) {

				minC = minB;

				minB = ar[i];

			} else if (minC > ar[i]) {

				minC = ar[i];

			}

		}

		return Math.max(maxA * maxB * maxC, maxA * minB * minC);

	}



	public int findMinimumElementInSortedArray(int[] ar) {

		int low = 0;

		int high = ar.length - 1;

		if (ar.length <= 1) {

			return 0;

		}

		while (low <= high) {

			int mid = (low + high) / 2;

			if ((mid == 0 && ar[mid] < ar[mid + 1]) || (mid == ar.length - 1 && ar[mid] < ar[mid - 1])

					|| (ar[mid] < ar[mid + 1] && ar[mid] < ar[mid - 1]))

				return mid;

			else if (ar[mid] < ar[high]) {

				high = mid - 1;

			} else

				low = mid + 1;

		}

		return -1;

	}



	public int minCoinChange(int[] ar, int val) {

		if (val == 0)

			return 0;

		int[] coins = new int[val + 1];

		coins[0] = 0;

		for (int i = 1; i <= val; i++) {

			coins[i] = Integer.MAX_VALUE;

		}



		for (int i = 1; i <= val; i++) {

			for (int j = 0; j < ar.length; j++) {

				if (ar[j] <= i) {

					int sub_res = coins[i - ar[j]];

					if (sub_res != Integer.MAX_VALUE && coins[i] > 1 + sub_res) {

						coins[i] = sub_res + 1;

					}

				}

			}

		}

		return coins[val];

	}



	public int findNextGreaterNumber(int val) {

		int len = String.valueOf(val).length();

		if (len == 1)

			return val;

		int[] arr = new int[len];

		int i = 0;

		while (val > 0) {

			int rem = val % 10;

			arr[arr.length - 1 - i] = rem;

			i++;

			val = val / 10;

		}

		for (i = arr.length - 1; i >= 0; i--) {

			if (arr[i - 1] < arr[i])

				break;

		}

		int smallerVal = i - 1;

		int indexReversed = -1;

		int diff = Integer.MAX_VALUE;

		for (int j = arr.length - 1; j > i - 1; j--) {

			if (diff > Math.abs(arr[j] - arr[smallerVal])) {

				diff = Math.abs(arr[j] - arr[smallerVal]);

				indexReversed = j;

			}

		}

		int temp = arr[smallerVal];

		arr[smallerVal] = arr[indexReversed];

		arr[indexReversed] = temp;

		int num = 0;

		for (i = 0; i <= smallerVal; i++) {

			num = num * 10 + arr[i];

		}

		int[] newArr = new int[arr.length - smallerVal - 1];

		int k = 0;

		for (i = smallerVal + 1; i < arr.length; i++) {

			newArr[k] = arr[i];

			k++;

		}

		Arrays.sort(newArr);

		for (i = 0; i < newArr.length; i++) {

			num = num * 10 + newArr[i];

		}

		return num;

	}



	public int findMagicNumber(int n) {

		int pow = 1;

		int sum = 0;

		while (n > 0) {

			pow = pow * 5;

			if ((n & 1) == 1) {

				sum = sum + pow;

			}

			n = n >> 1;

		}

		return sum;

	}	
	
	public boolean findPythagorasTriplet(int[] ar) {

		for (int i = 0; i < ar.length; i++) {

			ar[i] = ar[i] * ar[i];

		}

		Arrays.sort(ar);

		for (int i = ar.length - 1; i >= 2; i--) {

			int l = 0;

			int r = i - 1;

			while (l < r) {

				if (ar[l] + ar[r] == ar[i]) {

					return true;

				}

				if (ar[l] + ar[r] < ar[i]) {

					l++;

				} else

					r--;

			}

		}

		return false;

	}



	public boolean findPositiveSubArrayWithGivenSum(int[] ar, int sum) {

		int curr_sum = 0;

		int start = 0;

		for (int i = 0; i <= ar.length; i++) {

			while (curr_sum > sum && start < i - 1) {

				curr_sum = curr_sum - ar[start];

				start++;

			}

			if (curr_sum == sum) {

				System.out.println(start + " " + (i - 1));

				return true;

			}

			if (i < ar.length)

			curr_sum = curr_sum + ar[i];

		}

		return false;

	}



	public boolean findNegativeSubArrayWithGivenSum(int[] ar, int sum) {

		int curr_sum = 0;

		int start = 0;

		Map<Integer, Integer> map = new HashMap<Integer, Integer>();

		for (int i = 0; i < ar.length; i++) {

			curr_sum = curr_sum + ar[i];

			if (curr_sum == sum) {

				System.out.println(start + " " + (i));

				return true;

			}

			if (map.containsKey(sum - curr_sum)) {

				System.out.println(map.get(sum - curr_sum) + 1 + " " + i);

				return true;

			}

			map.put(curr_sum, i);

		}

		return false;

	}



	public int findNextGreaterElement(int[] arr) {

		int max = arr[0];

		boolean found = false;

		for (int i = 1; i < arr.length; i++) {

			if (arr[i] > max && !found) {

				max = arr[i];

				found=true;

			}

			else if(arr[i] < max){

				found=false;

			}

		}

		if (found)

			return max;

		return -1;

	}



	public int findLengthOfLargestSubArray(int[] ar) {

		int maxLen = 0;

		Map<Integer, Integer> map = new HashMap<Integer, Integer>();

		int sum = 0;

		for (int i = 0; i < ar.length; i++) {

			sum = sum + ar[i];

			if (sum == 0 && maxLen == 0)

				maxLen = 1;

			if (sum == 0)

				maxLen = i + 1;

			if (map.containsKey(sum)) {

				maxLen = Math.max(maxLen, i - map.get(sum));

			} else

				map.put(sum, i);



		}

		return maxLen;

	}



	public int findElementFistIncreasingThenDecreasing(int[] ar) {

		if (ar.length == 0)

			return -1;

		if (ar.length == 1)

			return ar[0];

		if (ar.length == 2) {

			if (ar[0] > ar[1])

				return ar[0];

			return ar[1];

		}



		int low = 0;

		int high = ar.length - 1;

		int mid = 0;

		while (low <= high) {

			mid = (low + high) / 2;

			if (mid == 0 || mid == ar.length - 1 || (ar[mid] > ar[mid + 1] && ar[mid] > ar[mid - 1])) {

				return mid;

			} else if (ar[mid] < ar[mid + 1] && ar[mid] > ar[mid - 1]) {

				low = mid + 1;

			}

			else{

				high=mid-1;

			}

		}

		return -1;

	}

		public int findSmallestPositiveNumber(Integer[] ar) {

		int size = ar.length;

		int shift=segregateArray(ar);

		int arr2[] = new int[size - shift];

		int j = 0;

		for (int i = shift; i < size; i++) {

			arr2[j] = ar[i];

			j++;

		}

		for (int i = 0; i < arr2.length; i++) {

			if (Math.abs(arr2[i]) - 1 < arr2.length && arr2[Math.abs(arr2[i]) - 1] > 0) {

				arr2[Math.abs(arr2[i]) - 1] = -1 * arr2[Math.abs(arr2[i]) - 1];

			}

		}



		for (int i = 0; i < arr2.length; i++) {

			if (arr2[i] > 0)

				return i + 1;

		}

		return 0;

	}



	public int segregateArray(Integer[] ar) {

		int k = 0;

		int i = 1;

		for (i = 0; i < ar.length; i++) {

			if (ar[i] <= 0) {

				int temp = ar[i];

				ar[i] = ar[k];

				ar[k] = temp;

				k++;

			}

		}

		return k;

	}



	public int[] findTwoMissingNumbers(int[] ar) {

		int val = 0;

		int xor = 0;

		int x = 0;

		int y = 0;

		for (int i = 0; i < ar.length; i++) {

			xor = xor ^ ar[i];

		}

		val = xor & ~(xor - 1);

		for (int i = 0; i < ar.length; i++) {

			if ((ar[i] & val) > 0) {

				x = x ^ ar[i];

			} else {

				y = y ^ ar[i];

			}

		}



		int[] arr = new int[2];

		arr[0] = x;

		arr[1] = y;

		return arr;

	}



	public int findMaximumWindowOf1(int[] arr, int m) {

		int maxWindow = 0;

		int wL = 0;

		int wR = 0;

		int zeroCount = 0;

		int bestL = 0;

		while (wR < arr.length) {

			if (zeroCount <= m) {

				if (arr[wR] == 0) {

					zeroCount++;

				}

				wR++;

			}

			if (zeroCount > m) {

				if (arr[wL] == 0)

					zeroCount--;

				wL++;

			}

			if (wR - wL > maxWindow) {

				maxWindow = wR - wL;

				bestL = wL;

			}

		}

		for (int i = 0; i < maxWindow; i++) {

			if (arr[bestL + i] == 0)

				System.out.print(bestL + i + " ");

		}



		return bestL;

	}



	public int floorValueInArray(int[] ar, int x) {

		int low = 0;

		int high = ar.length - 1;

		int mid = 0;

		while (low <= high) {

			mid = (low + high) / 2;

			if (mid == 0) {

				return -1;

			}

			if (mid == ar.length - 1 && ar[mid] < x) {

				return mid;

			}



			if (ar[mid] == x) {

				return mid;

			}

			if (ar[mid] > ar[mid - 1] && ar[mid - 1] <= x && ar[mid]>x) {

				return mid - 1;

			}

			else if(ar[mid]<x){

				low=mid+1;

			}

			else{

				high=mid-1;

			}

			if (low > high)

				return -1;

		}



		return mid;



	}



	public int findNextSparseNumber(int x){

		String s=Integer.toBinaryString(x);

		List<Character> list = new ArrayList<Character>();

		for (int i = 0; i < s.length(); i++) {

			list.add(s.charAt(s.length() - i - 1));

		}

		list.add(list.size(), '0');

		int i = 0;

		for (i = 0; i < list.size(); i++) {

			if (list.get(i) == '1' && list.get(i - 1) == '1' && list.get(i + 1) == '0') {

				list.set(i + 1, '1');

				break;

			}

		}

		int val = 0;

		for (int j = i; j >= 0; j--) {

			list.set(j, '0');

		}

		int k = 0;

		for (i = 0; i < list.size(); i++) {

			val = (int)(val + (Math.pow(2, k) * (Integer.parseInt(list.get(i) + ""))));

			k++;

		}

		return val;

	}



	public LinkedSet sortLinkedListAscendingDescending(LinkedSet node) {

		if (node == null)

			return null;

		List<LinkedSet> listNodes=splitList(node);

		LinkedSet temp1 = listNodes.get(0);

		LinkedSet temp2 = listNodes.get(1);

		LinkedSet finalNode=null;

		int f=0;

		LinkedSet temp=null;

		while(temp1!=null && temp2!=null){

			if(f==0){

				temp = temp1.val == Math.min(temp1.val, temp2.val) ? temp1 : temp2;

				f = 1;

			}

			else{

				temp=temp1.val==Math.max(temp1.val, temp2.val)?temp1:temp2;

				f = 0;

			}

			if (temp == temp1) {

				temp1 = temp1.next;

			} else {

				temp2 = temp2.next;

			}

			if(finalNode==null){

				finalNode = new LinkedSet(temp.val);

				this.head = finalNode;

			} else {

				finalNode.next = new LinkedSet(temp.val);

				finalNode = finalNode.next;

			}

		}

		temp = temp1 != null ? temp1 : temp2;

		if (temp != null)

			finalNode.next = new LinkedSet(temp.val);



		printLinkedList(this.head);

		return this.head;



	}
	
		public List<LinkedSet> splitList(LinkedSet node) {

		LinkedSet temp1 = node;

		LinkedSet temp2 = node.next;

		LinkedSet head1 = null;

		LinkedSet head2 = null;

		LinkedSet node1 = null;

		LinkedSet node2 = null;



		while (temp1 != null) {

			if (node1 == null) {

				node1 = new LinkedSet(temp1.val);

				head1 = node1;

			} else {

				node1.next = new LinkedSet(temp1.val);

				node1 = node1.next;

			}

			if (temp1.next != null)

				temp1 = temp1.next.next;

			else {

				temp1 = null;

			}

		}



		while (temp2 != null) {

			if (node2 == null) {

				node2 = new LinkedSet(temp2.val);

				head2 = node2;

			} else {

				node2.next = new LinkedSet(temp2.val);

				node2 = node2.next;

			}

			if (temp2.next != null)

				temp2 = temp2.next.next;

			else {

				temp2 = null;

			}

		}



		List<LinkedSet> list = new ArrayList<LinkedSet>();

		list.add(head1);

		list.add(head2);

		return list;

	}



	public Queue<Integer> implementStackUsingQueueInsert(Queue<Integer> q, int val) {

		int size = q.size();

		q.add(val);

		for (int i = 0; i < size; i++) {

			int x = q.remove();

			q.add(x);

		}

		return q;

	}



	public int implementStackUsingQueueDelete(Queue<Integer> queue) {

		int val = -1;

		if (!queue.isEmpty()) {

			val = queue.poll();

		}

		return val;

	}



	public void largestArrayWithEqualZeroesOnes(int[] ar) {

		Map<Integer, Integer> sumMap = new HashMap<Integer, Integer>();

		int sum = 0;

		int maxLen = 0;

		for (int i = 0; i < ar.length; i++) {

			if (ar[i] == 0) {

				sum = sum + -1;

			} else

				sum = sum + ar[i];

			if (sumMap.containsKey(sum)) {

				maxLen = Math.max(maxLen, i - sumMap.get(sum));

			}

			else if(sum==0 || !sumMap.containsKey(sum))

				sumMap.put(sum, i);

		}

		maxLen = Math.max(sumMap.get(0) + 1, maxLen);

	}



	public void maxSubStringWithoutRepeatingChars(String st) {

		Map<Character, Integer> map = new HashMap<Character, Integer>();

		int maxLen = 0;

		int lowestIndex = 0;

		int currIndex=0;

		for (int i = 0; i < st.length(); i++) {

			if (map.containsKey(st.charAt(i))) {

				if (maxLen < i - map.get(st.charAt(i))) {

				if (map.get(st.charAt(i)) >= lowestIndex) {

					lowestIndex = map.get(st.charAt(i)) + 1;

					}

					currIndex = lowestIndex;

					maxLen = Math.max(maxLen, i - currIndex);

					if (map.get(st.charAt(i)) < lowestIndex) {

						maxLen++;

				}

				}

				



			}

			map.put(st.charAt(i), i);

		}

		System.out.println(maxLen);

	}



	public int flipSubArray(int[] ar) {

		int zeroCount = 0;

		int maxDiff = 0;

		int currMax = 0;

		for (int i = 0; i < ar.length; i++) {

			if (ar[i] == 0) {

				zeroCount++;

			}

			int val = ar[i] == 1 ? 1 : -1;

			if (val + currMax > 0) {

				currMax = val + currMax;

			} else

				currMax = 0;

			maxDiff = Math.max(maxDiff, currMax);

		}

		return zeroCount + maxDiff;

	}



	public void maximizeArrandIndexDiff(int[] ar) {

		int maxSum = Integer.MIN_VALUE;

		int minSum = Integer.MAX_VALUE;

		int k = -1;

		for (int i = 0; i < ar.length; i++) {

			if (ar[i] - i > maxSum) {

				maxSum = ar[i] - i;

				k = i;

			}

			if (ar[i] - i < minSum && k != i) {

				minSum = ar[i] - i;

			}

		}



		System.out.println(maxSum - minSum);



	}



	public int findLeastCommonAncestor(TreeNode node, int n1, int n2) {

		if (node == null)

			return -1;

		if (node.val == n1 || node.val == n2)

			return node.val;

		int leftLCA = findLeastCommonAncestor(node.left, n1, n2);

		int rightLCA = findLeastCommonAncestor(node.right, n1, n2);



		if (leftLCA != -1 && rightLCA != -1) {

			return node.val;

		}

		return leftLCA != -1 ? leftLCA : rightLCA;

	}

	
public int maxProductSubarray(int[] ar) {

		int prev_min = ar[0];

		int prev_max = ar[0];

		int prod = ar[0];

		int curr_min = ar[0];

		int curr_max = ar[0];

		for (int i = 1; i < ar.length; i++) {

			curr_max = Math.max(Math.max(prev_min * ar[i], prev_max * ar[i]), ar[i]);

			curr_min = Math.min(Math.min(prev_min * ar[i], prev_max * ar[i]), ar[i]);

			prod = Math.max(prod, curr_max);

			prev_max = curr_max;

			prev_min = curr_min;

		}

		return prod;

	}



	public int findMaxLenNonOverlappingSubArr(int[] ar, int n) {

		int sum = 0;

		int count = 0;

		int f = 0;

		for (int i = 0; i < ar.length; i++) {

			count++;

			if (ar[i] == n) {

				f = 1;

				sum = sum + count;

				count = 0;

			}

			if (ar[i] > n) {

				count = 0;

				f = 0;

			}

		}

		if (f == 1)

			return sum + count;

		return sum;

	}



	public int maxSumRotationsar(int[] ar) {

		int currSum = 0;

		int maxSum = 0;

		int sum = 0;

		for (int i = 0; i < ar.length; i++) {

			sum = ar[i] + sum;

			currSum = currSum + (i * ar[i]);

		}

		maxSum = currSum;

		for (int i = 1; i < ar.length; i++) {

			currSum = currSum + sum - ar.length * ar[ar.length - i];

			maxSum = Math.max(currSum, maxSum);

		}

		return maxSum;

	}



	public int findMaxAlternateSum(int[] ar) {

		int excl_new = 0;

		int excl = 0;

		int incl = ar[0];

		for (int i = 1; i < ar.length; i++) {

			excl_new = Math.max(incl, excl);

			incl = excl + ar[i];

			excl = excl_new;

		}

		return Math.max(incl, excl);

	}



	public int findMaxSumCommonPoints(int[] ar1, int[] ar2) {

		Map<Integer, Boolean> map = new LinkedHashMap<Integer, Boolean>();

		for (int i = 0; i < ar1.length; i++) {

			map.put(ar1[i], false);

		}

		for (int i = 0; i < ar2.length; i++) {

			if (map.get(ar2[i]) != null)

				map.put(ar2[i], true);

		}



		int sum1 = 0;

		int sum2 = 0;

		int maxSum = 0;

		int i = 0;

		int j = 0;

		int f1 = 0;

		int f2 = 0;

		Iterator<Integer> it = map.keySet().iterator();

		while (it.hasNext()) {

			int val = it.next();

			if (!map.get(val))

				it.remove();

		}

		it = map.keySet().iterator();

		int val = it.hasNext() ? it.next() : Integer.MIN_VALUE;

		while (f1 != 2 && f2 != 2) {

			if (val == Integer.MIN_VALUE)

				break;

			if (f1 == 0)

			sum1 = sum1 + ar1[i];

			if (f2 == 0)

			sum2 = sum2 + ar2[j];

			if (f1 == 0) {

				i++;

			}

			if (f2 == 0) {

				j++;

			}

			if (i < ar1.length && ar1[i] == val) {

				f1 = 1;



			}

			if (j < ar2.length && ar2[j] == val) {

				f2 = 1;

			}

			if (f1 == 1 && f2 == 1) {

				sum1 = sum1 + ar1[i];

				sum2 = sum2 + ar2[j];

				maxSum = maxSum + Math.max(sum1, sum2);

				sum1 = 0;

				sum2 = 0;

				f1 = 0;

				f2 = 0;

				i++;

				j++;

				it.remove();

				if (it.hasNext()) {

					val = it.next();

				} else {

					f1 = 2;

					f2 = 2;

				}

			}

		}

		while (i < ar1.length) {

			sum1 = sum1 + ar1[i];

			i++;

		}



		while (j < ar2.length) {

			sum2 = sum2 + ar2[j];

			j++;

		}



		return maxSum + Math.max(sum1, sum2);

	}



	public static String removeSpecial(String str) {

		return str.replaceAll("[^a-zA-Z ]", "");

	}



	public LinkedSet mergeTwoSortedLists(LinkedSet a, LinkedSet b) {

		LinkedSet head = null;

		LinkedSet temp = null;



		while (a != null && b != null) {

			if (a.val >= b.val) {

				temp = mergeNode(temp, a.val);

				a = a.next;

			} else {

				temp = mergeNode(temp, b.val);

				b = b.next;

			}

			if (head == null)

				head = temp;

		}

		while (a != null) {

			temp = mergeNode(temp, a.val);

			a = a.next;

			if (head == null)

				head = temp;

		}

		while (b != null) {

			temp = mergeNode(temp, b.val);

			b = b.next;

			if (head == null)

				head = temp;

		}

		return head;

	}
	
		

	public LinkedSet mergeNode(LinkedSet temp, int val) {

		if (temp == null) {

			temp = new LinkedSet(val);

		} else {

			temp.next = new LinkedSet(val);

			temp = temp.next;

		}

		return temp;

	}



	public int printSquaresOfCharactersremovingK(String s,int k){

		Map<Character,Integer> map=new HashMap<Character,Integer>();

		List<Integer> list = new ArrayList<Integer>();

		int count=1;

		int sum = 0;

		for(int i=0;i<s.length();i++){

			if(map.containsKey(s.charAt(i)))

			{

				count = map.get(s.charAt(i)) + 1;

				map.put(s.charAt(i), count);

			}

			else{

				map.put(s.charAt(i), 1);

			}

		}

		list.addAll(map.values());

		Collections.sort(list);

		for (int i = list.size() - 1; i >= 0; i--) {

			int val = list.get(i);

			while (val > 0 && k > 0) {

				val = val - 1;

				k = k - 1;

			}

			sum = sum + val * val;

		}

		return sum;

	}



	public int checkAllRottenOranges(int[][] ar) {

		Queue<Interval> queue = new LinkedList<Interval>();

		for (int i = 0; i < ar.length; i++) {

			for (int j = 0; j < ar[i].length; j++) {

				if (ar[i][j] == 2) {

					queue.add(new Interval(i, j));

				}

			}

		}

		int ans = 0;

		queue.add(new Interval(-1, -1));

		while (!queue.isEmpty()) {

			boolean flag=false;

			while (!isDelemiter(queue.peek())) {

				Interval e = queue.peek();

				if (isValid(e.x + 1, e.y, ar) && ar[e.x + 1][e.y] == 1) {

					if (!flag) {

						flag = true;

						ans++;

					}

					e.x++;

					ar[e.x][e.y] = 2;

					queue.add(new Interval(e.x, e.y));

					e.x--;

				}

				if (isValid(e.x - 1, e.y, ar) && ar[e.x - 1][e.y] == 1) {

					if (!flag) {

						flag = true;

						ans++;

					}

					e.x--;

					ar[e.x][e.y] = 2;

					queue.add(new Interval(e.x, e.y));

					e.x++;

				}

				if (isValid(e.x, e.y + 1, ar) && ar[e.x][e.y + 1] == 1) {

					if (!flag) {

						flag = true;

						ans++;

					}

					e.y++;

					ar[e.x][e.y] = 2;

					queue.add(new Interval(e.x, e.y));

					e.y--;

				}

				if (isValid(e.x, e.y - 1, ar) && ar[e.x][e.y - 1] == 1) {

					if (!flag) {

						flag = true;

						ans++;

					}

					e.y--;

					ar[e.x][e.y] = 2;

					queue.add(new Interval(e.x, e.y));

					e.y++;

				}

				queue.remove();

			}

			queue.remove();

			if (!queue.isEmpty()) {

				queue.add(new Interval(-1, -1));

			}

		}

		return checkAll(ar) ? ans : -1;

	}



	public boolean checkAll(int[][] ar) {

		for (int i = 0; i < ar.length; i++) {

			for (int j = 0; j < ar[i].length; j++) {

				if (ar[i][j] == 1) {

					return false;

				}

			}

		}

		return true;

	}



	public boolean isDelemiter(Interval e) {

		return e.x == -1 && e.y == -1;

	}



	public boolean isValid(int x, int y, int[][] ar) {

		return x >= 0 && y >= 0 && x < ar.length && y < ar[0].length;

	}



	public List<Integer> nextGreaterElement(int[] ar) {

		List<Integer> list = new ArrayList<Integer>();

		for (int i = 0; i < ar.length; i++) {

			list.add(-1);

		}

		Stack<Integer> st = new Stack<Integer>();

		Stack<Integer> indexSt = new Stack<Integer>();

		for (int i = 0; i < ar.length; i++) {

			if (st.isEmpty()) {

				st.push(ar[i]);

				indexSt.push(i);

			} else {

				while (!st.isEmpty() && ar[i] >= st.peek()) {

					list.set(indexSt.peek(), ar[i]);

					st.pop();

					indexSt.pop();

				}

				st.push(ar[i]);

				indexSt.push(i);

			}

		}

		/*

		 * while (!st.isEmpty()) { list.add(indexSt.peek(), -1); st.pop(); indexSt.pop(); }

		 */

		return list;

	}



	public void getMinimumCoinChangeProblem(int c, int s) {

		int[][] coins = new int[c + 1][s + 1];

		for (int i = 0; i <= c; i++) {

			for (int j = 0; j <= s; j++) {

				if (i == 0 && j == 0) {

					coins[i][j] = 1;

				} else if (i == 0) {

					coins[i][j] = 0;

				} else {

					if (i > j) {

						coins[i][j] = coins[i - 1][j];

					} else {

						coins[i][j] = coins[i - 1][j] + coins[i][j - i];

					}

				}

			}

		}

		System.out.println(coins[c][s]);

	}



	public int getNumberOfPaths(int[][] ar, int m, int n, int k, int[][][] dp) {

		if (m == 0 && n == 0) {

			return k == ar[m][n] ? 1 : 0;

		} else if (m < 0 || n < 0)

			return 0;

		dp[m][n][k] = getNumberOfPaths(ar, m - 1, n, k - ar[m][n], dp)

				+ getNumberOfPaths(ar, m, n - 1, k - ar[m][n], dp);

		return dp[m][n][k];

	}



	public LinkedSet swapAdjacentElements(LinkedSet l) {

		int temp = 0;

		LinkedSet head = l;

		while (l != null && l.next != null) {

			temp = l.next.val;

			l.next.val = l.val;

			l.val = temp;

			l = l.next.next;

		}

		printLinkedList(head);

		return head;

	}



	public List<Integer> jumpingNumbers(int x) {

		List<Integer> list = new ArrayList<Integer>();

		for (int i = 1; i <= 9 && i <= x; i++) {

			printJumpingNumbers(x, i, list);

		}

		Collections.sort(list);

		return list;

	}



	public void printJumpingNumbers(int x, int i, List<Integer> list) {

		Queue<Integer> queue = new LinkedList<Integer>();

		queue.add(i);

		while (!queue.isEmpty()) {

			i = queue.poll();

			if (i <= x) {

				list.add(i);

				int lastDigit = i % 10;

				if (lastDigit == 0) {

					queue.add(i * 10 + (lastDigit + 1));

				} else if (lastDigit == 9) {

					queue.add(i * 10 + (lastDigit - 1));

				}

				else {

					queue.add(i * 10 + (lastDigit + 1));

					queue.add(i * 10 + (lastDigit - 1));

				}

			}

		}

	}		
			
			
		public void findCommonNodes(TreeNode a, TreeNode b) {

		Set<Integer> set = (Set<Integer>)printInorder(new HashSet<Integer>(), a);

		List<Integer> list = (List<Integer>)printInorder(new ArrayList<Integer>(), b);

		Iterator<Integer> it = list.iterator();

		while (it.hasNext()) {

			int val=it.next();

			if (!set.contains(val)) {

				it.remove();

			}

			else{

				System.out.print(val + " ");

			}

		}

	}



	public Collection<Integer> printInorder(Collection<Integer> set, TreeNode a) {

		if (a == null) {

			return null;

		}

		printInorder(set, a.left);

		set.add(a.val);

		printInorder(set, a.right);

		return set;

	}



	public void printAllPermutations(String s) {

		char[] str = s.toCharArray();

		int n = str.length;

		int opsize = (int)(Math.pow(2, n - 1));



		for (int counter = 0; counter < opsize; counter++) {

			for (int j = 0; j < n; j++) {



				System.out.print(str[j]);

				if ((counter & (1 << j)) > 0)

					System.out.print(" ");

			}

			System.out.println();

		}

	}



	public String rearrangeCharacters(String s) {

		int low = 0;

		int high = 1;

		String finalSt = "";

		if (high >= s.length()) {

			return s;

		}

		while (low < s.length() && high < s.length()) {

				if (s.charAt(low) == s.charAt(high))

					high++;

				else {

					finalSt = finalSt + s.charAt(low) + s.charAt(high);

					low++;

					high++;

				}

			}

		if (low < s.length() && finalSt.length() != s.length()) {

			finalSt = finalSt + s.charAt(low);

		}

		return finalSt.length() != s.length() ? "Not Possible" : finalSt;

		}



	public void insertQueueUsingStack(int x, Stack<Integer> st){

		if (st != null)

			st.push(x);

	}



	public int deleteQueueUsingStack(Stack<Integer> st) {

		int k = 0;

		int res = 0;

		if (st.size() == 1) {

			return st.pop();

		} else if (!st.isEmpty()) {

			k = st.pop();

			res = deleteQueueUsingStack(st);

			st.push(k);

			return res;

		}

		return -1;

	}



	public void queueOperations(Stack<Integer> st) {

		insertQueueUsingStack(1, st);

		insertQueueUsingStack(2, st);

		insertQueueUsingStack(3, st);



		System.out.println(deleteQueueUsingStack(st));

		System.out.println(deleteQueueUsingStack(st));

		System.out.println(deleteQueueUsingStack(st));

		System.out.println(deleteQueueUsingStack(st));

	}



	public LinkedSet removeEveryKthNode(LinkedSet l, int k) {

		LinkedSet head = l;

		int p = 1;

		int m=1;

		if (k == 1) {

			return null;

		}

		while (l != null && l.next != null) {

			if (p == k - 1) {

				l.next = l.next.next;

				p = 1;

				m++;

			} else {

				p++;

			}

			l = l.next;

		}

		return head;

	}



	public void replaceMaxElementOntheRight(int[] ar) {

		int maxElement = -1;

		int temp = -1;

		for (int i = ar.length - 1; i >= 0; i--) {

			temp = ar[i];

			ar[i] = maxElement;

			if (temp > maxElement) {

				maxElement = temp;

			}

		}

	}


	public void reverseReverseOrderTraversal(TreeNode node){

		List<Integer> list = new LinkedList<Integer>();

		int h = hieghtOfTree(node);

		for (int i = h - 1; i >= 0; i--) {

			reverseReverseOrderTraversal(node, i, list);

		}

		System.out.println(Arrays.toString(list.toArray()));

	}



	public void reverseReverseOrderTraversal(TreeNode node, int k, List<Integer> list) {

		if (node == null)

			return;

		if (k == 0) {

			list.add(node.val);

		}

		reverseReverseOrderTraversal(node.left, k - 1, list);

		reverseReverseOrderTraversal(node.right, k - 1, list);

	}



	public void reverseSentence(String s) {

		String[] st = s.split(" ");

		s = "";

		for (int i = st.length - 1; i >= 0; i--) {

			s = s + st[i].trim() + " ";

		}

		System.out.println(s.trim());

	}



	public boolean rootToLeafPath(TreeNode node, int k, int sum) {

		if (node == null) {

			return false;

		}

		sum = sum + node.val;

		if (sum == k) {

			return true;

		}

		if (rootToLeafPath(node.left, k, sum) || rootToLeafPath(node.right, k, sum)) {

			return true;

		}

		sum = sum - node.val;

		return false;

	}



	public int solve(int[] A) {

		int n = A.length;

		double count = 0;

		count = (int)(Math.round(Math.pow(2, n)) - 1);

		long bitsCombs = (long)Math.pow(2, n);

		for (int i = 0; i < bitsCombs; i++) {

			for (int j = 0; j < n; j++) {

				if ((i & (1 << j)) > 0) {

					if (findPrime(A[j])) {

						count++;

					}

				}

			}

		}

		return (int)(count % 10);

	}



	public boolean findPrime(int n) {

		if (n <= 1)

			return false;

		for (int i = 2; i <= n / 2; i++) {

			if (n % i == 0)

				return false;

		}

		return true;

	}



	public void findSubIndex(String str, String findStr) {

		int lastIndex = 0;

		int count = 0;



		while (lastIndex != -1) {



			lastIndex = str.indexOf(findStr, lastIndex);



			if (lastIndex != -1) {

				count++;

				lastIndex += findStr.length();

			}

		}

		System.out.println(count);

	}

	public int solve(String A) {



		int n = A.length();

		int prod = 1;

		String s = "";

		List<String> substrings = new ArrayList<String>();

		for (int i = 0; i <= n / 2; i++) {

			s = s + A.charAt(i);

			substrings.add(new String(s));

		}

		for (int i = 1; i <= n; i++) {

			prod = prod * i;

		}

		int f = 0;

		for (int i = 0; i < substrings.size(); i++) {

			int count=findOccurences(A, substrings.get(i));

			while (count > 1) {

				prod = prod * (substrings.get(i).length());

				count--;

			}

		}

		return prod;

	}



	public int findOccurences(String s, String findString) {

		int M = findString.length();

		int N = s.length();

		int res = 0;

		for (int i = 0; i <= N - M; i++) {

			int j;

			for (j = 0; j < M; j++)

				if (s.charAt(i + j) != findString.charAt(j))

					break;

			if (j == M) {

				res++;

				j = 0;

			}

		}

		return res;

	}



	public void serializeDeseralizeTree(TreeNode node) {

		List<Integer> list = new ArrayList<Integer>();

		serializeBinaryTree(node, list);

		node = null;

		node = deserializeBinaryTree(node, list, 0);

		list.clear();

		list = (List<Integer>)printInorder(list, node);

		System.out.println(Arrays.toString(list.toArray()));

	}



	public void serializeBinaryTree(TreeNode node, List<Integer> list) {

		if (node == null) {

			list.add(-1);

			return;

		}

		list.add(node.val);

		serializeBinaryTree(node.left, list);

		serializeBinaryTree(node.right, list);

	}

	

	public TreeNode deserializeBinaryTree(TreeNode node, List<Integer> list, int count) {

		Stack<TreeNode> st = new Stack<TreeNode>();

		node = new TreeNode(list.get(0));

		st.push(node);

		TreeNode temp = null;

		for (int i = 1; i < list.size(); i++) {

			temp = null;

			while (!st.isEmpty() && st.peek().val < list.get(i)) {

				temp = st.pop();

			}

			if (list.get(i) == -1)

				continue;

			if (temp != null) {

				temp.right = new TreeNode(list.get(i));

				st.push(temp.right);

			} else {

				temp = st.peek();

				temp.left = new TreeNode(list.get(i));

				st.push(temp.left);

			}

		}

		return node;

	}



	public void SlidingWindowMaximum(int[] ar, int k) {

		int minIndex = 0;

		int maxIndex = 0;

		int count = 0;

		int maxSoFar = Integer.MIN_VALUE;

		int nextMaxSoFar=Integer.MIN_VALUE;

		while (count <= ar.length) {

			if (maxIndex - minIndex < k) {

				if (count < ar.length && ar[count] > maxSoFar) {

					nextMaxSoFar = maxSoFar;

					maxSoFar = ar[count];



				} else if (count < ar.length && ar[count] > nextMaxSoFar && nextMaxSoFar != maxSoFar) {

					nextMaxSoFar = ar[count];

				}

				maxIndex++;

				count++;

			}

			else if (maxIndex - minIndex == k) {

				System.out.println(maxSoFar + " ");

				if (minIndex < ar.length && ar[minIndex] == maxSoFar) {

					maxSoFar = nextMaxSoFar;



				}

				minIndex++;

			}

		}

	}

	public void sortLinkedListWithAbsValues(LinkedSet node){

		LinkedSet curr = node.next;

		LinkedSet head=curr;

		LinkedSet prev=node;

		printLinkedList(head);

		while(curr!=null){

			if (prev.val > curr.val) {

				prev.next=curr.next;

				curr.next=head;

				head=curr;

				curr = prev;

			} else {

				prev=curr;

				curr = curr.next;

			}

		}

		printLinkedList(head);

	}



	public TreeNode createBSTWithSortedArray(int[] ar, int low, int high) {

		if(low>high){

			return null;

		}

		int mid=(low+high)/2;

		TreeNode node=new TreeNode(ar[mid]);

		node.left = createBSTWithSortedArray(ar, low, mid - 1);

		node.right = createBSTWithSortedArray(ar, mid + 1, high);

		return node;

	}



	public int celebrityProblem(int[][] ar) {

		Stack<Integer> st = new Stack<Integer>();

		for(int i=0;i<ar.length;i++){

			st.push(i);

		}

			int A=st.pop();

			int B=st.pop();

			while(st.size()>1){

				if(knows(A,B,ar)){

					A=st.pop();

				}

				else{

					B=st.pop();

				}

			}

		int C = st.pop();

		if (knows(C, B, ar))

			C = B;



		if (knows(C, A, ar))

			C = A;



		for (int i = 0; i < ar.length; i++) {

			if (i != C && (knows(C, i, ar) || !knows(i, C, ar))) {

				return -1;

			}

		}

		return C;

	}



	public boolean knows(int A, int B, int[][] ar) {

		return ar[A][B] == 1;

	}



	public int trappingRainWaterAr(int[] ar) {

		int[] maxFromLeft = new int[ar.length];

		int[] maxFromRight = new int[ar.length];

		int water = 0;

		maxFromLeft[0] = ar[0];

		maxFromRight[ar.length - 1] = ar[ar.length - 1];

		for (int i = 1; i < ar.length; i++) {

			maxFromLeft[i] = Math.max(maxFromLeft[i - 1], ar[i]);

		}

		for (int i = ar.length - 2; i >= 0; i--) {

			maxFromRight[i] = Math.max(maxFromRight[i + 1], ar[i]);

		}

		for (int i = 0; i < ar.length; i++) {

			water = water + (Math.min(maxFromLeft[i], maxFromRight[i]) - ar[i]);

		}

		return water;

	}



	public boolean treeIsomorphism(TreeNode node1, TreeNode node2) {

		if (node1 == null && node2 == null) {

			return true;

		} else if (node1 == null || node2 == null) {

			return false;

		} else if (node1.val != node2.val) {

			return false;

		} else if (treeIsomorphism(node1.left, node2.left) || treeIsomorphism(node1.right, node2.right)

				|| treeIsomorphism(node1.left, node2.right) || treeIsomorphism(node1.right, node2.left)) {

			return true;

		}

		return false;

	}



	public Interval findPairsWithNearZeroSum(int[] a) {

		int l = 0;

		int r = a.length - 1;

		int sum = 0;

		int min_sum = Integer.MAX_VALUE;

		Arrays.sort(a);

		int min_l = 0;

		int min_r = 0;

		while (l < r) {

			sum = a[l] + a[r];

			if (Math.abs(sum) < Math.abs(min_sum)) {

				min_sum = sum;

				min_l = l;

				min_r = r;

			}

			if (sum < 0)

				l++;

			else

				r--;

		}

		return new Interval(min_l, min_r);

	}



	public TreeNode addAllValues(TreeNode root, Sum sum) {

		if (root == null)

			return null;

		addAllValues(root.right, sum);

		sum.S = sum.S + root.val;

		root.val = sum.S;

		addAllValues(root.left, sum);

		return root;

	}

	public boolean findHamiltonianCycle(int[][] graph,int[] path,int pos ){

		if(pos==graph.length){

			if (graph[path[pos - 1]][path[0]] == pos) {

				return true;

			}

			else{

				return false;

			}

		}

		

		for(int v=1;v<graph.length;v++){

			if (isSafe(v, graph, path, pos)) {

				path[pos] = v;

				if (findHamiltonianCycle(graph, path, pos + 1)) {

					return true;

				}

				path[pos] = -1;

			}

		}

		return false;

	}



	public boolean isSafe(int v, int[][] graph, int[] path, int pos) {

		if (graph[path[pos - 1]][v] == 0)

			return false;

		for (int i = 0; i < pos; i++)

			if (path[i] == v) {

				return false;

			}

		return true;

	}

	public boolean sudoku(int[][] board, int n) {

		int row=-1;

		int col=-1;

		boolean isEmpty=true;

		for(int i=0;i<n;i++){

			for(int j=0;j<n;j++){

				if(board[i][j]==0){

					row=i;

					col=j;

					isEmpty=false;

					break;

				}

			}

			if (!isEmpty) {

				break;

			}

		}

		if(isEmpty){

			return true;

		}

		for(int i=1;i<=n;i++){

			if (isSafeSudoku(row, col, board, i)) {

				board[row][col] = i;

				if (sudoku(board, n)) {

					System.out.println("------------------------------------------------------");

					printMatrix(board);

					return true;

				}

				board[row][col] = 0;

			}

		}

		return false;

	}



	public boolean isSafeSudoku(int row, int col, int[][] board, int num) {

		for (int i = 0; i < board.length; i++) {

			if (board[i][col] == num)

				return false;

		}

		for (int i = 0; i < board.length; i++) {

			if (board[row][i] == num)

				return false;

		}



		int sqrt = (int)Math.sqrt(board.length);

		int rowStart = row - row % sqrt;

		int colStart = col - col % sqrt;



		for (int i = rowStart; i < sqrt + rowStart; i++) {

			for (int j = colStart; j < sqrt + colStart; j++) {

				if (board[i][j] == num)

					return false;

			}

		}

		return true;

	}



	public boolean solveMaze(int[][] maze, int x, int y, int n) {

		if (x == n - 1 && y == n - 1)

			return true;

		if (isMazeSafe(x, y, maze, n)) {

			if (solveMaze(maze, x + 1, y, n))

				return true;

			if (solveMaze(maze, x, y + 1, n))

				return true;

		}

		return false;

	}



	public boolean isMazeSafe(int x, int y, int[][] maze, int n) {

		return (x >= 0 && y >= 0 && x < n && y < n && maze[x][y] == 1);

	}



	public TreeMap<Integer, Integer> showBottomViewTree(TreeNode root, TreeMap<Integer, Integer> map,

			Queue<TreeNode> queue) {

		root.hd = 0;

		queue.add(root);

		while (!queue.isEmpty()) {

			TreeNode temp = queue.poll();

			int hd = temp.hd;

			map.put(hd, temp.val);



			if (temp.left != null) {

				temp.left.hd = hd - 1;

				queue.add(temp.left);

			}



			if (temp.right != null) {

				temp.right.hd = hd + 1;

				queue.add(temp.right);

			}

		}

		return map;

	}



	public LinkedSet cloneLinkedList(LinkedSet list) {

		LinkedSet cloneList = null;

		LinkedSet cloneHead = null;

		LinkedSet listHead = list;

		LinkedSet prev = null;

		while (list != null) {

			if (cloneHead == null) {

				cloneList = new LinkedSet(list.val);

				cloneHead = cloneList;

			} else {

				cloneList.next = new LinkedSet(list.val);

				cloneList = cloneList.next;

			}

			list = list.next;

		}

		cloneList = cloneHead;

		list = listHead;

		while(cloneList!=null)

		{

			prev = list;

			cloneList.random = list;

			list = list.next;

			prev.next = cloneList;

			cloneList = cloneList.next;

		}

		cloneList = cloneHead;

		while (cloneList != null) {

			if (cloneList.random.random != null)

				cloneList.random = cloneList.random.random.next;

			else

				cloneList.random = null;

			cloneList = cloneList.next;

		}

		return cloneHead;

	}



	public TreeNode cloneBinaryTreeLeftRight(TreeNode node, Map<TreeNode, TreeNode> map) {

		if (node == null) {

			return null;

		}

		TreeNode cloneNode = new TreeNode(node.val);

		if (clonedRoot == null)

			clonedRoot = cloneNode;

		if (root == null)

			root = node;

		map.put(node, cloneNode);

		cloneNode.left = cloneBinaryTreeLeftRight(node.left, map);

		cloneNode.right = cloneBinaryTreeLeftRight(node.right, map);

		cloneBinaryNode(root, map, clonedRoot);

		return clonedRoot;

	}



	public TreeNode cloneBinaryNode(TreeNode node, Map<TreeNode, TreeNode> map,TreeNode clonedNode) {

		if (node == null || clonedNode == null) {

			return clonedNode;

		}

		if (node.random == null) {

			clonedNode.random = null;

		} else

			clonedNode.random = map.get(node.random);

		cloneBinaryNode(node.left, map, clonedNode.left);

		cloneBinaryNode(node.right, map, clonedNode.right);

		return clonedNode;

	}

	public List<List<Integer>> combinationalSum(List<List<Integer>> res, List<Integer> list, int[] ar, int i, int sum) {

		if (sum < 0) {

			return res;

		}

		if (sum == 0) {

			res.add(new ArrayList<Integer>(list));

			return res;

		}



		while (i < ar.length && sum - ar[i] >= 0) {

			list.add(ar[i]);

			combinationalSum(res, list, ar, i, sum - ar[i]);

			i++;

			list.remove(list.size() - 1);

		}

		return res;

	}



	public int connectMinSumRopes(int[] ar) {

		PriorityQueue<Integer> queue = new PriorityQueue<Integer>();

		for (int i = 0; i < ar.length; i++) {

			queue.add(ar[i]);

		}

		int sum = 0;

		int finalSum = 0;

		while (queue.size() >= 2) {

			sum = queue.poll() + queue.poll();

			finalSum = sum + finalSum;

			queue.add(sum);

		}



		return finalSum;

	}

	

	public TreeNode createBinaryTreefromParentIndices(int[] ar) {

		TreeNode[] connected = new TreeNode[ar.length];

		for(int i=0;i<ar.length;i++){

			connected[i]=null;

		}

		for (int i = 0; i < ar.length; i++) {

			createBinaryTreeFromIndices(ar, connected, i);

		}

		return root;

	}



	public void createBinaryTreeFromIndices(int[] ar, TreeNode[] connected, int i) {

		if (connected[i] != null)

			return;

		TreeNode newNode = new TreeNode(i);

		connected[i] = newNode;

		if (ar[i] == -1) {

			root = newNode;

			return;

		} else if (connected[ar[i]] == null)

			createBinaryTreeFromIndices(ar, connected, ar[i]);

		TreeNode temp = connected[ar[i]];

		if (temp.left == null)

			temp.left = newNode;

		else

			temp.right = newNode;

	}



	public TreeNode createTree(int[] pre, char[] preLN, Sum s, TreeNode temp) {

		if (s.S == pre.length)

			return null;

		int index = s.S;

		temp = new TreeNode(pre[index]);

		s.S++;

		if (preLN[index] == 'N') {

			temp.left = createTree(pre, preLN, s, temp.left);

			temp.right = createTree(pre, preLN, s, temp.right);

		}

		return temp;

	}



	void printInorder(TreeNode node) {

		if (node == null)

			return;



		/* first recur on left child */

		printInorder(node.left);



		/* then print the data of node */

		System.out.print(node.val + " ");



		/* now recur on right child */

		printInorder(node.right);

	}



	public void convert_to_words(char[] num) {

		// Get number of digits

		// in given number

		int len = num.length;



		// Base cases

		if (len == 0) {

			System.out.println("empty string");

			return;

		}

		if (len > 4) {

			System.out.println("Length more than 4 is not supported");

			return;

		}



		/*

		 * The first string is not used, it is to make array indexing simple

		 */

		String[] single_digits = new String[] {

				"zero", "one", "two", "three", "four", "five", "six", "seven", "eight", "nine"

		};



		/*

		 * The first string is not used, it is to make array indexing simple

		 */

		String[] two_digits = new String[] {

				"", "ten", "eleven", "twelve", "thirteen", "fourteen", "fifteen", "sixteen", "seventeen", "eighteen",

				"nineteen"

		};



		/* The first two string are not used, they are to make array indexing simple */

		String[] tens_multiple = new String[] {

				"", "", "twenty", "thirty", "forty", "fifty", "sixty", "seventy", "eighty", "ninety"

		};



		String[] tens_power = new String[] {

				"hundred", "thousand"

		};



		/* Used for debugging purpose only */

		System.out.print(String.valueOf(num) + ": ");



		/* For single digit number */

		if (len == 1) {

			System.out.println(single_digits[num[0] - '0']);

			return;

		}



		/*

		 * Iterate while num is not '\0'

		 */

		int x = 0;

		while (x < num.length) {



			/* Code path for first 2 digits */

			if (len >= 3) {

				if (num[x] - '0' != 0) {

					System.out.print(single_digits[num[x] - '0'] + " ");

					System.out.print(tens_power[len - 3] + " ");

					// here len can be 3 or 4

				}

				--len;

			}



			/* Code path for last 2 digits */

			else {

				/*

				 * Need to explicitly handle 10-19. Sum of the two digits is used as index of "two_digits" array of

				 * strings

				 */

				if (num[x] - '0' == 1) {

					int sum = num[x] - '0' + num[x] - '0';

					System.out.println(two_digits[sum]);

					return;

				}



				/* Need to explicitely handle 20 */

				else if (num[x] - '0' == 2 && num[x + 1] - '0' == 0) {

					System.out.println("twenty");

					return;

				}



				/*

				 * Rest of the two digit numbers i.e., 21 to 99

				 */

				else {

					int i = (num[x] - '0');

					if (i > 0)

						System.out.print(tens_multiple[i] + " ");

					else

						System.out.print("");

					++x;

					if (num[x] - '0' != 0)

						System.out.println(single_digits[num[x] - '0']);

				}

			}

			++x;

		}

	}



	public int findNDigitNumbersWithSum(int n, int sum) {

		int ans = 0;

		for (int i = 1; i <= 9; i++) {

			ans += countNDigitNumbersWithSum(n - 1, sum - i);

		}

		return ans;

	}

	public int countNDigitNumbersWithSum(int n, int sum) {

		if (n == 0) {

			return sum == 0 ? 1 : 0;

		}

		if (sum == 0)

			return 1;



		int ans = 0;

		for (int i = 0; i <= 9; i++) {

			ans += countNDigitNumbersWithSum(n - 1, sum - i);

		}

		return ans;

	}



	public int countPossibleDecodings(char[] digits, int n) {

		if (n <= 1)

			return 1;

		int ans = 0;

		if (digits[n - 2] > '0') {

			ans += countPossibleDecodings(digits, n - 1);

		}



		if (digits[n - 2] == '1' || (digits[n - 2] == '2' && digits[n - 1] > 7)) {

			ans += countPossibleDecodings(digits, n - 2);

		}

		return ans;

	}



	public void deleteNodesWithRightGreaterValue(LinkedSet node) {

		printLinkedList(node);

		node=reverseLinkedSet(node);

		LinkedSet head=node;

		LinkedSet prev = node;

		LinkedSet curr = node.next;

		printLinkedList(node);

		int f = 0;

		while (curr != null) {

			f = 0;

			if (prev.val > curr.val) {

				prev.next = curr.next;

				curr = prev;

				f = 1;

			}

			prev = curr;

			curr = curr.next;

			if (f == 1)

			printLinkedList(node);

		}

		

		node = reverseLinkedSet(head);

		System.out.print("FInal LinkedList :");

		printLinkedList(node);

	}



	public void deleteAllOccurences(LinkedSet node, int k) {

		printLinkedList(node);

		LinkedSet head = null;

		LinkedSet curr = node;

		LinkedSet prev = null;

		int f = 0;

		while (curr != null) {

			f = 0;

			if (curr.val != k) {

				if (head == null) {

					head = curr;

				}

			}



			if (curr.val == k) {

				f = 1;

				if (prev != null)

					prev.next = curr.next;

			}

			prev = curr;

			curr = curr.next;

			if (f == 1)

				printLinkedList(head);

		}



		System.out.print("FInal LinkedList :");

		printLinkedList(head);

	}



	public boolean detectCycleInADirectedGraph(Graph g, int V) {

		Boolean recursion[] = new Boolean[V];

		Boolean visited[] = new Boolean[V];

		for (int i = 0; i < V; i++) {

			recursion[i] = false;

			visited[i] = false;

		}



		for (int i = 0; i < V; i++) {

			if (findCyclicDirectedGraph(i, g, recursion, visited)) {

				return true;

			}

		}

		return false;



	}



	public boolean findCyclicDirectedGraph(int i, Graph g, Boolean[] recursion, Boolean[] visited) {

		if (recursion[i]) {

			return true;

		}

		if (visited[i])

			return false;

		visited[i] = true;

		recursion[i] = true;



		List<Integer> list = g.adj[i];

		for (Integer c : list)

			if (findCyclicDirectedGraph(c, g, recursion, visited))

				return true;



		recursion[i] = false;



		return false;

	}



	public boolean detectCycleInUndirectedGraph(Graph g, int V) {

		Boolean[] visited = new Boolean[V];

		for (int i = 0; i < V; i++) {

			visited[i] = false;

		}

		for (int i = 0; i < V; i++) {

			if (!visited[i])

				if (findCyclicUndirectedGraph(i, g, -1, visited)) {

					return true;

				}

		}

		return false;

	}



	public boolean findCyclicUndirectedGraph(int v, Graph g, int parent, Boolean[] visited) {



		visited[v] = true;

		List<Integer> list = g.adj[v];

		for (Integer i : list) {

			if (!visited[i]) {

				if (findCyclicUndirectedGraph(i, g, v, visited))

					return true;

			} else if (parent != i) {

				return true;

			}

		}

		return false;

	}

public void detectLoopInLinkedList(LinkedSet node) {

		LinkedSet fast = node;

		LinkedSet slow = node;

		while (slow != null && fast != null && fast.next != null) {

			fast = fast.next.next;

			slow = slow.next;



			if (fast == slow) {

				break;

			}

		}

		LinkedSet curr = node;

		int i = 0;

		while (curr != null && curr.next != null) {

			if (curr == slow) {

				++i;

			}

			if (i == 2) {

				break;

			}

			curr = curr.next;

		}

		curr.next = null;

		printLinkedList(node);

	}

	

	public Map<Integer, List<Integer>> diagonalTraversalOfTree(TreeNode node, Map<Integer, List<Integer>> map, int d) {

		if(node==null){

			return map;

		}

		List<Integer> list = null;

		if(map.get(d)!=null){

			list = map.get(d);

			list.add(node.val);

		} else {

			list = new ArrayList<Integer>();

			list.add(node.val);

		}

		map.put(d, list);

		diagonalTraversalOfTree(node.left, map, d + 1);

		diagonalTraversalOfTree(node.right, map, d);

		return map;

	}



	public int eggDroppingProblem(int n, int k) {

		int[][] eggdrop = new int[n + 1][k + 1];

		for (int i = 0; i <= n; i++) {

			eggdrop[i][1] = 1;

			eggdrop[i][0] = 0;

		}

		for (int i = 0; i <= k; i++) {

			eggdrop[1][i] = i;

		}

		for (int i = 2; i <= n; i++) {

			for (int j = 2; j <= k; j++) {

				eggdrop[i][j] = Integer.MAX_VALUE;

				for (int x = 1; x <= j; x++) {

					int res = 1 + Math.max(eggdrop[i - 1][x - 1], eggdrop[i][j - x]);

					if (res < eggdrop[i][j]) {

						eggdrop[i][j] = res;

					}

				}

			}

		}

		return eggdrop[n][k];

	}



	public int longestPairSubSequence(List<Interval> intervals) {

		Collections.sort(intervals, new Comparator<Interval>() {

			@Override

			public int compare(Interval i1, Interval i2) {

				return i1.x.compareTo(i2.x);

			}

		});



		int[] mc = new int[intervals.size()];

		for (int i = 0; i < intervals.size(); i++)

			mc[i] = 1;



		for (int i = 1; i < intervals.size(); i++) {

			for (int j = 0; j < i; j++) {

				if (intervals.get(j).y < intervals.get(i).x && mc[i] < mc[j] + 1) {

					mc[i] = mc[j] + 1;

				}

			}

		}

		return mc[intervals.size() - 1];

	}



	public int maxBoxStacking(List<Box> boxes) {

		Box[] maxCombs = new Box[3 * boxes.size()];

		for (int i = 0; i < boxes.size(); i++) {

			maxCombs[3 * i] = new Box(boxes.get(i).x, Math.max(boxes.get(i).y, boxes.get(i).z),

					Math.min(boxes.get(i).y, boxes.get(i).z));

			maxCombs[3 * i + 1] = new Box(boxes.get(i).y, Math.max(boxes.get(i).x, boxes.get(i).z),

					Math.min(boxes.get(i).x, boxes.get(i).z));

			maxCombs[3 * i + 2] = new Box(boxes.get(i).z, Math.max(boxes.get(i).y, boxes.get(i).x),

					Math.min(boxes.get(i).y, boxes.get(i).x));

		}

		

		Arrays.sort(maxCombs);

		int[] msh = new int[maxCombs.length];

		int count = 3 * boxes.size();

        for (int i = 0; i < count; i++ ) 

			msh[i] = maxCombs[i].x;



		for(int i=1;i<maxCombs.length;i++){

			msh[i] = 0;

			int val = 0;

			for(int j=0;j<i;j++){

				if (maxCombs[i].y < maxCombs[j].y && maxCombs[i].z < maxCombs[j].z) {

					val = Math.max(val, msh[j]);

				}

				msh[i] = val + maxCombs[i].x;

			}

		}

		int max = Integer.MIN_VALUE;

		for (int i = 0; i < count; i++) {

			max = Math.max(max, msh[i]);

		}

		return max;

	}


		public int maximumSumRectangle(int[][] ar) {

		int maxSum = Integer.MIN_VALUE;

		int currSum = 0;

		int maxLeft = 0;

		int maxRight = 0;

		int maxTop = 0;

		int maxDown = 0;



		int[] kadaneArr = new int[ar.length];



		for (int i = 0; i < ar[0].length; i++) {

			Arrays.fill(kadaneArr, 0);

			for (int j = i; j < ar[0].length; j++) {

				for (int k = 0; k < ar.length; k++) {

					kadaneArr[k] = kadaneArr[k] + ar[k][j];

				}

					int[] arr = kadaneAlgo(kadaneArr);

					if (maxSum < arr[0]) {

						maxSum = arr[0];

						maxLeft = i;

						maxRight = j;

						maxTop = arr[1];

						maxDown = arr[2];

					}

			}

		}

		return maxSum;



	}



	public int[] kadaneAlgo(int[] kadane) {

		int[] arr = new int[3];

		arr[0] = Integer.MIN_VALUE;

		arr[1] = 0;

		arr[2] = -1;

		int max = Integer.MIN_VALUE;

		int sum = 0;

		int localStart = 0;

		for (int i = 0; i < kadane.length; i++) {

			sum = sum + kadane[i];

			if (sum < 0) {

				sum = 0;

				localStart = i + 1;

			} else if (sum > max) {

				max = sum;

				arr[0] = max;

				arr[1] = localStart;

				arr[2] = i;

			}

		}



		if (arr[2] == -1) {

			arr[0] = 0;

			for (int i = 0; i < kadane.length; i++) {

				if (kadane[i] > arr[0]) {

					arr[0] = kadane[i];

					arr[1] = i;

					arr[2] = i;

				}

			}

		}

		return arr;

	}



	public int findmaximumInsertionsforPalindrome(String st1, String st2) {

		int[][] table = new int[st1.length() + 1][st1.length() + 1];

		for (int i = 0; i <= st1.length(); i++) {

			for (int j = 0; j <= st2.length(); j++) {

				if (i == 0 || j == 0) {

					table[i][j] = 0;

				} else if (st1.charAt(i - 1) == st2.charAt(j - 1)) {

					table[i][j] = table[i - 1][j - 1] + 1;

				} else {

					table[i][j] = Math.max(table[i][j - 1], table[i - 1][j]);

				}

			}

		}

		return st1.length() - table[st1.length()][st2.length()];

	}



	public int findLongestIncreasingSubsequence(int[] arr) {

		int n = arr.length;

		int[] lis = new int[n];



		for (int i = 0; i < n; i++) {

			lis[i] = 1;

		}



		for (int i = 1; i < n; i++) {

			for (int j = 0; j < i; j++) {

				if (arr[i] > arr[j] && lis[i] < lis[j] + 1) {

					lis[i] = lis[j] + 1;

				}

			}

		}



		int max = Integer.MIN_VALUE;

		for (int i = 0; i < n; i++) {

			max = Math.max(max, lis[i]);

		}

		return max;

	}



	public void findKthElementBST(TreeNode node, int k, List<TreeNode> list) {

		if (node == null)

			return;

		findKthElementBST(node.left, k, list);

		list.add(node);

		if (list.size() == k) {

			System.out.println(node.val);

			return;

		}

		findKthElementBST(node.right, k, list);

	}



	public void findMaxAreaHistogram(Integer[] ar) {

		Stack<Integer> st=new Stack<Integer>();

		int max_Area = Integer.MIN_VALUE;

		int i = 0;

		while (i < ar.length) {

			if (st.isEmpty() || ar[st.peek()] <= ar[i]) {

				st.push(i++);

			}

			else {

				int top = st.pop();

				int area = ar[top] * (st.isEmpty() ? i : i - st.peek() - 1);

				if (area > max_Area)

					max_Area = area;

			}

		}



		while (!st.isEmpty()) {

			int top = st.pop();

			int area = ar[top] * (st.isEmpty() ? i : i - (top - 1));

			if (area > max_Area)

				max_Area = area;

		}



		System.out.println(max_Area);

	}

	private void getFormattedDate(String date) {

		String formatteddate = null;

		DateFormat df = new SimpleDateFormat("MMM-yyyy");

		try {

			Date d1 = df.parse(date);

			formatteddate = df.format(d1);

			String findlDate = formatteddate.replaceAll("-", " ");

		} catch (Exception ex) {

			System.out.println(ex);

		}



	}



	public LinkedSet flattenLinkedList(LinkedSet node) {

		if (node == null || node.right == null)

			return node;

		node.right = flattenLinkedList(node.right);

		node = merge(node, node.right);

		printLinkedList(node);

		return node;

	}



	public LinkedSet merge(LinkedSet a, LinkedSet b) {

		if (a == null)

			return b;

		if (b == null)

			return a;

		LinkedSet result = null;

		if (a.val < b.val) {

			result = a;

			result.next = merge(result.next, b);

		} else {

			result = b;

			result.next = merge(a, result.next);

		}

		return result;

	}



	public void findRevisionPages(int[] ar, int k) {

		Map<Integer, Integer> map = new HashMap<Integer, Integer>();

		for (int i = 0; i < ar.length; i++) {

			map.put(ar[i], i);

		}

		int maxSeq = Integer.MIN_VALUE;

		int seq = 1;

		int f = 1;

		int lastIndex = 0;

		for (int i = 0; i < ar.length; i++) {

			int x = ar[i];

			f = 1;

			lastIndex = map.get(x);

			seq = 1;

			while (f == 1) {

				x = x * k;

				if (map.containsKey(x) && lastIndex < map.get(x)) {

					seq++;

					maxSeq = Math.max(maxSeq, seq);

				} else {

					f = 0;

				}

			}

		}

		System.out.println(maxSeq);

	}



	public void knapsack(int[] values, int[] wt, int W) {

		int[][] knapSack = new int[values.length + 1][W + 1];

		for (int i = 0; i <= values.length; i++) {

			for (int w = 0; w <= W; w++) {

				if (i == 0 || w == 0) {

					knapSack[i][w] = 0;

				} else if (wt[i - 1] > w) {

					knapSack[i][w] = knapSack[i - 1][w];

				} else {

					knapSack[i][w] = Math.max(knapSack[i - 1][w - wt[i - 1]] + values[i - 1],

							knapSack[i - 1][w]);

				}

			}

		}

		System.out.println(knapSack[values.length][W]);

	}



	public int findMinimumArr(int[] ar, int k) {

		List<Integer> list = new LinkedList<Integer>();

		Queue<Integer> queue = new LinkedList<Integer>();

		Stack<Integer> stack = new Stack<Integer>();

		while (true) {

			queue = fillQueue(ar, queue);

			list = fillList(list, queue);

			int min_len = findMinListSize(list, k);

			if (min_len <= list.size()) {

				return min_len;

			} else {

				stack = fillStack(ar, stack);

				list = fillList(list, stack);

				min_len = findMinListSize(list, k);

				if (min_len <= list.size()) {

					return min_len;

				}

			}

		}



	}



	public int findMinListSize(List<Integer> list, int k) {

		int n = list.size();

		int curr_sum = 0, min_len = n + 1;

		int start = 0, end = 0;

		while (end < n) {

			while (curr_sum < k && end < n)

				curr_sum += list.get(end++);



			while (curr_sum >= k && start < n) {

				if (end - start < min_len)

					min_len = end - start;

				curr_sum -= list.get(start++);

			}

		}

		return min_len;

	}



	public Stack<Integer> fillStack(int[] ar, Stack<Integer> st) {

		st.clear();

		for (int i : ar) {

			st.push(i);

		}

		return st;

	}

	public Queue<Integer> fillQueue(int[] ar, Queue<Integer> queue) {

		queue.clear();

		for (int i : ar) {

			queue.add(i);

		}

		return queue;

	}



	public List<Integer> fillList(List<Integer> list, Queue<Integer> queue) {

		while (!queue.isEmpty()) {

			list.add(queue.poll());

		}

		return list;

	}



	public List<Integer> fillList(List<Integer> list, Stack<Integer> st) {

		while (st.size() > 1) {

			list.add(st.pop());

		}

		return list;

	}



	public void printMatrixDiagonally(int[][] ar) {

		int i = 0;

		int j = 0;

		int n = ar.length;

		boolean isUp = true;



		for (int k = 0; k <= n * n;) {

			if (isUp) {

				for (; i >= 0 && j < n; i--, j++) {

					System.out.println(ar[i][j] + " ");

					k++;

				}

				if (i < 0 && j <= n - 1)

					i = 0;

				if (j == n) {

					i = i + 2;

					j = j - 1;

				}

			} else {

				for (; i < n && j >= 0; i++, j--) {

					System.out.println(ar[i][j] + " ");

					k++;

				}

				if (i <= n - 1 && j < 0)

					j = 0;

				if (i == n) {

					j = j + 2;

					i = i - 1;

				}

			}

			isUp = !isUp;

		}

	}



	public boolean findCycleInGraph(Graph g, int i, boolean[] visited, int parent) {

		LinkedList<Integer>[] adj = g.adj;

		visited[i] = true;

		Iterator<Integer> it = adj[i].iterator();

		while (it.hasNext()) {

			int v = it.next();

			if (!visited[v]) {

				if (findCycleInGraph(g, v, visited, i))

					return true;

			} else if (v != parent) {

				return true;

			}

		}

		return false;

	}



	public boolean findCycle(Graph g, boolean[] visited) {



		for (int i = 0; i < 5; i++)

			visited[i] = false;

		for (int u = 0; u < 5; u++)

			if (!visited[u])

				if (findCycleInGraph(g, u, visited, -1))

					return true;



		return false;

	}

	public int findLengthOfLargestRegion(int[][] ar) {

		boolean[][] visited = new boolean[ar.length][ar[0].length];

		int res = 0;

		int count = 0;

		int max = Integer.MIN_VALUE;

		for (int i = 0; i < ar.length; i++) {

			for (int j = 0; j < ar[i].length; i++) {

				if (!visited[i][j]) {

					res = findMaxLengthIsland(ar, visited, i, j, 0);

					max = Math.max(res, max);

				}

			}

		}

		return max;

	}



	public int findMaxLengthIsland(int[][] ar, boolean[][] visited, int i, int j, int count) {

		int[] xArr = {

				-1, -1, -1, 0, 1, 1, 1, 0

		};

		int[] yArr = {

				-1, 0, 1, 1, 1, 0, -1, -1

		};



		visited[i][j] = true;



		for (int x = 0; x < xArr.length; x++) {

			for (int y = 0; y < yArr.length; y++) {

				if (safePoint(i + xArr[x], j + yArr[y], ar, visited)) {

					count++;

					count = findMaxLengthIsland(ar, visited, i + xArr[x], j + yArr[y], count);

				}

			}

		}

		return count;

	}



	public boolean safePoint(int i, int j, int[][] ar, boolean[][] visited) {

		return (i >= 0 && i < ar.length && j >= 0 && j < ar[0].length && ar[i][j] == 1 && !visited[i][j]);

	}



	static class LRUCache {

		static Deque<Integer> deque;



		static HashSet<Integer> set;



		static int cSize;



		public LRUCache(int n) {

			deque = new LinkedList<Integer>();

			set = new HashSet<Integer>();

			cSize = n;

		}



		public static int refer(int x) {

			int index = 0;

			if (!set.contains(x)) {

				if (deque.size() == cSize) {

					int last = deque.removeLast();

					set.remove(last);

				}

			} else {

				Iterator<Integer> it = deque.iterator();

				int i = 0;

				while (it.hasNext()) {

					int val = it.next();

					if (val == x) {

						index = i;

						deque.remove(val);

						break;

					}

					i++;

				}

			}

			deque.push(x);

			set.add(x);

			return index;



		}



		public static void display() {

			Iterator<Integer> itr = deque.iterator();

			while (itr.hasNext()) {

				System.out.print(itr.next() + " ");

			}

		}

	}



	public int LIS(int[] ar) {

		int[] lis = new int[ar.length];

		for (int i = 0; i < ar.length; i++)

			lis[i] = 1;

		for (int i = 1; i < ar.length; i++) {

			for (int j = 0; j < i; j++) {

				if (ar[i] > ar[j] && lis[i] < lis[j] + 1) {

					lis[i] = lis[j] + 1;

				}

			}

		}

		int max = Integer.MIN_VALUE;

		for (int i = 0; i < ar.length; i++)

			max = Math.max(max, lis[i]);

		return max;

	}

	

	public int findMax(int[] ar,int n){

		int excl_new=0;

		int excl=0;

		int incl=ar[0];

		

		for (int i = 1; i < ar.length; i++) {

			excl_new = Math.max(excl, incl);

			incl = excl + ar[i];

			excl=excl_new;

		}

		return Math.max(excl, incl);

	}



	public boolean findValidBST(TreeNode node) {

		if (node == null)

			return true;

		if (!findValidBST(node.left))

			return false;

		if (prev != null && prev.val > node.val)

			return false;

		prev = node;

		return findValidBST(node.right);

	}

	public static int findMissingEdges(Graph g, boolean[] visited, int v) {

		LinkedList<Integer>[] adj = g.adj;

		visited[v] = true;

		Iterator<Integer> it = g.adj[v].iterator();

		while (it.hasNext()) {

			int n = it.next();

			if (!visited[v]) {

				findMissingEdges(g, visited, n);

				count++;

			}

		}

		return count;

	}



	public static int findHeightOfTrees(int[] arr) {

		if (arr.length == 0)

			return 0;

		List<Integer> list = new ArrayList<Integer>();

		for (int i : arr) {

			if (list.size() == 0 || list.get(list.size() - 1) < i)

				list.add(i);

		}

		return list.size();

	}



	public void testCode() {

		}



	public long[] change(long[] z) {

		z[1] = 5;

		return z;

	}



	public int findOptimalProduct(int[] arr, int n) {

		int index = 0;

		Double[] prods = new Double[n];

		Double prod = 1.0D;

		for (int i = 0; i < n; i++) {

			prod = prod * arr[i];

			prods[i] = prod;

		}



		Double minProd = Double.MAX_VALUE;

		for (int i = 0; i < n; i++) {

			Double leftProd = prods[i];

			Double rightProd = prod / leftProd;

			if (leftProd - rightProd > 0 && minProd > leftProd - rightProd) {

				index = i + 1;

				minProd = leftProd - rightProd;

			}

		}



		return index;

	}



	public void test() {

		BigInteger ft = new BigInteger("5000");

		BigInteger fft = new BigInteger("50000");

		BigInteger fl = new BigInteger("500000");

		BigInteger total = BigInteger.ZERO;

		total = total.add(ft);

		total = total.add(fft);

		total = total.add(fl);

		System.out.println(total);

	}



	public boolean identicalTrees(TreeNode a, TreeNode b) {

		if (a == null && b == null) {

			return true;

		}

		if (a != null && b != null) {

			return (a.val == b.val && identicalTrees(a.left, b.right) && identicalTrees(a.right, b.right));

		}

		return false;

	}



	public static void reverseBitsNumber(int n) {

		int reverse_num = 0;

		int numBits = 0;

		int temp = 0;

		while (temp <= n) {

			temp = (int)(temp + Math.pow(2, numBits));

			numBits++;

		}

		for (int i = 0; i < numBits; i++) {

			if ((n & (1 << i)) == 1)

				reverse_num |= 1 << ((numBits - 1) - i);

		}



		System.out.println(reverse_num);

	}

	public void sortLinkedList(LinkedSet node) {

		if (node == null)

			return;

		LinkedSet prev = node;

		LinkedSet head = node;

		LinkedSet curr = node.next;

		printLinkedList(head);

		while (curr != null) {

			if (curr.val < prev.val) {

				prev.next = curr.next;

				curr.next = head;

				head = curr;

				curr = prev;

			} else {

				prev = curr;

			}

			curr = curr.next;

		}

		printLinkedList(head);

	}



	// { 12, 1, 78, 90, 57, 89, 56 };

	public void slidingMax(int[] ar, int k) {

		int n = ar.length;

		Deque<Integer> q = new LinkedList<Integer>();

		int i = 0;

		for (i = 0; i < k; i++) {

			while (!q.isEmpty() && ar[i] >= ar[q.peekLast()]) {

				q.removeLast();

			}

			q.addLast(i);

		}



		for (; i < n; i++) {

			System.out.print(ar[q.peek()] + "->");

			while (!q.isEmpty() && q.peek() <= i - k) {

				q.removeFirst();

			}



			while (!q.isEmpty() && ar[i] >= ar[q.peekLast()]) {

				q.removeLast();

			}



			q.addLast(i);

		}

		System.out.print(ar[q.peek()]);



	}



	public boolean searchAnElementRotatedArray(int k) {

		int[] ar = {

				5, 6, 7, 8, 9, 10, 1, 2, 3

		};

		int pivot = findPivot(ar, 0, ar.length - 1);

		if(pivot==-1)

			return binarySrch(ar, 0, ar.length - 1, k);

		if (ar[0] > k) {

			return binarySrch(ar, pivot + 1, ar.length - 1, k);

		} else

			return binarySrch(ar, 0, pivot - 1, k);

	}



	private boolean binarySrch(int[] ar, int low, int high,int k) {

		if(low<=high){

			int mid=(low+high)/2;

			if (ar[mid] == k)

				return true;

			else if (ar[mid] < k)

				return binarySrch(ar, mid + 1, high, k);

			return binarySrch(ar, low, mid - 1, k);

		}

		return false;

	}



	private int findPivot(int[] ar, int low, int high) {

		if (low > high)

			return -1;

			int mid = (low + high) / 2;

			if (mid == low || mid == high || (ar[mid] > ar[mid - 1] && ar[mid] > ar[mid + 1])) {

				return mid;

			} else if (ar[mid] > low) {

				return findPivot(ar, mid + 1, high);

			} else {

				return findPivot(ar, low, mid - 1);

			}

	}



	public void printMatrixSpiral(int[][] ar, int k) {

		int dir=0;

		int left=0;

		int right = ar[0].length - 1;

		int top=0;

		int bottom = ar.length - 1;

		int count = 0;

		int temp = -1;

		while (top < bottom && left < right) {

			if ((dir % 4) == 0) {

				for (int j = left; j <= right; j++) {

					System.out.print(ar[top][j] + "-");

					count++;

					if (count == k)

						temp = ar[top][j];

				}

				dir++;

				top++;

			}

			if ((dir % 4) == 1) {

				for (int j = top; j <= bottom; j++) {

					System.out.print(ar[j][right] + "-");

					count++;

					if (count == k)

						temp = ar[j][right];

				}

				dir++;

				right--;

			}

			if ((dir % 4) == 2) {

				for (int j = right; j >= left; j--) {

					System.out.print(ar[bottom][j] + "-");

					count++;

					if (count == k)

						temp = ar[bottom][j];

				}

				dir++;

				bottom--;

			}

			if ((dir % 4) == 3) {

				for (int j = bottom; j >= top; j--) {

					System.out.print(ar[j][left] + "-");

					count++;

					if (count == k)

						temp = ar[j][left];

				}

				dir++;

				left++;

			}

		}

		System.out.println("Element at " + k + " position :" + temp);

	}



	public void printJumpingNumbers(int x) {

		System.out.println("0 ");

		for (int i = 1; i <= 9 && i <= x; i++) {

			this.bfsJumping(x, i);

		}

	}

		private void bfsJumping(int x, int i) {

		Queue<Integer> q = new LinkedList<Integer>();

		q.add(i);



		while (!q.isEmpty()) {

			int temp = q.poll();

			if (temp <= x) {

				System.out.print(temp + "-");

				int lastDigit = temp % 10;

				if (lastDigit == 0)

					q.add(10 * temp + (lastDigit + 1));

				else if (lastDigit == 9)

					q.add(10 * temp + (lastDigit - 1));

				else {

					q.add(10 * temp + (lastDigit - 1));

					q.add(10 * temp + (lastDigit + 1));

				}

			}

		}



	}



	public void nge(int[] ar) {

		Stack<Integer> st = new Stack<Integer>();

		for (int i = ar.length - 1; i >= 0; i--) {

			while (!st.isEmpty() && ar[i] >= st.peek())

				st.pop();

			System.out.println(st.isEmpty() ? "-1" : st.peek());

			st.push(ar[i]);

		}

	}



	public void alternateElementsMaxSum(int[] ar) {

		int excl = 0;

		int incl = ar[0];

		int exclNew = -1;



		for (int i = 1; i < ar.length; i++) {

			exclNew = (incl > excl) ? incl : excl;

			incl = excl + ar[i];

			excl = exclNew;

		}



		System.out.println(Math.max(incl, excl));

	}



	public void findMaxFlippingZeroes(int[] ar) {

		int zeroCount = 0;

		int maxCount = 0;

		int count = 0;

		for (int i = 0; i < ar.length; i++) {

			if (ar[i] == 0)

				zeroCount++;

			int val = (ar[i] == 1) ? 1 : -1;

			count = Math.max(val, count + val);

			maxCount = Math.max(maxCount, count);

		}

		maxCount = Math.max(0, maxCount);

		System.out.println(zeroCount + maxCount);

	}



	public void findMaxProduct(int[] ar) {

		int maxProd = 0;

		int minProd = 0;

		for (int i = 0; i < ar.length; i++) {

			if (ar[i] < 0) {

				int temp = maxProd;

				maxProd = minProd;

				minProd = temp;

			}

			maxProd = Math.max(ar[i], maxProd * ar[i]);

			minProd = Math.max(ar[i], minProd * ar[i]);

		}

		System.out.println(Math.max(minProd, maxProd));

	}

	

	public int findDistanceBetweenNode(TreeNode a, TreeNode b, TreeNode root) {

		if (root == null)

			return 0;

		if (root.val > a.val && root.val > b.val) {

			return findDistanceBetweenNode(a, b, root.left);

		} else if (root.val < a.val && root.val < b.val) {

			return findDistanceBetweenNode(a, b, root.right);

		} else {

			return findNodeDistance(a, root) + findNodeDistance(b, root);

		}

	}



	public int findNodeDistance(TreeNode a, TreeNode root) {

		if (root == null || root.val == a.val)

			return 0;

		else if (root.val > a.val)

			return 1 + findNodeDistance(a, root.left);

		return 1 + findNodeDistance(a, root.right);

	}



	public int sortedAndRotatedArray(int[] ar) {

		int mid = 0;

		int low = 0;

		int high = ar.length - 1;

		while (low <= high) {

			mid = (low + high) / 2;

			if ((mid == 0 && ar[mid] > ar[mid + 1]) || (mid == ar.length - 1 && ar[mid] > ar[mid - 1])

					|| (ar[mid - 1] < ar[mid] && ar[mid + 1] < ar[mid])) {

				return mid;

			} else if (ar[low] < ar[mid]) {

				low = mid + 1;

			} else

				high = mid - 1;

		}

		return -1;

	}



	public int findElement(int[] ar, int k) {

		if (ar.length == 1)

			return ar[0] == k ? 0 : -1;

		int pivot = sortedAndRotatedArray(ar);

		if (ar[pivot] == k)

			return pivot;

		if (pivot == -1)

			return -1;

		if (ar[pivot - 1] > k) {

			for (int i = 0; i < pivot; i++) {

				if (ar[i] == k)

					return i;

			}

		} else {

			for (int i = pivot + 1; i < ar.length; i++) {

				if (ar[i] == k)

					return i;

			}

		}

		return -1;

	}

	public void executeFuturetask() {

		ExecutorService executor = Executors.newFixedThreadPool(10);

		List<Future<String>> list = new ArrayList<Future<String>>();

		final AtomicInteger count = new AtomicInteger(0);

		Callable<String> callable = new Callable<String>() {



			@Override

			public String call() {

				if ((count.incrementAndGet() % 2) != 0)

					return "Hi";

				return "Hello";

			}

		};



		for (int i = 0; i < 50; i++) {

			Future<String> fut = executor.submit(callable);

			list.add(fut);

		}



		for (Future<String> fut : list) {

			try {

				// print the return value of Future, notice the output delay in console

				// because Future.get() waits for task to get completed

				System.out.println(fut.get());

			} catch (InterruptedException | ExecutionException e) {

				e.printStackTrace();

			}

		}

		// shut down the executor service now

		executor.shutdown();

	}



	public void writeLogs(String projectId, String podName) {

		String to = "deepak.srivastava@barclays.com";// change accordingly

		String from = "deepak.srivastava@barclays.com";

		String host = "localhost";// or IP address



		// Get the session object

		Properties properties = System.getProperties();

		properties.setProperty("mail.smtp.host", host);

		Session session = Session.getDefaultInstance(properties);



		// compose the message

		try {

			MimeMessage message = new MimeMessage(session);

			message.setFrom(new InternetAddress(from));

			message.addRecipient(Message.RecipientType.TO, new InternetAddress(to));

			message.setSubject("Ping");

			message.setText("Hello, this is example of sending email  ");



			// Send message

			Transport.send(message);

			System.out.println("message sent successfully....");



		} catch (MessagingException mex) {

			// mex.printStackTrace();

			// System.exit(0);

		}

	}

}





