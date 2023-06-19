describe('Slider Test', () => {
    it('should validate the range value of the slider', () => {
      cy.visit('https://www.lambdatest.com/selenium-playground');
      
        
      // Click on "Drag & Drop Sliders" option
      cy.contains('Drag & Drop Sliders').click();
      
      // Select the slider "Default value 15"
      cy.get('#slider1 input[type="range"]').as('slider');
      
      // Drag the slider to make it 95
      cy.get('@slider').invoke('val', 95).trigger('input');
      
      // Validate the range value shows 95
      cy.get('@slider').should('have.value', '95');
    });
  });
  
