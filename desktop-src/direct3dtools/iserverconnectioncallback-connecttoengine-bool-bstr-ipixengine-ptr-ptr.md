---
description: 連接到本機電腦上遠端引擎的另一個實例。
MS-HAID: vspixengine.IServerConnectionCallback\_ConnectToEngine\_BOOL\_BSTR\_IPixEngine\_ptr\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IServerConnectionCallback：： ConnectToEngine 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 56D67449-EA8B-4AD0-94D7-B3CDB7F0ABC8
api_name:
- IServerConnectionCallback.ConnectToEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1506075066767cba95c7fec768fa27e858bd6a10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109740"
---
# <a name="span-idvspixengineiserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptrspaniserverconnectioncallbackconnecttoengine-method"></a><span data-ttu-id="5c2a0-103"><span id="vspixengine.iserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptr"></span>IServerConnectionCallback：： ConnectToEngine 方法</span><span class="sxs-lookup"><span data-stu-id="5c2a0-103"><span id="vspixengine.iserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptr"></span>IServerConnectionCallback::ConnectToEngine method</span></span>

<span data-ttu-id="5c2a0-104">連接到本機電腦上遠端引擎的另一個實例。</span><span class="sxs-lookup"><span data-stu-id="5c2a0-104">Connect to another instance of a remote engine on the local machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c2a0-105">語法</span><span class="sxs-lookup"><span data-stu-id="5c2a0-105">Syntax</span></span>


```C++
HRESULT ConnectToEngine(
   BOOL          bLegacyConnection,
   BSTR          runAddress,
   IPixEngine ** ppEngineCreated
);
```

## <a name="parameters"></a><span data-ttu-id="5c2a0-106">參數</span><span class="sxs-lookup"><span data-stu-id="5c2a0-106">Parameters</span></span>

<span data-ttu-id="5c2a0-107">*bLegacyConnection* </span><span class="sxs-lookup"><span data-stu-id="5c2a0-107">*bLegacyConnection* </span></span>  
<span data-ttu-id="5c2a0-108">如果引擎使用的是舊版，則為 true，否則為 false。</span><span class="sxs-lookup"><span data-stu-id="5c2a0-108">true if the engine uses is legacy, otherwise false.</span></span>

<span data-ttu-id="5c2a0-109">*runAddress* </span><span class="sxs-lookup"><span data-stu-id="5c2a0-109">*runAddress* </span></span>  
<span data-ttu-id="5c2a0-110">包含本機電腦名稱稱的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="5c2a0-110">A COM string containing the name of the local machine.</span></span>

<span data-ttu-id="5c2a0-111">*ppEngineCreated* </span><span class="sxs-lookup"><span data-stu-id="5c2a0-111">*ppEngineCreated* </span></span>  
<span data-ttu-id="5c2a0-112">傳回時，為引擎實例的位址。</span><span class="sxs-lookup"><span data-stu-id="5c2a0-112">On return, the address of the engine instance.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c2a0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c2a0-113">Return value</span></span>

<span data-ttu-id="5c2a0-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5c2a0-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5c2a0-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5c2a0-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c2a0-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c2a0-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5c2a0-117">標頭</span><span class="sxs-lookup"><span data-stu-id="5c2a0-117">Header</span></span></p></td><td><span data-ttu-id="5c2a0-118">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="5c2a0-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5c2a0-119"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c2a0-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5c2a0-120">**IServerConnectionCallback**</span><span class="sxs-lookup"><span data-stu-id="5c2a0-120">**IServerConnectionCallback**</span></span>](/windows/desktop/direct3dtools/iserverconnectioncallback)

 

 
