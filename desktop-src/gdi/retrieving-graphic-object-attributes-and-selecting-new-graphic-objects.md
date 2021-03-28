---
title: 取出物件屬性，選取 [新增物件]
description: 應用程式可以藉由呼叫 GetCurrentObject 和 GetObject 函式，來取得畫筆、筆刷、調色板、字型或點陣圖的屬性。
ms.assetid: 09d8412f-a67d-48d5-9c04-9233dee43cf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b18dcef03bf769e8b2d11574429b64f481b1a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972524"
---
# <a name="retrieve-object-attributes-select-new-objects"></a>取出物件屬性，選取 [新增物件]

應用程式可以藉由呼叫 [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) 和 [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) 函式，來取得畫筆、筆刷、調色板、字型或點陣圖的屬性。 **GetCurrentObject** 函式會傳回一個控制碼，識別目前選取到 DC 的物件。**GetObject** 函數會傳回描述物件屬性的結構。

下列範例顯示應用程式如何取出目前的筆刷屬性，並使用抓取的資料來判斷是否需要選取新的筆刷。


```C++
    HDC hdc;                     // display DC handle  
    HBRUSH hbrushNew, hbrushOld; // brush handles  
    HBRUSH hbrush;               // brush handle  
    LOGBRUSH lb;                 // logical-brush structure  
 
    // Retrieve a handle identifying the current brush.  
 
    hbrush = GetCurrentObject(hdc, OBJ_BRUSH); 
 
    // Retrieve a LOGBRUSH structure that contains the  
    // current brush attributes.  
 
    GetObject(hbrush, sizeof(LOGBRUSH), &lb); 
 
    // If the current brush is not a solid-black brush,  
    // replace it with the solid-black stock brush.  
 
    if ((lb.lbStyle != BS_SOLID) 
           || (lb.lbColor != 0x000000)) 
    { 
        hbrushNew = GetStockObject(BLACK_BRUSH); 
        hbrushOld = SelectObject(hdc, hbrushNew); 
    } 
 
    // Perform painting operations with the white brush.  
 
 
    // After completing the last painting operation with the new  
    // brush, the application should select the original brush back  
    // into the device context and delete the new brush.  
    // In this example, hbrushNew contains a handle to a stock object.  
    // It is not necessary (but it is not harmful) to call  
    // DeleteObject on a stock object. If hbrushNew contained a handle  
    // to a brush created by a function such as CreateBrushIndirect,  
    // it would be necessary to call DeleteObject.  
 
    SelectObject(hdc, hbrushOld); 
    DeleteObject(hbrushNew); 
```



> [!Note]
>
> 應用程式會在第一次呼叫 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函式時，儲存原始筆刷控制碼。 這個控制碼已儲存，如此一來，當您使用新的筆刷完成最後一個繪製作業之後，就可以將原始筆刷選取回 DC。 將原始筆刷選取回 DC 之後，會刪除新的筆刷，釋出 GDI 堆積中的記憶體。

 

 

 



