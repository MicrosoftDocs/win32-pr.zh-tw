---
title: ORPC_DBG_ALL 結構
description: ORPC \_ DBG \_ ALL 結構是用來將參數傳遞至 IOrpcDebugNotify 介面的方法。
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- ORPC_DBG_ALL 結構 COM
- LPORPC_DBG_ALL 結構指標 COM
topic_type:
- apiref
api_name:
- ORPC_DBG_ALL
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17f5b09e5fe2f668bf2bcd21e2e7fe6f0f766a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094208"
---
# <a name="orpc_dbg_all-structure"></a>ORPC \_ DBG \_ ALL 結構

**ORPC \_ DBG \_ ALL** 結構是用來將參數傳遞至 [**IOrpcDebugNotify**](iorpcdebugnotify.md)介面的方法。

> [!Note]  
> [**IOrpcDebugNotify**](iorpcdebugnotify.md)介面的每個方法都會使用不同的成員組合。 如果成員未表示為方法所使用，則會在傳遞至該方法時未定義。

 

## <a name="syntax"></a>語法


```C++
typedef struct ORPC_DBG_ALL {
  BYTE              *pSignature;
  RPCOLEMESSAGE     *pMessage;
  const IID         *refiid;
  IRpcChannelBuffer *pChannel;
  IUnknown          *pUnkProxyMgr;
  void              *pInterface;
  IUnknown          *pUnkObject;
  HRESULT           hresult;
  void              *pvBuffer;
  ULONG             *cbBuffer;
  ULONG             *lpcbBuffer;
  void              *reserved;
} ORPC_DBG_ALL, *LPORPC_DBG_ALL;
```



## <a name="members"></a>成員

<dl> <dt>

**pSignature**
</dt> <dd>

**位元組** 緩衝區的指標，其中包含：

-   前四個位元組：遞增記憶體順序中的 ASCII 字元 "MARB"。
-   接下來的16個位元組：識別所呼叫之通知的 **GUID** 。 它包含下列其中一項：
    1.  [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)：9ED14F80-9673-101A-B07B-00DD01113F11
    2.  [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):D a45f3e0-9673-101A-B07B-00DD01113F11
    3.  [**ClientNotify**](iorpcdebugnotify-clientnotify.md)：4F60E540-9674-101A-B07B-00DD01113F11
    4.  [**ServerNotify**](iorpcdebugnotify-servernotify.md)：1084FA00-9674-101A-B07B-00DD01113F11
    5.  [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)：22080240-9674-101A-B07B-00DD01113F11
    6.  [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)：2FC09500-9674-101A-B07B-00DD01113F11
-   接下來四個位元組：保留供日後使用。

> [!Note]
>
> 供 [**IOrpcDebugNotify**](iorpcdebugnotify.md) 介面的所有方法使用。

 

</dd> <dt>

**pMessage**
</dt> <dd>

[**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage)結構的指標，其中包含 RPC 資料封送處理資訊。

> [!Note]
>
> 由 [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)、 [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)、 [**ClientNotify**](iorpcdebugnotify-clientnotify.md)、 [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)、 [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)和 [**ServerNotify**](iorpcdebugnotify-servernotify.md) 方法所使用。

 

</dd> <dt>

**refiid**
</dt> <dd>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)介面的 IID 指標。

> [!Note]
>
> 由 [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)、 [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)、 [**ClientNotify**](iorpcdebugnotify-clientnotify.md)、 [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)、 [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)和 [**ServerNotify**](iorpcdebugnotify-servernotify.md) 方法所使用。

 

</dd> <dt>

**pChannel**
</dt> <dd>

伺服器上 COM RPC 通道實 [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) 介面的指標。

> [!Note]
>
> 由 [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)、 [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)和 [**ServerNotify**](iorpcdebugnotify-servernotify.md) 方法所使用。

 

</dd> <dt>

**pUnkProxyMgr**
</dt> <dd>

此偵錯工具調用所涉及之物件的 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面指標。 可能是 **Null**，但這會減少偵錯工具的功能。

> [!Note]
>
> 由 [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)、 [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)和 [**ClientNotify**](iorpcdebugnotify-clientnotify.md) 方法所使用。

 

</dd> <dt>

**pInterface**
</dt> <dd>

此 RPC 將叫用之方法的 COM 介面指標。 不得為 **Null**。

> [!Note]
>
> 由 [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)、 [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)和 [**ServerNotify**](iorpcdebugnotify-servernotify.md) 方法所使用。

 

</dd> <dt>

**>punkobject**
</dt> <dd>

必須是 **Null**。

> [!Note]
>
> 由 [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)、 [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)和 [**ServerNotify**](iorpcdebugnotify-servernotify.md) 方法所使用。

 

</dd> <dt>

**hresult**
</dt> <dd>

以下是每個通知的成員用途變更：

[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)：用戶端偵錯工具將傳送至伺服器偵錯工具的位元組數目。 如果為零，則不需要傳送任何資訊。

[**ClientNotify**](iorpcdebugnotify-clientnotify.md)：最後一個 RPC 的 **HRESULT** 。

[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)：用戶端偵錯工具將傳送至伺服器偵錯工具的位元組數目。 如果為零，則不需要傳送任何資訊。

> [!Note]
>
> 由 [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)、 [**ClientNotify**](iorpcdebugnotify-clientnotify.md)和 [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) 方法所使用。

 

</dd> <dt>

**pvBuffer**
</dt> <dd>

[**ORPC \_ DBG \_ 緩衝區**](orpc-dbg-buffer.md)結構的指標，其中包含 RPC 封送處理的偵錯工具資訊。 如果 **cbBuffer** 為零，則為未定義。

> [!Note]
>
> 由 [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)、 [**ClientNotify**](iorpcdebugnotify-clientnotify.md)、 [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)和 [**ServerNotify**](iorpcdebugnotify-servernotify.md) 方法所使用。

 

</dd> <dt>

**cbBuffer**
</dt> <dd>

**PvBuffer** 所指向之資料的長度（以位元組為單位）。

> [!Note]
>
> 由 [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)、 [**ClientNotify**](iorpcdebugnotify-clientnotify.md)、 [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)和 [**ServerNotify**](iorpcdebugnotify-servernotify.md) 方法所使用。

 

</dd> <dt>

**lpcbBuffer**
</dt> <dd>

用戶端偵錯工具將傳送至伺服器偵錯工具的位元組數目。 如果為零，則不需要傳送任何資訊。 此值會取代 **hresult** 中傳回的值。

> [!Note]
>
> 由 [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)、 [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) 方法使用。

 

</dd> <dt>

**保留**
</dt> <dd>

保留的。 請勿使用。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORPC \_ DBG \_ 緩衝區**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC \_ INIT 引數 \_**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

