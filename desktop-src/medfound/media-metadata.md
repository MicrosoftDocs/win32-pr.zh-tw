---
description: 媒體中繼資料
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: 媒體中繼資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb17f286673663976e17b4178239507765c2101
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106975600"
---
# <a name="media-metadata"></a>媒體中繼資料

媒體檔案包含描述檔案內容的屬性。 在 Microsoft 媒體基礎中，這些屬性可以分類如下：

-   **媒體類型屬性** 會指定編碼參數，例如編碼演算法 (媒體子類型) 、影片框架大小、影片畫面播放速率、音訊位元速率和音訊取樣率。 如需媒體類型屬性的詳細資訊，請參閱 [媒體類型](media-types.md)。
-   **中繼資料** 包含媒體內容的描述性資訊，例如標題、演出者、編輯器和內容類型。 中繼資料也可以描述編碼參數。 透過中繼資料存取此資訊的速度，會比透過媒體類型屬性更快。
-   **DRM 屬性** 包含使用限制的資訊。 目前媒體基礎不支援透過中繼資料的 DRM 屬性，但 **PKEY \_ DRM \_ IsProtected** 屬性除外。

有兩種方式可以在媒體基礎中讀取中繼資料：

-   [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)介面 (媒體基礎第1版中繼資料) 。
-   Windows Shell [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面 (Shell 中繼資料) 。

Shell 中繼資料不只會與媒體檔案相關，而是在系統上的檔案範圍更廣。

下表比較每個中繼資料 API 的功能和限制。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>媒體基礎 v1 中繼資料</th>
<th>Shell 中繼資料</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>需要 Windows Vista 或更新版本。</td>
<td>需要 Windows 7。
<blockquote>
[!Note]<br />
一般而言，Shell 中繼資料不需要 Windows 7，但是媒體基礎不支援 Windows 7 之前的 Shell 中繼資料。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>屬性與 Shell 屬性系統不相容。</td>
<td>屬性與 Shell 屬性系統相容。</td>
</tr>
<tr class="odd">
<td>屬性可套用至整個檔案，或在資料流程層級套用。</td>
<td>僅支援檔案層級的屬性。 不支援資料流程層級屬性。</td>
</tr>
<tr class="even">
<td>屬性可以有多種語言的值。</td>
<td>不支援多種語言的值。</td>
</tr>
<tr class="odd">
<td>屬性索引鍵是寬字元字串。</td>
<td>屬性索引鍵是 <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> 值。</td>
</tr>
<tr class="even">
<td>屬性值為 <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> 值。</td>
<td>屬性值為 <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> 值。</td>
</tr>
</tbody>
</table>



 

## <a name="in-this-section"></a>本節內容



| 主題                                                                                     | 描述                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Shell 中繼資料提供者](shell-metadata-providers.md)<br/>                       | 從 Windows 7 開始，媒體基礎會透過 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面公開中繼資料。<br/> |
| [媒體檔案的中繼資料屬性](metadata-properties-for-media-files.md)<br/> | 本主題列出媒體檔案最常見的中繼資料屬性。<br/>                                                           |
| [Windows Vista 中的中繼資料提供者](metadata-providers-in-windows-vista.md)<br/> | 在 Windows Vista 中，媒體基礎會透過 [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) 介面公開中繼資料。<br/>                   |



 

如果您正在執行自訂媒體來源，並且想要公開 Shell 中繼資料，請參閱 [自訂媒體檔案的中繼資料提供者](custom-metadata-providers-for-media-files.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎程式設計指南](media-foundation-programming-guide.md)
</dt> </dl>

 

 
