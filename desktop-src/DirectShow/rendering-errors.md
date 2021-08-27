---
description: 轉譯錯誤
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: 轉譯錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e5af72ccf7ca76b2d4899178757282f1879c06052d2db2f3e1d929ddeef0f53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050608"
---
# <a name="rendering-errors"></a>轉譯錯誤

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

Microsoft® DirectShow®編輯服務 (DES) 會定義用來記錄轉譯錯誤的各種錯誤碼。 如果專案未正確轉譯，轉譯引擎會呼叫 [**IAMErrorLog：： LogError**](iamerrorlog-logerror.md) 方法。 下表摘要說明 **LogError** 提供的參數：

-   錯誤碼包含在 *ErrorCode* 參數中。
-   描述包含在 ErrorString 參數中。
-   描述包含在 *ErrorString* 參數中。
-   如果有額外的資訊， **variant** 型別就會包含在 *pExtraInfo* 所指向之 **變異** 的 **vt** 成員中。

> [!Note]  
> 此處所述的錯誤碼不是 **HRESULT** 值。 如需 DES 特定的 **HRESULT** 傳回值清單，請參閱 [錯誤和成功碼](error-and-success-codes.md)。

 



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>錯誤碼</th>
<th>描述</th>
<th>額外資訊</th>
<th>Variant 型別</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DEX_IDS_BAD_SOURCE_NAME</td>
<td>檔案名不存在，或 DirectShow 無法辨識副檔名。</td>
<td>檔案名稱</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_BAD_SOURCE_NAME2</td>
<td>檔案類型與副檔名不符，或檔案已損毀。</td>
<td>檔案名稱</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_MISSING_SOURCE_NAME</td>
<td>檔案名是必要的，但未提供。</td>
<td>無</td>
<td>不適用</td>
</tr>
<tr class="even">
<td>DEX_IDS_UNKNOWN_SOURCE</td>
<td>無法剖析此來源所提供的資料來源。</td>
<td>無</td>
<td>不適用</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INSTALL_PROBLEM</td>
<td>非預期的錯誤。 部分 DirectShow 元件未正確安裝。</td>
<td>無</td>
<td>不適用</td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SOURCE_NAMES</td>
<td>來源篩選不接受檔案名。</td>
<td>無</td>
<td>不適用</td>
</tr>
<tr class="odd">
<td>DEX_IDS_BAD_MEDIATYPE</td>
<td>不支援群組的媒體類型。</td>
<td>群組編號</td>
<td><strong>int</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_STREAM_NUMBER</td>
<td>此來源的資料流程號碼無效。</td>
<td>串流號碼</td>
<td><strong>int</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_OUTOFMEMORY</td>
<td>記憶體不足。</td>
<td>無</td>
<td>不適用</td>
</tr>
<tr class="even">
<td>DEX_IDS_DIBSEQ_NOTALLSAME</td>
<td>序列中的一個點陣圖與其他點陣圖的類型不同。</td>
<td>點陣圖名稱</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_CLIPTOOSHORT</td>
<td>剪輯的媒體時間無效，或與裝置無關的點陣圖 (DIB) 順序太短。
<blockquote>
[!Note]<br />
如果發生其他轉譯錯誤，雖然媒體時間有效，仍可能發生此錯誤。
</blockquote>
<br/></td>
<td>無</td>
<td>不適用</td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_DXT</td>
<td>效果或轉換 (CLSID) 的類別識別碼無效。</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_DEFAULT_DXT</td>
<td>預設效果或轉換的 CLSID 無效。</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_3D</td>
<td>您的 DirectX 版本不支援三維轉換。</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_BROKEN_DXT</td>
<td>此效果不是正確的類型或已中斷。</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SUCH_PROPERTY</td>
<td>物件上不存在這類屬性。</td>
<td>屬性名稱</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_ILLEGAL_PROPERTY_VAL</td>
<td>這個屬性的值不合法。</td>
<td>指定的值</td>
<td><strong>變異</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_XML</td>
<td>XML 檔案中有語法錯誤。</td>
<td>行號</td>
<td>VT_I4 (4 位元組整數) </td>
</tr>
<tr class="odd">
<td>DEX_IDS_CANT_FIND_FILTER</td>
<td>在 XML 中找不到依類別和實例指定的篩選。</td>
<td> (實例) 的易記名稱</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_DISK_WRITE_ERROR</td>
<td>將 XML 檔案寫入磁片時發生錯誤。</td>
<td>無</td>
<td>不適用</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_AUDIO_FX</td>
<td>CLSID 不是有效的 DirectShow 音訊效果篩選。</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_CANT_FIND_COMPRESSOR</td>
<td>找不到壓縮檔以產生指定的壓縮格式。</td>
<td>無</td>
<td>不適用</td>
</tr>
</tbody>
</table>



 

永遠不會發生下列錯誤。 如果您遇到上述其中一個錯誤，請將錯誤報表傳送給 Microsoft。



| 錯誤碼                 | 描述                                 |
|----------------------------|---------------------------------------------|
| DEX \_ 識別碼 \_ 時間軸 \_ 剖析  | 剖析時間軸時發生未預期的錯誤。      |
| DEX \_ 識別碼 \_ 圖形 \_ 錯誤     | 建立篩選圖形時發生未預期的錯誤。 |
| DEX \_ 識別碼 \_ 方格 \_ 錯誤      | 內部方格發生未預期的錯誤。    |
| DEX \_ 識別碼 \_ 介面 \_ 錯誤 | 取得介面時發生未預期的錯誤。      |



 

 

 




