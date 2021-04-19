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
# <a name="mxdw-configuration-settings"></a>MXDW 設定

Microsoft XPS Document Writer (MXDW) 可讓使用者從任何 Windows 應用程式進行列印，以建立 XPS 檔檔。 應用程式開發人員可以使用 [列印架構](./printschema.md)的 PrintTicket 和 PrintCapabilities 部分，來控制 MXDW 的下列輸出設定。

## <a name="jobinterleaving"></a>JobInterleaving

JobInterleaving 設定會控制 XPS 檔的內容交錯順序。 如需作業交錯的詳細資訊，請參閱 [XML 檔規格](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)。 MXDW 支援這項設定的下列兩個選項：

-   **Off** -這個選項會停用交錯，讓檔中每個 content 專案的所有資料都是連續的，以改善隨機存取的效率。 此選項最適合用來查看 XPS 檔。
-   **On** -這個選項會啟用交錯，以便將每個內容專案的資料細分並重新排序，以提供更有效率的連續處理。 此選項最適用于 web 下載和列印。

下列範例是包含 JobInterleaving 設定的 PrintCapabilities XML 範例。


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



PrintTicket XML 很類似，不同之處在于它會指定特定的選項。 如需詳細資訊，請參閱 [列印架構](./printschema.md) 。

因為 JobInterleaving 不是其中一個 [Print Schema Public 關鍵字](./print-schema-public-keywords.md)，所以您必須在 PrintCapabilities (或 printticket) 檔開頭的 **PrintCapabilities** (或 **printticket) 標記** 中包含命名空間 (的宣告，如下列範例所示：


```XML
<psf:PrintCapabilities 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="jobimagetype"></a>JobImageType

JobImageType 會控制內嵌點陣圖格式的輸出格式。 MXDW 支援此設定的下列四個選項：

-   **JPEGHigh** -這個選項會指定具有高階壓縮的 JPEG 影像。 此選項會產生最小的檔案大小，但影像品質最低。
-   **JPEGMed** -這個選項會指定具有中壓縮層級的 JPEG 影像。 此選項可為檔案大小和影像品質提供最佳平衡。
-   **JPEGLow** -這個選項會指定低層級壓縮的 JPEG 影像。 此選項會產生最小的檔案大小和高影像品質。
-   **Png** -這個選項會指定不失真壓縮的 PNG 影像格式。 此選項會產生最大的檔案大小和最高的影像品質。

JobImageType 設定的 PrintCapabilities XML 如下所示：


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



PrintTicket XML 很類似，不同之處在于它會指定特定的選項。 如需詳細資訊，請參閱 [列印架構](./printschema.md) 。

因為 JobImageType 不是其中一個 [Print Schema Public 關鍵字](./print-schema-public-keywords.md)，所以您必須在 PrintCapabilities (或 printticket) 檔開頭的 **PrintCapabilities** (或 **printticket) 標記** 中包含命名空間 (的宣告，如下列範例所示：


```XML
<psf:PrintTicket 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[列印架構](./printschema.md)
</dt> <dt>

[XPS 規格與授權下載](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
