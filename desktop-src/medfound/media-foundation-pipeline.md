---
description: Microsoft 媒體基礎中的管線層是直接產生或處理媒體資料的架構層。
ms.assetid: d6396246-ddc4-4e24-9371-35ddbef59b8a
title: 媒體基礎管線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f307049d7f88ca6b50479bdb261c75ba20f9b41e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106992635"
---
# <a name="media-foundation-pipeline"></a><span data-ttu-id="fdbf1-103">媒體基礎管線</span><span class="sxs-lookup"><span data-stu-id="fdbf1-103">Media Foundation Pipeline</span></span>

<span data-ttu-id="fdbf1-104">Microsoft 媒體基礎中的 *管線* 層是直接產生或處理媒體資料的架構層。</span><span class="sxs-lookup"><span data-stu-id="fdbf1-104">The *pipeline* layer in Microsoft Media Foundation is the layer of the architecture that directly generates or processes media data.</span></span>

<span data-ttu-id="fdbf1-105">大部分的應用程式不會直接在管線元件上呼叫方法，雖然可以這樣做。</span><span class="sxs-lookup"><span data-stu-id="fdbf1-105">Most applications do not call methods directly on the pipeline components, although it is possible to do so.</span></span> <span data-ttu-id="fdbf1-106">如果您要撰寫自訂管線元件，請閱讀這些主題。</span><span class="sxs-lookup"><span data-stu-id="fdbf1-106">Read these topics if you are writing a custom pipeline component.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fdbf1-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="fdbf1-107">In this section</span></span>



| <span data-ttu-id="fdbf1-108">主題</span><span class="sxs-lookup"><span data-stu-id="fdbf1-108">Topic</span></span>                                                                     | <span data-ttu-id="fdbf1-109">描述</span><span class="sxs-lookup"><span data-stu-id="fdbf1-109">Description</span></span>                                                                                                                           |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fdbf1-110">媒體來源</span><span class="sxs-lookup"><span data-stu-id="fdbf1-110">Media Sources</span></span>](media-sources.md)<br/>                             | <span data-ttu-id="fdbf1-111">媒體來源會產生媒體資料，通常是從檔案、捕獲裝置或網路串流。</span><span class="sxs-lookup"><span data-stu-id="fdbf1-111">Media sources generate media data, typically from a file, capture device, or network stream.</span></span> <br/>                              |
| [<span data-ttu-id="fdbf1-112">媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="fdbf1-112">Media Foundation Transforms</span></span>](media-foundation-transforms.md)<br/> | <span data-ttu-id="fdbf1-113">媒體基礎轉換 (MFTs) 處理媒體資料。</span><span class="sxs-lookup"><span data-stu-id="fdbf1-113">Media Foundation transforms (MFTs) process media data.</span></span> <span data-ttu-id="fdbf1-114">例如，媒體基礎中的編解碼器會實作為 MFTs。</span><span class="sxs-lookup"><span data-stu-id="fdbf1-114">For example, codecs in Media Foundation are implemented as MFTs.</span></span> <br/>   |
| [<span data-ttu-id="fdbf1-115">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="fdbf1-115">Media Sinks</span></span>](media-sinks.md)<br/>                                 | <span data-ttu-id="fdbf1-116">媒體接收器會使用媒體資料。</span><span class="sxs-lookup"><span data-stu-id="fdbf1-116">Media sinks consume media data.</span></span> <span data-ttu-id="fdbf1-117">例如，媒體接收器可能會將資料寫入檔案，或透過網路傳送資料。</span><span class="sxs-lookup"><span data-stu-id="fdbf1-117">For example, a media sink might write the data to a file, or send the data over a network.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="fdbf1-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="fdbf1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdbf1-119">媒體基礎和 COM</span><span class="sxs-lookup"><span data-stu-id="fdbf1-119">Media Foundation and COM</span></span>](media-foundation-and-com.md)
</dt> <dt>

[<span data-ttu-id="fdbf1-120">媒體基礎架構</span><span class="sxs-lookup"><span data-stu-id="fdbf1-120">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 




