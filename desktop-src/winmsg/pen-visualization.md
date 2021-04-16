---
description: 應用程式或 UI 架構會使用下列常數，識別當偵測到其中一個所列的畫筆手勢時，如何處理 UI 意見反應。
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: '畫筆視覺效果 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a09aa8892647315eccbb1e8b3ca443e01c1ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513436"
---
# <a name="pen-visualization"></a><span data-ttu-id="4d812-103">畫筆視覺效果</span><span class="sxs-lookup"><span data-stu-id="4d812-103">Pen Visualization</span></span>

<span data-ttu-id="4d812-104">應用程式或 UI 架構會使用下列常數，識別當偵測到其中一個所列的畫筆手勢時，如何處理 UI 意見反應。</span><span class="sxs-lookup"><span data-stu-id="4d812-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when one of the listed pen gestures is detected.</span></span>

<span data-ttu-id="4d812-105">這些常數會搭配 **spi \_ GETPENVISUALIZATION** 和 **Spi \_ SETPENVISUALIZATION** 參數和 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) 函式使用。</span><span class="sxs-lookup"><span data-stu-id="4d812-105">These constants are used with the **SPI\_GETPENVISUALIZATION** and **SPI\_SETPENVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<dl> <dt>

<span data-ttu-id="4d812-106"><span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="4d812-106"><span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d812-107">0x0000</span><span class="sxs-lookup"><span data-stu-id="4d812-107">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="4d812-108">指定所有畫筆手勢的 UI 回饋都是 off。</span><span class="sxs-lookup"><span data-stu-id="4d812-108">Specifies that UI feedback for all pen gestures is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d812-109"><span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION \_ 于**</span><span class="sxs-lookup"><span data-stu-id="4d812-109"><span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d812-110">0x0023</span><span class="sxs-lookup"><span data-stu-id="4d812-110">0x0023</span></span>
</dt> <dt>



<span data-ttu-id="4d812-111">指定所有畫筆手勢的 UI 意見反應都是開啟的。</span><span class="sxs-lookup"><span data-stu-id="4d812-111">Specifies that UI feedback for all pen gestures is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d812-112"><span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**PENVISUALIZATION \_ 分流**</span><span class="sxs-lookup"><span data-stu-id="4d812-112"><span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**PENVISUALIZATION\_TAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d812-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="4d812-113">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="4d812-114">指定畫筆點擊的 UI 意見反應。</span><span class="sxs-lookup"><span data-stu-id="4d812-114">Specifies UI feedback for a pen tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d812-115"><span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PENVISUALIZATION \_ DOUBLETAP**</span><span class="sxs-lookup"><span data-stu-id="4d812-115"><span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PENVISUALIZATION\_DOUBLETAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d812-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="4d812-116">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="4d812-117">指定畫筆點兩下的 UI 意見反應。</span><span class="sxs-lookup"><span data-stu-id="4d812-117">Specifies UI feedback for a pen double tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4d812-118"><span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**PENVISUALIZATION 資料 \_ 指標**</span><span class="sxs-lookup"><span data-stu-id="4d812-118"><span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**PENVISUALIZATION\_CURSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d812-119">0x0020</span><span class="sxs-lookup"><span data-stu-id="4d812-119">0x0020</span></span>
</dt> <dt>



<span data-ttu-id="4d812-120">指定畫筆游標的 UI 意見反應。</span><span class="sxs-lookup"><span data-stu-id="4d812-120">Specifies UI feedback for the pen cursor.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d812-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d812-121">Requirements</span></span>



| <span data-ttu-id="4d812-122">需求</span><span class="sxs-lookup"><span data-stu-id="4d812-122">Requirement</span></span> | <span data-ttu-id="4d812-123">值</span><span class="sxs-lookup"><span data-stu-id="4d812-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4d812-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d812-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4d812-125">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d812-125">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4d812-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d812-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4d812-127">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d812-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4d812-128">標頭</span><span class="sxs-lookup"><span data-stu-id="4d812-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d812-129"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="4d812-129"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d812-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d812-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d812-131">設定常數</span><span class="sxs-lookup"><span data-stu-id="4d812-131">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="4d812-132">**連絡人視覺效果**</span><span class="sxs-lookup"><span data-stu-id="4d812-132">**Contact Visualization**</span></span>](contact-visualization.md)
</dt> <dt>

[<span data-ttu-id="4d812-133">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="4d812-133">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="4d812-134">輸入意見設定</span><span class="sxs-lookup"><span data-stu-id="4d812-134">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

