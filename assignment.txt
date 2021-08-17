// 1st problem solution

function seerToMon(seer) {

    if (seer < 0) {
        var errorMessage = "It's not acceptable input";
        return errorMessage;
    }
    else if (typeof seer != "number") {
        var errorMessage = "please input a number";
        return errorMessage;
    }
    var Mon = seer / 40;
    return Mon;
}

console.log(seerToMon(240));

// 2nd problem solution

function totalSales(ShirtNumber, PantNumber, ShoeNumber) {
    if (ShirtNumber < 0 || PantNumber < 0 || ShoeNumber < 0) {
        var errorMessage = "It's not acceptable input";
        return errorMessage;
    }
    else if (typeof ShirtNumber != "number" || typeof PantNumber != "number" || typeof ShoeNumber != "number") {
        var errorMessage = "please input numbers";
        return errorMessage;
    }
    let totalShirtPrice = ShirtNumber * 100;
    let totalPantPrice = PantNumber * 200;
    let totalShoePrice = ShoeNumber * 500;

    let totalPrice = totalShirtPrice + totalPantPrice + totalShoePrice;
    return totalPrice;

}

let money = totalSales(4, 3, 1);
console.log(money);


// 3rd problem solution

function deliveryCost(tshirtNumber) {
    if (tshirtNumber < 0) {
        var errorMessage = "It's not acceptable input";
        return errorMessage;
    }
    else if (typeof tshirtNumber != "number") {
        var errorMessage = "please input a number";
        return errorMessage;
    }
    else if (tshirtNumber <= 100) {
        var shippingCost = tshirtNumber * 100;
        return shippingCost;
    }
    else if (tshirtNumber > 100 && tshirtNumber <= 200) {
        var tshirtCountAfter100 = tshirtNumber - 100;
        var shippingCost = (100 * 100) + tshirtCountAfter100 * 80;
        return shippingCost;
    }
    else {
        var tshirtCountAfter200 = tshirtNumber - 200;
        var shippingCost = (100 * 100) + (100 * 80) + tshirtCountAfter200 * 50;
        return shippingCost;
    }

}

console.log(deliveryCost(250));


// 4th problem solution

function perfectFriend(friends) {
    if (Array.isArray(friends) != true) {
        var errorMessage = "please enter an array";
        return errorMessage;
    }
    for (let friend of friends) {
        if (typeof friend != "string") {
            var errorMessage = "input is not acceptable ";
            return errorMessage;
        }
        else if (friend.length == 5) {
            return friend;
        }
    }

}

var friendsArray = ["ron", "Abdullah", "Rafi", "fahim", "abir", "akash", "sifat"]
console.log(perfectFriend(friendsArray));
