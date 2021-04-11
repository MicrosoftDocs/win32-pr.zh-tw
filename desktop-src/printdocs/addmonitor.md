---
description: AddMonitor 函式會安裝本機埠監視器，並連結設定、資料和監視檔案。
ms.assetid: 6a556422-5360-42d2-b177-dba0498c06d8
title: 'AddMonitor 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMonitor
- AddMonitorA
- AddMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 40b45c4dc05580837a2cf4a001cf8d18e646e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027462"
---
# <a name="addmonitor-function"></a>AddMonitor 函式

**AddMonitor** 函式會安裝本機埠監視器，並連結設定、資料和監視檔案。

## <a name="syntax"></a>語法


```C++
BOOL AddMonitor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pMonitors
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定要安裝監視的伺服器名稱。 針對僅支援本機安裝監視的系統，此字串應為 **Null**。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PMonitors* 所指向的結構版本。 此值必須是2。

</dd> <dt>

*pMonitors* \[在\]
</dt> <dd>

[**監視器 \_ 資訊 \_ 2**](monitor-info-2.md)結構的指標。 如果 *pMonitors* 結構的 **PEnvironment** 成員是 **Null**，則會使用目前的呼叫端環境 (用戶端) ，而不是目的地 (伺服器) 。

請注意，如果環境與伺服器的環境不相符，則呼叫會失敗，也就是說，您只能加入針對伺服器架構所撰寫的監視器。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

呼叫端必須有 [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)。

在應用程式呼叫 **AddMonitor** 函式之前，必須將監視器所需的所有檔案複製到 SYSTEM32 目錄。

若要判斷目前已安裝的埠監視器，請呼叫 [**EnumMonitors**](enummonitors.md) 函式。

若要移除 **AddMonitor** 所新增的監視器，請呼叫 [**DeleteMonitor**](deletemonitor.md) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **AddMonitorW** (Unicode) 和 **AddMonitorA** (ANSI) <br/>                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeleteMonitor**](deletemonitor.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**監視 \_ 資訊 \_ 2**](monitor-info-2.md)
</dt> </dl>

 

