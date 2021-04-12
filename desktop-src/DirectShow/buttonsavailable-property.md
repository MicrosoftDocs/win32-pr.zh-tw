---
description: ButtonsAvailable 屬性會抓取目前功能表上的總按鈕數目。
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: ButtonsAvailable 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cab4afdd9f6e23a376bb72885810b8464f180d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385770"
---
# <a name="buttonsavailable-property"></a><span data-ttu-id="ff667-103">ButtonsAvailable 屬性</span><span class="sxs-lookup"><span data-stu-id="ff667-103">ButtonsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="ff667-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="ff667-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ff667-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="ff667-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ff667-106">屬性會抓取 `ButtonsAvailable` 目前功能表上的總按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="ff667-106">The `ButtonsAvailable` property retrieves the total number of buttons on the current menu.</span></span>

``` syntax
[ iButtons = ] MSWebDVD.ButtonsAvailable
```

## <a name="return-value"></a><span data-ttu-id="ff667-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff667-107">Return Value</span></span>

<span data-ttu-id="ff667-108">傳回代表按鈕數目的整數值。</span><span class="sxs-lookup"><span data-stu-id="ff667-108">Returns an integer value representing the number of buttons.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff667-109">備註</span><span class="sxs-lookup"><span data-stu-id="ff667-109">Remarks</span></span>

<span data-ttu-id="ff667-110">這個屬性是唯讀的，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="ff667-110">This property is read-only with no default value.</span></span> <span data-ttu-id="ff667-111">將 [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) 設為 **true** 之後，執行自訂滑鼠處理時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="ff667-111">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="ff667-112">呼叫這個方法，以取得有效按鈕編號範圍的上限。</span><span class="sxs-lookup"><span data-stu-id="ff667-112">Call this method to retrieve the upper limit for the range of valid button numbers.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff667-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff667-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff667-114">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="ff667-114">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="ff667-115">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="ff667-115">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="ff667-116">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="ff667-116">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="ff667-117">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="ff667-117">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="ff667-118">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="ff667-118">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



