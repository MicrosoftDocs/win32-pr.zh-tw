---
description: 強制插入主要畫面格
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: '強制插入主要畫面格 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d053f97c7aff08f61fa56d07db0a28b20c797d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468624"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a><span data-ttu-id="6439b-103">強制插入主要畫面格 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="6439b-103">Forced Key Frame Insertion (Microsoft Media Foundation)</span></span>

<span data-ttu-id="6439b-104">當您設定影片編碼器物件時，可以在編碼內容中設定主要畫面格的最大間隔。</span><span class="sxs-lookup"><span data-stu-id="6439b-104">When you configure a video encoder object, you can set a maximum interval for key frames in the encoded content.</span></span> <span data-ttu-id="6439b-105">不過，編解碼器會將主要畫面格放在該間隔內，如內容所規定;主要畫面格間隔不是常數。</span><span class="sxs-lookup"><span data-stu-id="6439b-105">However, the codec will place key frames within that interval as dictated by the content; the key frame interval is not constant.</span></span> <span data-ttu-id="6439b-106">對於某些應用程式而言，主要畫面格距離相當重要。</span><span class="sxs-lookup"><span data-stu-id="6439b-106">For some applications, the key frame distance is very important.</span></span> <span data-ttu-id="6439b-107">例如，影片編輯應用程式需要主要畫面格位於編輯器的邏輯位置，例如場景中斷和拍攝轉換。</span><span class="sxs-lookup"><span data-stu-id="6439b-107">For example, a video editing application needs key frames at locations that are logical to an editor, like at scene breaks and shot transitions.</span></span>

<span data-ttu-id="6439b-108">強制插入主要畫面格是一項功能，可讓您要求輸入框架以主要畫面格的形式編碼。</span><span class="sxs-lookup"><span data-stu-id="6439b-108">Forced key frame insertion is a feature that enables you to request that an input frame be encoded as a key frame.</span></span> <span data-ttu-id="6439b-109">編碼器會嘗試接受這些要求，但針對編碼會話設定的緩衝區設定 (位元速率和緩衝區視窗) 一律優先。</span><span class="sxs-lookup"><span data-stu-id="6439b-109">The encoder will try to honor these requests, but the buffer settings (bit rate and buffer window) configured for the encoding session always take precedence.</span></span>

<span data-ttu-id="6439b-110">影片編碼器物件會執行強制的主要畫面格插入，以回應附加至輸入範例的資料單位延伸模組。</span><span class="sxs-lookup"><span data-stu-id="6439b-110">The video encoder objects implement forced key frame insertion as a response to a data unit extension attached to the input sample.</span></span> <span data-ttu-id="6439b-111">如需有關資料單位延伸的詳細資訊，請參閱 [使用資料單位延伸](usingdataunitextensions.md)。</span><span class="sxs-lookup"><span data-stu-id="6439b-111">For more information about data unit extensions, see [Using Data Unit Extensions](usingdataunitextensions.md).</span></span>

<span data-ttu-id="6439b-112">強制主要畫面格插入的延伸模組資料是以下列 GUID 值來識別： **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**。</span><span class="sxs-lookup"><span data-stu-id="6439b-112">The extension data for forced key frame insertion is identified by the following GUID value: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**.</span></span> <span data-ttu-id="6439b-113">個別的延伸模組為 **BOOL** 值。</span><span class="sxs-lookup"><span data-stu-id="6439b-113">The individual extensions are **BOOL** values.</span></span> <span data-ttu-id="6439b-114">將值設定為 **TRUE** ，表示主要畫面格要求。</span><span class="sxs-lookup"><span data-stu-id="6439b-114">Set the value to **TRUE** to indicate a key frame request.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6439b-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="6439b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6439b-116">使用資料單位延伸模組</span><span class="sxs-lookup"><span data-stu-id="6439b-116">Using Data Unit Extensions</span></span>](usingdataunitextensions.md)
</dt> <dt>

[<span data-ttu-id="6439b-117">使用影片</span><span class="sxs-lookup"><span data-stu-id="6439b-117">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



