---
description: 深入瞭解： JetGetErrorInfoW 函數
title: JetGetErrorInfoW 函式
TOCTitle: JetGetErrorInfoW Function
ms:assetid: 7a84f937-7a16-434e-896d-789f316ee833
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475859(v=EXCHG.10)
ms:contentKeyID: 37033565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetErrorInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f459d98ee2cc3c0bb1b57eb5cd4fb630d076836b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468975"
---
# <a name="jetgeterrorinfow-function"></a>JetGetErrorInfoW 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgeterrorinfow-function"></a>JetGetErrorInfoW 函式

資料庫引擎的 **JetGetErrorInfoW** 函數 BAS_。

注意：本檔是以可延伸儲存體引擎的初步發行版本為基礎。 此資訊可能隨時變更。

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a>參數

*pvCoNtext*

需要擴充錯誤資訊的內容或錯誤值。 傳入的值取決於 *InfoLevel* 參數值。

*pvResult*

將接收資訊的緩衝區指標。 緩衝區的類型取決於 *InfoLevel* 參數值。 呼叫端必須設定為適當地對齊緩衝區。

*cbMax*

傳入的 *pvResult* 結構大小上限。

*InfoLevel*

將針對錯誤資訊/內容抓取的資訊類型是由 *pvCoNtext* 參數指定。 儲存在 *pvResult* 中的資料格式取決於 *InfoLevel*。

下表列出此參數的可能值。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_ErrorInfoSpecificErr</p> | <p><em>pvCoNtext</em> 會被視為 <a href="gg269297(v=exchg.10).md">JET_ERR</a>/Error 程式碼， <em>pvResult</em> 會被視為 <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>，而 <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> 結構的欄位則會適當地填入。</p> | 



*grbit*

保留的。

### <a name="return-value"></a>傳回值

此函數會傳回 [JET_ERR](./extensible-storage-engine-error-codes.md) 資料類型，其中包含下表所列的其中一個傳回碼。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含與另一個參數的值結合時沒有意義的值。 發生下列情況時， <strong>JetGetErrorInfo</strong> 可能會發生這種情況：</p><ul><li><p>指定的 <em>InfoLevel</em> 參數值無效。</p></li><li><p>指定的 <em>grbit</em> 值無效。</p></li><li><p>指定的 <em>pvResult</em> 參數緩衝區的 <em>cbMax</em> 值小於這個 <em>InfoLevel</em> 參數的輸出所需的大小。</p></li><li><p>針對 <em>InfoLevel</em> = JET_ErrorInfoSpecificErr，傳入的 <a href="gg294092(v=exchg.10).md">JET_ERR</a> 值對引擎而言是未知的。</p></li></ul> | 
| <p>JET_errDisabledFunctionality</p> | <p>如果此 windows SKU 不支援此功能，將會傳回此錯誤。</p> | 



成功時，適用于要求之錯誤內容/值的輸出緩衝區將會設定為所要求的擴充錯誤資訊。

失敗時，輸出緩衝區的狀態將會是未定義的。

### <a name="remarks"></a>備註

[JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md)函式和 [JET_ERRCAT](./jet-errcat.md)的常數群組包含 *InfoLevel* = JET_ErrorInfoSpecificErr 所傳回之擴充錯誤資訊的相關檔。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows 8。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows 8 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>注意：只會執行 <strong>JetGetErrorInfoW</strong> (Unicode) 。 此 API 沒有 (ANSI) 版本。</p> | 

