---
title: IOrpcDebugNotify 介面
description: 提供遠端偵錯功能。
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- IOrpcDebugNotify 介面 COM
- IOrpcDebugNotify 介面 COM，描述
topic_type:
- apiref
api_name:
- IOrpcDebugNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4db08daf93997b2a7fa0ed383591cb5d111ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509426"
---
# <a name="iorpcdebugnotify-interface"></a>IOrpcDebugNotify 介面

提供遠端偵錯功能。

## <a name="when-to-implement"></a>執行時機

執行此介面可讓您透過 RPC 進行遠端偵錯。

## <a name="when-to-use"></a>使用時機

當「軟體例外狀況」不應該用於 COM 偵錯工具通知時，此介面應該用於同進程遠端偵錯程式。 它可讓同進程偵錯工具透過使用這些方法的直接呼叫來通知。

## <a name="members"></a>成員

**IOrpcDebugNotify** 介面繼承自 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)介面。 **IOrpcDebugNotify** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IOrpcDebugNotify** 介面具有這些方法。



| 方法                                                              | 描述                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)       | 從用戶端偵錯工具將資料傳送至伺服器偵錯工具。<br/>         |
| [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) | 從用戶端偵錯工具抓取 RPC 緩衝區大小。<br/>        |
| [**ClientNotify**](iorpcdebugnotify-clientnotify.md)               | 通知用戶端傳出的偵錯工具要求至伺服器。<br/>   |
| [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)       | 從伺服器偵錯工具將資料傳送至用戶端偵錯工具。<br/>         |
| [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) | 從伺服器端偵錯工具抓取 RPC 緩衝區大小。<br/>        |
| [**ServerNotify**](iorpcdebugnotify-servernotify.md)               | 通知伺服器來自用戶端的傳入偵錯工具要求。<br/> |



 

## <a name="remarks"></a>備註

包含 **IOrpcDebugNotify** 介面的匯入程式庫不包含在 Microsoft WINDOWS 軟體開發套件 (SDK) 中。 應用程式可以使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 和 [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) 函式，從 oleaut.dll 中取出 [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) 的函式指標，並透過 **IOrpcDebugNotify** 介面提供這些方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>N/A</dt> </dl> |
| Idl<br/>                      | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> <dt>

[**ORPC \_ DBG \_ 緩衝區**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC \_ INIT 引數 \_**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> </dl>

 

