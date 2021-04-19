---
description: IMFPMPHost：： CreateObjectByCLSID 方法的可遠端執行版本。
ms.assetid: be96be6d-47de-4d2b-81fc-13079de33888
title: 'RemoteCreateObjectByCLSID (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e57307ece851484675d01a699037647efad771d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974542"
---
# <a name="remotecreateobjectbyclsid"></a><span data-ttu-id="84666-103">RemoteCreateObjectByCLSID</span><span class="sxs-lookup"><span data-stu-id="84666-103">RemoteCreateObjectByCLSID</span></span>

<span data-ttu-id="84666-104">[**IMFPMPHost：： CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid)方法的可遠端執行版本。</span><span class="sxs-lookup"><span data-stu-id="84666-104">Remotable version of the [**IMFPMPHost::CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) method.</span></span>

``` syntax
[call_as(CreateObjectByCLSID)]
HRESULT RemoteCreateObjectByCLSID( 
    REFCLSID clsid,
    BYTE *pbData, 
    DWORD cbData, 
    REFIID riid,
    void **ppv
);
```

## <a name="remarks"></a><span data-ttu-id="84666-105">備註</span><span class="sxs-lookup"><span data-stu-id="84666-105">Remarks</span></span>

<span data-ttu-id="84666-106">應用程式無法直接呼叫這個方法，而物件也不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="84666-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="84666-107">方法不會出現在介面的 vtable 中。</span><span class="sxs-lookup"><span data-stu-id="84666-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="84666-108">如果跨進程界限呼叫 [**CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。</span><span class="sxs-lookup"><span data-stu-id="84666-108">If [**CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="84666-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="84666-109">Requirements</span></span>



| <span data-ttu-id="84666-110">需求</span><span class="sxs-lookup"><span data-stu-id="84666-110">Requirement</span></span> | <span data-ttu-id="84666-111">值</span><span class="sxs-lookup"><span data-stu-id="84666-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84666-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84666-112">Minimum supported client</span></span><br/> | <span data-ttu-id="84666-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84666-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="84666-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84666-114">Minimum supported server</span></span><br/> | <span data-ttu-id="84666-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84666-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="84666-116">標頭</span><span class="sxs-lookup"><span data-stu-id="84666-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="84666-117"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="84666-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="84666-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="84666-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="84666-119"><dt>Mfuuid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="84666-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="84666-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84666-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84666-121">**IMFPMPHost**</span><span class="sxs-lookup"><span data-stu-id="84666-121">**IMFPMPHost**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost)
</dt> <dt>

[<span data-ttu-id="84666-122">PMP 媒體會話</span><span class="sxs-lookup"><span data-stu-id="84666-122">PMP Media Session</span></span>](pmp-media-session.md)
</dt> <dt>

[<span data-ttu-id="84666-123">受保護的媒體路徑</span><span class="sxs-lookup"><span data-stu-id="84666-123">Protected Media Path</span></span>](protected-media-path.md)
</dt> </dl>

 

 




