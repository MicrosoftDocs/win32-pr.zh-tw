---
title: RPC NDR 介面參考
description: Microsoft RPC NDR 目前支援下列功能和結構
ms.assetid: 2EBB2DD6-60DD-4C9F-9F79-231383B28517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5f1d7aa19cff36da67e807a671ec176c0d303610f5c0f6629940d5e132f47ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073348"
---
# <a name="rpc-ndr-interface-reference"></a>RPC NDR 介面參考

Microsoft RPC NDR 目前支援下列功能和結構：

-   [**CStdStubBuffer \_ AddRef**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_addref)
-   [**CStdStubBuffer \_ 連線**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_connect)
-   [**CStdStubBuffer \_ CountRefs**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_countrefs)
-   [**CStdStubBuffer \_ DebugServerQueryInterface**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_debugserverqueryinterface)
-   [**CStdStubBuffer \_ DebugServerRelease**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_debugserverrelease)
-   [**CStdStubBuffer \_ 中斷連線**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_disconnect)
-   [**CStdStubBuffer \_ 調用**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_invoke)
-   [**CStdStubBuffer \_ IsIIDSupported**](/windows/desktop/api/RpcProxy/nf-rpcproxy-cstdstubbuffer_isiidsupported)
-   [**CStdStubBuffer \_ QueryInterface**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_queryinterface)
-   [**IUnknown \_ AddRef \_ Proxy**](/windows/desktop/api/unknwnbase/nf-unknwnbase-iunknown_addref_proxy)
-   [**IUnknown \_ QueryInterface \_ Proxy**](/windows/desktop/api/unknwnbase/nf-unknwnbase-iunknown_queryinterface_proxy)
-   [**IUnknown \_ 發行 \_ Proxy**](/windows/desktop/api/unknwnbase/nf-unknwnbase-iunknown_queryinterface_proxy)
-   [**NdrAsyncClientCall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrasyncclientcall)
-   [**NdrClearOutParameters**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrclearoutparameters)
-   [**NdrClientCall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrclientcall)
-   [**NdrClientCall2**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrclientcall2)
-   [**NdrConformantArrayUnmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantarrayunmarshall)
-   [**NdrConformantStringBufferSize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantstringbuffersize)
-   [**NdrConformantStringMarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantstringmarshall)
-   [**NdrConformantStringUnmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantstringunmarshall)
-   [**NdrCoNtextHandleInitialize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcontexthandleinitialize)
-   [**NdrCoNtextHandleSize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcontexthandlesize)
-   [**NdrCoNtextHandleMemorySize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcontexthandlememorysize)
-   [**NdrConvert**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconvert)
-   [**NdrCStdStubBuffer \_ 版本**](/previous-versions/aa374242(v=vs.80))
-   [**NdrCStdStubBuffer2 \_ 版本**](/previous-versions/aa374240(v=vs.80))
-   [**NdrDllCanUnloadNow**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllcanunloadnow)
-   [**NdrDllGetClassObject**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllgetclassobject)
-   [**NdrDllRegisterProxy**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllregisterproxy)
-   [**NdrDllUnregisterProxy**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllunregisterproxy)
-   [**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
-   [**NdrInterfacePointerBufferSize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointerbuffersize)
-   [**NdrInterfacePointerFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointerfree)
-   [**NdrInterfacePointerMarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointermarshall)
-   [**NdrInterfacePointerUnmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointerunmarshall)
-   [**NdrOleAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndroleallocate)
-   [**NdrOleFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrolefree)
-   [**NdrPointerBufferSize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointerbuffersize)
-   [**NdrPointerFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointerfree)
-   [**NdrPointerMarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointermarshall)
-   [**NdrPointerUnmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointerunmarshall)
-   [**NdrProxyErrorHandler**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxyerrorhandler)
-   [**NdrProxyFreeBuffer**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxyfreebuffer)
-   [**NdrProxyGetBuffer**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxygetbuffer)
-   [**NdrProxyInitialize**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxyinitialize)
-   [**NdrProxySendReceive**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxysendreceive)
-   [**NdrSimpleTypeMarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimpletypemarshall)
-   [**NdrSimpleTypeUnmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimpletypeunmarshall)
-   [**NdrStubCall2**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrstubcall2)
-   [**NdrStubForwardingFunction**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrstubforwardingfunction)
-   [**NdrStubGetBuffer**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrstubgetbuffer)
-   [**NdrStubInitialize**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrstubinitialize)
-   [**NdrUserMarshalBufferSize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalbuffersize)
-   [**NdrUserMarshalFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalfree)
-   [**NdrUserMarshalMarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalmarshall)
-   [**MIDL \_ 存根 \_ DESC**](/windows/desktop/api/Rpcndr/ns-rpcndr-midl_stub_desc)
-   [**MIDL \_ 存根 \_ 訊息**](/windows/desktop/api/Rpcndr/ns-rpcndr-midl_stub_message)
-   [**ProxyFileInfo**](/windows/win32/api/rpcproxy/ns-rpcproxy-proxyfileinfo)
-   [**RPC \_ 訊息**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message)

 

 