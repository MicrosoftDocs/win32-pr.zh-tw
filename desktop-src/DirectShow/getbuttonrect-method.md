---
description: GetButtonRect 方法會在視窗座標中，取得指定之按鈕的矩形。
ms.assetid: 359e9483-d7ba-45b0-882b-5a4c56dc0350
title: GetButtonRect 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 752c90637ee58aaa862245b29536dc71ad8e9a1c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108524"
---
# <a name="getbuttonrect-method"></a><span data-ttu-id="c6642-103">GetButtonRect 方法</span><span class="sxs-lookup"><span data-stu-id="c6642-103">GetButtonRect Method</span></span>

> [!Note]  
> <span data-ttu-id="c6642-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="c6642-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c6642-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="c6642-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c6642-106">`GetButtonRect`方法會在視窗座標中，取得指定之按鈕的矩形。</span><span class="sxs-lookup"><span data-stu-id="c6642-106">The `GetButtonRect` method retrieves the rectangle for the specified button, in window coordinates.</span></span>

``` syntax
[ oButton = ] MSWebDVD.GetButtonRect(iButton)
```

## <a name="parameters"></a><span data-ttu-id="c6642-107">參數</span><span class="sxs-lookup"><span data-stu-id="c6642-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6642-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span><span class="sxs-lookup"><span data-stu-id="c6642-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span></span>
</dt> <dd>

<span data-ttu-id="c6642-109">將按鈕編號指定為整數。</span><span class="sxs-lookup"><span data-stu-id="c6642-109">Specifies the button number as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6642-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6642-110">Return Value</span></span>

<span data-ttu-id="c6642-111">傳回定義矩形的 [DVDRect](dvdrect-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="c6642-111">Returns a [DVDRect](dvdrect-object.md) object that defines the rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6642-112">備註</span><span class="sxs-lookup"><span data-stu-id="c6642-112">Remarks</span></span>

<span data-ttu-id="c6642-113">將 [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) 設為 **true** 之後，執行自訂滑鼠處理時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="c6642-113">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6642-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6642-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6642-115">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="c6642-115">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="c6642-116">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="c6642-116">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="c6642-117">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="c6642-117">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="c6642-118">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="c6642-118">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="c6642-119">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="c6642-119">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



