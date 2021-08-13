---
title: 範例擴充功能類型
description: 範例擴充功能類型
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- Windows媒體格式 SDK，範例延伸模組
- Advanced Systems Format (ASF) 、範例延伸模組
- ASF (Advanced Systems Format) ，範例延伸模組
- Windows媒體格式 SDK，資料單位延伸模組
- Advanced Systems Format (ASF) 、資料單位延伸模組
- ASF (Advanced Systems Format) 、資料單位延伸模組
- Windows媒體格式 SDK，緩衝區屬性
- Advanced Systems Format (ASF) ，buffer 屬性
- ASF (Advanced Systems Format) ，buffer 屬性
- 範例延伸模組，類型
- 資料單位延伸模組，類型
- 緩衝區屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94161486fee7a31419f2e7fb9af2ed7fc968f00e8b43b81c58254547ec2f74e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119345388"
---
# <a name="sample-extension-types"></a>範例擴充功能類型

範例延伸模組（也稱為資料單位延伸 () 或緩衝區屬性）是附加至 ASF 檔案之 data 區段中媒體範例的資料項目目。 Windows 媒體格式 SDK 中定義了數種類型的範例延伸模組。 您也可以建立自己的延伸模組類型。

若要使用範例延伸模組，您必須在設定檔的串流設定資料中識別延伸模組類型。 呼叫 [**IWMStreamConfig2：： AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) 方法，將資料流程設定為接受擴充資料的範例。

您必須藉由呼叫 [**INSSBuffer3：： SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) 方法，將個別範例延伸模組新增至輸入範例。 讀取範例時，您可以呼叫 [**INSSBuffer3：： GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) 方法來取得延伸模組資料。 您也可以使用 [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) 介面的方法來列舉附加至範例的資料單位延伸模組。

下表列出預先定義的資料單位延伸模組識別碼，並說明附加至每個的範例的資料。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>範例延伸模組 GUID</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WM_SampleExtensionGUID_OutputCleanPoint</td>
<td>資料會指出此範例是否為 <a href="wmformat-glossary.md"><em>cleanpoint</em></a>。 值為零表示此範例不是 cleanpoint。 非零值表示它是 cleanpoint。 此範例資料單位延伸 (的) 類型是在撰寫以協力廠商編解碼器編碼的 precompressed 媒體資料流程時，用來追蹤 cleanpoints。</td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_Timecode</td>
<td>資料是 <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> 結構，其中包含與範例相關聯的 SMPTE 時間代碼資料。這項應付的大小一律是 WM_SampleExtension_Timecode_Size，也就是14個位元組。<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_FileName</td>
<td>這種類型的範例延伸模組用於檔案資料流程。 檔案資料流程範例中的資料是資料檔案的片段。 範例延伸模組中的資料會指定從中取得範例內容的檔案名。檔案名是寬字元字串，其中包含副檔名格式的檔案名，而不含任何路徑資訊。<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_ContentType</td>
<td>資料會識別此範例所包含的內容類型。 這種類型的範例延伸模組可搭配交錯式影片串流使用。所有交錯內容都使用 WM_CT_INTERLACED 旗標，並以位 <strong>or</strong> 結合 WM_CT_BOTTOM_FIELD_FIRST、WM_CT_TOP_FIELD_FIRST 或 WM_CT_REPEAT_FIRST_FIELD。<br/> 在編碼過程中不會使用欄位順序，但會使用壓縮的範例進行維護，以便將其傳遞至轉譯硬體。 使用不正確的欄位順序來播放交錯式內容，會在影片中引進運動抖動等成品。<br/> 這項應付的大小一律是 WM_SampleExtension_ContentType_Size。<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_PixelAspectRatio</td>
<td>資料會指出範例中內容的圖元外觀比例。 這只適用于影片。此延伸模組類型是用來識別非正方形圖元的長寬比。 如需詳細資訊，請參閱 <a href="to-read-and-write-video-streams-with-non-square-pixels.md">以非正方形圖元讀取和寫入影片串流</a>。<br/> 外觀比例值會儲存為位元組下限的單字，而其最大的位元組是 Y 的外觀。 例如，16:9 會儲存為0x0910。<br/> 這項應付的大小一律是 WM_SampleExtension_PixelAspectRatio_Size，也就是2個位元組。<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_SampleDuration</td>
<td>資料表示緩衝區物件中所含樣本的持續時間（以毫秒為單位）。 在播放時，如果已設定此項，讀取器物件將會使用它來覆寫現有的範例持續時間值。這是因為影片資料流程上的 SDK 執行時間元件會自動設定此項，其位元速率為 100 kbps 或更高，而到期資訊的額外負荷並不重要。 它不會針對速率低於 100 kbps 的資料流程進行設定。 應用程式不應手動設定，因為高位速率資料流程上的寫入器 () 將會以自己的資料覆寫該值。<br/> 這項應付的大小一律是 WM_SampleExtension_SampleDuration_Size，也就是2個位元組。<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_ChromaLocation</td>
<td>資料表示 I420 影片格式所使用的色度次取樣類型。此延伸模組的值會設定為下列其中一個值：<br/>
<ul>
<li>WM_CL_INTERLACED420</li>
<li>WM_CL_PROGRESSIVE420</li>
</ul>
設定檔中未設定此資料單位延伸模組。 它包含在來自解碼器的範例輸出中。<br/> 這項應付的大小一律是 WM_SampleExtension_ChromaLocation_Size，也就是1個位元組。<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_ColorSpaceInfo</td>
<td>資料會提供用於目前影片框架之色彩空間的相關資訊。此延伸模組的值是 <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> 結構。<br/> 設定檔中未設定此資料單位延伸模組。 它包含在來自解碼器的範例輸出中。<br/> 這項應付的大小一律是 WM_SampleExtension_ColorSpaceInfo_Size，也就是3個位元組。<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_UserDataInfo</td>
<td>資料是自訂的使用者資料。資料的前四個位元組包含自訂資料的大小。<br/> 下一個位元組包含範例延伸模組中提供的使用者資料類型。 支援下列類型：<br/>
<ul>
<li>0x1F-序列層級使用者資料</li>
<li>0x1E-進入點層級使用者資料</li>
<li>Bugcheck 0x1d-框架層級使用者資料</li>
<li>0x1C-欄位層級使用者資料</li>
<li>0x1B 配量層級使用者資料</li>
</ul>
第六個和後續的位元組包含使用者資料。 前四個位元組中的數位所指定的使用者資料有許多位元組。<br/> 設定檔中未設定此資料單位延伸模組。 它包含在從解碼器輸出的範例中。<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_SampleProtectionSalt</td>
<td>資料會以範例加密。 此範例延伸模組類型用於從非 ASF 檔案格式匯入的內容，以及 Windows 媒體 DRM 以外的版權保護設定。匯入受保護的內容時，每個範例都必須包含唯一的 salt。 此值通常是單純增加的計數器。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計參考**](programming-reference.md)
</dt> </dl>

 

 





