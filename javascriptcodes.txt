// Subscribe form Validation
var submitBtn = document.getElementById("submit-btn");
var subscribeEmail = document.getElementById("email");
var errorMsg = document.getElementById("errorMsg");

// Add the click event listener to trigger the submit button 
submitBtn.addEventListener('click', function(e){
    e.preventDefault();

    if(subscribeEmail.value === ""){
        errorMsg.style.backgroundColor = "#726DA8";
        errorMsg.innerHTML = "Please fill in your email!";
    } else{
        errorMsg.style.backgroundColor = "#726DA8";
        subscribeEmail.value = "";
        errorMsg.innerHTML = "Your email has been received!";
    }

    setTimeout(function(){
        errorMsg.style.backgroundColor = null;
        errorMsg.innerHTML = "";
    }, 3000)
})


// Get a Quote form validation
var userNameQuote = document.getElementById("username-quote");
var emailQuote = document.getElementById("email-quote");
var messageQuote = document.getElementById("message-quote");
var submitQuoteBtn = document.getElementById("submit-quote");
var quoteErrorMsg = document.getElementById("quoteErrorMsg");

// Add the click event listener to trigger the submit quote button 
submitQuoteBtn.addEventListener('click', function(e){
    e.preventDefault();

    if(userNameQuote.value === "" || emailQuote.value === "" || messageQuote.value === "" ){
        //what should happen?
        quoteErrorMsg.style.backgroundColor = "#b8336a";
        quoteErrorMsg.innerHTML = "Please ensure all inputs are filled!";
    } else {
        userNameQuote.value = "";
        emailQuote.value = "";
        messageQuote.value = "";
        quoteErrorMsg.style.backgroundColor = "#b8336a";
        quoteErrorMsg.innerHTML = "Your Message has been received!";
    }

    setTimeout(function(){
        quoteErrorMsg.style.backgroundColor = null;
        quoteErrorMsg.innerHTML = "";
    }, 3000)
})
