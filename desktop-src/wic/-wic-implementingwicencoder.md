---
description: 執行 WIC-Enabled 編碼器
ms.assetid: 9c1a4fa4-30b9-445f-8aee-46711355ace7
title: 執行 WIC-Enabled 編碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e65f969ba7c65e6860009b2fc998024d358301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193712"
---
# <a name="implementing-a-wic-enabled-encoder"></a><span data-ttu-id="8a729-103">執行 WIC-Enabled 編碼器</span><span class="sxs-lookup"><span data-stu-id="8a729-103">Implementing a WIC-Enabled Encoder</span></span>

## <a name="introduction"></a><span data-ttu-id="8a729-104">簡介</span><span class="sxs-lookup"><span data-stu-id="8a729-104">Introduction</span></span>

<span data-ttu-id="8a729-105">執行 Windows 影像處理元件 (WIC) 編碼器需要撰寫兩個類別，也就是執行 WIC 解碼器的情況。</span><span class="sxs-lookup"><span data-stu-id="8a729-105">Implementing a Windows Imaging Component (WIC) encoder requires writing two classes, as is also true for implementing a WIC decoder.</span></span> <span data-ttu-id="8a729-106">這些類別上的介面直接對應至 Windows 影像處理元件運作方式的 [編碼](-wic-howwicworks.md) 區段中所述的編碼器責任。</span><span class="sxs-lookup"><span data-stu-id="8a729-106">The interfaces on these classes correspond directly to the encoder responsibilities outlined in the [Encoding](-wic-howwicworks.md) section of How The Windows Imaging Component Works.</span></span>

<span data-ttu-id="8a729-107">其中一個類別會提供容器層級的服務，並管理容器內個別影像框架的序列化。</span><span class="sxs-lookup"><span data-stu-id="8a729-107">One of the classes provides container-level services and manages the serialization of the individual image frames within the container.</span></span> <span data-ttu-id="8a729-108">這個類別會實 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) 介面。</span><span class="sxs-lookup"><span data-stu-id="8a729-108">This class implements the [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) interface.</span></span> <span data-ttu-id="8a729-109">如果您的影像格式支援容器層級的中繼資料，您也必須在這個類別上執行 [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) 介面。</span><span class="sxs-lookup"><span data-stu-id="8a729-109">If your image format supports container-level metadata, you must also implement the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface on this class.</span></span>

<span data-ttu-id="8a729-110">另一個類別會提供框架層級的服務，並針對容器中的每個框架執行影像位的實際編碼。</span><span class="sxs-lookup"><span data-stu-id="8a729-110">The other class provides frame-level services and does the actual encoding of the image bits for each frame in the container.</span></span> <span data-ttu-id="8a729-111">它也會逐一查看每個框架的中繼資料區塊，並要求適當的中繼資料寫入器來序列化區塊。</span><span class="sxs-lookup"><span data-stu-id="8a729-111">It also iterates through the metadata blocks for each frame and requests the appropriate metadata writers to serialize the blocks.</span></span> <span data-ttu-id="8a729-112">這個類別會實 **IWICBitmapFrameEncode** 介面和 [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) 介面。</span><span class="sxs-lookup"><span data-stu-id="8a729-112">This class implements the **IWICBitmapFrameEncode** interface and the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface.</span></span> <span data-ttu-id="8a729-113">此類別應該具有在具現化時，容器層級類別初始化的 IStream 成員， **Commit** 方法會將框架資料序列化至該成員。</span><span class="sxs-lookup"><span data-stu-id="8a729-113">This class should have an IStream member that the container-level class initializes on instantiation, into which the **Commit** method will serialize the frame data.</span></span>

<span data-ttu-id="8a729-114">在某些情況下（例如 raw 格式），編解碼器作者可能不希望應用程式能夠編碼或重新編碼為原始格式，因為原始檔案的目的是要包含與相機完全相同的感應器資料。</span><span class="sxs-lookup"><span data-stu-id="8a729-114">In some cases, such as raw formats, the codec author may not want applications to be able to encode or re-encode to the raw format, because the purpose of a raw file is to contain the sensor data exactly as it came from the camera.</span></span> <span data-ttu-id="8a729-115">在編解碼器作者不想啟用編碼的情況下，仍必須執行基本編碼器，才可啟用新增中繼資料。</span><span class="sxs-lookup"><span data-stu-id="8a729-115">In cases where the codec author doesn’t want to enable encoding, it is still necessary to implement a rudimentary encoder just to enable adding metadata.</span></span> <span data-ttu-id="8a729-116">在這種情況下，編碼器只需要支援寫入中繼資料所需的方法，並可從解碼器複製不變的影像位。</span><span class="sxs-lookup"><span data-stu-id="8a729-116">In that case, the encoder need only support those methods necessary for writing metadata, and can copy the image bits untouched from the decoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a729-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="8a729-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8a729-118">**參考**</span><span class="sxs-lookup"><span data-stu-id="8a729-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8a729-119">**IWICBitmapEncoder**</span><span class="sxs-lookup"><span data-stu-id="8a729-119">**IWICBitmapEncoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

<span data-ttu-id="8a729-120">**概念**</span><span class="sxs-lookup"><span data-stu-id="8a729-120">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8a729-121">執行 IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="8a729-121">Implementing IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[<span data-ttu-id="8a729-122">編碼器介面</span><span class="sxs-lookup"><span data-stu-id="8a729-122">Encoder Interfaces</span></span>](-wic-encoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="8a729-123">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="8a729-123">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="8a729-124">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="8a729-124">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



