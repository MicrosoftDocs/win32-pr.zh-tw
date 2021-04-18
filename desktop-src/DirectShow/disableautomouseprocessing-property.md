---
description: DisableAutoMouseProcessing 屬性會啟用或停用 MSWebDVD 物件的滑鼠處理功能。
ms.assetid: d438deb8-3c6d-49c1-923b-d4c57e236fc9
title: DisableAutoMouseProcessing 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606392acd4030d68af9590555a40d571d70c581
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467476"
---
# <a name="disableautomouseprocessing-property"></a><span data-ttu-id="53171-103">DisableAutoMouseProcessing 屬性</span><span class="sxs-lookup"><span data-stu-id="53171-103">DisableAutoMouseProcessing Property</span></span>

> [!Note]  
> <span data-ttu-id="53171-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="53171-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="53171-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="53171-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="53171-106">`DisableAutoMouseProcessing`屬性會啟用或停用 **MSWebDVD** 物件的滑鼠處理功能。</span><span class="sxs-lookup"><span data-stu-id="53171-106">The `DisableAutoMouseProcessing` property enables or disables the **MSWebDVD** object's mouse-processing functionality.</span></span>

``` syntax
[ bMouseProcessing = ] MSWebDVD.DisableAutoMouseProcessing
```

## <a name="return-value"></a><span data-ttu-id="53171-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="53171-107">Return Value</span></span>

<span data-ttu-id="53171-108">傳回布林值，指出是否要停用預設的滑鼠處理。</span><span class="sxs-lookup"><span data-stu-id="53171-108">Returns a boolean value indicating whether to disable the default mouse processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="53171-109">備註</span><span class="sxs-lookup"><span data-stu-id="53171-109">Remarks</span></span>

<span data-ttu-id="53171-110">這個屬性是讀取/寫入，預設值是 false。</span><span class="sxs-lookup"><span data-stu-id="53171-110">This property is read/write with a default value of false.</span></span> <span data-ttu-id="53171-111">依預設， **MSWebDVD** 物件會自動處理 DVD 螢幕功能表上的滑鼠動作;使用者可以反白顯示並啟用功能表按鈕，而不需要由應用程式進行特殊程式設計。</span><span class="sxs-lookup"><span data-stu-id="53171-111">The **MSWebDVD** object automatically handles mouse actions for DVD on-screen menus by default; users can highlight and activate menu buttons without special programming by the application.</span></span> <span data-ttu-id="53171-112">應用程式可以將這個屬性設定為 **true**，以關閉這個預設的滑鼠處理功能。</span><span class="sxs-lookup"><span data-stu-id="53171-112">An application can turn off this default mouse-handling functionality by setting this property to **true**.</span></span> <span data-ttu-id="53171-113">當自動關閉滑鼠處理功能時，應用程式必須使用各種按鈕相關的方法和屬性，來處理螢幕功能表上的滑鼠移動和滑鼠點擊。</span><span class="sxs-lookup"><span data-stu-id="53171-113">When the automatic mouse processing is turned off, an application must use the various button-related methods and properties to handle mouse moves and mouse clicks on the on-screen menus.</span></span> <span data-ttu-id="53171-114">此外，應用程式也可以使用按鈕相關的方法來覆寫自動滑鼠處理，即使當 `DisableAutoMouseProcessing` 設定為 **false** 時也一樣。</span><span class="sxs-lookup"><span data-stu-id="53171-114">Also, an application can use the button-related methods to override the automatic mouse handling even when when `DisableAutoMouseProcessing` is set to **false**.</span></span>

 

 



