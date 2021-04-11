---
title: WIC 函數
description: 本節包含 Windows 影像處理元件 (WIC) 函數的相關資訊。
ms.assetid: 6f948df6-5b70-4f1e-b01d-3841d7819acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ce53f51f439ab5d0a697c824a1d37db7fd755f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847971"
---
# <a name="wic-functions"></a><span data-ttu-id="46894-103">WIC 函數</span><span class="sxs-lookup"><span data-stu-id="46894-103">WIC functions</span></span>

<span data-ttu-id="46894-104">本節包含 Windows 影像處理元件 (WIC) 函數的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="46894-104">This section contains information about the Windows Imaging Component (WIC) functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="46894-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="46894-105">In this section</span></span>



| <span data-ttu-id="46894-106">主題</span><span class="sxs-lookup"><span data-stu-id="46894-106">Topic</span></span>                                                                                      | <span data-ttu-id="46894-107">描述</span><span class="sxs-lookup"><span data-stu-id="46894-107">Description</span></span>                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46894-108">*ProgressNotificationCallback*</span><span class="sxs-lookup"><span data-stu-id="46894-108">*ProgressNotificationCallback*</span></span>](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)<br/>   | <span data-ttu-id="46894-109">進行編解碼器元件的進度時，所呼叫的應用程式定義回呼函數。</span><span class="sxs-lookup"><span data-stu-id="46894-109">Application defined callback function called when codec component progress is made.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="46894-110">**WICConvertBitmapSource**</span><span class="sxs-lookup"><span data-stu-id="46894-110">**WICConvertBitmapSource**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-wicconvertbitmapsource)<br/>             | <span data-ttu-id="46894-111">從給定的 **IWICBitmapSource** 取得所需像素格式的 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 。</span><span class="sxs-lookup"><span data-stu-id="46894-111">Obtains a [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) in the desired pixel format from a given **IWICBitmapSource**.</span></span><br/>                                                                           |
| [<span data-ttu-id="46894-112">**WICCreateBitmapFromSection**</span><span class="sxs-lookup"><span data-stu-id="46894-112">**WICCreateBitmapFromSection**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsection)<br/>     | <span data-ttu-id="46894-113">傳回由 Windows 圖形裝置介面的圖元所支援的 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) (GDI) 區段控制碼。</span><span class="sxs-lookup"><span data-stu-id="46894-113">Returns a [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) that is backed by the pixels of a Windows Graphics Device Interface (GDI) section handle.</span></span><br/>                                                |
| [<span data-ttu-id="46894-114">**WICCreateBitmapFromSectionEx**</span><span class="sxs-lookup"><span data-stu-id="46894-114">**WICCreateBitmapFromSectionEx**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsectionex)<br/> | <span data-ttu-id="46894-115">傳回由 GDI 區段控制碼的圖元所支援的 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 。</span><span class="sxs-lookup"><span data-stu-id="46894-115">Returns a [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) that is backed by the pixels of a GDI section handle.</span></span><br/>                                                                                    |
| [<span data-ttu-id="46894-116">**WICGetMetadataContentSize**</span><span class="sxs-lookup"><span data-stu-id="46894-116">**WICGetMetadataContentSize**</span></span>](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicgetmetadatacontentsize)<br/>       | <span data-ttu-id="46894-117">傳回指定之 [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)所包含之中繼資料內容的大小。</span><span class="sxs-lookup"><span data-stu-id="46894-117">Returns the size of the metadata content contained by the specified [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter).</span></span> <span data-ttu-id="46894-118">傳回的大小帳戶，用於標頭和中繼資料的長度。</span><span class="sxs-lookup"><span data-stu-id="46894-118">The returned size accounts for the header and the length of the metadata.</span></span><br/> |
| [<span data-ttu-id="46894-119">**WICMapGuidToShortName**</span><span class="sxs-lookup"><span data-stu-id="46894-119">**WICMapGuidToShortName**</span></span>](/windows/desktop/api/WinCodec/nf-wincodec-wicmapguidtoshortname)<br/>               | <span data-ttu-id="46894-120">取得與指定 GUID 相關聯的簡短名稱。</span><span class="sxs-lookup"><span data-stu-id="46894-120">Obtains the short name associated with a given GUID.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="46894-121">**WICMapSchemaToName**</span><span class="sxs-lookup"><span data-stu-id="46894-121">**WICMapSchemaToName**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-wicmapschematoname)<br/>                     | <span data-ttu-id="46894-122">取得與給定架構相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="46894-122">Obtains the name associated with a given schema.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="46894-123">**WICMapShortNameToGuid**</span><span class="sxs-lookup"><span data-stu-id="46894-123">**WICMapShortNameToGuid**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-wicmapshortnametoguid)<br/>               | <span data-ttu-id="46894-124">取得與指定簡短名稱相關聯的 GUID。</span><span class="sxs-lookup"><span data-stu-id="46894-124">Obtains the GUID associated with the given short name.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="46894-125">**WICMatchMetadataContent**</span><span class="sxs-lookup"><span data-stu-id="46894-125">**WICMatchMetadataContent**</span></span>](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent)<br/>           | <span data-ttu-id="46894-126">取得指定之容器格式的元資料格式 GUID，以及最符合給定資料流程內內容的廠商。</span><span class="sxs-lookup"><span data-stu-id="46894-126">Obtains a metadata format GUID for a specified container format and vendor that best matches the content within a given stream.</span></span><br/>                                                                            |
| [<span data-ttu-id="46894-127">**WICSerializeMetadataContent**</span><span class="sxs-lookup"><span data-stu-id="46894-127">**WICSerializeMetadataContent**</span></span>](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent)<br/>   | <span data-ttu-id="46894-128">將中繼資料寫入至指定的資料流程。</span><span class="sxs-lookup"><span data-stu-id="46894-128">Writes metadata into a given stream.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="46894-129">WIC Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="46894-129">WIC Proxy Functions</span></span>](wic-proxy-functions.md)<br/>                                  | <span data-ttu-id="46894-130">本節包含 WIC proxy 函數。</span><span class="sxs-lookup"><span data-stu-id="46894-130">This section contains the WIC proxy functions.</span></span><br/>                                                                                                                                                             |



 

 

 




