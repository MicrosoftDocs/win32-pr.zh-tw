---
description: 轉譯錯誤
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: 轉譯錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31d49c5fbb82457282decdaa07152e75db6bc3e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482584"
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

 




| 錯誤碼 | 描述 | 額外資訊 | Variant 型別 | 
|------------|-------------|-------------------|--------------|
| DEX_IDS_BAD_SOURCE_NAME | 檔案名不存在，或 DirectShow 無法辨識副檔名。 | 檔案名稱 | <strong>BSTR</strong> | 
| DEX_IDS_BAD_SOURCE_NAME2 | 檔案類型與副檔名不符，或檔案已損毀。 | 檔案名稱 | <strong>BSTR</strong> | 
| DEX_IDS_MISSING_SOURCE_NAME | 檔案名是必要的，但未提供。 | 無 | 不適用 | 
| DEX_IDS_UNKNOWN_SOURCE | 無法剖析此來源所提供的資料來源。 | 無 | 不適用 | 
| DEX_IDS_INSTALL_PROBLEM | 非預期的錯誤。 部分 DirectShow 元件未正確安裝。 | 無 | 不適用 | 
| DEX_IDS_NO_SOURCE_NAMES | 來源篩選不接受檔案名。 | 無 | 不適用 | 
| DEX_IDS_BAD_MEDIATYPE | 不支援群組的媒體類型。 | 群組編號 | <strong>int</strong> | 
| DEX_IDS_STREAM_NUMBER | 此來源的資料流程號碼無效。 | 串流號碼 | <strong>int</strong> | 
| DEX_IDS_OUTOFMEMORY | 記憶體不足。 | 無 | 不適用 | 
| DEX_IDS_DIBSEQ_NOTALLSAME | 序列中的一個點陣圖與其他點陣圖的類型不同。 | 點陣圖名稱 | <strong>BSTR</strong> | 
| DEX_IDS_CLIPTOOSHORT | 剪輯的媒體時間無效，或與裝置無關的點陣圖 (DIB) 順序太短。<blockquote>[!Note]<br />如果發生其他轉譯錯誤，雖然媒體時間有效，仍可能發生此錯誤。</blockquote><br /> | 無 | 不適用 | 
| DEX_IDS_INVALID_DXT | 效果或轉換 (CLSID) 的類別識別碼無效。 | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_INVALID_DEFAULT_DXT | 預設效果或轉換的 CLSID 無效。 | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_NO_3D | 您的 DirectX 版本不支援三維轉換。 | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_BROKEN_DXT | 此效果不是正確的類型或已中斷。 | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_NO_SUCH_PROPERTY | 物件上不存在這類屬性。 | 屬性名稱 | <strong>BSTR</strong> | 
| DEX_IDS_ILLEGAL_PROPERTY_VAL | 這個屬性的值不合法。 | 指定的值 | <strong>變異</strong> | 
| DEX_IDS_INVALID_XML | XML 檔案中有語法錯誤。 | 行號 | VT_I4 (4 位元組整數)  | 
| DEX_IDS_CANT_FIND_FILTER | 在 XML 中找不到依類別和實例指定的篩選。 |  (實例) 的易記名稱 | <strong>BSTR</strong> | 
| DEX_IDS_DISK_WRITE_ERROR | 將 XML 檔案寫入磁片時發生錯誤。 | 無 | 不適用 | 
| DEX_IDS_INVALID_AUDIO_FX | CLSID 不是有效的 DirectShow 音訊效果篩選。 | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_CANT_FIND_COMPRESSOR | 找不到壓縮檔以產生指定的壓縮格式。 | 無 | 不適用 | 




 

永遠不會發生下列錯誤。 如果您遇到上述其中一個錯誤，請將錯誤報表傳送給 Microsoft。



| 錯誤碼                 | 描述                                 |
|----------------------------|---------------------------------------------|
| DEX \_ 識別碼 \_ 時間軸 \_ 剖析  | 剖析時間軸時發生未預期的錯誤。      |
| DEX \_ 識別碼 \_ 圖形 \_ 錯誤     | 建立篩選圖形時發生未預期的錯誤。 |
| DEX \_ 識別碼 \_ 方格 \_ 錯誤      | 內部方格發生未預期的錯誤。    |
| DEX \_ 識別碼 \_ 介面 \_ 錯誤 | 取得介面時發生未預期的錯誤。      |



 

 

 




