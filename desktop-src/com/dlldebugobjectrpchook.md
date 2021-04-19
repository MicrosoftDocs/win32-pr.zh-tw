---
title: DllDebugObjectRPCHook 函式
description: 由 COM Dll 匯出，以啟用遠端偵錯程式。
ms.assetid: a0f8bf12-0889-452d-84d0-255c5c143bc1
keywords:
- DllDebugObjectRPCHook 函式 COM
topic_type:
- apiref
api_name:
- DllDebugObjectRPCHook
api_location:
- ole32.dll
- API-MS-Win-Core-Com-private-l1-1-0.dll
- ComBase.dll
- API-MS-Win-Core-COM-Private-l1-1-1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62fffe6cc2d9ca650442d0a1c3fea2048fc6c84b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968997"
---
# <a name="dlldebugobjectrpchook-function"></a>DllDebugObjectRPCHook 函式

由 COM Dll 匯出，以啟用遠端偵錯程式。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI DllDebugObjectRPCHook(
   BOOL             fTrace,
   LPORPC_INIT_ARGS lpOrpcInitArgs
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fTrace* 
</dt> <dd>

若 **為 TRUE**，則會啟用遠端偵錯程式。 如果 **為 FALSE**，則不會啟用遠端偵錯程式。

</dd> <dt>

*lpOrpcInitArgs* 
</dt> <dd>

[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)引數結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，**則為 TRUE** ，否則為 **FALSE**

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>N/A</dt> </dl>       |
| 程式庫<br/>                  | <dl> <dt>Ole32.lib .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ole32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> <dt>

[**ORPC \_ DBG \_ 緩衝區**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC \_ INIT 引數 \_**](orpc-init-args.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 





