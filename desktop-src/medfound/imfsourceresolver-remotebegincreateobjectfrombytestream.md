---
description: IMFSourceResolver：： BeginCreateObjectFromByteStream 方法的可遠端執行版本。
ms.assetid: 960b5c51-b9b1-4956-a270-abfb7eedd482
title: 'RemoteBeginCreateObjectFromByteStream (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2cf089f0b80e83373c36731de4bd9a36d8835b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973688"
---
# <a name="remotebegincreateobjectfrombytestream"></a><span data-ttu-id="372c9-103">RemoteBeginCreateObjectFromByteStream</span><span class="sxs-lookup"><span data-stu-id="372c9-103">RemoteBeginCreateObjectFromByteStream</span></span>

<span data-ttu-id="372c9-104">[**IMFSourceResolver：： BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)方法的可遠端執行版本。</span><span class="sxs-lookup"><span data-stu-id="372c9-104">Remotable version of the [**IMFSourceResolver::BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) method.</span></span>

``` syntax
[call_as(BeginCreateObjectFromByteStream)]
HRESULT RemoteBeginCreateObjectFromByteStream(
    IMFByteStream* pByteStream,
    LPCWSTR pwszURL,
    IPropertyStore *pProps,
    DWORD dwFlags,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="372c9-105">備註</span><span class="sxs-lookup"><span data-stu-id="372c9-105">Remarks</span></span>

<span data-ttu-id="372c9-106">應用程式無法直接呼叫這個方法，而物件也不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="372c9-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="372c9-107">方法不會出現在介面的 vtable 中。</span><span class="sxs-lookup"><span data-stu-id="372c9-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="372c9-108">如果跨進程界限呼叫 [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。</span><span class="sxs-lookup"><span data-stu-id="372c9-108">If [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="372c9-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="372c9-109">Requirements</span></span>



| <span data-ttu-id="372c9-110">需求</span><span class="sxs-lookup"><span data-stu-id="372c9-110">Requirement</span></span> | <span data-ttu-id="372c9-111">值</span><span class="sxs-lookup"><span data-stu-id="372c9-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="372c9-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="372c9-112">Minimum supported client</span></span><br/> | <span data-ttu-id="372c9-113">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="372c9-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="372c9-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="372c9-114">Minimum supported server</span></span><br/> | <span data-ttu-id="372c9-115">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="372c9-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="372c9-116">標頭</span><span class="sxs-lookup"><span data-stu-id="372c9-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="372c9-117"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="372c9-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="372c9-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="372c9-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="372c9-119"><dt>Mfuuid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="372c9-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="372c9-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="372c9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="372c9-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="372c9-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




