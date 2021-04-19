---
description: IMFMediaStream：： RequestSample 方法的可遠端執行版本。
ms.assetid: 05ed4de0-fe5c-4183-8f1d-55d5a27e436a
title: 'RemoteRequestSample (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c8b06f0501de9cc041bf5776adb5e17e59a8c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001687"
---
# <a name="remoterequestsample"></a><span data-ttu-id="c7d62-103">RemoteRequestSample</span><span class="sxs-lookup"><span data-stu-id="c7d62-103">RemoteRequestSample</span></span>

<span data-ttu-id="c7d62-104">[**IMFMediaStream：： RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)方法的可遠端執行版本。</span><span class="sxs-lookup"><span data-stu-id="c7d62-104">Remotable version of the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>

``` syntax
[call_as(RequestSample)]
HRESULT RemoteRequestSample();
```

## <a name="remarks"></a><span data-ttu-id="c7d62-105">備註</span><span class="sxs-lookup"><span data-stu-id="c7d62-105">Remarks</span></span>

<span data-ttu-id="c7d62-106">應用程式無法直接呼叫這個方法，而物件也不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="c7d62-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="c7d62-107">方法不會出現在介面的 vtable 中。</span><span class="sxs-lookup"><span data-stu-id="c7d62-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="c7d62-108">如果跨進程界限呼叫 [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。</span><span class="sxs-lookup"><span data-stu-id="c7d62-108">If [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7d62-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7d62-109">Requirements</span></span>



| <span data-ttu-id="c7d62-110">需求</span><span class="sxs-lookup"><span data-stu-id="c7d62-110">Requirement</span></span> | <span data-ttu-id="c7d62-111">值</span><span class="sxs-lookup"><span data-stu-id="c7d62-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d62-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7d62-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c7d62-113">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7d62-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="c7d62-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7d62-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c7d62-115">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7d62-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="c7d62-116">標頭</span><span class="sxs-lookup"><span data-stu-id="c7d62-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7d62-117"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="c7d62-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="c7d62-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="c7d62-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7d62-119"><dt>Mfuuid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7d62-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="c7d62-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7d62-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d62-121">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="c7d62-121">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)
</dt> </dl>

 

 




