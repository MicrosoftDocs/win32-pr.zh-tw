---
description: IMFWorkQueueServicesEX：： BeginRegisterPlatformWorkQueueWithMMCSSEx 的可遠端執行版本。
ms.assetid: 75af7ce6-9b74-4d61-b7f2-5d07538f91cf
title: RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d519d13f1e23927f1d34a18d5c5f860e007881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194865"
---
# <a name="remotebeginregisterplatformworkqueuewithmmcssex"></a><span data-ttu-id="3e056-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx</span><span class="sxs-lookup"><span data-stu-id="3e056-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx</span></span>

<span data-ttu-id="3e056-104">[**IMFWorkQueueServicesEX：： BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex)的可遠端執行版本。</span><span class="sxs-lookup"><span data-stu-id="3e056-104">Remotable version of [**IMFWorkQueueServicesEX::BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex).</span></span>

``` syntax
[call_as(BeginRegisterPlatformWorkQueueWithMMCSSEx)]
HRESULT RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx(
    DWORD dwPlatformWorkQueue,
    LPCWSTR wszClass,
    DWORD dwTaskId, 
    LONG lPriority,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="3e056-105">備註</span><span class="sxs-lookup"><span data-stu-id="3e056-105">Remarks</span></span>

<span data-ttu-id="3e056-106">應用程式無法直接呼叫這個方法，而物件也不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="3e056-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="3e056-107">方法不會出現在介面的 vtable 中。</span><span class="sxs-lookup"><span data-stu-id="3e056-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="3e056-108">如果跨進程界限呼叫 [**BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。</span><span class="sxs-lookup"><span data-stu-id="3e056-108">If [**BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e056-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e056-109">Requirements</span></span>



| <span data-ttu-id="3e056-110">需求</span><span class="sxs-lookup"><span data-stu-id="3e056-110">Requirement</span></span> | <span data-ttu-id="3e056-111">值</span><span class="sxs-lookup"><span data-stu-id="3e056-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3e056-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e056-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3e056-113">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e056-113">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3e056-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e056-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3e056-115">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e056-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3e056-116">標頭</span><span class="sxs-lookup"><span data-stu-id="3e056-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e056-117"><dt>Mfidl .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3e056-117"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e056-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e056-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e056-119">**IMFWorkQueueServicesEx**</span><span class="sxs-lookup"><span data-stu-id="3e056-119">**IMFWorkQueueServicesEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
</dt> </dl>

 

 




