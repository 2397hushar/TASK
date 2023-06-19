

describe('submit form data', () => {

  it('page loading', () => {

cy.visit('https://www.lambdatest.com/selenium-playground') 

  cy.contains('Input Form Submit').click();

  cy.get('#name').type("tushar")
  cy.get('#inputEmail4').type("tusharsangale6855@gmail.com")
  cy.get('input[type="password"]').type("tushar1233")
  cy.get('#company').type("Google")
  cy.get('#websitename').type("www.google.com")
  cy.get(':nth-child(3) > .pr-20 > .w-full').select("India");
  cy.get('#inputCity').type("Mumbai")
  cy.get("input[name='address_line1']").type("Mumbai East")
  cy.get("input[name='address_line2']").type("Mumbai Wast")
cy.get("input[placeholder='State']").type("Maharashtra")
cy.get('#inputZip').type("413738")

cy.get('.bg-lambda-900').click();



cy.get("p[class='success-msg hidden").should("have.text",'Thanks for contacting us, we will get back to you shortly.')

cy.window().then((win) => {
  win.close();
});


  })
    
    })
  
  






