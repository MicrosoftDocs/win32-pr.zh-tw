---
description: IMFTopologyNode：： GetInputPrefType 方法的可遠端執行版本。
ms.assetid: b02cf739-97a9-4bb0-abb1-0da491857c50
title: 'RemoteGetInputPrefType (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6461e804d6066b467378742ff02c8e708f5f6714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691120"
---
# <a name="remotegetinputpreftype"></a><span data-ttu-id="f8060-103">RemoteGetInputPrefType</span><span class="sxs-lookup"><span data-stu-id="f8060-103">RemoteGetInputPrefType</span></span>

<span data-ttu-id="f8060-104">[**IMFTopologyNode：： GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype)方法的可遠端執行版本。</span><span class="sxs-lookup"><span data-stu-id="f8060-104">Remotable version of the [**IMFTopologyNode::GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) method.</span></span>

``` syntax
[call_as(GetInputPrefType)] 
HRESULT RemoteGetInputPrefType(
    DWORD dwInputIndex,
    DWORD *pcbData,
    BYTE **ppbData
);
```

## <a name="remarks"></a><span data-ttu-id="f8060-105">備註</span><span class="sxs-lookup"><span data-stu-id="f8060-105">Remarks</span></span>

<span data-ttu-id="f8060-106">應用程式無法直接呼叫這個方法，而物件也不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="f8060-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="f8060-107">方法不會出現在介面的 vtable 中。</span><span class="sxs-lookup"><span data-stu-id="f8060-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="f8060-108">如果跨進程界限呼叫 [**GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) ，媒體基礎 proxy/stub DLL 會將呼叫轉譯為遠端方法的呼叫，然後再將它轉譯回來。</span><span class="sxs-lookup"><span data-stu-id="f8060-108">If [**GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8060-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8060-109">Requirements</span></span>



| <span data-ttu-id="f8060-110">需求</span><span class="sxs-lookup"><span data-stu-id="f8060-110">Requirement</span></span> | <span data-ttu-id="f8060-111">值</span><span class="sxs-lookup"><span data-stu-id="f8060-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8060-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8060-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f8060-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8060-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f8060-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f8060-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f8060-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8060-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f8060-116">標頭</span><span class="sxs-lookup"><span data-stu-id="f8060-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8060-117"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="f8060-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="f8060-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="f8060-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8060-119"><dt>Mfuuid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8060-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="f8060-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8060-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8060-121">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="f8060-121">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




