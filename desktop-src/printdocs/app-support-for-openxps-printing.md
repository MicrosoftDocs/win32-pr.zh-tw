---
description: OpenXPS 是檔的開放 XML 檔規格格式，而且是以 (ECMA) 標準規格的歐洲貨箱 maker 關聯為基礎。
ms.assetid: 52FB5B3F-BEBF-4851-8BE9-5DC7AE535313
title: OpenXPS 列印的應用程式支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914d8c365209ea3486bedd5e0352e63a8e31086f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983477"
---
# <a name="app-support-for-openxps-printing"></a><span data-ttu-id="f8c3c-103">OpenXPS 列印的應用程式支援</span><span class="sxs-lookup"><span data-stu-id="f8c3c-103">App Support for OpenXPS Printing</span></span>

<span data-ttu-id="f8c3c-104">OpenXPS 是檔的開放 XML 檔規格格式，它是以 (ECMA) 標準規格的歐洲電腦製造商關聯為基礎。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-104">OpenXPS is the Open XML Paper Specification format for documents, and it’s based on the European Computer Manufacturers Association (ECMA) standard specification.</span></span>

<span data-ttu-id="f8c3c-105">Windows 8 透過 v4 列印驅動程式模型提供完整的 OpenXPS 列印支援，並持續支援 Microsoft XPS 格式。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-105">Windows 8 provides full support for OpenXPS printing via the v4 print driver model, side-by-side with continued support for the Microsoft XPS format.</span></span> <span data-ttu-id="f8c3c-106">本主題的重點在於與 Windows 應用程式開發人員相關的這項支援的部分。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-106">And this topic focuses on the portion of this support that is relevant to Windows application developers.</span></span> <span data-ttu-id="f8c3c-107">如需 OpenXPS 支援之驅動程式需求的詳細資訊，請參閱 [OpenXPS 的驅動程式支援](/windows-hardware/drivers/print/printer-driver-overview)。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-107">For information about driver requirements for OpenXPS support, see [Driver Support for OpenXPS](/windows-hardware/drivers/print/printer-driver-overview).</span></span>

## <a name="sending-xps-data-to-the-print-system"></a><span data-ttu-id="f8c3c-108">將 XPS 資料傳送至列印系統</span><span class="sxs-lookup"><span data-stu-id="f8c3c-108">Sending XPS data to the Print System</span></span>

<span data-ttu-id="f8c3c-109">建議您使用 [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) 將所有 XPS 列印工作傳送至列印系統。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-109">We recommend that you use [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) for sending all XPS print jobs to the print system.</span></span> <span data-ttu-id="f8c3c-110">**IPrintDocumentPackageTarget** 可在沒有序列化的情況下，接受 XPS 物件模型 (OM) ，這有助於改善整體效能。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-110">**IPrintDocumentPackageTarget** accepts the XPS object model (OM) without serialization, and that helps to improve the overall performance.</span></span>

<span data-ttu-id="f8c3c-111">以下是 **IPrintDocumentPackageTarget** 介面的簡短摘要：</span><span class="sxs-lookup"><span data-stu-id="f8c3c-111">Here's a brief summary of the **IPrintDocumentPackageTarget** interface:</span></span>

-   <span data-ttu-id="f8c3c-112">此介面支援從量身打造的解決方案和桌面應用程式進行列印。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-112">This interface supports printing from tailored solutions as well as desktop applications.</span></span>

-   <span data-ttu-id="f8c3c-113">針對桌面應用程式，這可以用來取代 [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1)。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-113">For desktops apps, this can be used in place of [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).</span></span>

-   <span data-ttu-id="f8c3c-114">適用于 Windows 7 Service Pack 1 (SP1) + Platform Update 和 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-114">Available on Windows 7 with Service Pack 1 (SP1) + Platform Update, and Windows 8.</span></span>

-   <span data-ttu-id="f8c3c-115">在專案中包含 *DocumentTarget* ，以使用這些 api。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-115">Include *DocumentTarget.h* in projects to use these APIs.</span></span>

<span data-ttu-id="f8c3c-116">使用 OpenXPS 檔的應用程式應該注意，OpenXPS 的 MIME 類型如下所示：</span><span class="sxs-lookup"><span data-stu-id="f8c3c-116">Applications that consume OpenXPS documents should note that the MIME type for OpenXPS is as follows:</span></span>

<dl> <span data-ttu-id="f8c3c-117">應用程式 \\ .oxps</span><span class="sxs-lookup"><span data-stu-id="f8c3c-117">application\\oxps</span></span>  
</dl>

## <a name="sending-openxps-data-to-the-xps-print-api"></a><span data-ttu-id="f8c3c-118">將 OpenXPS 資料傳送至 XPS 列印 API</span><span class="sxs-lookup"><span data-stu-id="f8c3c-118">Sending OpenXPS data to the XPS Print API</span></span>

<span data-ttu-id="f8c3c-119">在 OpenXPS 的特定情況下，XPS OM 接受 MSXPS 和 OpenXPS，並提供轉換和序列化為任一格式的方法。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-119">Specific to OpenXPS, XPS OM accepts both MSXPS and OpenXPS, and provides methods for conversion and serialization to either format.</span></span> <span data-ttu-id="f8c3c-120">這可讓應用程式開發人員在需要的情況下，與目標驅動程式無關。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-120">This allows application developers to be agnostic of the target driver, if they want.</span></span> <span data-ttu-id="f8c3c-121">這也表示應用程式開發人員可以一律將列印工作以 XPS OM 的形式提交至 StartXpsPrintJob1 或 IDocumentPackageTarget，並知道列印系統將會處理任何必要的轉換。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-121">This also means that app developers can always submit print jobs as XPS OM to either StartXpsPrintJob1 or IDocumentPackageTarget, knowing that the print system will handle any necessary conversion.</span></span>

<span data-ttu-id="f8c3c-122">當然，防止 XPS 格式之間的轉換將會改善端對端的效能。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-122">Of course, preventing conversion between XPS formats will improve end-to-end performance.</span></span> <span data-ttu-id="f8c3c-123">從應用程式中，開發人員可以檢查下列登錄機碼，以判斷目標列印驅動程式慣用的 XPS 格式：</span><span class="sxs-lookup"><span data-stu-id="f8c3c-123">From the application, the developer can check the following registry key to determine the preferred XPS format of the targeted print driver:</span></span>

``` syntax
HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Print\Printers\[PrintDriverName]\PrintDriverData\XpsFormat
```

<span data-ttu-id="f8c3c-124">一旦決定了慣用的 XPS 格式之後，應用程式就可以提供不需要轉換的 XPS OM 物件。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-124">Once the preferred XPS format has been determined, the application can provide XPS OM objects that will not require conversion.</span></span> <span data-ttu-id="f8c3c-125">特別注意的是，在 OpenXPS 的 MSXPS 和 JPEGXR 中使用 HD 相片。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-125">Of particular note is the use of HD Photo in MSXPS and JPEGXR in OpenXPS.</span></span> <span data-ttu-id="f8c3c-126">從 JPEGXR 轉換到 HD 相片相當輕量，因為這項轉換的主要差異在於，HD 相片會忽略 JPEGXR 所需的4個控制位。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-126">Converting from JPEGXR to HD Photo is relatively lightweight since the primary difference in this conversion is that HD Photo ignores 4 control bits that JPEGXR requires.</span></span> <span data-ttu-id="f8c3c-127">不過，從 HD 相片轉換成 JPEGXR 需要重新編碼整個映射，才能產生必要的控制項位。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-127">However, converting from HD Photo to JPEGXR requires the entire image to be re-encoded in order to generate the required control bits.</span></span> <span data-ttu-id="f8c3c-128">因此，提供高解析度映射的 JPEGXR 映射可確保與 OpenXPS 的相容性，並將 MSXPS 映射的轉換成本降至最低。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-128">Thus, providing JPEGXR images for high-resolution images will ensure compatibility with OpenXPS and minimize the conversion cost of the image for MSXPS.</span></span>

<span data-ttu-id="f8c3c-129">*Xpsobjectmodel \_ 1. h* 標頭會定義 OpenXPS 的其他 api 和物件。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-129">The *Xpsobjectmodel\_1.h* header defines the additional APIs and objects for OpenXPS.</span></span> <span data-ttu-id="f8c3c-130">和 IXpsOMObjectFactory1 介面會提供其他方法來進行映射轉換。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-130">And the IXpsOMObjectFactory1 interface provides additional methods for image conversion.</span></span> <span data-ttu-id="f8c3c-131">語法如下：</span><span class="sxs-lookup"><span data-stu-id="f8c3c-131">Here's the syntax:</span></span>


```C++
IXpsOMObjectFactory1->ConvertHDPhotoToJpegXR(IXpsOMImageResource *imageResource);

IXpsOMObjectFactory1->ConvertJpegXRToHDPhoto(IXpsOMImageResource *imageResource);
```



<span data-ttu-id="f8c3c-132">Windows 8 提供下列新的和更新的列舉。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-132">Windows 8 provides the following new and updated enumerations.</span></span>

<span data-ttu-id="f8c3c-133">新列舉：</span><span class="sxs-lookup"><span data-stu-id="f8c3c-133">New enumeration:</span></span>

<dl>

[<span data-ttu-id="f8c3c-134">**XPS \_ 檔 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="f8c3c-134">**XPS\_DOCUMENT\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)  
</dl>

<span data-ttu-id="f8c3c-135">已更新列舉</span><span class="sxs-lookup"><span data-stu-id="f8c3c-135">Updated enumeration</span></span>

<dl>

[<span data-ttu-id="f8c3c-136">**XPS \_ 映射 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="f8c3c-136">**XPS\_IMAGE\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)  
</dl>

<span data-ttu-id="f8c3c-137">新的 GetDocumentType 方法可讓應用程式判斷檔的 XPS 格式。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-137">The new GetDocumentType methods allow an application to determine the XPS format of documents.</span></span> <span data-ttu-id="f8c3c-138">這些都可在 [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1)、 [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1)和 [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1)中使用。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-138">These are available in [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1), and [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1).</span></span> <span data-ttu-id="f8c3c-139">以下是一份方法清單。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-139">Here's a list of the methods.</span></span>

<dl>

[<span data-ttu-id="f8c3c-140">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span><span class="sxs-lookup"><span data-stu-id="f8c3c-140">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)  
[<span data-ttu-id="f8c3c-141">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span><span class="sxs-lookup"><span data-stu-id="f8c3c-141">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)  
[<span data-ttu-id="f8c3c-142">**IXpsOMPackage1：： GetDocumentType**</span><span class="sxs-lookup"><span data-stu-id="f8c3c-142">**IXpsOMPackage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)  
[<span data-ttu-id="f8c3c-143">**IXpsOMPage1：： GetDocumentType**</span><span class="sxs-lookup"><span data-stu-id="f8c3c-143">**IXpsOMPage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)  
</dl>

<span data-ttu-id="f8c3c-144">Windows 8 提供下列新的錯誤碼以支援 OpenXPS：</span><span class="sxs-lookup"><span data-stu-id="f8c3c-144">Windows 8 provides the following new error codes in support of OpenXPS:</span></span>

<dl> <span data-ttu-id="f8c3c-145">XPS \_ E 不相符 \_ \_ 的命名空間。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-145">XPS\_E\_MISMATCHED\_NAMESPACE.</span></span> <dl> <span data-ttu-id="f8c3c-146">如果有不相符的命名空間，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-146">This error is returned, if there is a mismatched namespace.</span></span>  
</dl> </dd> XPS\_E\_ABSOLUTE\_REFERENCE. <dl> <span data-ttu-id="f8c3c-147">如果 MSXPS 在內部參考中使用絕對 Uri，或嘗試使用內部參考來序列化資料流程中的，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-147">This error is returned if MSXPS uses absolute URIs in internal references, or attempts to use internal references to serialize in the stream.</span></span> <span data-ttu-id="f8c3c-148">這是因為 XPS OM 會產生相對的 Uri。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-148">That is because XPS OM generates relative URIs.</span></span> <span data-ttu-id="f8c3c-149">而且，雖然 MSXPS 支援相對和絕對 Uri，但 OpenXPS 需要相對的 Uri。</span><span class="sxs-lookup"><span data-stu-id="f8c3c-149">And although MSXPS supports both relative and absolute URIs, OpenXPS requires relative URIs.</span></span>  
</dl> </dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="f8c3c-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8c3c-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8c3c-151">OpenXPS 的驅動程式支援</span><span class="sxs-lookup"><span data-stu-id="f8c3c-151">Driver Support for OpenXPS</span></span>](/windows-hardware/drivers/print/printer-driver-overview)
</dt> <dt>

[<span data-ttu-id="f8c3c-152">**IPrintDocumentPackageTarget**</span><span class="sxs-lookup"><span data-stu-id="f8c3c-152">**IPrintDocumentPackageTarget**</span></span>](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)
</dt> <dt>

[<span data-ttu-id="f8c3c-153">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span><span class="sxs-lookup"><span data-stu-id="f8c3c-153">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)
</dt> <dt>

[<span data-ttu-id="f8c3c-154">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span><span class="sxs-lookup"><span data-stu-id="f8c3c-154">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)
</dt> <dt>

[<span data-ttu-id="f8c3c-155">**IXpsOMPackage1：： GetDocumentType**</span><span class="sxs-lookup"><span data-stu-id="f8c3c-155">**IXpsOMPackage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)
</dt> <dt>

[<span data-ttu-id="f8c3c-156">**IXpsOMPage1：： GetDocumentType**</span><span class="sxs-lookup"><span data-stu-id="f8c3c-156">**IXpsOMPage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)
</dt> <dt>

[<span data-ttu-id="f8c3c-157">**XPS \_ 檔 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="f8c3c-157">**XPS\_DOCUMENT\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)
</dt> <dt>

[<span data-ttu-id="f8c3c-158">**XPS \_ 映射 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="f8c3c-158">**XPS\_IMAGE\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)
</dt> </dl>

 

 
