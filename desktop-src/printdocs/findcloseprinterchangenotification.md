---
description: FindClosePrinterChangeNotification 函式會關閉藉由呼叫 FindFirstPrinterChangeNotification 函數所建立的變更通知物件。
ms.assetid: 2b4758f8-af0a-494b-8f1b-8ea6ee73c79b
title: 'FindClosePrinterChangeNotification 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindClosePrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 17ec31b1f2992b4311e42e149d39b68b3d724a3d943d67df7c4c5fce88122606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112488"
---
# <a name="findcloseprinterchangenotification-function"></a>FindClosePrinterChangeNotification 函式

**FindClosePrinterChangeNotification** 函式會關閉藉由呼叫 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)函數所建立的變更通知物件。 與變更通知物件相關聯的印表機或列印伺服器，將不會再由該物件監視。

## <a name="syntax"></a>語法


```C++
BOOL FindClosePrinterChangeNotification(
  _In_ HANDLE hChange
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hChange* \[在\]
</dt> <dd>

要關閉之變更通知物件的控制碼。 這是藉由呼叫 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) 函式所建立的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

在呼叫 **FindClosePrinterChangeNotification** 函式之後，您無法在後續的 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)或 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)呼叫中使用 *hChange* 控制碼。

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

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> </dl>

 

 




