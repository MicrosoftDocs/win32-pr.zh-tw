---
description: ExpertIndicateStatus 函式會指出完成捕獲檔案的專家分析完成百分比。
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: 'ExpertIndicateStatus 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertIndicateStatus
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f9f40e339b450496ec4b0aff1f3e951c4d7468fa22f7b2ff3dd2f84de6b92354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012266"
---
# <a name="expertindicatestatus-function"></a>ExpertIndicateStatus 函式

**ExpertIndicateStatus** 函式會指出專家的 capture 分析完成百分比。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI ExpertIndicateStatus(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  EXPERTSTATUSENUMERATION Status,
  _In_  DWORD                   SubStatus,
  _In_  char                    *sztext,
  _Out_ long                    PercentDone
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hExpertKey* \[在\]
</dt> <dd>

獨特的專家識別碼。 網路監視器在呼叫 [Run](run.md)函式時，將 *hExpertKey* 傳遞給專家。

</dd> <dt>

*狀態* \[在\]
</dt> <dd>

分析目前的狀態。 指定下列其中一個 [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) 值。



| 值                                                                                                                                                                                 | 意義                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <dt>**EXPERTSTATUS \_ 非使用中**</dt> </dl> | 專家從未開始。 <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <dt>**EXPERTSTATUS \_ 開始**</dt> </dl> | 專家即將開始。 <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <dt>**EXPERTSTATUS \_ 正在執行**</dt> </dl>    | 專家正在正常執行。 <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <dt>**EXPERTSTATUS \_ 問題**</dt> </dl>    | 子狀態參數中指定的問題已停止專家。 <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <dt>**EXPERTSTATUS 已 \_ 中止**</dt> </dl>    | 網路監視器已停止專家。 <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <dt>**EXPERTSTATUS \_ 完成**</dt> </dl>             | 專家已成功完成分析。 <br/>                     |



 

</dd> <dt>

子 *狀態* \[在\]
</dt> <dd>

*狀態* 參數所提供之資訊的延伸或澄清。

</dd> <dt>

*sztext* \[在\]
</dt> <dd>

選擇性的文字狀態指標。

此參數值可以是 **Null**。

</dd> <dt>

*PercentDone* \[擴展\]
</dt> <dd>

專家已處理的捕獲資料百分比。

當專家成功完成捕獲檔案的分析時，系統會將百分比設定為100。 將會忽略大於99的任何數位。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值為 NMERR \_ 專家 \_ 終止; 專家必須立即清除並返回，而不需要完成 capture。

## <a name="remarks"></a>備註

**ExpertIndicateStatus** 函式只能由執行 [執行](run.md)或 [設定](configure.md)匯出函數的專家呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |
