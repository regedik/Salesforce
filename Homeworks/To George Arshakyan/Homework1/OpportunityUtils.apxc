public class OpportunityUtils {
    
    private static final Integer AMOUNT_OF_OPPORTUNITY_LINE_ITEM = 10;
    
    public static void insertTenOLIsPerOpportunity(List<Opportunity> oppList) {
        List<OpportunityLineItem> listOfOpportunityLineItem = new List<OpportunityLineItem>();
        
        // To create OpportunityLineItem record it is required to set PricebookEntryId
        PricebookEntry pricebook = [SELECT Id FROM PricebookEntry LIMIT 1];
        
        for (Opportunity opp : oppList) {
            for (Integer i = 0; i<AMOUNT_OF_OPPORTUNITY_LINE_ITEM; i++) {
            	listOfOpportunityLineItem.add(new OpportunityLineItem(Quantity = 0.5, TotalPrice = 10, 
                		PricebookEntryId = pricebook.Id, OpportunityId = opp.Id));
            }
        }
        
        insert listOfOpportunityLineItem;
    }
}