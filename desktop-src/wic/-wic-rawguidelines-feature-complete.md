---
description: 功能完整性：建議的介面
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 功能完整性：建議的介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1dba4bcc029b2205985afb443526376c0eecb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989972"
---
# <a name="feature-completeness-recommended-interfaces"></a>功能完整性：建議的介面

下表列出 Windows 影像處理元件原始編解碼器應執行的 (WIC) 介面。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>介面</th>
<th>必須用於</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></td>
<td>解碼器</td>
<td>表示解碼影像檔案的起點。 提供容器層級屬性的存取，例如縮圖、框架和調色板。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></td>
<td>解碼器</td>
<td>代表容器內的特定影像框架，可提供框架層級屬性的存取權。 這是將實際影像位解碼的介面。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></td>
<td>解碼器</td>
<td>從影像檔案讀取時，需要用來列舉中繼資料區塊，並叫用適當的中繼資料讀取器。 <br/>
<blockquote>
[!Note]<br />
如果原始容器格式與 TIFF 相容，或使用標準 IFDs 或 IRBs 來儲存 EXIF 或 XMP 中繼資料，則編解碼器作者可以選擇叫用內建的中繼資料讀取器，而不是自行撰寫。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></td>
<td>解碼器</td>
<td>允許呼叫者針對已解碼的影像指定所需的縮放、裁剪、旋轉或像素格式，以大幅提升效能。 例如，Microsoft 的 JPEG 和無線資料包協定 (WDP) 解碼器使用金字塔優化配置，可在目標點陣圖小於來源點陣圖時，更快速地進行解碼。 &quot; &quot; 當內嵌的預覽遺失或小於其最大維度的1024圖元時，Windows Vista (和更新版本的) 將會嘗試使用此介面從原始影像中解壓縮快速預覽。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></td>
<td>解碼器</td>
<td>RAW 格式的必要參數。 公開原始影像處理特有的參數。 原始編解碼器應該支援將這些參數視為套用至編解碼器的許多參數。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></td>
<td>編碼器</td>
<td>代表編碼影像檔案的起點。 此介面是用來設定容器層級的屬性，例如縮圖、框架和調色板。 您也必須叫用中繼資料寫入器，以啟用影像檔的中繼資料持續性。 基於這些原因，即使不支援將主要點陣圖編碼為原始格式，也需要這個介面。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></td>
<td>編碼器</td>
<td>代表容器內的特定映射框架。 此介面是用來將實際的影像位編碼，並設定每個畫面格的中繼資料和屬性。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></td>
<td>編碼器</td>
<td>當序列化影像檔案時，需要用來逐一查看中繼資料區塊，並叫用適當的中繼資料寫入器。<br/>
<blockquote>
[!Note]<br />
如果原始的容器格式與 TIFF 相容，編解碼器作者可以選擇叫用內建的中繼資料寫入器，而不是自行撰寫。
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[相機原始影像格式的 WIC 指導方針](-wic-rawguidelines.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




