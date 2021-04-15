---
description: 限制模式設定檔和設定建立
ms.assetid: 550f5413-eaa4-4530-867e-fd9b1907cadf
title: 限制模式設定檔和設定建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a424505b3934131527f249176f9fe0984b320a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385661"
---
# <a name="restricted-mode-profile-and-configuration-establishment"></a><span data-ttu-id="af554-103">限制模式設定檔和設定建立</span><span class="sxs-lookup"><span data-stu-id="af554-103">Restricted Mode Profile and Configuration Establishment</span></span>

<span data-ttu-id="af554-104">由於 DirectX VA 可以解碼各種類型的資料，針對上述每一種類型的資料，在 DirectX VA 中支援的多個解碼設定 (例如，使用位流緩衝區與主機剩餘差異解碼的比較，或不加密每個相關類型的緩衝區，而不加密每個相關的緩衝區類型，因此在) 上，我們相信您只需要為每個唯一的資料類型和解碼設定指定唯一的 GUID。</span><span class="sxs-lookup"><span data-stu-id="af554-104">Due to the variety of types of data that can be decoded by DirectX VA, and the multiple decoding configurations supported within DirectX VA for each of these types of data (for example, using bitstream buffers versus host residual difference decoding versus accelerator-based IDCT with and without encryption of each relevant type of buffer, and so on), we believe it would be somewhat ungainly to simply specify a unique GUID for every unique data type and decoding configuration.</span></span> <span data-ttu-id="af554-105">這會建立大量的 Guid (例如，如果每個都有16個 DirectX VA 和16設定的設定檔，則需要有256個定義的 Guid，而只需要 4 kb 的記憶體就能容納全部。</span><span class="sxs-lookup"><span data-stu-id="af554-105">This would create a large number of GUIDs (for example, hypothetically if there were 16 profiles of DirectX VA and 16 configurations possible for each, there would need to be 256 defined GUIDs—requiring 4 kilobytes of memory just to hold them all.</span></span> <span data-ttu-id="af554-106">此問題是決定如何將 DirectX VA 對應到 **IAMVideoAccelerator** 的最困難部分，而作業定義的其餘部分大多相當簡單。</span><span class="sxs-lookup"><span data-stu-id="af554-106">This issue is the most difficult part of determining how to map DirectX VA into **IAMVideoAccelerator**, with the remainder of the operational definition mostly being quite straightforward.</span></span> <span data-ttu-id="af554-107">因此，我們只會針對每個受限制模式配置) 檔的資料類型 (指定唯一的 GUID，並允許額外的 GUID 與每一種加密類型相關聯。</span><span class="sxs-lookup"><span data-stu-id="af554-107">As a result, we specify a unique GUID only for each type of data (for each restricted mode profile) and allow an additional GUID to be associated with each type of encryption.</span></span> <span data-ttu-id="af554-108">然後，會使用探查和鎖定作業來建立每個 DirectX VA 函式類型的設定，以使用探查和鎖定作業來建立解碼器與加速器之間的解碼設定。</span><span class="sxs-lookup"><span data-stu-id="af554-108">The decoding configuration is then established between the decoder and accelerator by a lower-level subordinate negotiation using probing and locking operations to establish configurations for each type of DirectX VA function.</span></span>

 

 



