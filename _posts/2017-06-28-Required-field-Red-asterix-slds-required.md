---
published: true
---

### Simple code explaining use of slds-required to get red asterixs for input fields label.

o/p

![slds-required]({{site.baseurl}}/_posts/slds-required red asterix for input controls.png)

```html
                            <div class="slds-form-element">
                                <label class="slds-form-element__label" for="cusinfocomp-input4">
                                    <!-- NCS-00784 2017-03-25 darshan.gosar@bluewolf.com Updated to include check for isTHNK as Email is mandatory for THNK subscription -->    
                                    <aura:if isTrue="{!v.required}">
                                        <abbr class="slds-required" title="required" aura:id="emailReq">*											</abbr>
                                    </aura:if>
                                    Email Address</label>
                                <div class="slds-form-element__control">
                                    <ui:inputText aura:id="cusinfocomp-input4" class="slds-input" value="{!v.contact.Email}" blur="{!c.checkValidate}"/>
                                </div>
                            </div>
```
