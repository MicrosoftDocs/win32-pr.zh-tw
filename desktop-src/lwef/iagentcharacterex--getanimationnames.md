---
title: IAgentCharacterEx GetAnimationNames
description: IAgentCharacterEx GetAnimationNames
ms.assetid: d565b258-dc12-422b-a13d-aeec56057f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9cb1bc1b51b0bead2f071e0cd8561ef055ef6b7eb7986b3be969208452331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478023"
---
# <a name="iagentcharacterexgetanimationnames"></a>IAgentCharacterEx::GetAnimationNames

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetAnimationNames(
   IUnknown ** punkEnum // address of IUnknown interface
);
```

抓取字元的動畫名稱。

-   傳回 **\_ [確定]** 表示作業成功。

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

字元動畫集合的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面位址。

</dd> </dl>

此函數可讓您列舉字元的動畫名稱。 集合中的專案沒有屬性，因此無法直接存取個別專案。 若要存取集合，請查詢 punkEnum 以取得 IEnumVARIANT 介面：


```c++
IEnumVARIANT pEnum;
VARIANT vAnimName;
DWORD dwRetrieved;

hRes = punkEnum->QueryInterface(IID_IEnumVARIANT, (LPVOID *)&pEnum);

if (SUCCEEDED(hRes)) {

    while (TRUE) {

         hRes = pEnum->Next(1, &vAnimName, &dwRetrieved);

         if (hRes != NOERROR)
            break;

         // vAnimName.bstrVal is the animation name

         VariantClear(&vAnimName);
    } 

    pEnum->Release();
}

punkEnum->Release();
```



> [!Note]  
> 針對 ACF 字元，集合會傳回已針對該字元定義的所有動畫，並新增至已使用 [**Get**](https://www.bing.com/search?q=**Get**) 方法抓取的動畫。
