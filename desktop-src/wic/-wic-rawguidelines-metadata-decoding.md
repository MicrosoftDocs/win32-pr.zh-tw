---
description: 解碼
ms.assetid: ff7e5e66-e1ea-49fc-909f-de361214afc3
title: 解碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6700865d55ba7349447f5e41285d60446f0e4630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851203"
---
# <a name="decoding"></a><span data-ttu-id="67de6-103">解碼</span><span class="sxs-lookup"><span data-stu-id="67de6-103">Decoding</span></span>

<span data-ttu-id="67de6-104">為了適當地支援中繼資料，解碼器作者必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="67de6-104">To properly support metadata, decoder authors must do the following:</span></span>

-   <span data-ttu-id="67de6-105">執行 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 和 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 介面。</span><span class="sxs-lookup"><span data-stu-id="67de6-105">Implement [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interfaces.</span></span>
-   <span data-ttu-id="67de6-106">在框架解碼上執行 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 。</span><span class="sxs-lookup"><span data-stu-id="67de6-106">Implement [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) on the frame decoder.</span></span> <span data-ttu-id="67de6-107">如果編解碼器支援容器層級的中繼資料，則必須在容器層級的解碼器以及框架解碼器上，執行此介面。</span><span class="sxs-lookup"><span data-stu-id="67de6-107">If the codec supports container-level metadata, this interface must be implemented on the container-level decoder as well as on the frame decoder.</span></span>
-   <span data-ttu-id="67de6-108">解碼影像資料流程時，請呼叫 [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)：：[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) ，以具現化每個中繼資料區塊的中繼資料讀取器。</span><span class="sxs-lookup"><span data-stu-id="67de6-108">While decoding the image stream, call [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) to instantiate a metadata reader for each metadata block.</span></span> <span data-ttu-id="67de6-109"> (編解碼器所實行的任何新中繼資料讀取器都必須向 WIC 註冊。 ) </span><span class="sxs-lookup"><span data-stu-id="67de6-109">(Any new metadata readers that the codec implements must be registered with WIC.)</span></span>

    <span data-ttu-id="67de6-110">此解碼器不應自行建立中繼資料讀取器，而是使用 WIC 根據資料流程中的中繼資料區塊來建立它們。</span><span class="sxs-lookup"><span data-stu-id="67de6-110">The decoder should not create metadata readers on its own, but rather use WIC to create them based on the metadata blocks in the stream.</span></span> <span data-ttu-id="67de6-111">此解碼器必須在找到的所有區塊上進行這項作業，即使它們不是 docoder 的原生已知，因為未來的中繼資料讀取器可能會安裝在系統上，以瞭解如何處理這些中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="67de6-111">The decoder must do this on all blocks that it finds, even if they are not natively known to the docoder, because future metadata readers might be installed on the system that do understand how to handle these metadata blocks.</span></span>

-   <span data-ttu-id="67de6-112">如果沒有區塊的元資料處理程式，請使用中繼資料建立選項具現化未知的中繼資料讀取器。</span><span class="sxs-lookup"><span data-stu-id="67de6-112">If there is no metadata handler for a block, instantiate the unknown metadata reader by using the metadata creation options.</span></span>
-   <span data-ttu-id="67de6-113">透過 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 介面公開中繼資料讀取器的集合。</span><span class="sxs-lookup"><span data-stu-id="67de6-113">Expose the collection of metadata readers through the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67de6-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="67de6-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="67de6-115">**概念**</span><span class="sxs-lookup"><span data-stu-id="67de6-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="67de6-116">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="67de6-116">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="67de6-117">相機原始影像格式的 WIC 指導方針</span><span class="sxs-lookup"><span data-stu-id="67de6-117">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="67de6-118">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="67de6-118">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



