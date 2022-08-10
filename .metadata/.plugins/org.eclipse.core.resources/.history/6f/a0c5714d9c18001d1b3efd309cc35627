package com.hexaware.java8examples.practicequestion;

import java.util.ArrayList;
import java.util.stream.Collectors;
import java.util.List;

public class AddingSeller {
	ArrayList<Seller> sellerList = new ArrayList<Seller>(); 
	public void addingelements() {
		
		Seller obj = new Seller(1,"Gaurav","g@gmail.com","Lucknow");
		Seller obj1 = new Seller(2,"Bhuvana","bh@gmail.com","Hyderabad");
		Seller obj2 = new Seller(3,"Vishwas","v@gmail.com","Delhi");
		Seller obj3 = new Seller(4,"Vyankatesh","vy@gmail.com","Noida");
		sellerList.add(obj);
		sellerList.add(obj1);
		sellerList.add(obj2);
		sellerList.add(obj3);
	}
	public void display() {
		sellerList.stream().forEach((seller) -> System.out.println(seller));
	}
	public void addNewSeller(int sellerId, String sellerName, String sellerLocation, String sellerEmail) {
		Seller objj = new Seller(sellerId,sellerName, sellerLocation, sellerEmail);
		sellerList.add(objj);
		System.out.println("New Seller Added");
		display();
	}
	
	
	public void searchById(int id) {
		sellerList.stream()
		.filter((seller) -> id == seller.getSellerId())
		.forEach((seller) -> System.out.println(seller));
	}
	
	
	public void deleteById(int id) {
		
		sellerList =  (ArrayList<Seller>) sellerList.stream()
		.filter((seller) -> id != seller.getSellerId())
		.collect(Collectors.toList());
		
		sellerList.stream()
		.forEach((seller) -> System.out.println(seller));
	}
	
	public void updateById(int id, String name, String location, String email) {
		sellerList.stream()
		.filter((seller) -> id == seller.getSellerId())
		.forEach((seller) -> {
			seller.setSellerId(id);
			seller.setSellerName(name);
			seller.setSellerEmail(email);
			seller.setSellerLocation(location);
		});
		
		sellerList.stream().forEach((seller) -> System.out.println(seller));

	}
	
	public void displayByLocation(String location) {
		sellerList.stream()
		.filter((seller) -> location.equals(seller.getSellerLocation()))
		.forEach((seller) -> System.out.println(seller));
	}
	
	
}
