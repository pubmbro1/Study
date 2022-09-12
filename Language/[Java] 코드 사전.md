#HashMap Value 값으로 정렬

        List<Integer> list = new ArrayList<>(hm.keySet());
        Collections.sort(list, (o1, o2) -> Double.compare(hm.get(o2), hm.get(o1)));
        answer = list.stream().mapToInt(Integer::intValue).toArray();


# n진수 뒤집기와 parseInt로 진법 변환
        
        a = new StringBuilder(a).reverse().toString();
        return Integer.parseInt(a,n);
