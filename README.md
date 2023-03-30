# car-rental
1. Create a new custom object for cars by going to Setup > Object Manager and clicking the New Custom Object button. Give the object a label and name, such as "Car", and add the following fields:

Name (Text)
Model (Picklist with values of "Honda Civic", "Toyota Corolla", and "Ford Mustang")
Color (Text)
Rental Rate (Currency)
2. Create a new Visualforce page for booking a car by going to Setup > Develop > Pages and clicking the New button. Give the page a name, such as "CarBooking", and paste the following code into the markup editor:
<apex:page controller="CarRentalController">
    <apex:form>
        <apex:pageBlock title="Car Rental Booking">
            <apex:pageMessages />
            <apex:pageBlockSection>
                <apex:inputField value="{!selectedCarModel}" label="Car Model"/>
                <apex:inputField value="{!selectedPickupDate}" label="Pick-up Date"/>
                <apex:inputField value="{!selectedReturnDate}" label="Return Date"/>
            </apex:pageBlockSection>
            <apex:pageBlockButtons>
                <apex:commandButton action="{!bookCar}" value="Book Car"/>
            </apex:pageBlockButtons>
        </apex:pageBlock>
    </apex:form>
</apex:page>
