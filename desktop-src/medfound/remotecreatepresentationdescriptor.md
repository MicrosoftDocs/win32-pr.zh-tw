---
description: IMFMediaSource：： CreatePresentationDescriptor 方法的可遠端執行版本。
ms.assetid: 9ad6793e-32ca-471b-8639-41098b3e8216
title: 'RemoteCreatePresentationDescriptor (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c02d78c1febe8c1a82ae3e91c50e06c750bcfef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114365"
---
# <a name="remotecreatepresentationdescriptor"></a><span data-ttu-id="1d813-103">RemoteCreatePresentationDescriptor</span><span class="sxs-lookup"><span data-stu-id="1d813-103">RemoteCreatePresentationDescriptor</span></span>

<span data-ttu-id="1d813-104">[**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)方法的可遠端執行版本。</span><span class="sxs-lookup"><span data-stu-id="1d813-104">Remotable version of the [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) method.</span></span>

``` syntax
[call_as(CreatePresentationDescriptor)]
HRESULT RemoteCreatePresentationDescriptor(
    DWORD *pcbPD,
    BYTE **pbPD,
    IMFPresentationDescriptor **ppRemotePD
);
```

## <a name="remarks"></a><span data-ttu-id="1d813-105">備註</span><span class="sxs-lookup"><span data-stu-id="1d813-105">Remarks</span></span>

<span data-ttu-id="1d813-106">應用程式無法直接呼叫這個方法，而物件也不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="1d813-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="1d813-107">方法不會出現在介面的 vtable 中。</span><span class="sxs-lookup"><span data-stu-id="1d813-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="1d813-108">如果跨進程界限呼叫 [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。</span><span class="sxs-lookup"><span data-stu-id="1d813-108">If [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d813-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d813-109">Requirements</span></span>



| <span data-ttu-id="1d813-110">需求</span><span class="sxs-lookup"><span data-stu-id="1d813-110">Requirement</span></span> | <span data-ttu-id="1d813-111">值</span><span class="sxs-lookup"><span data-stu-id="1d813-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d813-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d813-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1d813-113">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d813-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="1d813-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d813-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1d813-115">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d813-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="1d813-116">標頭</span><span class="sxs-lookup"><span data-stu-id="1d813-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d813-117"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="1d813-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="1d813-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="1d813-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="1d813-119"><dt>Mfuuid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d813-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="1d813-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d813-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d813-121">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="1d813-121">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 




