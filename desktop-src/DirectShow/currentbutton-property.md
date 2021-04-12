---
description: CurrentButton 屬性會抓取選取的功能表按鈕數目。
ms.assetid: bd9720bc-068a-4f29-aa2d-1c6b550f789c
title: CurrentButton 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c12def9f9a73c9538781bde6940b03bfb376fcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317720"
---
# <a name="currentbutton-property"></a><span data-ttu-id="931ad-103">CurrentButton 屬性</span><span class="sxs-lookup"><span data-stu-id="931ad-103">CurrentButton Property</span></span>

> [!Note]  
> <span data-ttu-id="931ad-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="931ad-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="931ad-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="931ad-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="931ad-106">屬性會抓取 `CurrentButton` 所選功能表按鈕的數目。</span><span class="sxs-lookup"><span data-stu-id="931ad-106">The `CurrentButton` property retrieves the number of the selected menu button.</span></span>

``` syntax
[ iButton = ] MSWebDVD.CurrentButton
```

## <a name="return-value"></a><span data-ttu-id="931ad-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="931ad-107">Return Value</span></span>

<span data-ttu-id="931ad-108">傳回代表按鈕的整數值。</span><span class="sxs-lookup"><span data-stu-id="931ad-108">Returns an integer value representing the button.</span></span>

## <a name="remarks"></a><span data-ttu-id="931ad-109">備註</span><span class="sxs-lookup"><span data-stu-id="931ad-109">Remarks</span></span>

<span data-ttu-id="931ad-110">這個屬性是唯讀的，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="931ad-110">This property is read-only with no default value.</span></span> <span data-ttu-id="931ad-111">將 [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) 設為 **true** 之後，執行自訂滑鼠處理時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="931ad-111">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="931ad-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="931ad-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="931ad-113">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="931ad-113">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="931ad-114">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="931ad-114">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="931ad-115">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="931ad-115">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="931ad-116">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="931ad-116">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="931ad-117">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="931ad-117">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="931ad-118">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="931ad-118">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



