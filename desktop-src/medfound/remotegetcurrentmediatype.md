---
description: IMFMediaTypeHandler：： GetCurrentMediaType 方法的可遠端執行版本。
ms.assetid: f7f69adb-2a4a-47a9-bb92-ad9d005b962f
title: 'RemoteGetCurrentMediaType (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc168198e8402d83538c046967d1d851ae2532b1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981924"
---
# <a name="remotegetcurrentmediatype"></a><span data-ttu-id="e88c9-103">RemoteGetCurrentMediaType</span><span class="sxs-lookup"><span data-stu-id="e88c9-103">RemoteGetCurrentMediaType</span></span>

<span data-ttu-id="e88c9-104">[**IMFMediaTypeHandler：： GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype)方法的可遠端執行版本。</span><span class="sxs-lookup"><span data-stu-id="e88c9-104">Remotable version of the [**IMFMediaTypeHandler::GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) method.</span></span>

``` syntax
[call_as(GetCurrentMediaType)]
HRESULT RemoteGetCurrentMediaType(
    BYTE **ppbData,
    DWORD *pcbData
);
```

## <a name="remarks"></a><span data-ttu-id="e88c9-105">備註</span><span class="sxs-lookup"><span data-stu-id="e88c9-105">Remarks</span></span>

<span data-ttu-id="e88c9-106">應用程式無法直接呼叫這個方法，而物件也不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="e88c9-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="e88c9-107">方法不會出現在介面的 vtable 中。</span><span class="sxs-lookup"><span data-stu-id="e88c9-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="e88c9-108">如果跨進程界限呼叫 [**GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。</span><span class="sxs-lookup"><span data-stu-id="e88c9-108">If [**GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

<span data-ttu-id="e88c9-109">如果已安裝 Windows Media Format 11 SDK 可轉散發元件，則可在下列平臺上使用此介面：</span><span class="sxs-lookup"><span data-stu-id="e88c9-109">This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:</span></span>

-   <span data-ttu-id="e88c9-110">Windows XP Service Pack 2 (SP2) 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="e88c9-110">Windows XP with Service Pack 2 (SP2) and later.</span></span>
-   <span data-ttu-id="e88c9-111">Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) 和 KB925766 (年10月 2006) 安裝的 Windows XP Media Center Edition 更新彙總套件。</span><span class="sxs-lookup"><span data-stu-id="e88c9-111">Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e88c9-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e88c9-112">Requirements</span></span>



| <span data-ttu-id="e88c9-113">需求</span><span class="sxs-lookup"><span data-stu-id="e88c9-113">Requirement</span></span> | <span data-ttu-id="e88c9-114">值</span><span class="sxs-lookup"><span data-stu-id="e88c9-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e88c9-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e88c9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e88c9-116">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e88c9-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="e88c9-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e88c9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e88c9-118">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e88c9-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="e88c9-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e88c9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e88c9-120"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="e88c9-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="e88c9-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="e88c9-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="e88c9-122"><dt>Mfuuid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e88c9-122"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="e88c9-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e88c9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e88c9-124">**IMFMediaTypeHandler**</span><span class="sxs-lookup"><span data-stu-id="e88c9-124">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
</dt> </dl>

 

 




