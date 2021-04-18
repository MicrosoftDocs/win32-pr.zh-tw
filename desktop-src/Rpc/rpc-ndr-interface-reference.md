---
title: RPC NDR 介面參考
description: Microsoft RPC NDR 目前支援下列功能和結構
ms.assetid: 2EBB2DD6-60DD-4C9F-9F79-231383B28517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a802720c584d08112c733135c3bb5640e7679c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315826"
---
# <a name="rpc-ndr-interface-reference"></a><span data-ttu-id="2869d-103">RPC NDR 介面參考</span><span class="sxs-lookup"><span data-stu-id="2869d-103">RPC NDR Interface Reference</span></span>

<span data-ttu-id="2869d-104">Microsoft RPC NDR 目前支援下列功能和結構：</span><span class="sxs-lookup"><span data-stu-id="2869d-104">Microsoft RPC NDR currently supports the following functions and structures:</span></span>

-   [<span data-ttu-id="2869d-105">**CStdStubBuffer \_ AddRef**</span><span class="sxs-lookup"><span data-stu-id="2869d-105">**CStdStubBuffer\_AddRef**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_addref)
-   [<span data-ttu-id="2869d-106">**CStdStubBuffer \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="2869d-106">**CStdStubBuffer\_Connect**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_connect)
-   [<span data-ttu-id="2869d-107">**CStdStubBuffer \_ CountRefs**</span><span class="sxs-lookup"><span data-stu-id="2869d-107">**CStdStubBuffer\_CountRefs**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_countrefs)
-   [<span data-ttu-id="2869d-108">**CStdStubBuffer \_ DebugServerQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="2869d-108">**CStdStubBuffer\_DebugServerQueryInterface**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_debugserverqueryinterface)
-   [<span data-ttu-id="2869d-109">**CStdStubBuffer \_ DebugServerRelease**</span><span class="sxs-lookup"><span data-stu-id="2869d-109">**CStdStubBuffer\_DebugServerRelease**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_debugserverrelease)
-   [<span data-ttu-id="2869d-110">**CStdStubBuffer \_ 中斷連線**</span><span class="sxs-lookup"><span data-stu-id="2869d-110">**CStdStubBuffer\_Disconnect**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_disconnect)
-   [<span data-ttu-id="2869d-111">**CStdStubBuffer \_ 調用**</span><span class="sxs-lookup"><span data-stu-id="2869d-111">**CStdStubBuffer\_Invoke**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_invoke)
-   [<span data-ttu-id="2869d-112">**CStdStubBuffer \_ IsIIDSupported**</span><span class="sxs-lookup"><span data-stu-id="2869d-112">**CStdStubBuffer\_IsIIDSupported**</span></span>](/windows/desktop/api/RpcProxy/nf-rpcproxy-cstdstubbuffer_isiidsupported)
-   [<span data-ttu-id="2869d-113">**CStdStubBuffer \_ QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="2869d-113">**CStdStubBuffer\_QueryInterface**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_queryinterface)
-   [<span data-ttu-id="2869d-114">**IUnknown \_ AddRef \_ Proxy**</span><span class="sxs-lookup"><span data-stu-id="2869d-114">**IUnknown\_AddRef\_Proxy**</span></span>](/windows/desktop/api/unknwnbase/nf-unknwnbase-iunknown_addref_proxy)
-   [<span data-ttu-id="2869d-115">**IUnknown \_ QueryInterface \_ Proxy**</span><span class="sxs-lookup"><span data-stu-id="2869d-115">**IUnknown\_QueryInterface\_Proxy**</span></span>](/windows/desktop/api/unknwnbase/nf-unknwnbase-iunknown_queryinterface_proxy)
-   [<span data-ttu-id="2869d-116">**IUnknown \_ 發行 \_ Proxy**</span><span class="sxs-lookup"><span data-stu-id="2869d-116">**IUnknown\_Release\_Proxy**</span></span>](/windows/desktop/api/unknwnbase/nf-unknwnbase-iunknown_queryinterface_proxy)
-   [<span data-ttu-id="2869d-117">**NdrAsyncClientCall**</span><span class="sxs-lookup"><span data-stu-id="2869d-117">**NdrAsyncClientCall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrasyncclientcall)
-   [<span data-ttu-id="2869d-118">**NdrClearOutParameters**</span><span class="sxs-lookup"><span data-stu-id="2869d-118">**NdrClearOutParameters**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrclearoutparameters)
-   [<span data-ttu-id="2869d-119">**NdrClientCall**</span><span class="sxs-lookup"><span data-stu-id="2869d-119">**NdrClientCall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrclientcall)
-   [<span data-ttu-id="2869d-120">**NdrClientCall2**</span><span class="sxs-lookup"><span data-stu-id="2869d-120">**NdrClientCall2**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrclientcall2)
-   [<span data-ttu-id="2869d-121">**NdrConformantArrayUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="2869d-121">**NdrConformantArrayUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantarrayunmarshall)
-   [<span data-ttu-id="2869d-122">**NdrConformantStringBufferSize**</span><span class="sxs-lookup"><span data-stu-id="2869d-122">**NdrConformantStringBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantstringbuffersize)
-   [<span data-ttu-id="2869d-123">**NdrConformantStringMarshall**</span><span class="sxs-lookup"><span data-stu-id="2869d-123">**NdrConformantStringMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantstringmarshall)
-   [<span data-ttu-id="2869d-124">**NdrConformantStringUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="2869d-124">**NdrConformantStringUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantstringunmarshall)
-   [<span data-ttu-id="2869d-125">**NdrCoNtextHandleInitialize**</span><span class="sxs-lookup"><span data-stu-id="2869d-125">**NdrContextHandleInitialize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcontexthandleinitialize)
-   [<span data-ttu-id="2869d-126">**NdrCoNtextHandleSize**</span><span class="sxs-lookup"><span data-stu-id="2869d-126">**NdrContextHandleSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcontexthandlesize)
-   [<span data-ttu-id="2869d-127">**NdrCoNtextHandleMemorySize**</span><span class="sxs-lookup"><span data-stu-id="2869d-127">**NdrContextHandleMemorySize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcontexthandlememorysize)
-   [<span data-ttu-id="2869d-128">**NdrConvert**</span><span class="sxs-lookup"><span data-stu-id="2869d-128">**NdrConvert**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconvert)
-   <span data-ttu-id="2869d-129">[**NdrCStdStubBuffer \_ 版本**](/previous-versions/aa374242(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="2869d-129">[**NdrCStdStubBuffer\_Release**](/previous-versions/aa374242(v=vs.80))</span></span>
-   <span data-ttu-id="2869d-130">[**NdrCStdStubBuffer2 \_ 版本**](/previous-versions/aa374240(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="2869d-130">[**NdrCStdStubBuffer2\_Release**](/previous-versions/aa374240(v=vs.80))</span></span>
-   [<span data-ttu-id="2869d-131">**NdrDllCanUnloadNow**</span><span class="sxs-lookup"><span data-stu-id="2869d-131">**NdrDllCanUnloadNow**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllcanunloadnow)
-   [<span data-ttu-id="2869d-132">**NdrDllGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="2869d-132">**NdrDllGetClassObject**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllgetclassobject)
-   [<span data-ttu-id="2869d-133">**NdrDllRegisterProxy**</span><span class="sxs-lookup"><span data-stu-id="2869d-133">**NdrDllRegisterProxy**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllregisterproxy)
-   [<span data-ttu-id="2869d-134">**NdrDllUnregisterProxy**</span><span class="sxs-lookup"><span data-stu-id="2869d-134">**NdrDllUnregisterProxy**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllunregisterproxy)
-   [<span data-ttu-id="2869d-135">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="2869d-135">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
-   [<span data-ttu-id="2869d-136">**NdrInterfacePointerBufferSize**</span><span class="sxs-lookup"><span data-stu-id="2869d-136">**NdrInterfacePointerBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointerbuffersize)
-   [<span data-ttu-id="2869d-137">**NdrInterfacePointerFree**</span><span class="sxs-lookup"><span data-stu-id="2869d-137">**NdrInterfacePointerFree**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointerfree)
-   [<span data-ttu-id="2869d-138">**NdrInterfacePointerMarshall**</span><span class="sxs-lookup"><span data-stu-id="2869d-138">**NdrInterfacePointerMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointermarshall)
-   [<span data-ttu-id="2869d-139">**NdrInterfacePointerUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="2869d-139">**NdrInterfacePointerUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointerunmarshall)
-   [<span data-ttu-id="2869d-140">**NdrOleAllocate**</span><span class="sxs-lookup"><span data-stu-id="2869d-140">**NdrOleAllocate**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndroleallocate)
-   [<span data-ttu-id="2869d-141">**NdrOleFree**</span><span class="sxs-lookup"><span data-stu-id="2869d-141">**NdrOleFree**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrolefree)
-   [<span data-ttu-id="2869d-142">**NdrPointerBufferSize**</span><span class="sxs-lookup"><span data-stu-id="2869d-142">**NdrPointerBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointerbuffersize)
-   [<span data-ttu-id="2869d-143">**NdrPointerFree**</span><span class="sxs-lookup"><span data-stu-id="2869d-143">**NdrPointerFree**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointerfree)
-   [<span data-ttu-id="2869d-144">**NdrPointerMarshall**</span><span class="sxs-lookup"><span data-stu-id="2869d-144">**NdrPointerMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointermarshall)
-   [<span data-ttu-id="2869d-145">**NdrPointerUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="2869d-145">**NdrPointerUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointerunmarshall)
-   [<span data-ttu-id="2869d-146">**NdrProxyErrorHandler**</span><span class="sxs-lookup"><span data-stu-id="2869d-146">**NdrProxyErrorHandler**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxyerrorhandler)
-   [<span data-ttu-id="2869d-147">**NdrProxyFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="2869d-147">**NdrProxyFreeBuffer**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxyfreebuffer)
-   [<span data-ttu-id="2869d-148">**NdrProxyGetBuffer**</span><span class="sxs-lookup"><span data-stu-id="2869d-148">**NdrProxyGetBuffer**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxygetbuffer)
-   [<span data-ttu-id="2869d-149">**NdrProxyInitialize**</span><span class="sxs-lookup"><span data-stu-id="2869d-149">**NdrProxyInitialize**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxyinitialize)
-   [<span data-ttu-id="2869d-150">**NdrProxySendReceive**</span><span class="sxs-lookup"><span data-stu-id="2869d-150">**NdrProxySendReceive**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxysendreceive)
-   [<span data-ttu-id="2869d-151">**NdrSimpleTypeMarshall**</span><span class="sxs-lookup"><span data-stu-id="2869d-151">**NdrSimpleTypeMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimpletypemarshall)
-   [<span data-ttu-id="2869d-152">**NdrSimpleTypeUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="2869d-152">**NdrSimpleTypeUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimpletypeunmarshall)
-   [<span data-ttu-id="2869d-153">**NdrStubCall2**</span><span class="sxs-lookup"><span data-stu-id="2869d-153">**NdrStubCall2**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrstubcall2)
-   [<span data-ttu-id="2869d-154">**NdrStubForwardingFunction**</span><span class="sxs-lookup"><span data-stu-id="2869d-154">**NdrStubForwardingFunction**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrstubforwardingfunction)
-   [<span data-ttu-id="2869d-155">**NdrStubGetBuffer**</span><span class="sxs-lookup"><span data-stu-id="2869d-155">**NdrStubGetBuffer**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrstubgetbuffer)
-   [<span data-ttu-id="2869d-156">**NdrStubInitialize**</span><span class="sxs-lookup"><span data-stu-id="2869d-156">**NdrStubInitialize**</span></span>](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrstubinitialize)
-   [<span data-ttu-id="2869d-157">**NdrUserMarshalBufferSize**</span><span class="sxs-lookup"><span data-stu-id="2869d-157">**NdrUserMarshalBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalbuffersize)
-   [<span data-ttu-id="2869d-158">**NdrUserMarshalFree**</span><span class="sxs-lookup"><span data-stu-id="2869d-158">**NdrUserMarshalFree**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalfree)
-   [<span data-ttu-id="2869d-159">**NdrUserMarshalMarshall**</span><span class="sxs-lookup"><span data-stu-id="2869d-159">**NdrUserMarshalMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalmarshall)
-   [<span data-ttu-id="2869d-160">**MIDL \_ 存根 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="2869d-160">**MIDL\_STUB\_DESC**</span></span>](/windows/desktop/api/Rpcndr/ns-rpcndr-midl_stub_desc)
-   [<span data-ttu-id="2869d-161">**MIDL \_ 存根 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="2869d-161">**MIDL\_STUB\_MESSAGE**</span></span>](/windows/desktop/api/Rpcndr/ns-rpcndr-midl_stub_message)
-   [<span data-ttu-id="2869d-162">**ProxyFileInfo**</span><span class="sxs-lookup"><span data-stu-id="2869d-162">**ProxyFileInfo**</span></span>](/windows/win32/api/rpcproxy/ns-rpcproxy-proxyfileinfo)
-   [<span data-ttu-id="2869d-163">**RPC \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="2869d-163">**RPC\_MESSAGE**</span></span>](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message)

 

 