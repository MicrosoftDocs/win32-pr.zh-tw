---
title: 產生對話方塊來選取限制的格式
description: 產生對話方塊來選取限制的格式
ms.assetid: 486ba928-e06d-4ab0-a642-ba0fe16c8291
keywords:
- 音訊壓縮管理員 (的) 、產生對話方塊
- " (音效壓縮管理員) 、產生對話方塊"
- 進行中的範例，產生對話方塊
- 產生對話方塊
- acmFormatChoose 函式
- 音訊壓縮管理員 (的) ，選取受限制的格式
- " (音效壓縮管理員) ，選取受限格式"
- 未通過範例，選取受限制的格式
- 選取限制的格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800945f4003c0fbe47d7916e0a1bf707745ff6d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021581"
---
# <a name="producing-a-dialog-box-for-selecting-restricted-formats"></a><span data-ttu-id="73340-112">產生對話方塊來選取限制的格式</span><span class="sxs-lookup"><span data-stu-id="73340-112">Producing a Dialog Box for Selecting Restricted Formats</span></span>

<span data-ttu-id="73340-113">您可能會想要使用 [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) 函式所建立的對話方塊，但限制或控制對話方塊中的格式。</span><span class="sxs-lookup"><span data-stu-id="73340-113">You might want to use the dialog box created by the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, but limit or control the formats in the dialog box.</span></span> <span data-ttu-id="73340-114">若要這樣做，您可以使用 ACMFORMATCHOOSE \_ STYLEF \_ ENABLEHOOK 旗標來攔截對話程式。</span><span class="sxs-lookup"><span data-stu-id="73340-114">You can do this by using the ACMFORMATCHOOSE\_STYLEF\_ENABLEHOOK flag to hook the dialog procedure.</span></span> <span data-ttu-id="73340-115">然後，應用程式可以藉由回應對話方塊的訊息程式中的 [**MM \_ \_ FORMATCHOOSE**](mm-acm-formatchoose.md) 訊息來篩選格式。</span><span class="sxs-lookup"><span data-stu-id="73340-115">The application can then filter the formats by responding to the [**MM\_ACM\_FORMATCHOOSE**](mm-acm-formatchoose.md) message in the message procedure for the dialog box.</span></span>

 

 




