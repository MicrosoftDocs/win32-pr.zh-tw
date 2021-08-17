---
description: FreePrinterNotifyInfo 函式會釋放由 FindNextPrinterChangeNotification 函數所建立的系統組態緩衝區。
ms.assetid: e50d4718-3682-486b-9d07-ddddd0b284dc
title: 'FreePrinterNotifyInfo 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePrinterNotifyInfo
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 37340bc7d5ba576735c7bf4cc1ef8ac40b07377e829353d35452ed0fa5307891
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091948"
---
# <a name="freeprinternotifyinfo-function"></a>FreePrinterNotifyInfo 函式

**FreePrinterNotifyInfo** 函式會釋放由 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)函數所建立的系統組態緩衝區。

## <a name="syntax"></a>語法


```C++
BOOL FreePrinterNotifyInfo(
  _In_ PPRINTER_NOTIFY_INFO pPrinterNotifyInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPrinterNotifyInfo* \[在\]
</dt> <dd>

從 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)函式的呼叫傳回的 [**印表機 \_ 通知 \_ 資訊**](printer-notify-info.md)緩衝區指標。 **FreePrinterNotifyInfo** 會將這個緩衝區解除配置。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**印表機 \_ 通知 \_ 資訊**](printer-notify-info.md)
</dt> </dl>

 

 




