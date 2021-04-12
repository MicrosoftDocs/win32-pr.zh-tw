---
title: 設定文字資料流程
description: 設定文字資料流程
ms.assetid: d99baac5-69e5-4e0a-9cd6-35b288d8181a
keywords:
- 資料流程，設定文字資料流程
- 編解碼器，設定文字資料流程
- 文字資料流程，設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460369eaae02f636f8ddda8bcca4f29ecfc2e1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462237"
---
# <a name="configuring-text-streams"></a><span data-ttu-id="7fb37-106">設定文字資料流程</span><span class="sxs-lookup"><span data-stu-id="7fb37-106">Configuring Text Streams</span></span>

<span data-ttu-id="7fb37-107">文字資料流程基本上與自訂任意資料流程相同。</span><span class="sxs-lookup"><span data-stu-id="7fb37-107">Text streams are essentially the same as custom arbitrary streams.</span></span> <span data-ttu-id="7fb37-108">沒有與文字資料流程相關聯的設定資訊可識別文字編碼類型，因此寫入器物件無法驗證範例。</span><span class="sxs-lookup"><span data-stu-id="7fb37-108">There is no configuration information associated with a text stream to identify the type of text encoding, so the writer object cannot verify samples.</span></span>

<span data-ttu-id="7fb37-109">若要設定文字資料流程，您必須確定 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構包含 WMMEDIATYPE 文字的主要媒體類型 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7fb37-109">To configure a text stream, you must ensure that the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure contains a major media type of WMMEDIATYPE\_TEXT.</span></span> <span data-ttu-id="7fb37-110">您也必須設定資料流程的位元速率和緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="7fb37-110">You must also set a bit rate and buffer window for the stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fb37-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="7fb37-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fb37-112">**計算任意資料流程的位元速率和緩衝區視窗值**</span><span class="sxs-lookup"><span data-stu-id="7fb37-112">**Calculating Bit Rate and Buffer Window Values for Arbitrary Streams**</span></span>](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="7fb37-113">**所有資料流程通用的設定**</span><span class="sxs-lookup"><span data-stu-id="7fb37-113">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="7fb37-114">**設定任意資料流程類型**</span><span class="sxs-lookup"><span data-stu-id="7fb37-114">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="7fb37-115">**文字資料流**</span><span class="sxs-lookup"><span data-stu-id="7fb37-115">**Text Streams**</span></span>](text-streams.md)
</dt> </dl>

 

 




