---
title: RunningTask. EnginePID 屬性
description: 針對腳本，取得正在執行工作之引擎 (進程) 的處理序識別碼。
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- EnginePID 屬性工作排程器
- EnginePID 屬性工作排程器，RunningTask 物件
- RunningTask 物件工作排程器、EnginePID 屬性
topic_type:
- apiref
api_name:
- RunningTask.EnginePID
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd725c44fc85e82d3693d9467956d3040aad2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969181"
---
# <a name="runningtaskenginepid-property"></a>RunningTask. EnginePID 屬性

針對腳本，取得正在執行工作之引擎 (進程) 的處理序識別碼。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a>屬性值

正在執行工作之引擎的處理序識別碼。

## <a name="remarks"></a>備註

這個屬性所傳回的處理序識別碼無法直接附加至字串。 傳回的值必須先透過呼叫傳回值的 [CInt](/previous-versions//fctcwhw9(v=vs.85)) 函式，轉換成整數值。


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

