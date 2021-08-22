---
title: 使用 Active Desktop 物件
description: 本文包含屬於 Windows Shell API 一部分之 ActiveDesktop 物件的資訊。 此物件透過其 IActiveDesktop 介面，可讓您新增、移除和變更桌面上的專案。
ms.assetid: 68d72b0f-f5e9-4fff-bb13-4c60d1dd7009
keywords:
- ActiveDesktop 物件
- Active Desktop
- 列舉，桌面專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6daf1b5fbc73286619f07c8af76fbbce53bcaa8962cc88cf20f5af74bbdec82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610658"
---
# <a name="using-the-active-desktop-object"></a>使用 Active Desktop 物件

\[只有 Windows XP 或更早版本才支援這項功能。 \]

本文包含屬於 Windows Shell API 一部分之 **ActiveDesktop** 物件的資訊。 此物件透過其 [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) 介面，可讓您新增、移除和變更桌面上的專案。

## <a name="overview-of-the-active-desktop-interface"></a>Active Desktop 介面總覽

-   [存取 Active Desktop](#accessing-the-active-desktop)
-   [新增桌面專案](#adding-a-desktop-item)
-   [列舉桌面專案](#enumerating-the-desktop-items)

Active Desktop 是 microsoft Internet Explorer 4.0 中引進的一項功能，可讓您將 HTML 檔案和專案 (例如 Microsoft ActiveX 控制項和 JAVA applet) 直接加入您的桌面。 [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop)介面是 Windows Shell API 的一部分，用來以程式設計方式加入、移除和修改桌面上的專案。 您也可以使用 (CDF) 檔的通道定義格式來新增 Active Desktop 專案。

### <a name="accessing-the-active-desktop"></a>存取 Active Desktop

若要存取 Active Desktop，用戶端應用程式必須使用 CoCreateInstance 函式建立 ActiveDesktop 物件的實例， (CLSID \_ ActiveDesktop) [](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，並取得物件 [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop)介面的指標。

下列範例顯示如何取出 [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) 介面的指標。


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

//Insert code to call the IActiveDesktop methods

// Call the Release method
pActiveDesktop->Release();
```



### <a name="adding-a-desktop-item"></a>新增桌面專案

您可以使用三種方法來新增桌面專案： [**IActiveDesktop：： AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem)、 [**IActiveDesktop：： AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)和 [**IActiveDesktop：： AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl)。 每個新增至 Active Desktop 的桌面專案都必須有不同的來源 URL。

[**IActiveDesktop：： AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)和 [**IActiveDesktop：： AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl)方法都會提供選項，以顯示可在將桌面專案加入 Active Desktop 之前顯示的各種使用者介面。 介面會驗證使用者是否要將桌面專案新增至其 Active Desktop。 這些介面也會通知使用者 URL 安全性區域設定所保證的任何安全性風險，如果使用者想要建立此桌面專案的訂用帳戶，他們會要求他們。 這兩種方法也提供隱藏使用者介面的方法。 [**IActiveDesktop：： AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem)方法需要呼叫 [**IActiveDesktop：： ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) ，才能更新登錄。 若為 **IActiveDesktop：： AddDesktopItemWithUI**，用戶端應用程式必須立即釋放 [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) 介面，然後使用 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函式來抓取 **ActiveDesktop** 物件實例的介面，該實例包含新加入的桌面專案。

[**IActiveDesktop：： AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem)方法會在沒有任何使用者介面的情況下，將指定的桌面專案新增至 Active Desktop，除非 URL 安全性區域設定阻止它。 如果 URL 安全性區域設定不允許在不提示使用者的情況下新增桌面專案，則方法會失敗。 **IActiveDesktop：： AddDesktopItem** 也需要呼叫 [**IActiveDesktop：： ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) ，才能更新登錄。

下列範例示範如何使用 [**IActiveDesktop：： AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) 方法新增桌面專案。


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

// Initialize the COMPONENT structure
compDesktopItem.dwSize = sizeof(COMPONENT);

// Insert code that adds the information about the desktop item 
// to the COMPONENT structure

// Add the desktop item
pActiveDesktop->AddDesktopItem(&compDesktopItem,0);

// Save the changes to the registry
pActiveDesktop->ApplyChanges(AD_APPLY_ALL);
```



### <a name="enumerating-the-desktop-items"></a>列舉桌面專案

若要列舉目前安裝在 Active Desktop 上的桌面專案，用戶端應用程式必須使用 [**IActiveDesktop：： GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount)方法來取出安裝的桌面專案總數，然後建立一個使用桌面專案索引來呼叫 [**IActiveDesktop：： GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem)方法，以抓取每個桌面專案 [**元件**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component)結構的迴圈。

下列範例示範一種列舉桌面專案的方式。


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;
int intCount;
int intIndex = 0;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

pActiveDesktop->GetDesktopItemCount(&intCount,0);

compDesktopItem.dwSize = sizeof(COMPONENT);

while(intIndex<=(intCount-1))
{
    //get the COMPONENT structure for the current desktop item
    pActiveDesktop->GetDesktopItem(intIndex, &compDesktopItem,0);

    //Insert code that processes the structure

    //Increment the index
    intIndex++;

    //Insert code to clean-up structure for next component
}

// Call the Release method
pActiveDesktop->Release();
```



 

 