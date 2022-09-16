형변환
======

https://coding-factory.tistory.com/130

## String[] <-> int[] 
        int[] nums = Arrays.stream(strings).mapToInt(Integer::parseInt).toArray();

        String[] strArray = Arrays.stream(intArray).mapToObj(String::valueOf).toArray(String[]::new);

## String <-> int[]
        String str = Arrays.toString(arr);

        int[] digits = Stream.of(str.split("")).mapToInt(Integer::parseInt).toArray();

## String <-> char[]
        char[] chs = str.toCharArray();

        String str = String.valueOf(arr);

## String[] <-> List
        List<String> list = Arrays.asList(arr);
        
## Integer <-> int
        int b[] = Arrays.stream(a).mapToInt(Integer::intValue).toArray(); 

        Integer b[] = Arrays.stream(a).boxed().toArray(Integer[]::new); 
        
## Long to int 
        int l = Long.valueOf(left).intValue();





## HashMap Value 값으로 정렬

        List<Integer> list = new ArrayList<>(hm.keySet());
        Collections.sort(list, (o1, o2) -> Double.compare(hm.get(o2), hm.get(o1)));
        answer = list.stream().mapToInt(Integer::intValue).toArray();


## n진수 뒤집기와 parseInt로 진법 변환
        
        a = new StringBuilder(a).reverse().toString();
        return Integer.parseInt(a,n);
        
## 행렬 row col 구하기
        3x3 행렬을 1,2,3,4,5,6,7,8,9 라고 나타낼 때,
        5에 해당하는 row와 col의 값은 5의 index(=4)를 n(=3)으로 나눈 뒤 1을 더한다. 
        4/3+1 , 4%3+1
