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


  

  
  

  


  
