---
description: Intel Advanced Vector Extensions (AVX) 是 Intel 架構的256位 SIMD 浮點數向量擴充功能。 它包含指令和註冊集合的延伸。
ms.assetid: 76357e08-a53c-4490-b08d-1c26900a3826
title: Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 454c8bd5090463cefa1b0ff3a27ef7a04787db0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385852"
---
# <a name="intel-avx"></a><span data-ttu-id="77c08-104">Intel AVX</span><span class="sxs-lookup"><span data-stu-id="77c08-104">Intel AVX</span></span>

## <a name="purpose"></a><span data-ttu-id="77c08-105">目的</span><span class="sxs-lookup"><span data-stu-id="77c08-105">Purpose</span></span>

<span data-ttu-id="77c08-106">Intel Advanced Vector Extensions (AVX) 是 Intel 架構的256位 SIMD 浮點數向量擴充功能。</span><span class="sxs-lookup"><span data-stu-id="77c08-106">Intel Advanced Vector Extensions (AVX) is a 256-bit SIMD floating point vector extension of Intel architecture.</span></span> <span data-ttu-id="77c08-107">它包含指令和註冊集合的延伸。</span><span class="sxs-lookup"><span data-stu-id="77c08-107">It includes extensions to both instruction and register sets.</span></span>

<span data-ttu-id="77c08-108">Microsoft 開發了一些 API 增強功能（例如 XState 函式），可讓應用程式存取和操作擴充的處理器功能資訊和狀態，包括 Intel AVX。</span><span class="sxs-lookup"><span data-stu-id="77c08-108">Microsoft has developed some API enhancements, such as XState functions, that enable applications to access and manipulate extended processor feature information and state, including Intel AVX.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="77c08-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="77c08-109">In this section</span></span>



| <span data-ttu-id="77c08-110">主題</span><span class="sxs-lookup"><span data-stu-id="77c08-110">Topic</span></span>                                                                     | <span data-ttu-id="77c08-111">描述</span><span class="sxs-lookup"><span data-stu-id="77c08-111">Description</span></span>                                                                                                                                               |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77c08-112">使用 XState 內容</span><span class="sxs-lookup"><span data-stu-id="77c08-112">Working with XState Context</span></span>](working-with-xstate-context.md)<br/> | <span data-ttu-id="77c08-113">本檔包含的範例示範如何使用 XState 內容函式，線上程上取得和設定擴充功能。</span><span class="sxs-lookup"><span data-stu-id="77c08-113">This document contains an example that demonstrates how to use the XState context functions to retrieve and set extended features on a thread.</span></span><br/> |
| [<span data-ttu-id="77c08-114">AVX 函式</span><span class="sxs-lookup"><span data-stu-id="77c08-114">AVX Functions</span></span>](avx-functions.md)<br/>                             | <span data-ttu-id="77c08-115">Intel AVX 函式</span><span class="sxs-lookup"><span data-stu-id="77c08-115">Intel AVX functions</span></span><br/>                                                                                                                            |



 

## <a name="developer-audience"></a><span data-ttu-id="77c08-116">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="77c08-116">Developer audience</span></span>

<span data-ttu-id="77c08-117">Intel AVX 的設計目的是要讓高度浮點數計算的應用程式使用，而且可以向量化。</span><span class="sxs-lookup"><span data-stu-id="77c08-117">Intel AVX is designed for use by applications that are strongly floating point compute intensive and can be vectorized.</span></span> <span data-ttu-id="77c08-118">範例應用程式包括音訊處理和音訊編解碼器、影像和影片編輯應用程式、金融服務分析和模型軟體，以及製造和工程軟體。</span><span class="sxs-lookup"><span data-stu-id="77c08-118">Example applications include audio processing and audio codecs, image and video editing applications, financial services analysis and modeling software, and manufacturing and engineering software.</span></span>

 

 




