---
description: ActivateAtPosition 方法會在指定的位置啟用 [功能表] 按鈕。
ms.assetid: eddc4880-dd78-4d96-8bff-c5c883a19927
title: ActivateAtPosition 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64a83e7fcbc00990c7be7d1a99638a1b4a3de14b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109720"
---
# <a name="activateatposition-method"></a><span data-ttu-id="4e4b5-103">ActivateAtPosition 方法</span><span class="sxs-lookup"><span data-stu-id="4e4b5-103">ActivateAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="4e4b5-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="4e4b5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4e4b5-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="4e4b5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4e4b5-106">ActivateAtPosition 方法會在指定的位置啟用 [功能表] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="4e4b5-106">The ActivateAtPosition method activates the menu button at the specified position.</span></span>

``` syntax
        MSWebDVD.ActivateAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="4e4b5-107">參數</span><span class="sxs-lookup"><span data-stu-id="4e4b5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e4b5-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="4e4b5-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="4e4b5-109">指定 x 座標做為整數。</span><span class="sxs-lookup"><span data-stu-id="4e4b5-109">Specifies x-coordinate as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="4e4b5-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="4e4b5-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="4e4b5-111">將 y 座標指定為整數。</span><span class="sxs-lookup"><span data-stu-id="4e4b5-111">Specifies the y-coordinate as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e4b5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e4b5-112">Return Value</span></span>

<span data-ttu-id="4e4b5-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="4e4b5-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e4b5-114">備註</span><span class="sxs-lookup"><span data-stu-id="4e4b5-114">Remarks</span></span>

<span data-ttu-id="4e4b5-115">將 [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) 設為 **true** 之後，執行自訂滑鼠處理時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="4e4b5-115">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e4b5-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e4b5-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e4b5-117">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="4e4b5-117">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="4e4b5-118">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="4e4b5-118">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="4e4b5-119">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="4e4b5-119">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="4e4b5-120">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="4e4b5-120">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="4e4b5-121">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="4e4b5-121">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="4e4b5-122">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="4e4b5-122">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



