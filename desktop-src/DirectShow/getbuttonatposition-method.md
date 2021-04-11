---
description: GetButtonAtPosition 方法會在指定的座標處抓取按鈕的數目，而不需要選取或啟用它。
ms.assetid: ac933d0d-db2e-488f-b661-2fdc9f5acb39
title: GetButtonAtPosition 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9347929946a6f26cac4652a5357bd6454c80446c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108525"
---
# <a name="getbuttonatposition-method"></a><span data-ttu-id="8fafc-103">GetButtonAtPosition 方法</span><span class="sxs-lookup"><span data-stu-id="8fafc-103">GetButtonAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="8fafc-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="8fafc-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8fafc-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="8fafc-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8fafc-106">`GetButtonAtPosition`方法會在指定的座標處抓取按鈕的數目，而不選取或啟用它。</span><span class="sxs-lookup"><span data-stu-id="8fafc-106">The `GetButtonAtPosition` method retrieves the number of the button at the specified coordinates without selecting or activating it.</span></span>

``` syntax
[ iButton = ] MSWebDVD.GetButtonAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="8fafc-107">參數</span><span class="sxs-lookup"><span data-stu-id="8fafc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fafc-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="8fafc-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="8fafc-109">將滑鼠指標的 x 座標指定為整數。</span><span class="sxs-lookup"><span data-stu-id="8fafc-109">Specifies the x-coordinate of the mouse pointer as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="8fafc-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="8fafc-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="8fafc-111">將滑鼠指標的 y 座標指定為整數。</span><span class="sxs-lookup"><span data-stu-id="8fafc-111">Specifies the y-coordinate of the mouse pointer as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fafc-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8fafc-112">Return Value</span></span>

<span data-ttu-id="8fafc-113">傳回整數值，指定指定位置的按鈕（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="8fafc-113">Returns an integer value specifying the button, if any, at the specified position.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fafc-114">備註</span><span class="sxs-lookup"><span data-stu-id="8fafc-114">Remarks</span></span>

<span data-ttu-id="8fafc-115">如果指定的座標沒有任何按鈕，這個方法會傳回零。</span><span class="sxs-lookup"><span data-stu-id="8fafc-115">This method returns zero if no button is present at the given coordinates.</span></span> <span data-ttu-id="8fafc-116">將 [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) 設為 **true** 之後，執行自訂滑鼠處理時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="8fafc-116">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="8fafc-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fafc-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fafc-118">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="8fafc-118">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="8fafc-119">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="8fafc-119">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="8fafc-120">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="8fafc-120">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="8fafc-121">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="8fafc-121">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="8fafc-122">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="8fafc-122">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="8fafc-123">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="8fafc-123">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



