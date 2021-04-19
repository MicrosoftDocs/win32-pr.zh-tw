---
description: Microsoft XPS Document Writer (MXDW) 可讓使用者從任何 Windows 應用程式進行列印，以建立 XPS 檔檔。
ms.assetid: 1fa50337-2df7-48d3-a179-0ca5ae3dfda3
title: MXDW 設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4026a99baa33ec50bc3ad129ef6610a428f83ab
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106986453"
---
# <a name="mxdw-configuration-settings"></a><span data-ttu-id="04090-103">MXDW 設定</span><span class="sxs-lookup"><span data-stu-id="04090-103">MXDW Configuration Settings</span></span>

<span data-ttu-id="04090-104">Microsoft XPS Document Writer (MXDW) 可讓使用者從任何 Windows 應用程式進行列印，以建立 XPS 檔檔。</span><span class="sxs-lookup"><span data-stu-id="04090-104">The Microsoft XPS Document Writer (MXDW) enables users to create XPS document files by printing from any Windows application.</span></span> <span data-ttu-id="04090-105">應用程式開發人員可以使用 [列印架構](./printschema.md)的 PrintTicket 和 PrintCapabilities 部分，來控制 MXDW 的下列輸出設定。</span><span class="sxs-lookup"><span data-stu-id="04090-105">Applications developers can control the following output settings of the MXDW using the PrintTicket and PrintCapabilities parts of the [Print Schema](./printschema.md).</span></span>

## <a name="jobinterleaving"></a><span data-ttu-id="04090-106">JobInterleaving</span><span class="sxs-lookup"><span data-stu-id="04090-106">JobInterleaving</span></span>

<span data-ttu-id="04090-107">JobInterleaving 設定會控制 XPS 檔的內容交錯順序。</span><span class="sxs-lookup"><span data-stu-id="04090-107">The JobInterleaving setting controls the content interleaving order for the XPS Documents.</span></span> <span data-ttu-id="04090-108">如需作業交錯的詳細資訊，請參閱 [XML 檔規格](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)。</span><span class="sxs-lookup"><span data-stu-id="04090-108">For information about job interleaving, see the [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span> <span data-ttu-id="04090-109">MXDW 支援這項設定的下列兩個選項：</span><span class="sxs-lookup"><span data-stu-id="04090-109">MXDW supports the following two options for this setting:</span></span>

-   <span data-ttu-id="04090-110">**Off** -這個選項會停用交錯，讓檔中每個 content 專案的所有資料都是連續的，以改善隨機存取的效率。</span><span class="sxs-lookup"><span data-stu-id="04090-110">**Off** - This option disables interleaving so that all data for each content element in the document is contiguous, which improves the efficiency of random access.</span></span> <span data-ttu-id="04090-111">此選項最適合用來查看 XPS 檔。</span><span class="sxs-lookup"><span data-stu-id="04090-111">This option is best for viewing an XPS document.</span></span>
-   <span data-ttu-id="04090-112">**On** -這個選項會啟用交錯，以便將每個內容專案的資料細分並重新排序，以提供更有效率的連續處理。</span><span class="sxs-lookup"><span data-stu-id="04090-112">**On** - This option enables interleaving so that data for each content element is broken up and reordered for more efficient sequential processing.</span></span> <span data-ttu-id="04090-113">此選項最適用于 web 下載和列印。</span><span class="sxs-lookup"><span data-stu-id="04090-113">This option is best for web download and printing.</span></span>

<span data-ttu-id="04090-114">下列範例是包含 JobInterleaving 設定的 PrintCapabilities XML 範例。</span><span class="sxs-lookup"><span data-stu-id="04090-114">The following example is an example of the PrintCapabilities XML that includes the JobInterleaving setting.</span></span>


```XML
<psf:Feature name="ns0000:JobInterleaving">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Interleaving</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:OFF" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">Off - Best for viewing</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:ON" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">On - Best for the web/printing</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



<span data-ttu-id="04090-115">PrintTicket XML 很類似，不同之處在于它會指定特定的選項。</span><span class="sxs-lookup"><span data-stu-id="04090-115">The PrintTicket XML is similar, except that it specifies a particular option.</span></span> <span data-ttu-id="04090-116">如需詳細資訊，請參閱 [列印架構](./printschema.md) 。</span><span class="sxs-lookup"><span data-stu-id="04090-116">See the [Print Schema](./printschema.md) for details.</span></span>

<span data-ttu-id="04090-117">因為 JobInterleaving 不是其中一個 [Print Schema Public 關鍵字](./print-schema-public-keywords.md)，所以您必須在 PrintCapabilities (或 printticket) 檔開頭的 **PrintCapabilities** (或 **printticket) 標記** 中包含命名空間 (的宣告，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="04090-117">Since JobInterleaving is not one of the [Print Schema Public Keywords](./print-schema-public-keywords.md), you must include a declaration of the namespace (in this case "ns0000" in the **PrintCapabilities** (or **PrintTicket**) tag at the beginning of the PrintCapabilities (or PrintTicket) document, as shown in the following example:</span></span>


```XML
<psf:PrintCapabilities 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="jobimagetype"></a><span data-ttu-id="04090-118">JobImageType</span><span class="sxs-lookup"><span data-stu-id="04090-118">JobImageType</span></span>

<span data-ttu-id="04090-119">JobImageType 會控制內嵌點陣圖格式的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="04090-119">JobImageType controls the output format of embedded bitmap formats.</span></span> <span data-ttu-id="04090-120">MXDW 支援此設定的下列四個選項：</span><span class="sxs-lookup"><span data-stu-id="04090-120">MXDW supports the following four options for this setting:</span></span>

-   <span data-ttu-id="04090-121">**JPEGHigh** -這個選項會指定具有高階壓縮的 JPEG 影像。</span><span class="sxs-lookup"><span data-stu-id="04090-121">**JPEGHigh** - This option specifies the JPEG image with a high level of compression.</span></span> <span data-ttu-id="04090-122">此選項會產生最小的檔案大小，但影像品質最低。</span><span class="sxs-lookup"><span data-stu-id="04090-122">This option produces the smallest file size, but the lowest image quality.</span></span>
-   <span data-ttu-id="04090-123">**JPEGMed** -這個選項會指定具有中壓縮層級的 JPEG 影像。</span><span class="sxs-lookup"><span data-stu-id="04090-123">**JPEGMed** - This option specifies the JPEG image with a medium level of compression.</span></span> <span data-ttu-id="04090-124">此選項可為檔案大小和影像品質提供最佳平衡。</span><span class="sxs-lookup"><span data-stu-id="04090-124">This option provides the best balance of file size and image quality.</span></span>
-   <span data-ttu-id="04090-125">**JPEGLow** -這個選項會指定低層級壓縮的 JPEG 影像。</span><span class="sxs-lookup"><span data-stu-id="04090-125">**JPEGLow** - This option specifies the JPEG image with a low level of compression.</span></span> <span data-ttu-id="04090-126">此選項會產生最小的檔案大小和高影像品質。</span><span class="sxs-lookup"><span data-stu-id="04090-126">This option produces the least reduction in file size and high image quality.</span></span>
-   <span data-ttu-id="04090-127">**Png** -這個選項會指定不失真壓縮的 PNG 影像格式。</span><span class="sxs-lookup"><span data-stu-id="04090-127">**PNG** - This option specifies the PNG image format with lossless compression.</span></span> <span data-ttu-id="04090-128">此選項會產生最大的檔案大小和最高的影像品質。</span><span class="sxs-lookup"><span data-stu-id="04090-128">This option produces the largest file size and the highest image quality.</span></span>

<span data-ttu-id="04090-129">JobImageType 設定的 PrintCapabilities XML 如下所示：</span><span class="sxs-lookup"><span data-stu-id="04090-129">The PrintCapabilities XML of the JobImageType setting appears below:</span></span>


```XML
<psf:Feature name="ns0000:JobImageType">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Images</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:JPEGHigh" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Maximum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGMed" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
        <psf:Value xsi:type="xsd:string">JPG - Medium compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGLow" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Minimum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:PNG" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">PNG - Lossless compression</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



<span data-ttu-id="04090-130">PrintTicket XML 很類似，不同之處在于它會指定特定的選項。</span><span class="sxs-lookup"><span data-stu-id="04090-130">The PrintTicket XML is similar, except that it specifies a particular option.</span></span> <span data-ttu-id="04090-131">如需詳細資訊，請參閱 [列印架構](./printschema.md) 。</span><span class="sxs-lookup"><span data-stu-id="04090-131">See the [Print Schema](./printschema.md) for details.</span></span>

<span data-ttu-id="04090-132">因為 JobImageType 不是其中一個 [Print Schema Public 關鍵字](./print-schema-public-keywords.md)，所以您必須在 PrintCapabilities (或 printticket) 檔開頭的 **PrintCapabilities** (或 **printticket) 標記** 中包含命名空間 (的宣告，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="04090-132">Since JobImageType is not one of the [Print Schema Public Keywords](./print-schema-public-keywords.md), you must include a declaration of the namespace (in this case "ns0000" in the **PrintCapabilities** (or **PrintTicket**) tag at the beginning of the PrintCapabilities (or PrintTicket) document, as shown in the following example:</span></span>


```XML
<psf:PrintTicket 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="related-topics"></a><span data-ttu-id="04090-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="04090-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04090-134">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="04090-134">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="04090-135">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="04090-135">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[<span data-ttu-id="04090-136">列印架構</span><span class="sxs-lookup"><span data-stu-id="04090-136">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="04090-137">XPS 規格與授權下載</span><span class="sxs-lookup"><span data-stu-id="04090-137">XPS Specification and License Downloads</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
