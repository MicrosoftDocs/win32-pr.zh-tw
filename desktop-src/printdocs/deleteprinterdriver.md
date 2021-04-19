---
description: DeletePrinterDriver 函數會從伺服器上支援的驅動程式名稱清單中移除指定的印表機驅動程式名稱。
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
title: 'DeletePrinterDriver 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriver
- DeletePrinterDriverA
- DeletePrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 9e84730be0d20100c2da42aa357f35c08cfb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974435"
---
# <a name="deleteprinterdriver-function"></a>DeletePrinterDriver 函式

**DeletePrinterDriver** 函數會從伺服器上支援的驅動程式名稱清單中移除指定的印表機驅動程式名稱。

若要刪除與驅動程式相關聯的檔案，以及從伺服器支援的驅動程式名稱清單中移除指定的印表機驅動程式名稱，請使用 [**DeletePrinterDriverEx**](deleteprinterdriverex.md) 函數。

只有當指定的環境未使用任何驅動程式版本時， **DeletePrinterDriver** 才會刪除驅動程式。 [**DeletePrinterDriverEx**](deleteprinterdriverex.md) 可以刪除特定版本的驅動程式。

## <a name="syntax"></a>語法


```C++
BOOL DeletePrinterDriver(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定要從中刪除驅動程式之伺服器的名稱。 如果此參數為 **Null**，則會在本機移除印表機驅動程式名稱。

</dd> <dt>

*pEnvironment* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定要從中刪除驅動程式 (例如，Windows x86、Windows IA64 或 Windows x64) 的環境。 如果此參數為 **Null**，則會從目前的呼叫應用程式和用戶端電腦的環境中刪除驅動程式名稱， (不是目的地應用程式和列印伺服器) 。

</dd> <dt>

*pDriverName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定應該刪除之驅動程式的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

呼叫端必須有 [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)。

**DeletePrinterDriver** 函式不會刪除相關聯的檔案，只會從 [**EnumPrinterDrivers**](enumprinterdrivers.md)函數所傳回的清單中移除驅動程式名稱。

在呼叫 **DeletePrinterDriver** 之前，您必須刪除所有使用印表機驅動程式的印表機物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **DeletePrinterDriverW** (Unicode) 和 **DeletePrinterDriverA** (ANSI) <br/>                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDriverEx**](deleteprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> </dl>

 

