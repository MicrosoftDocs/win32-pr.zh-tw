---
title: IAgentCharacterEx GetAnimationNames
description: IAgentCharacterEx GetAnimationNames
ms.assetid: d565b258-dc12-422b-a13d-aeec56057f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31dcb7ea34a9f0d833f8c1665a092fe4f3a30e7
ms.sourcegitcommit: baa7cd1709e48672f5f07ff83a9c9d5699c0efcd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/14/2021
ms.locfileid: "106992621"
---
# <a name="iagentcharacterexgetanimationnames"></a><span data-ttu-id="44816-103">IAgentCharacterEx::GetAnimationNames</span><span class="sxs-lookup"><span data-stu-id="44816-103">IAgentCharacterEx::GetAnimationNames</span></span>

<span data-ttu-id="44816-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="44816-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAnimationNames(
   IUnknown ** punkEnum // address of IUnknown interface
);
```

<span data-ttu-id="44816-105">抓取字元的動畫名稱。</span><span class="sxs-lookup"><span data-stu-id="44816-105">Retrieves the animation names for a character.</span></span>

-   <span data-ttu-id="44816-106">傳回 **\_ [確定]** 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="44816-106">Returns **S\_OK** to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="44816-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="44816-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="44816-108">字元動畫集合的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面位址。</span><span class="sxs-lookup"><span data-stu-id="44816-108">The address of the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface for the character's animation collection.</span></span>

</dd> </dl>

<span data-ttu-id="44816-109">此函數可讓您列舉字元的動畫名稱。</span><span class="sxs-lookup"><span data-stu-id="44816-109">This function enables you to enumerate the names of the animations for a character.</span></span> <span data-ttu-id="44816-110">集合中的專案沒有屬性，因此無法直接存取個別專案。</span><span class="sxs-lookup"><span data-stu-id="44816-110">Items in the collection have no properties, so individual items cannot be accessed directly.</span></span> <span data-ttu-id="44816-111">若要存取集合，請查詢 punkEnum 以取得 IEnumVARIANT 介面：</span><span class="sxs-lookup"><span data-stu-id="44816-111">To access the collection, query punkEnum for the IEnumVARIANT interface:</span></span>


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
> <span data-ttu-id="44816-112">針對 ACF 字元，集合會傳回已針對該字元定義的所有動畫，並新增至已使用 [**Get**](https://www.bing.com/search?q=**Get**) 方法抓取的動畫。</span><span class="sxs-lookup"><span data-stu-id="44816-112">For ACF characters, the collection returns all the animations that have been defined for the character, adding to the ones that have been retrieved with the [**Get**](https://www.bing.com/search?q=**Get**) method.</span></span>
