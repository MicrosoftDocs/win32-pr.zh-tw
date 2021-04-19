---
description: 編碼
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: '編碼 (Windows 影像處理元件) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6d15b983b7455d0fe0c406cbad64dbbb77588b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985023"
---
# <a name="encoding-windows-imaging-component"></a><span data-ttu-id="ef49b-103">編碼 (Windows 影像處理元件) </span><span class="sxs-lookup"><span data-stu-id="ef49b-103">Encoding (Windows Imaging Component)</span></span>

<span data-ttu-id="ef49b-104">編碼器作者必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="ef49b-104">The encoder author must do the following:</span></span>

-   <span data-ttu-id="ef49b-105">執行 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) 和 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 介面。</span><span class="sxs-lookup"><span data-stu-id="ef49b-105">Implement [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) interfaces.</span></span>
-   <span data-ttu-id="ef49b-106">在畫面格編碼器上執行 [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) 。</span><span class="sxs-lookup"><span data-stu-id="ef49b-106">Implement [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) on the frame encoder.</span></span> <span data-ttu-id="ef49b-107">如果編解碼器支援容器層級的中繼資料，則必須在容器層級編碼器以及框架編碼器上實作為此介面。</span><span class="sxs-lookup"><span data-stu-id="ef49b-107">If the codec supports container-level metadata, this interface must be implemented on the container-level encoder as well as on the frame encoder.</span></span>
-   <span data-ttu-id="ef49b-108">如果容器格式隱含地包含任何必要的中繼資料區塊，請為每個這類區塊具現化中繼資料寫入器。</span><span class="sxs-lookup"><span data-stu-id="ef49b-108">If the container format implicitly contains any mandatory metadata blocks, instantiate a metadata writer for each such block.</span></span> <span data-ttu-id="ef49b-109">例如，TIFF 格式需要介面裝置 (每個框架的 IFD) ，因此必須一律公開 IFD 寫入器。</span><span class="sxs-lookup"><span data-stu-id="ef49b-109">For example, the TIFF format requires an interface device (IFD) for each frame, so the IFD writer must always be exposed.</span></span>
-   <span data-ttu-id="ef49b-110">執行管理中繼資料寫入器集合的支援。</span><span class="sxs-lookup"><span data-stu-id="ef49b-110">Implement support for managing the collection of metadata writers.</span></span> <span data-ttu-id="ef49b-111">區塊寫入器會針對可編碼的中繼資料區塊類型，管理任何順序需求或容器限制。</span><span class="sxs-lookup"><span data-stu-id="ef49b-111">The block writer manages any order requirements or container restrictions on the kinds of metadata blocks that can be encoded.</span></span> <span data-ttu-id="ef49b-112">區塊寫入器必須確認是否有任何新的中繼資料寫入器可內嵌在容器格式內。</span><span class="sxs-lookup"><span data-stu-id="ef49b-112">The block writer must verify that any new metadata writers can be embedded within the container format.</span></span>
-   <span data-ttu-id="ef49b-113">編碼影像資料流程時，請呼叫 [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) 將每個中繼資料寫入器的內容序列化為數據流。</span><span class="sxs-lookup"><span data-stu-id="ef49b-113">When encoding the image stream, call [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) to serialize each metadata writer’s content into the stream.</span></span> <span data-ttu-id="ef49b-114">如果中繼資料區塊包含 "critical" 中繼資料，則編碼器必須先設定重要的中繼資料專案，然後再要求中繼資料寫入器序列化內容。</span><span class="sxs-lookup"><span data-stu-id="ef49b-114">If the metadata block contains "critical" metadata the encoder must set the critical metadata items before asking the metadata writer to serialize content.</span></span>
-   <span data-ttu-id="ef49b-115">檢查是否有任何未知的元資料處理程式，以確保不會有多餘的中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="ef49b-115">Check for any unknown metadata handlers to ensure that redundant metadata blocks are not present.</span></span> <span data-ttu-id="ef49b-116">這點很重要，因為在解碼或編碼案例中保留中繼資料時，未知的區塊可能是強制中繼資料區塊的重複項。</span><span class="sxs-lookup"><span data-stu-id="ef49b-116">This is important because, while preserving metadata in a decode or encode scenario, unknown blocks might be a duplicate of mandatory metadata blocks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef49b-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef49b-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ef49b-118">**概念**</span><span class="sxs-lookup"><span data-stu-id="ef49b-118">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ef49b-119">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="ef49b-119">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="ef49b-120">相機原始影像格式的 WIC 指導方針</span><span class="sxs-lookup"><span data-stu-id="ef49b-120">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="ef49b-121">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="ef49b-121">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



