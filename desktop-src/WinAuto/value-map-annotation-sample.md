---
title: 值對應注釋範例
description: 值對應注釋範例
ms.assetid: f95233ee-c825-482e-880b-63212014b505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ad1008e2e3ce039ead09c43b37d9ef0500da3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969441"
---
# <a name="value-map-annotation-sample"></a>值對應注釋範例

剪下、貼上和修改下列程式碼範例，以供您自己使用。 遵循標示為/TODO/的批註中的指示 \* \* 。


```C++
/*  TODO
 *  Delete / modify these sample mapping strings as
 *  appropriate.
 *  See <oleacc.h> for the possible states and roles, and
 *  their numeric values.
 */

LPCWSTR g_ListOrTreeStateMap = 
    L"A:0"     // 0 -> use regular image, 1 -> use state image, 2-> use overlay image. 
    L":0:0x00" // image 0 is normal  
    L":1:0x10" // image 1 is checked - STATE_SYSTEM_CHECKED 
    L":";

LPCWSTR g_ListOrTreeRoleMap = 
    L"A:0"     // 0 -> use regular image, 1 -> use state image, 2-> use overlay image. 
    L":0:0x2C" // image 0 is check box - ROLE_SYSTEM_CHECKBUTTON (ie. check box) 
    L":1:0x2C" // image 1 is also check box 
    L":";


// This is an example for a slider that has 5 positions, 
// ranging from Cold (0) to Hot (5). 
// Note - because this contains textual strings, the entire 
// string should be loaded from a localized resource, or 
// it should be built at run time from localized strings. 
// This non-localization-friendly string is used here for 
// illustrative purposes only. 
LPCWSTR g_SliderValueMap = 
    L"A:0" // always 0 for slider maps 
    L":0:Cold"
    L":1:Cool"
    L":2:Warm"
    L":3:Toasty"
    L":4:Hot"
    L":";


[ ... ]

// 
//  Skeleton code to set property map for a control 
// 
//  Do this after shortly after the corresponding control is 
//  created (for example, when handling WM_INITDIALOG) 
// 
//  Assumptions: 
//  hwndListOrTree is the HWND of a listview or 
//  treeview(listview, treeview), 
//  hwndSlider is the HWND of a slider. 
// 

    IAccPropServices * pAccPropSvc = NULL;
    HRESULT hr;
    hr = CoCreateInstance( CLSID_AccPropServices, NULL,
CLSCTX_SERVER, IID_IAccPropServices, (void **) & pAccPropSvc )
);
    if( hr == S_OK && pAccPropSvc )
    {
        /*  TODO
         *  For a listview or treeview, both role and state
         *  maps are typically set here.
         *  For sliders, only the value map is set.
         *  Delete / modify as appropriate.
         *
         */
        pAccPropSvc->SetHwndPropStr( hwndListOrTree,
OBJID_CLIENT, 0, PROPID_ACC_ROLEMAP, g_ListOrTreeRoleMap ) );
        pAccPropSvc->SetHwndPropStr( hwndListOrTree,
OBJID_CLIENT, 0, PROPID_ACC_STATEMAP, g_ListOrTreeStateMap ) );

        pAccPropSvc->SetHwndPropStr( hwndSlider, OBJID_CLIENT,
0, PROPID_ACC_VALUEMAP, g_SliderValueMap );

        pAccPropSvc->Release();
    }
```



 

 




