---
layout: page
navigation_title: Membership
title: New Members
index: 3
---
{% capture text %}
<p>
    If you would like more information on becoming a member, send us a message below or at <b>ugasbi16@gmail.com</b>! A semester-long membership is <b>$20</b>, and a yearly membership is <b>$30</b>. Membership includes ability to attend all events/meetings for free, free t-shirt, your resume in a resume book given out to top business intelligence companies, and ability to vote and participate in annual executive board elections.
</p>
{% endcapture %}
{% capture image %}
<img src="http://ugasbi.weebly.com/uploads/8/0/8/1/80816214/14067771-1755717001350266-5769605577768963058-o-orig_orig.jpg">
{% endcapture %}
<div class="row">
<div class="col-md-6 col-sm-12">
{{ text }}
<div class="col-md-12">
    <button type="button" class="btn btn-success btn-lg btn-block">Yearly Membership</button>
    <button type="button" class="btn btn-info btn-lg btn-block">Monthly Membership</button>
</div>
</div>
<div class="col-md-6 col-sm-12 sm-offset">
{{ image }}
</div>
</div>

<div class="row">
    <hr />
    <div class="col-md-12 col-sm-12">
    <h4 class="contact-title">Questions? Comments? Contact Us!</h4>
    <form action="https://getsimpleform.com/messages?form_api_token=bd935738dde5d3606ce553ff3922d30e" method="post">
    <input type='hidden' name='redirect_to' value='{{ site.baseurl }}' />
        <div class="form-group">
            <label for="name" class="cols-sm-2 control-label">Your Name</label>
            <div class="cols-sm-10">
                <div class="input-group">
                    <span class="input-group-addon"><i class="fa fa-user fa" aria-hidden="true"></i></span>
                    <input type="text" class="form-control" name="name" id="name"  placeholder="Enter your Name"/>
                </div>
            </div>
        </div>
        <div class="form-group">
            <label for="email" class="cols-sm-2 control-label">Your Email</label>
            <div class="cols-sm-10">
                <div class="input-group">
                    <span class="input-group-addon"><i class="fa fa-envelope fa" aria-hidden="true"></i></span>
                    <input type="text" class="form-control" name="email" id="email"  placeholder="Enter your Email"/>
                </div>
            </div>
        </div>
        <div class="form-group">
            <label for="comments" class="cols-sm-2 control-label">Comments</label>
            <div class="cols-sm-10">
                <div class="input-group">
                    <span class="input-group-addon"><i class="fa fa-users fa" aria-hidden="true"></i></span>
                    <textarea class="form-control" name="comments" id="comments"  placeholder="Comments or questions!" rows="5"></textarea>
                </div>
            </div>
        </div>
        <div class="form-group ">
            <input class="btn btn-primary btn-lg btn-block login-button" type='submit' value='Send Message' />
        </div>  
    </form>
</div>
</div>