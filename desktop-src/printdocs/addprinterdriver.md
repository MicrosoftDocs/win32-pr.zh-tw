---
description: AddPrinterDriver 函式會安裝本機或遠端印表機驅動程式，並產生設定、資料和驅動程式檔案的關聯。
ms.assetid: 0f762800-f5a5-40ea-8be1-7fd8bda23788
title: 'AddPrinterDriver 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriver
- AddPrinterDriverA
- AddPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: de5a9e9d16a47dfe8b9620edc9acdc5c5fd4d552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693880"
---
# <a name="addprinterdriver-function"></a>AddPrinterDriver 函式

**AddPrinterDriver** 函式會安裝本機或遠端印表機驅動程式，並產生設定、資料和驅動程式檔案的關聯。

若要在安裝或升級印表機驅動程式時有更大的彈性，請使用 [**AddPrinterDriverEx**](addprinterdriverex.md) 函式，因為它允許嚴格升級、嚴格降級、複製較新的檔案，以及複製所有檔案 (無論檔案時間戳記) 。

> [!Note]  
> 不再建議您安裝不含驅動程式套件的印表機驅動程式。 請改用 [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) 。

 

## <a name="syntax"></a>語法


```C++
BOOL AddPrinterDriver(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pDriverInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定應該安裝驅動程式之伺服器的名稱。

如果 *pName* 為 **Null**，驅動程式將會安裝在本機。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PDriverInfo* 所指向的結構版本。

此值可以是2、3、4、6或8。

</dd> <dt>

*pDriverInfo* \[在\]
</dt> <dd>

包含印表機驅動程式資訊之結構的指標。 這取決於 *層級* 的值。



| 值 | 印表機磁片磁碟機結構                  |
|-------|------------------------------------------|
| 2     | [**驅動程式 \_ 資訊 \_ 2**](driver-info-2.md) |
| 3     | [**驅動程式 \_ 資訊 \_ 3**](driver-info-3.md) |
| 4     | [**驅動程式 \_ 資訊 \_ 4**](driver-info-4.md) |
| 6     | [**驅動程式 \_ 資訊 \_ 6**](driver-info-6.md) |
| 8     | [**驅動程式 \_ 資訊 \_ 8**](driver-info-8.md) |



 

如果 *pDriverInfo* 所指向之結構的 **PEnvironment** 成員為 **Null**，則會使用目前的呼叫端/用戶端環境 (不是目的地/伺服器) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

呼叫端必須有 [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)。

在應用程式呼叫 **AddPrinterDriver** 函式之前，驅動程式所需的所有檔案都必須複製到系統的印表機驅動程式目錄。 應用程式可以藉由呼叫 [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) 函式來取得此目錄的名稱。

應用程式可以藉由呼叫 [**EnumPrinterDrivers**](enumprinterdrivers.md) 函式來判斷目前安裝的印表機驅動程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **AddPrinterDriverW** (Unicode) 和 **AddPrinterDriverA** (ANSI) <br/>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> <dt>

[**驅動程式 \_ 資訊 \_ 2**](driver-info-2.md)
</dt> <dt>

[**驅動程式 \_ 資訊 \_ 3**](driver-info-3.md)
</dt> <dt>

[**驅動程式 \_ 資訊 \_ 4**](driver-info-4.md)
</dt> <dt>

[**驅動程式 \_ 資訊 \_ 6**](driver-info-6.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriverDirectory**](getprinterdriverdirectory.md)
</dt> </dl>

 

