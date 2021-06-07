---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 .ICO 編解碼器的相關資訊。
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: .ICO 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329a53a3b5d386c5e5386141162c608dc9db1ec0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444468"
---
# <a name="ico-format-overview"></a><span data-ttu-id="66bc8-103">.ICO 格式總覽</span><span class="sxs-lookup"><span data-stu-id="66bc8-103">ICO Format Overview</span></span>

<span data-ttu-id="66bc8-104">本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 .ICO 編解碼器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="66bc8-104">This topic provides information about the native ICO codec available through Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="66bc8-105">編解碼器身分識別</span><span class="sxs-lookup"><span data-stu-id="66bc8-105">Codec Identity</span></span>

<span data-ttu-id="66bc8-106">下表提供編解碼器識別資訊。</span><span class="sxs-lookup"><span data-stu-id="66bc8-106">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="66bc8-107">元件</span><span class="sxs-lookup"><span data-stu-id="66bc8-107">Component</span></span>            | <span data-ttu-id="66bc8-108">描述</span><span class="sxs-lookup"><span data-stu-id="66bc8-108">Description</span></span>       |
|------------------------|-------------------|
| <span data-ttu-id="66bc8-109"> (s 的正式名稱) </span><span class="sxs-lookup"><span data-stu-id="66bc8-109">Formal Name(s)</span></span>         | <span data-ttu-id="66bc8-110"> (.ICO) 的圖示格式</span><span class="sxs-lookup"><span data-stu-id="66bc8-110">Icon Format (ICO)</span></span> |
| <span data-ttu-id="66bc8-111">副檔名 (s) </span><span class="sxs-lookup"><span data-stu-id="66bc8-111">File Name Extension(s)</span></span> | <span data-ttu-id="66bc8-112">.ico</span><span class="sxs-lookup"><span data-stu-id="66bc8-112">ico</span></span>               |
| <span data-ttu-id="66bc8-113">MIME 類型 (MIME type)</span><span class="sxs-lookup"><span data-stu-id="66bc8-113">MIME type</span></span>              | <span data-ttu-id="66bc8-114">影像/.ico</span><span class="sxs-lookup"><span data-stu-id="66bc8-114">image/ico</span></span>         |
| <span data-ttu-id="66bc8-115">規格支援</span><span class="sxs-lookup"><span data-stu-id="66bc8-115">Specification Support</span></span>  |                   |



 

<span data-ttu-id="66bc8-116">下表列出用來識別原生 .ICO 編解碼器元件的 Guid。</span><span class="sxs-lookup"><span data-stu-id="66bc8-116">The following table lists the GUIDs used to identify the native ICO codec components.</span></span>



| <span data-ttu-id="66bc8-117">元件</span><span class="sxs-lookup"><span data-stu-id="66bc8-117">Component</span></span>        | <span data-ttu-id="66bc8-118">易記名稱</span><span class="sxs-lookup"><span data-stu-id="66bc8-118">Friendly Name</span></span>            | <span data-ttu-id="66bc8-119">GUID</span><span class="sxs-lookup"><span data-stu-id="66bc8-119">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="66bc8-120">容器格式</span><span class="sxs-lookup"><span data-stu-id="66bc8-120">Container Format</span></span> | <span data-ttu-id="66bc8-121">GUID \_ ContainerFormatIco</span><span class="sxs-lookup"><span data-stu-id="66bc8-121">GUID\_ContainerFormatIco</span></span> | <span data-ttu-id="66bc8-122">a3a860c4-338f-4c17-919afba4b5628f21</span><span class="sxs-lookup"><span data-stu-id="66bc8-122">a3a860c4-338f-4c17-919afba4b5628f21</span></span> |
| <span data-ttu-id="66bc8-123">解碼器</span><span class="sxs-lookup"><span data-stu-id="66bc8-123">Decoder</span></span>          | <span data-ttu-id="66bc8-124">CLSID \_ WICIcoDecoder</span><span class="sxs-lookup"><span data-stu-id="66bc8-124">CLSID\_WICIcoDecoder</span></span>     | <span data-ttu-id="66bc8-125">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span><span class="sxs-lookup"><span data-stu-id="66bc8-125">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span></span> |
| <span data-ttu-id="66bc8-126">編碼器</span><span class="sxs-lookup"><span data-stu-id="66bc8-126">Encoder</span></span>          | <span data-ttu-id="66bc8-127">無法使用</span><span class="sxs-lookup"><span data-stu-id="66bc8-127">NOT AVAILABLE</span></span>            | <span data-ttu-id="66bc8-128">無法使用</span><span class="sxs-lookup"><span data-stu-id="66bc8-128">NOT AVAILABLE</span></span>                       |



 

## <a name="encoding"></a><span data-ttu-id="66bc8-129">編碼</span><span class="sxs-lookup"><span data-stu-id="66bc8-129">Encoding</span></span>

<span data-ttu-id="66bc8-130">WIC 不提供原生的 .ICO 影像編碼器。</span><span class="sxs-lookup"><span data-stu-id="66bc8-130">WIC does not provide a native ICO image encoder.</span></span>

## <a name="decoding"></a><span data-ttu-id="66bc8-131">解碼</span><span class="sxs-lookup"><span data-stu-id="66bc8-131">Decoding</span></span>

<span data-ttu-id="66bc8-132">WIC 解碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="66bc8-132">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="66bc8-133">如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。</span><span class="sxs-lookup"><span data-stu-id="66bc8-133">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="66bc8-134">如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="66bc8-134">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 



