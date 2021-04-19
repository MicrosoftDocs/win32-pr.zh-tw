---
description: 應用程式或 UI 架構會使用下列常數，識別當偵測到其中一個所列出的手勢時，如何處理 UI 意見反應。
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: '手勢視覺效果 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551934380e1d5ec0902818466f5840e1dc6718e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990418"
---
# <a name="gesture-visualization"></a><span data-ttu-id="6dfcc-103">手勢視覺效果</span><span class="sxs-lookup"><span data-stu-id="6dfcc-103">Gesture Visualization</span></span>

<span data-ttu-id="6dfcc-104">應用程式或 UI 架構會使用下列常數，識別當偵測到其中一個所列出的手勢時，如何處理 UI 意見反應。</span><span class="sxs-lookup"><span data-stu-id="6dfcc-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when one of the listed gestures is detected.</span></span>

<span data-ttu-id="6dfcc-105">這些常數會搭配 **spi \_ GETGESTUREVISUALIZATION** 和 **Spi \_ SETGESTUREVISUALIZATION** 參數和 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) 函式使用。</span><span class="sxs-lookup"><span data-stu-id="6dfcc-105">These constants are used with the **SPI\_GETGESTUREVISUALIZATION** and **SPI\_SETGESTUREVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<span data-ttu-id="6dfcc-106">**注意**</span><span class="sxs-lookup"><span data-stu-id="6dfcc-106">**Note**</span></span>  

<span data-ttu-id="6dfcc-107">若要取得或設定畫筆視覺效果資訊，建議您使用 **spi \_ GETPENVISUALIZATION** 和 **spi \_ SETPENVISUALIZATION** 參數，以及在 [ [**畫筆視覺效果**](pen-visualization.md)] 中列出的常數。</span><span class="sxs-lookup"><span data-stu-id="6dfcc-107">For retrieving or setting pen visualization info, we recommend that you use the **SPI\_GETPENVISUALIZATION** and **SPI\_SETPENVISUALIZATION** parameters and the constants listed in [**Pen Visualization**](pen-visualization.md).</span></span>

<dl> <dt>

<span data-ttu-id="6dfcc-108"><span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="6dfcc-108"><span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dfcc-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="6dfcc-109">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="6dfcc-110">指定所有手勢的 UI 意見反應都是 off。</span><span class="sxs-lookup"><span data-stu-id="6dfcc-110">Specifies that UI feedback for all gestures is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6dfcc-111"><span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION \_ 于**</span><span class="sxs-lookup"><span data-stu-id="6dfcc-111"><span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dfcc-112">0x001F</span><span class="sxs-lookup"><span data-stu-id="6dfcc-112">0x001F</span></span>
</dt> <dt>



<span data-ttu-id="6dfcc-113">指定所有手勢的 UI 意見反應都是開啟的。</span><span class="sxs-lookup"><span data-stu-id="6dfcc-113">Specifies that UI feedback for all gestures is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6dfcc-114"><span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**GESTUREVISUALIZATION \_ 分流**</span><span class="sxs-lookup"><span data-stu-id="6dfcc-114"><span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**GESTUREVISUALIZATION\_TAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dfcc-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="6dfcc-115">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="6dfcc-116">指定點擊的 UI 意見反應。</span><span class="sxs-lookup"><span data-stu-id="6dfcc-116">Specifies UI feedback for a tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6dfcc-117"><span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION \_ DOUBLETAP**</span><span class="sxs-lookup"><span data-stu-id="6dfcc-117"><span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION\_DOUBLETAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dfcc-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="6dfcc-118">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="6dfcc-119">指定點兩下的 UI 意見反應。</span><span class="sxs-lookup"><span data-stu-id="6dfcc-119">Specifies UI feedback for a double tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6dfcc-120"><span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION \_ PRESSANDTAP**</span><span class="sxs-lookup"><span data-stu-id="6dfcc-120"><span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION\_PRESSANDTAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dfcc-121">0x0004</span><span class="sxs-lookup"><span data-stu-id="6dfcc-121">0x0004</span></span>
</dt> <dt>



<span data-ttu-id="6dfcc-122">指定按下和點的 UI 回饋。</span><span class="sxs-lookup"><span data-stu-id="6dfcc-122">Specifies UI feedback for a press and tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6dfcc-123"><span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION \_ PRESSANDHOLD**</span><span class="sxs-lookup"><span data-stu-id="6dfcc-123"><span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION\_PRESSANDHOLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dfcc-124">0x0008</span><span class="sxs-lookup"><span data-stu-id="6dfcc-124">0x0008</span></span>
</dt> <dt>



<span data-ttu-id="6dfcc-125">指定按下並按住的 UI 意見反應。</span><span class="sxs-lookup"><span data-stu-id="6dfcc-125">Specifies UI feedback for a press and hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6dfcc-126"><span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION \_ RIGHTTAP**</span><span class="sxs-lookup"><span data-stu-id="6dfcc-126"><span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION\_RIGHTTAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dfcc-127">0x0010</span><span class="sxs-lookup"><span data-stu-id="6dfcc-127">0x0010</span></span>
</dt> <dt>



<span data-ttu-id="6dfcc-128">指定以滑鼠右鍵按一下的 UI 意見反應。</span><span class="sxs-lookup"><span data-stu-id="6dfcc-128">Specifies UI feedback for a right tap.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6dfcc-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="6dfcc-129">Requirements</span></span>



| <span data-ttu-id="6dfcc-130">需求</span><span class="sxs-lookup"><span data-stu-id="6dfcc-130">Requirement</span></span> | <span data-ttu-id="6dfcc-131">值</span><span class="sxs-lookup"><span data-stu-id="6dfcc-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6dfcc-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6dfcc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6dfcc-133">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dfcc-133">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6dfcc-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6dfcc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6dfcc-135">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dfcc-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6dfcc-136">標頭</span><span class="sxs-lookup"><span data-stu-id="6dfcc-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dfcc-137"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="6dfcc-137"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dfcc-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6dfcc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dfcc-139">設定常數</span><span class="sxs-lookup"><span data-stu-id="6dfcc-139">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="6dfcc-140">**連絡人視覺效果**</span><span class="sxs-lookup"><span data-stu-id="6dfcc-140">**Contact Visualization**</span></span>](contact-visualization.md)
</dt> <dt>

[<span data-ttu-id="6dfcc-141">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="6dfcc-141">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="6dfcc-142">輸入意見設定</span><span class="sxs-lookup"><span data-stu-id="6dfcc-142">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

