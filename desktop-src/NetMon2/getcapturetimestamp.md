---
description: GetCaptureTimeStamp 函式會傳回 capture 開始錄製畫面格的時間和日期。
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: 'GetCaptureTimeStamp 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 93ae1c94a5e83d0029aba4403ad4ba23db0f4006bb5b9be68cc469939e63c734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366633"
---
# <a name="getcapturetimestamp-function"></a>GetCaptureTimeStamp 函式

**GetCaptureTimeStamp** 函式會傳回 capture 開始錄製畫面格的時間和日期。

## <a name="syntax"></a>語法


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hCapture* \[在\]
</dt> <dd>

捕捉的控制碼。 如需取得 capture 控制碼的詳細資訊，請參閱本 **GetCaptureTimeStamp** 主題的「備註」一節。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值是 [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構的指標。

如果函式不成功，則傳回值為 **Null**。

## <a name="remarks"></a>備註

**GetCaptureTimeStamp** 函式會傳回網路封包提供者 (NPP) 開始收集資料的時間，而不是當專家載入要分析的捕獲時。

請勿覆寫 **SYSTEMTIME** 結構中的資料。 資料是捕捉的一部分。 嘗試修改資料會造成存取違規。

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetCaptureTimeStamp** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 

