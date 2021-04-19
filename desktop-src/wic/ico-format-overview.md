---
description: 本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 .ICO 編解碼器的相關資訊。
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: .ICO 格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d370497e9231d6deb8d1793a26a53565b5cd99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988411"
---
# <a name="ico-format-overview"></a><span data-ttu-id="6af7c-103">.ICO 格式總覽</span><span class="sxs-lookup"><span data-stu-id="6af7c-103">ICO Format Overview</span></span>

<span data-ttu-id="6af7c-104">本主題提供可透過 Windows 影像處理元件 (WIC) 取得之原生 .ICO 編解碼器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6af7c-104">This topic provides information about the native ICO codec available through Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="6af7c-105">編解碼器身分識別</span><span class="sxs-lookup"><span data-stu-id="6af7c-105">Codec Identity</span></span>

<span data-ttu-id="6af7c-106">下表提供編解碼器識別資訊。</span><span class="sxs-lookup"><span data-stu-id="6af7c-106">The following table provides codec identification information.</span></span>



|                        |                   |
|------------------------|-------------------|
| <span data-ttu-id="6af7c-107"> (s 的正式名稱) </span><span class="sxs-lookup"><span data-stu-id="6af7c-107">Formal Name(s)</span></span>         | <span data-ttu-id="6af7c-108"> (.ICO) 的圖示格式</span><span class="sxs-lookup"><span data-stu-id="6af7c-108">Icon Format (ICO)</span></span> |
| <span data-ttu-id="6af7c-109">副檔名 (s) </span><span class="sxs-lookup"><span data-stu-id="6af7c-109">File Name Extension(s)</span></span> | <span data-ttu-id="6af7c-110">.ico</span><span class="sxs-lookup"><span data-stu-id="6af7c-110">ico</span></span>               |
| <span data-ttu-id="6af7c-111">MIME 類型 (MIME type)</span><span class="sxs-lookup"><span data-stu-id="6af7c-111">MIME type</span></span>              | <span data-ttu-id="6af7c-112">影像/.ico</span><span class="sxs-lookup"><span data-stu-id="6af7c-112">image/ico</span></span>         |
| <span data-ttu-id="6af7c-113">規格支援</span><span class="sxs-lookup"><span data-stu-id="6af7c-113">Specification Support</span></span>  |                   |



 

<span data-ttu-id="6af7c-114">下表列出用來識別原生 .ICO 編解碼器元件的 Guid。</span><span class="sxs-lookup"><span data-stu-id="6af7c-114">The following table lists the GUIDs used to identify the native ICO codec components.</span></span>



| <span data-ttu-id="6af7c-115">元件</span><span class="sxs-lookup"><span data-stu-id="6af7c-115">Component</span></span>        | <span data-ttu-id="6af7c-116">易記名稱</span><span class="sxs-lookup"><span data-stu-id="6af7c-116">Friendly Name</span></span>            | <span data-ttu-id="6af7c-117">GUID</span><span class="sxs-lookup"><span data-stu-id="6af7c-117">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="6af7c-118">容器格式</span><span class="sxs-lookup"><span data-stu-id="6af7c-118">Container Format</span></span> | <span data-ttu-id="6af7c-119">GUID \_ ContainerFormatIco</span><span class="sxs-lookup"><span data-stu-id="6af7c-119">GUID\_ContainerFormatIco</span></span> | <span data-ttu-id="6af7c-120">a3a860c4-338f-4c17-919afba4b5628f21</span><span class="sxs-lookup"><span data-stu-id="6af7c-120">a3a860c4-338f-4c17-919afba4b5628f21</span></span> |
| <span data-ttu-id="6af7c-121">解碼器</span><span class="sxs-lookup"><span data-stu-id="6af7c-121">Decoder</span></span>          | <span data-ttu-id="6af7c-122">CLSID \_ WICIcoDecoder</span><span class="sxs-lookup"><span data-stu-id="6af7c-122">CLSID\_WICIcoDecoder</span></span>     | <span data-ttu-id="6af7c-123">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span><span class="sxs-lookup"><span data-stu-id="6af7c-123">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span></span> |
| <span data-ttu-id="6af7c-124">編碼器</span><span class="sxs-lookup"><span data-stu-id="6af7c-124">Encoder</span></span>          | <span data-ttu-id="6af7c-125">無法使用</span><span class="sxs-lookup"><span data-stu-id="6af7c-125">NOT AVAILABLE</span></span>            | <span data-ttu-id="6af7c-126">無法使用</span><span class="sxs-lookup"><span data-stu-id="6af7c-126">NOT AVAILABLE</span></span>                       |



 

## <a name="encoding"></a><span data-ttu-id="6af7c-127">編碼</span><span class="sxs-lookup"><span data-stu-id="6af7c-127">Encoding</span></span>

<span data-ttu-id="6af7c-128">WIC 不提供原生的 .ICO 影像編碼器。</span><span class="sxs-lookup"><span data-stu-id="6af7c-128">WIC does not provide a native ICO image encoder.</span></span>

## <a name="decoding"></a><span data-ttu-id="6af7c-129">解碼</span><span class="sxs-lookup"><span data-stu-id="6af7c-129">Decoding</span></span>

<span data-ttu-id="6af7c-130">WIC 解碼 API 設計成與編解碼器無關，且已啟用 WIC 的編解碼器影像解碼本質上是相同的。</span><span class="sxs-lookup"><span data-stu-id="6af7c-130">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="6af7c-131">如需影像解碼的詳細資訊，請參閱 [解碼總覽](-wic-creating-decoder.md)。</span><span class="sxs-lookup"><span data-stu-id="6af7c-131">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="6af7c-132">如需使用已解碼之影像資料的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="6af7c-132">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 



