---
description: 應用程式或 UI 架構會使用下列常數，來識別偵測到輸入連絡人時如何處理 UI 意見反應。
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: '連絡人視覺效果 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100892624f3e656e33ddf798c5795eeab6b11a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320252"
---
# <a name="contact-visualization"></a><span data-ttu-id="4374d-103">連絡人視覺效果</span><span class="sxs-lookup"><span data-stu-id="4374d-103">Contact Visualization</span></span>

<span data-ttu-id="4374d-104">應用程式或 UI 架構會使用下列常數，來識別偵測到輸入連絡人時如何處理 UI 意見反應。</span><span class="sxs-lookup"><span data-stu-id="4374d-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when an input contact is detected.</span></span>

<span data-ttu-id="4374d-105">這些常數會搭配 **spi \_ GETCONTACTVISUALIZATION** 和 **Spi \_ SETCONTACTVISUALIZATION** 參數和 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) 函式使用。</span><span class="sxs-lookup"><span data-stu-id="4374d-105">These constants are used with the **SPI\_GETCONTACTVISUALIZATION** and **SPI\_SETCONTACTVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<dl> <dt>

<span data-ttu-id="4374d-106"><span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="4374d-106"><span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4374d-107">0x0000</span><span class="sxs-lookup"><span data-stu-id="4374d-107">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="4374d-108">指定所有連絡人的 UI 意見反應都是 off。</span><span class="sxs-lookup"><span data-stu-id="4374d-108">Specifies UI feedback for all contacts is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4374d-109"><span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION \_ 于**</span><span class="sxs-lookup"><span data-stu-id="4374d-109"><span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4374d-110">0x0001</span><span class="sxs-lookup"><span data-stu-id="4374d-110">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="4374d-111">指定所有連絡人的 UI 回饋。</span><span class="sxs-lookup"><span data-stu-id="4374d-111">Specifies UI feedback for all contacts is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4374d-112"><span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION \_ PRESENTATIONMODE**</span><span class="sxs-lookup"><span data-stu-id="4374d-112"><span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION\_PRESENTATIONMODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4374d-113">0x0002</span><span class="sxs-lookup"><span data-stu-id="4374d-113">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="4374d-114">使用簡報模式視覺效果，指定所有連絡人的 UI 意見反應。</span><span class="sxs-lookup"><span data-stu-id="4374d-114">Specifies UI feedback for all contacts is on with presentation mode visuals.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4374d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4374d-115">Requirements</span></span>



| <span data-ttu-id="4374d-116">需求</span><span class="sxs-lookup"><span data-stu-id="4374d-116">Requirement</span></span> | <span data-ttu-id="4374d-117">值</span><span class="sxs-lookup"><span data-stu-id="4374d-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4374d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4374d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4374d-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4374d-119">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4374d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4374d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4374d-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4374d-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4374d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="4374d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4374d-123"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="4374d-123"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4374d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4374d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4374d-125">設定常數</span><span class="sxs-lookup"><span data-stu-id="4374d-125">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="4374d-126">**手勢視覺效果**</span><span class="sxs-lookup"><span data-stu-id="4374d-126">**Gesture Visualization**</span></span>](gesture-visualization.md)
</dt> <dt>

[<span data-ttu-id="4374d-127">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="4374d-127">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="4374d-128">輸入意見設定</span><span class="sxs-lookup"><span data-stu-id="4374d-128">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

