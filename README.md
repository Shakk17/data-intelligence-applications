# Team project for Data Intelligence Applications course @ PoliMi (AY 18/19)

This project has been realized by Bonfanti Luca, Crippa Dominic, Krasniqi Filip and Pina Alessandro.

It received a mark of **30/30 (cum laude)** by professor Gatti.

The project consisted in solving two tasks: the first one regards the concept of **Online Pricing**, while the second one is about **Online Advertising**.

## Online Pricing

**Online pricing** is a problem subject to many factors that can affect its complexity.

Such a problem consists in choosing, given a demand curve, the selling price to maximize profit given by the sale of a certain product.

In a context in which the demand curve is unknown, such a function can be learned by an algorithm that is able to compute it for defined values of price. 

The complexity of the problem depends on how this function varies. Usually, the demand curve is not only a function of the price, but also of the time (non stationary environments). 

A common formalization of this problem has a distinction between *abrupt changes* and *smooth changes*. 

The first one describes how the function varies between big intervals of time named phases (e.g. seasons), identified by unknown breakpoints.
The second one describes how the function varies inside a phase. 

Together with this aspect (that literally introduces a demand curve as a function depending on two variables), we also need to consider the presence of contexts. 

A **context** identifies how different classes of users are combined together into subcontexts, each of which is described by a demand curve that follows the previously described characteristics. 
Being aware of this issue, an algorithm that selects the best price to maximize the profit should do the same by also considering the possible context alternatives. 

**Profit maximization** would be a problem of selecting not only the best price, but also the best context, i.e., how to group the classes of users.

The **goal** of this report is to show how we formalized the problem and applied **Multi-Armed Bandit algorithms** to find the best setting, while showing results in terms of regret in two different scenarios: with and without context generation. 


## Online Advertising

**Online advertising** is a problem that has become very popular since the digitalization of our society. 

In a typical online advertising setting we have 3 different roles:
- the *user/customer*, the people that are targeted by the ads;
- the *publisher*, whoever owns the platform on which the ads are published;
- the *advertiser*, whoever wants to publish the ads.

There are many different formats for an advertising campaign, but we focus our attention on **search and social advertising**. 

For both of these formats we choose as payment schema the cost per click schema, i.e. the advertiser pays the publisher only when the targeted user clicks on the ad displayed.

The **goal** of this report is to show an **algorithm that maximizes the reward** provided from clicks as a function of the budget in a simulated scenario containing different sub-campaigns, and an **algorithm that selects how to group the users** assuming that they are characterized by different features that imply different reward curves.
