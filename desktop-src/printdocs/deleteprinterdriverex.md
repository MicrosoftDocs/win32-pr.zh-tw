---
description: DeletePrinterDriverEx 函式會從伺服器上支援的驅動程式名稱清單中移除指定的印表機驅動程式名稱，並刪除與驅動程式相關聯的檔案。 此函數也可以刪除驅動程式的特定版本。
ms.assetid: 1a3d7c7f-1d45-4877-a8f7-a77f40e3c319
title: 'DeletePrinterDriverEx 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverEx
- DeletePrinterDriverExA
- DeletePrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b88ef38236961286875a1885dad9dde936887d13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993176"
---
# <a name="deleteprinterdriverex-function"></a>DeletePrinterDriverEx 函式

**DeletePrinterDriverEx** 函式會從伺服器上支援的驅動程式名稱清單中移除指定的印表機驅動程式名稱，並刪除與驅動程式相關聯的檔案。 此函數也可以刪除驅動程式的特定版本。

## <a name="syntax"></a>語法


```C++
BOOL DeletePrinterDriverEx(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName,
  _In_ DWORD  dwDeleteFlag,
  _In_ DWORD  dwVersionFlag
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定要從中刪除驅動程式之伺服器的名稱。 如果此參數為 **Null**，此函式會從本機電腦刪除印表機驅動程式。

</dd> <dt>

*pEnvironment* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定要從中刪除驅動程式的環境 (例如 Windows NT x86、Windows IA64 或 Windows x64) 。 如果此參數為 **Null**，則會從目前的呼叫應用程式和用戶端電腦的環境中刪除驅動程式名稱， (不是目的地應用程式和列印伺服器) 。

</dd> <dt>

*pDriverName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定要刪除之驅動程式的名稱。

</dd> <dt>

*dwDeleteFlag* \[在\]
</dt> <dd>

用來刪除驅動程式檔案和版本的選項。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                                                     | 意義                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DPD_DELETE_SPECIFIC_VERSION"></span><span id="dpd_delete_specific_version"></span><dl> <dt>**DPD \_ 刪除 \_ 特定 \_ 版本**</dt> </dl> | 刪除在 *dwVersionFlag* 中指定的版本。 這並不確定會從伺服器支援的驅動程式清單中移除驅動程式。<br/>                  |
| <span id="DPD_DELETE_UNUSED_FILES"></span><span id="dpd_delete_unused_files"></span><dl> <dt>**DPD \_ 刪除 \_ 未使用的檔案 \_**</dt> </dl>             | 移除任何未使用的驅動程式檔案。<br/>                                                                                                                                           |
| <span id="DPD_DELETE_ALL_FILES"></span><span id="dpd_delete_all_files"></span><dl> <dt>**DPD \_ 刪除 \_ 所有 \_ 檔案**</dt> </dl>                      | 只有在所有相關聯的檔案都可以移除時，才會刪除驅動程式。 如果有其他安裝的驅動程式正在使用任何驅動程式的檔案，刪除作業將會失敗。<br/> |



 

如果 \_ \_ 未指定 DPD 刪除特定 \_ 版本，則函式會刪除所有版本的驅動程式（如果沒有使用的話）。 如果 DPD \_ 刪除 \_ 未使用的檔案 \_ ，或未 \_ 指定 DPD 刪除所有檔案 \_ ，則該函式不 \_ 會刪除驅動程式檔案。

</dd> <dt>

*dwVersionFlag* \[在\]
</dt> <dd>

要刪除的驅動程式版本。 此參數可以是0、1、2或3。 只有在 *dwDeleteFlag* 包含 DPD \_ DELETE \_ 特定版本旗標時，才會使用此參數 \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

在函數刪除驅動程式檔案之前，它會呼叫驅動程式的 **DrvDriverEvent** 函式，讓驅動程式能夠移除任何未使用的私用檔案。 如需有關 **DrvDriverEvent** 的詳細資訊，請參閱 Microsoft Windows 驅動程式開發工具組 (DDK) 。

如果目前已載入驅動程式檔案，則函式會將它們移至臨時目錄，並在重新開機時將它們標示為刪除。

在呼叫 **DeletePrinterDriverEx** 之前，您必須刪除所有使用印表機驅動程式的印表機物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **DeletePrinterDriverExW** (Unicode) 和 **DeletePrinterDriverExA** (ANSI) <br/>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> </dl>

 

 




