---
description: SelectAtPosition 方法會在指定的滑鼠指標座標中選取功能表按鈕。
ms.assetid: 005ec550-e04c-4dae-aa5d-d79afefe48ed
title: SelectAtPosition 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97bc9feaa4855baac75fca0e776a26a6975b235a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687803"
---
# <a name="selectatposition-method"></a><span data-ttu-id="7351e-103">SelectAtPosition 方法</span><span class="sxs-lookup"><span data-stu-id="7351e-103">SelectAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="7351e-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="7351e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7351e-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="7351e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7351e-106">`SelectAtPosition`方法會在指定的滑鼠指標座標中選取功能表按鈕。</span><span class="sxs-lookup"><span data-stu-id="7351e-106">The `SelectAtPosition` method selects the menu button at the specified mouse pointer coordinates.</span></span>

``` syntax
MSWebDVD.SelectAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="7351e-107">參數</span><span class="sxs-lookup"><span data-stu-id="7351e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7351e-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="7351e-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="7351e-109">將 x 座標指定為整數。</span><span class="sxs-lookup"><span data-stu-id="7351e-109">Specifies the x-coordinate as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="7351e-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="7351e-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="7351e-111">將 y 座標指定為整數。</span><span class="sxs-lookup"><span data-stu-id="7351e-111">Specifies the y-coordinate as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7351e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="7351e-112">Return Value</span></span>

<span data-ttu-id="7351e-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="7351e-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7351e-114">備註</span><span class="sxs-lookup"><span data-stu-id="7351e-114">Remarks</span></span>

<span data-ttu-id="7351e-115">將 [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) 設為 **true** 之後，執行自訂滑鼠處理時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="7351e-115">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="7351e-116">選取只會反白顯示按鈕。</span><span class="sxs-lookup"><span data-stu-id="7351e-116">Selecting merely highlights the button.</span></span> <span data-ttu-id="7351e-117">若要傳送與已選取之按鈕相關聯的命令，請呼叫 [**ActivateButton**](activatebutton-method.md)。</span><span class="sxs-lookup"><span data-stu-id="7351e-117">To send the command associated with a button that has been selected, call [**ActivateButton**](activatebutton-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7351e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7351e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7351e-119">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="7351e-119">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="7351e-120">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="7351e-120">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="7351e-121">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="7351e-121">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="7351e-122">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="7351e-122">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="7351e-123">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="7351e-123">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> </dl>

 

 



