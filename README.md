# salesbit_project_submission

This project is make with the help of Angular on the frondend side and the server takes the help of node.js.

###Entities -
Block-
    block_no: {type: String, required: true, unique: true},
    yard:{type:String, default:''},
    yard_history:{type:Array, default:[]},
    date: {type:String, default:''},
    hsn_code: {type:String, default:''},
    quarry: {type:String, default:''},
    grade: {type:String},
    shade:{type:String},
    weight:{type:Number, default:0},
    dim_1:{type:Number, default:0},
    dim_2:{type:Number, default:0},
    dim_3:{type:Number, default:0},
    note:{type:String, default:''},
    slabs:{type:Boolean, default:false},
    sold:{type:Number, default:0},
    reserved:{type:Number, default:0},
    transportation_cost:{type:Number, default:0},
    cost:{type:Number, default:0},
    in_transit:{type:Boolean, default:false},
    has_children:{type:Boolean, default:false},
    children:{type:Array, default:[]},
    is_child:{type:Boolean, default:false},
    company:{type:String, default:''},
    unit:{type:String, default:''},
    processing_cost:{type:Number, default:0},
    processor:{type:String, default:''},
    layer_type:{type:String}
    
 Company -
    company: {type:String, require:true, unique:true},
    line_1: {type:String, default:''},
    line_2: {type:String, default:''},
    line_3: {type:String, default:''},
    terms:{type:String, default:''}
    
 Invoice-
    trade_id: {type: String, required: true, unique: true},
    date: {type: String, default:''},
    dispatched: {type: Boolean, default:false},
    company: {type: String, default:''},
    igst: {type: Number, default:0},
    cgst: {type:Number, default: 0},
    sgst: {type: Number, default:0},
    shipping_address: {type:String, default:''},
    supply_state:{type:String, default:''},
    sale_type: {type:String, default:''},
    party: {type: String, default:''},
    user: {type: String, required: true},
    eway_bill_no: {type: String, default: ''},
    royalty_no: {type: String, default: ''},
    transportation_mode: {type: String, default:''},
    customer_ref_no: {type: String, default: ''},
    quotation: {type: Boolean}
 
 Quarry-
    quarry: {type:String, require:true, unique:true},
    quarry_address: {type:String, default:''},
    specific_gravity:{type:Number, default:0},
    block_type:{type:String, default:''},
    grade:{type:String, default:''},
    shade:{type:String, default:''},
    hsn_code:{type:String, default:''},
    slabs_hsn_code: {type:String, default: ''}

Slabs-
    block_no:{type: String, require:true, unique:true},
    yard:{type: String, default:''},
    yard_history:{type:Array, default: []},
    processor:{type: String, default:''},
    date:{type:String, default:''},
    dim_1:{type:Number, default:0},
    dim_2:{type:Number, default:0},
    dim_3:{type:Number, default:0},
    no_of_slabs:{type:Number, default:0},
    transportation_cost:{type:Number, default:0},
    processing_cost:{type:Number, default:0},
    cost:{type:Number, default:0},
    lost:{type:Number, default:0},
    weight:{type:Number, default:0},
    note:{type:String, default:''},
    sold:{type:Number, default:0},
    reserved: {type:Number, default:0},
    polished: {type:Boolean, default:false},
    polishing_cost: {type: Number, default:0},
    polishing_date: {type: String, default:''},
    in_transit:{type:Boolean, default:false},
    slabs_hsn_code: {type:String, default:''},
    unit: {type:Number, default:''}
    
Trade - 
    block_no: {type:String, require:true},
    trade_id: {type:String, default:''},
    user: {type: String, default:''},
    slabs: {type:Boolean, default:false},
    is_child: {type: Boolean, default:false},
    sold:{type:Number, require:true},
    reserved:{type:Number, require:true},
    cost:{type:Number, default:0},
    qty: {type: Number, default:0},
    r_dim_1:{type:Number, default:0},
    r_dim_2:{type:Number, default:0},
    r_dim_3:{type:Number, default:0},
    dim_1:{type:Number, default:0},
    dim_2:{type:Number, default:0},
    dim_3:{type:Number, default:0},
    round_off: {type: Boolean, default:false},
    hsn: {type: String, defult:''},
    quotation: {type: Boolean}
    
 User-
    user: {type:String, require:true, unique:true},
    name: {type:String, require:true},
    password: {type:String, require:true},
    admin_role: {type:Boolean, default:false},
    moderator_role:{type:Boolean, default:false},
    salesman_role:{type:Boolean, default:false},
    forgot_password_secret:{type:String, default:''}
    
Yard -
    yard: {type:String, require:true, unique:true},
    yard_address: {type:String, default:''}

Abstract:
. Introduction
This Software Requirements Specification provides a complete description of all
the functions and specifications of the webapp Salesbit.
The main objective of this web application is to ease the workflow of mining
industries by making them able to manage all their inventory and sales data
effortlessly and analysing the reports for any scope of improvement.
1.2. Scope
The scope of this project is very broad as it can be used by any stone mining
industry, it could be granite, marble, etc. Some other advantages are :
-> As it is a webapp, it can be used on any platform.
-> Data updates instantly, so it can be used by any person regardless of where
he/she is located, as they view the real-tim

This system will be used in Three User Modules which are Administrator,
Manager, and Salesman. As all of these have different requirements the modules
are designed to meet their needs and avoid any type of confusion. The Uses of
all three User Modules have been described below.
[1] User can do the following functions in the Administrator Module
-> View overall Stock/Sales figures.
-> Assign Roles to other users (Manager or Salesman).
-> View Sales activity.
[2] User can do the following functions in the Administrator Module
13
-> Add/Remove Block.
-> Add/Remove Company.
-> Add/Remove Quarry.
-> Add/Remove Yard.
-> Add/Remove Party.
-> Add/Remove Units.
-> Process/Move blocks.
[3] User can do the following functions in the Salesman Module
-> View Inventory.
-> Sell or Reserve Blocks/Slabs

This solution will solve the problem of stock and sales
management for the excavation/mining industry. This can
also reduce the manpower required for managing the data
during the process thus improving the business efficiency.
This web application covers all the aspects of stock and sales
management from the excavation of stone to processing to
selling it off.

