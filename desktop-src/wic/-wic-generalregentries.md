---
description: 一般登錄專案
ms.assetid: 6a140c7f-df8c-4a8e-9e4d-dbb38901e14f
title: 一般登錄專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7c3514adcc0aeaaf9adadd2b71dfdffcd8d408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978224"
---
# <a name="general-registry-entries"></a><span data-ttu-id="81fce-103">一般登錄專案</span><span class="sxs-lookup"><span data-stu-id="81fce-103">General Registry Entries</span></span>


<span data-ttu-id="81fce-104">下列登錄專案必須分別針對解碼器和編碼器進行：</span><span class="sxs-lookup"><span data-stu-id="81fce-104">The following registry entries must be made separately for both the decoder and the encoder:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Encoder/Decoder CLSID}
         Author = Author's Name
         Description = Your Codec Description
         DeviceManufacturer = Manufacturer's Name
         DeviceModels = Device,Device
         FriendlyName = Codec Friendly Name
         Date = mm-dd-yyyy
         Vendor = {GUID_Vendor}
         ContainerFormat = {GUID_ContainerFormat}
         Version = Major.Minor.Build.Number
         SpecVersion = Major.Minor.Build.Number
         MimeTypes = Your Mime Type
         SupportAnimation = 0|1
         SupportChromakey = 0|1
         SupportLossless = 0|1
         SupportMultiframe = 0|1
         Formats
            {Supported PixelFormat GUID 1}
            {Supported PixelFormat GUID ...}
            {Supported PixelFormat GUID N}
         ArbitrationPriority  = 0-10
```

<span data-ttu-id="81fce-105">FriendlyName、VendorGUID、ContainerFormat、Mimetype、FileExtensions 和格式專案都是必要專案。</span><span class="sxs-lookup"><span data-stu-id="81fce-105">The FriendlyName, VendorGUID, ContainerFormat, MimeTypes, FileExtensions, and Formats entries are required.</span></span> <span data-ttu-id="81fce-106">所有其他專案都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="81fce-106">All of the others are optional.</span></span>

<span data-ttu-id="81fce-107">請注意，DeviceManufacturer 和 DeviceModels 專案是原始編解碼器特有的，而且是指編解碼器適用的攝影機製造商和相機型號。</span><span class="sxs-lookup"><span data-stu-id="81fce-107">Note that the DeviceManufacturer and DeviceModels entries are specific to raw codecs and refer to the camera manufacturer and camera models that the codec is applicable to.</span></span> <span data-ttu-id="81fce-108">規格版本是編解碼器符合的映射格式規格版本。</span><span class="sxs-lookup"><span data-stu-id="81fce-108">The spec version is the version of the image format specification with which the codec complies.</span></span> <span data-ttu-id="81fce-109">格式專案會指定編解碼器所支援的像素格式。</span><span class="sxs-lookup"><span data-stu-id="81fce-109">The Formats entry specifies the pixel formats supported by the codec.</span></span> <span data-ttu-id="81fce-110">編解碼器可支援一個以上的像素格式。</span><span class="sxs-lookup"><span data-stu-id="81fce-110">A codec may support more than one pixel format.</span></span> <span data-ttu-id="81fce-111">在這種情況下，您會在 HKEY \_ 類別的 \_ 根 \\ CLSID \\ {編碼器/解碼器 clsid} \\ 格式下輸入多個索引鍵。</span><span class="sxs-lookup"><span data-stu-id="81fce-111">In that case, you would enter multiple keys under HKEY\_CLASSES\_ROOT\\CLSID\\{Encoder/Decoder CLSID}\\Formats.</span></span>

## <a name="arbitrationpriority"></a><span data-ttu-id="81fce-112">ArbitrationPriority</span><span class="sxs-lookup"><span data-stu-id="81fce-112">ArbitrationPriority</span></span>

<span data-ttu-id="81fce-113">從 Windows 8 開始，ArbitrationPriority 是新的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="81fce-113">Starting in Windows 8, ArbitrationPriority is a new registry entry.</span></span> <span data-ttu-id="81fce-114">有效的值為0到10。</span><span class="sxs-lookup"><span data-stu-id="81fce-114">Valid values are 0 through 10.</span></span> <span data-ttu-id="81fce-115">當 ArbitrationPriority 索引鍵存在時，此機碼的值會指示 WIC 將相關編解碼器的優先順序設定為較低 ArbitrationPriority 值的任何其他編解碼器後方。</span><span class="sxs-lookup"><span data-stu-id="81fce-115">When the ArbitrationPriority key is present, the value of this key will instruct WIC to prioritize the associated codec behind any other codecs with a lower ArbitrationPriority value.</span></span> <span data-ttu-id="81fce-116">這項評估會在現有的 WIC 編解碼器仲裁發生之前發生，並確保相關聯的編解碼器會優先于任何競爭的編解碼器，即使它是一樣或更有能力。</span><span class="sxs-lookup"><span data-stu-id="81fce-116">This evaluation occurs before the existing WIC codec arbitration occurs, and ensures the associated codec is prioritized below any competing codec, even if it is as or more capable.</span></span> <span data-ttu-id="81fce-117">登錄中未定義明確 ArbitrationPriority 值的任何編解碼器都會預設為優先權0。</span><span class="sxs-lookup"><span data-stu-id="81fce-117">Any codec that doesn’t have an explicit ArbitrationPriority value defined in the registry will default to Priority 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81fce-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="81fce-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="81fce-119">**概念**</span><span class="sxs-lookup"><span data-stu-id="81fce-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="81fce-120">編解碼器安裝和註冊</span><span class="sxs-lookup"><span data-stu-id="81fce-120">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="81fce-121">編碼器特定的登錄專案</span><span class="sxs-lookup"><span data-stu-id="81fce-121">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)
</dt> <dt>

[<span data-ttu-id="81fce-122">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="81fce-122">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="81fce-123">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="81fce-123">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="81fce-124">**Windows 影像處理元件的運作方式：編解碼器探索和仲裁**</span><span class="sxs-lookup"><span data-stu-id="81fce-124">**How the Windows Imaging Component Works: Codec Discovery and Arbitration**</span></span>](-wic-howwicworks.md)
</dt> </dl>

 

 



