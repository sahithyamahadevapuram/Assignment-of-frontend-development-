# Assignment-of-frontend-development-
based on questions 
1. Find the missing numbers in the series.
2
3
10
15
26
35
50
63
public static int getMissingNumber(int[] inputArray, int n)
{
    int i, total;
    total = (n + 1) * (n + 2) / 2;
    for (i = 0; i < n; i++)
         total -= inputArray[i];
 
    return total;
}
Call this from Main method.
2
3
10
15
26
35
50
63
static void Main(string[] args)
{
  int[] arrValues = new int[] { 2,3,10,15,26,35,50,63 };
  int number = getMissingNumber(arrValues, arrValues.Length);
  Console.WriteLine("The missing number is "+ number);
  Console.ReadLine();
}

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>



2. Create a dynamic component in Angular which has nested components in the fallowing manner
import { Directive, ViewContainerRef } from '@angular/core';

@Directive({
  selector: '[adHost]',
})
export class AdDirective {
  constructor(public viewContainerRef: ViewContainerRef) { }
}
            <div class="nested component-example">
              <h3>x component</h3>
              <ng-template adHost></ng-template>
            </div>
          export class AdBannerComponent implements OnInit, OnDestroy {
  @Input() ads: AdItem[];
  currentAdIndex = -1;
  @ViewChild(AdDirective, {static: true}) adHost: AdDirective;
  interval: any;

  constructor(private componentFactoryResolver: ComponentFactoryResolver) { }

  ngOnInit() {
    this.loadComponent();
    this.getAds();
  }

  ngOnDestroy() {
    clearInterval(this.interval);
  }

  loadComponent() {
    this.currentAdIndex = (this.currentAdIndex + 1) % this.ads.length;
    const adItem = this.ads[this.currentAdIndex];

    const componentFactory = this.x component.resolve (component(adItem.component);

    const viewContainerRef = this.adHost.viewContainerRef;
    viewContainerRef.clear();

    const componentRef = viewContainerRef.createComponent<AdComponent>(X component);
    componentRef.instance.data = adItem.data;
  }

  getAds() {
    this.interval = setInterval(() => {
      this.loadComponent();
    }, x component);
  }
}
import { Component, Input } from '@angular/core';

import { Adcomponent } from './ad.component';

@Component({
  template: `
    <div class="ComponentY">
      <h4>{{data.headline}}</h4>

      {{data.body}}
    </div>
  `
})
export {x1{y1,y2},x2{y3,y4}}Component implements AdComponent {
  @Input() data: any;

}


>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>



3.Making a form

import { Component } from '@angular/core';
import { FormGroup, FormControl } from '@angular/forms';

@Component({
  selector: 'app-profile-editor',
  templateUrl: './profile-editor.component.html',
  styleUrls: ['./profile-editor.component.css']
})
export class ProfileEditorComponent {
  profileForm = new FormGroup({
    phoneNumber1: new FormControl(''),
    phonenumber2: new FormControl(''),
    phonenumber3: new FormGroup({
      nth phoneNumber: new FormControl(''),
    })
  });
}
<div formGroupName="address">
  <h3>Address</h3>

  <label>
    phoneNumber1:
    <input type="text" formControlName="phoneNumber1">
  </label>

  <label>
    phoneNumber2:
    <input type="text" formControlName="phoneNumber2">
  </label>
  
  <label>
    phoneNumber3:
    <input type="text" formControlName="phoneNumber3">
  </label>

  <label>
    nth phoneNumbern:
    <input type="text" formControlName="poneNumberN">
  </label>
</div>
<input type="submit"/>

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>


4.In the home module make 4 components.place the 4 components in 4 different corners of the screen like so.....

import { Component } from '@angular/core';
import { FormGroup, FormControl } from '@angular/forms';

@Component({
  selector: 'app-profile-editor',
  templateUrl: './profile-editor.component.html',
  styleUrls: ['./profile-editor.component.css']
})
export class ProfileEditorComponent {
  profileForm = new FormGroup({
    ABC123: new FormControl(''),
    ABC123: new FormControl(''),
    ABC123: new FormGroup({
    })
  });
}
<div formGroupName="address">
  <h3>Address</h3>

  <label>
    Street:
    <input type="text" formControlName="ABC123">
  </label>

  <label>
    City:
    <input type="text" formControlName="ABC123">
  </label>
  
  <label>
    State:
    <input type="text" formControlName="ABC123">
  </label>

  <label>
    Zip Code:
    <input type="text" formControlName="ABC123">
  </label>
</div>






          
