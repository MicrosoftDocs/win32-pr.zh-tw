---
description: 媒體基礎轉換
ms.assetid: cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0
title: 媒體基礎轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0518ced06169f6d998bdad1747878d109e0676
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106998564"
---
# <a name="media-foundation-transforms"></a><span data-ttu-id="1b3d6-103">媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="1b3d6-103">Media Foundation Transforms</span></span>

<span data-ttu-id="1b3d6-104">媒體基礎轉換 (MFTs) 提供用來處理媒體資料的一般模型。</span><span class="sxs-lookup"><span data-stu-id="1b3d6-104">Media Foundation transforms (MFTs) provide a generic model for processing media data.</span></span> <span data-ttu-id="1b3d6-105">MFTs 可用於 (Dsp) 的解碼器、編碼器和數位訊號處理器。</span><span class="sxs-lookup"><span data-stu-id="1b3d6-105">MFTs are used for decoders, encoders, and digital signal processors (DSPs).</span></span> <span data-ttu-id="1b3d6-106">簡而言之，位於媒體來源和媒體接收器之間媒體管線中的任何事物，都是一個 MFT。</span><span class="sxs-lookup"><span data-stu-id="1b3d6-106">In short, anything that sits in the media pipeline between the media source and the media sink is an MFT.</span></span>

<span data-ttu-id="1b3d6-107">本節描述 MFT 程式設計模型，以及如何使用特定 MFTs 類型的建議（例如，解碼器）來執行 MFT。</span><span class="sxs-lookup"><span data-stu-id="1b3d6-107">This section describes the MFT programming model and how to implement an MFT, with recommendations for specific types of MFTs, such as decoders.</span></span>



| <span data-ttu-id="1b3d6-108">主題</span><span class="sxs-lookup"><span data-stu-id="1b3d6-108">Topic</span></span>                                                                    | <span data-ttu-id="1b3d6-109">描述</span><span class="sxs-lookup"><span data-stu-id="1b3d6-109">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b3d6-110">關於 MFTs</span><span class="sxs-lookup"><span data-stu-id="1b3d6-110">About MFTs</span></span>](about-mfts.md)                                             | <span data-ttu-id="1b3d6-111">提供 MFTs 的簡短總覽</span><span class="sxs-lookup"><span data-stu-id="1b3d6-111">Provides a brief overview of MFTs</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="1b3d6-112">基本 MFT 處理模型</span><span class="sxs-lookup"><span data-stu-id="1b3d6-112">Basic MFT Processing Model</span></span>](basic-mft-processing-model.md)             | <span data-ttu-id="1b3d6-113">更詳細地說明使用 MFT 處理資料的基本模型。</span><span class="sxs-lookup"><span data-stu-id="1b3d6-113">Describes in more detail the basic model for processing data with an MFT.</span></span>                                                                                                                           |
| [<span data-ttu-id="1b3d6-114">非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="1b3d6-114">Asynchronous MFTs</span></span>](asynchronous-mfts.md)                               | <span data-ttu-id="1b3d6-115">描述替代基本模型的非同步處理模型。</span><span class="sxs-lookup"><span data-stu-id="1b3d6-115">Describes an asynchronous processing model that is an alternative to the basic model.</span></span><br/> <span data-ttu-id="1b3d6-116">非同步處理是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="1b3d6-116">Asynchronous processing was introduced in Windows 7.</span></span> <span data-ttu-id="1b3d6-117">並非所有的 MFT 都支援此模型。</span><span class="sxs-lookup"><span data-stu-id="1b3d6-117">Not every MFT supports this model.</span></span><br/> |
| [<span data-ttu-id="1b3d6-118">註冊和列舉 MFTs</span><span class="sxs-lookup"><span data-stu-id="1b3d6-118">Registering and Enumerating MFTs</span></span>](registering-and-enumerating-mfts.md) | <span data-ttu-id="1b3d6-119">如何註冊 MFT 以及如何列舉登錄中的 MFTs。</span><span class="sxs-lookup"><span data-stu-id="1b3d6-119">How to register an MFT and how to enumerate MFTs in the registry.</span></span>                                                                                                                                   |
| [<span data-ttu-id="1b3d6-120">使用限制領域</span><span class="sxs-lookup"><span data-stu-id="1b3d6-120">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)               | <span data-ttu-id="1b3d6-121">描述解除鎖定具有使用規定限制之 MFT 的機制。</span><span class="sxs-lookup"><span data-stu-id="1b3d6-121">Describes the mechanism for unlocking an MFT that has field-of-use restrictions.</span></span>                                                                                                                    |
| [<span data-ttu-id="1b3d6-122">MFT 和 DMO 的比較</span><span class="sxs-lookup"><span data-stu-id="1b3d6-122">Comparison of MFTs and DMOs</span></span>](comparison-of-mfts-and-dmos.md)           | <span data-ttu-id="1b3d6-123">摘要說明 MFTs 與 DMOs 之間的差異。</span><span class="sxs-lookup"><span data-stu-id="1b3d6-123">Summarizes the differences between MFTs and DMOs.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="1b3d6-124">撰寫自訂的 MFT</span><span class="sxs-lookup"><span data-stu-id="1b3d6-124">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)                         | <span data-ttu-id="1b3d6-125">撰寫自訂 MFT 的指導方針。</span><span class="sxs-lookup"><span data-stu-id="1b3d6-125">Guidelines for writing a custom MFT.</span></span>                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="1b3d6-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="1b3d6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b3d6-127">媒體基礎管線</span><span class="sxs-lookup"><span data-stu-id="1b3d6-127">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)
</dt> <dt>

[<span data-ttu-id="1b3d6-128">媒體基礎架構</span><span class="sxs-lookup"><span data-stu-id="1b3d6-128">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="1b3d6-129">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="1b3d6-129">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




