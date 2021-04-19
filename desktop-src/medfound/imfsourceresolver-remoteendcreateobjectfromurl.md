---
description: IMFSourceResolver：： EndCreateObjectFromURL 方法的可遠端執行版本。
ms.assetid: 42764869-9cbc-4f41-a3af-f2d869db9f99
title: 'RemoteEndCreateObjectFromURL (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fff650dca012b58dc6fd46b26f13b1c2ac3c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971045"
---
# <a name="remoteendcreateobjectfromurl"></a><span data-ttu-id="88427-103">RemoteEndCreateObjectFromURL</span><span class="sxs-lookup"><span data-stu-id="88427-103">RemoteEndCreateObjectFromURL</span></span>

<span data-ttu-id="88427-104">[**IMFSourceResolver：： EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl)方法的可遠端執行版本。</span><span class="sxs-lookup"><span data-stu-id="88427-104">Remotable version of the [**IMFSourceResolver::EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) method.</span></span>

``` syntax
[call_as(EndCreateObjectFromURL)]
HRESULT RemoteEndCreateObjectFromURL(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a><span data-ttu-id="88427-105">備註</span><span class="sxs-lookup"><span data-stu-id="88427-105">Remarks</span></span>

<span data-ttu-id="88427-106">應用程式無法直接呼叫這個方法，而物件也不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="88427-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="88427-107">方法不會出現在介面的 vtable 中。</span><span class="sxs-lookup"><span data-stu-id="88427-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="88427-108">如果跨進程界限呼叫 [**EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。</span><span class="sxs-lookup"><span data-stu-id="88427-108">If [**EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="88427-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="88427-109">Requirements</span></span>



| <span data-ttu-id="88427-110">需求</span><span class="sxs-lookup"><span data-stu-id="88427-110">Requirement</span></span> | <span data-ttu-id="88427-111">值</span><span class="sxs-lookup"><span data-stu-id="88427-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88427-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88427-112">Minimum supported client</span></span><br/> | <span data-ttu-id="88427-113">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88427-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="88427-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88427-114">Minimum supported server</span></span><br/> | <span data-ttu-id="88427-115">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88427-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="88427-116">標頭</span><span class="sxs-lookup"><span data-stu-id="88427-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="88427-117"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="88427-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="88427-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="88427-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="88427-119"><dt>Mfuuid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="88427-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="88427-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88427-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88427-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="88427-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




