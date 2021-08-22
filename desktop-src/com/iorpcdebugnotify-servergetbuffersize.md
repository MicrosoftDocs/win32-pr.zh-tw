---
title: IOrpcDebugNotify ServerGetBufferSize 方法
description: 從伺服器端偵錯工具抓取 RPC 緩衝區大小。
ms.assetid: 1e9ef194-c85b-4f6d-8b89-1f7ee6941189
keywords:
- ServerGetBufferSize 方法 COM
- ServerGetBufferSize 方法 COM，IOrpcDebugNotify 介面
- IOrpcDebugNotify 介面 COM，ServerGetBufferSize 方法
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerGetBufferSize
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570c7371b1aa19bf5a7b3932a9560103ba0b7f25072ad7cb69d5bd53e82bb90e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500728"
---
# <a name="iorpcdebugnotifyservergetbuffersize-method"></a>IOrpcDebugNotify：： ServerGetBufferSize 方法

從伺服器端偵錯工具抓取 RPC 緩衝區大小。

> [!Note]  
> 包含 **ServerGetBufferSize** 函式的匯入程式庫不包含在 Microsoft Windows 軟體開發套件 (SDK) 中。 應用程式可以使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 和 [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) 函式，從 oleaut.dll 中取出 [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) 的函式指標，並透過 [**IOrpcDebugNotify**](iorpcdebugnotify.md) 介面提供此函數。

 

## <a name="syntax"></a>語法


```C++
void ServerGetBufferSize(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpOrpcDebugAll* 
</dt> <dd>

[**ORPC \_ DBG \_ 所有**](orpc-dbg-all.md)結構的指標，其中包含 COM RPC 系統傳遞給偵錯工具的通知特定資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>N/A</dt> </dl> |
| IDL<br/>                      | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORPC \_ INIT 引數 \_**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

