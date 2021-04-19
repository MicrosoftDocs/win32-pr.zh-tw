---
description: SelectAndActivateButton 方法會選取並啟用指定的按鈕。
ms.assetid: fa6239ea-0478-41f1-9515-d67a7fad11db
title: SelectAndActivateButton 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717af00becd5f00f55b166353246f92ea7dfd1bd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973739"
---
# <a name="selectandactivatebutton-method"></a><span data-ttu-id="66d16-103">SelectAndActivateButton 方法</span><span class="sxs-lookup"><span data-stu-id="66d16-103">SelectAndActivateButton Method</span></span>

> [!Note]  
> <span data-ttu-id="66d16-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="66d16-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="66d16-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="66d16-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="66d16-106">`SelectAndActivateButton`方法會選取並啟用指定的按鈕。</span><span class="sxs-lookup"><span data-stu-id="66d16-106">The `SelectAndActivateButton` method selects and activates the specified button.</span></span>

``` syntax
MSWebDVD.SelectAndActivateButton(iButton)
```

## <a name="parameters"></a><span data-ttu-id="66d16-107">參數</span><span class="sxs-lookup"><span data-stu-id="66d16-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66d16-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span><span class="sxs-lookup"><span data-stu-id="66d16-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span></span>
</dt> <dd>

<span data-ttu-id="66d16-109">將按鈕指定為整數。</span><span class="sxs-lookup"><span data-stu-id="66d16-109">Specifies the button as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66d16-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="66d16-110">Return Value</span></span>

<span data-ttu-id="66d16-111">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="66d16-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66d16-112">備註</span><span class="sxs-lookup"><span data-stu-id="66d16-112">Remarks</span></span>

<span data-ttu-id="66d16-113">將 [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) 設為 **true** 之後，執行自訂滑鼠處理時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="66d16-113">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="66d16-114">這個方法會反白顯示指定的按鈕，並自動啟動它。</span><span class="sxs-lookup"><span data-stu-id="66d16-114">This method highlights the specified button and activate it automatically.</span></span>

## <a name="see-also"></a><span data-ttu-id="66d16-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66d16-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d16-116">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="66d16-116">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="66d16-117">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="66d16-117">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="66d16-118">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="66d16-118">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="66d16-119">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="66d16-119">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="66d16-120">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="66d16-120">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="66d16-121">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="66d16-121">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



