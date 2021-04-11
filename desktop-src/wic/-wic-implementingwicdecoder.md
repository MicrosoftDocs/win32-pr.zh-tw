---
description: 深入瞭解：實施 WIC-Enabled 的解碼器
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: 執行 WIC-Enabled 的解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebd6d56258bf18e6cc914a40efa4cd3a57a92fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850647"
---
# <a name="implementing-a-wic-enabled-decoder"></a><span data-ttu-id="76c27-103">執行 WIC-Enabled 的解碼器</span><span class="sxs-lookup"><span data-stu-id="76c27-103">Implementing a WIC-Enabled Decoder</span></span>


<span data-ttu-id="76c27-104">執行 Windows 影像處理元件 (WIC) 解碼器需要撰寫兩個類別。</span><span class="sxs-lookup"><span data-stu-id="76c27-104">Implementing a Windows Imaging Component (WIC) decoder requires writing two classes.</span></span> <span data-ttu-id="76c27-105">這些類別上的介面直接對應至[Windows 影像處理元件運作方式](-wic-howwicworks.md)的[解碼](-wic-howwicworks.md)章節中所述的解碼器責任。</span><span class="sxs-lookup"><span data-stu-id="76c27-105">The interfaces on these classes correspond directly to the decoder responsibilities outlined in the [Decoding](-wic-howwicworks.md) section of [How The Windows Imaging Component Works](-wic-howwicworks.md).</span></span>

<span data-ttu-id="76c27-106">其中一個類別會提供容器層級的服務，並執行 [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="76c27-106">One of the classes provides container-level services and implements the [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) interface.</span></span> <span data-ttu-id="76c27-107">如果您的影像格式支援容器層級的中繼資料，您也必須在這個類別上執行 [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="76c27-107">If your image format supports container-level metadata, you must also implement the [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) interface on this class.</span></span> <span data-ttu-id="76c27-108">建議您在解碼器和編碼器上同時支援 [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) 介面，以支援更佳的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="76c27-108">It is recommended that you support the [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) interface on both the decoder and encoder to support a better user experience.</span></span>

<span data-ttu-id="76c27-109">您將會執行的另一個類別會提供框架層級的服務，並對容器中的每個框架執行映射位的實際解碼。</span><span class="sxs-lookup"><span data-stu-id="76c27-109">The other class you will implement provides frame-level services and does the actual decoding of the image bits for each frame in the container.</span></span> <span data-ttu-id="76c27-110">這個類別會實 [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) 介面和 [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="76c27-110">This class implements the [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) interface and the [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) interface.</span></span> <span data-ttu-id="76c27-111">如果您要撰寫原始格式的解碼器，也可以在這個類別上執行 [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="76c27-111">If you are writing a decoder for a raw format, you also implement the [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) interface on this class.</span></span> <span data-ttu-id="76c27-112">除了所需的介面，強烈建議您在此類別上執行 [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) 介面，以針對您的影像格式啟用最佳的可能效能。</span><span class="sxs-lookup"><span data-stu-id="76c27-112">In addition to the required interfaces, it is highly recommended that you implement the [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) interface on this class to enable the best possible performance for your image format.</span></span>

<span data-ttu-id="76c27-113">WIC 提供的其中一個物件是 [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)。</span><span class="sxs-lookup"><span data-stu-id="76c27-113">One of the objects provided by WIC is the [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span> <span data-ttu-id="76c27-114">您經常使用此物件上的 [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) 介面來建立各種元件。</span><span class="sxs-lookup"><span data-stu-id="76c27-114">You frequently use the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) interface on this object to create various components.</span></span> <span data-ttu-id="76c27-115">因為通常會使用它，所以您應該將它的參考保留為您的解碼器和編碼器類別的成員屬性。</span><span class="sxs-lookup"><span data-stu-id="76c27-115">Because it is used frequently, you should keep a reference to it as a member property on both your decoder and encoder classes.</span></span>


```C++
IWICImagingFactory* m_pImagingFactory = NULL;
IWICComponentFactory* m_pComponentFactory = NULL;
HRESULT hr;
      
hr = CoCreateInstance(CLSID_WICImagingFactory, NULL,
  CLSCTX_INPROC_SERVER, IID_IWICImagingFactory,
  (LPVOID*) m_pImagingFactory);

hr = m_pImagingFactory->QueryInterface(
  IID_IWICComponentFactory, (void**)&m_pComponentFactory);
```



## <a name="related-topics"></a><span data-ttu-id="76c27-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="76c27-116">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="76c27-117">**概念**</span><span class="sxs-lookup"><span data-stu-id="76c27-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="76c27-118">Windows 影像處理元件的運作方式</span><span class="sxs-lookup"><span data-stu-id="76c27-118">How The Windows Imaging Component Works</span></span>](-wic-howwicworks.md)
</dt> <dt>

[<span data-ttu-id="76c27-119">解碼器介面</span><span class="sxs-lookup"><span data-stu-id="76c27-119">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="76c27-120">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="76c27-120">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="76c27-121">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="76c27-121">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="76c27-122">WIC 中繼資料總覽</span><span class="sxs-lookup"><span data-stu-id="76c27-122">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="76c27-123">編碼總覽</span><span class="sxs-lookup"><span data-stu-id="76c27-123">Encoding Overview</span></span>](-wic-creating-encoder.md)
</dt> </dl>

 

 



