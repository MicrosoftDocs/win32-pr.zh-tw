---
description: 等候指定引擎的關機 (封鎖呼叫) 。
MS-HAID: vspixengine.IServerConnectionCallback\_WaitForShutdown\_IPixEngine\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IServerConnectionCallback：： WaitForShutdown 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B70229D5-3C41-4B50-8336-A1271A9EBE81
api_name:
- IServerConnectionCallback.WaitForShutdown
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d98bd5f398748e6e62a099bcc2be94b5e5f27bc8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109737"
---
# <a name="span-idvspixengineiserverconnectioncallback_waitforshutdown_ipixengine_ptrspaniserverconnectioncallbackwaitforshutdown-method"></a><span data-ttu-id="e31a7-103"><span id="vspixengine.iserverconnectioncallback_waitforshutdown_ipixengine_ptr"></span>IServerConnectionCallback：： WaitForShutdown 方法</span><span class="sxs-lookup"><span data-stu-id="e31a7-103"><span id="vspixengine.iserverconnectioncallback_waitforshutdown_ipixengine_ptr"></span>IServerConnectionCallback::WaitForShutdown method</span></span>

<span data-ttu-id="e31a7-104">等候指定引擎的關機 (封鎖呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="e31a7-104">Wait for shutdown of the specified engine (Blocking call).</span></span>

## <a name="syntax"></a><span data-ttu-id="e31a7-105">語法</span><span class="sxs-lookup"><span data-stu-id="e31a7-105">Syntax</span></span>


```C++
HRESULT WaitForShutdown(
   IPixEngine * pEngine
);
```

## <a name="parameters"></a><span data-ttu-id="e31a7-106">參數</span><span class="sxs-lookup"><span data-stu-id="e31a7-106">Parameters</span></span>

<span data-ttu-id="e31a7-107">*pEngine* </span><span class="sxs-lookup"><span data-stu-id="e31a7-107">*pEngine* </span></span>  
<span data-ttu-id="e31a7-108">要關閉的引擎。</span><span class="sxs-lookup"><span data-stu-id="e31a7-108">The engine to shut down.</span></span>

## <a name="return-value"></a><span data-ttu-id="e31a7-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e31a7-109">Return value</span></span>

<span data-ttu-id="e31a7-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e31a7-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e31a7-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e31a7-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e31a7-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e31a7-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e31a7-113">標頭</span><span class="sxs-lookup"><span data-stu-id="e31a7-113">Header</span></span></p></td><td><span data-ttu-id="e31a7-114">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="e31a7-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e31a7-115"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="e31a7-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e31a7-116">**IServerConnectionCallback**</span><span class="sxs-lookup"><span data-stu-id="e31a7-116">**IServerConnectionCallback**</span></span>](/windows/desktop/direct3dtools/iserverconnectioncallback)

 

 
