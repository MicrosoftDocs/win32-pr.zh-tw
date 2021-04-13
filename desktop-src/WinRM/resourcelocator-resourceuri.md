---
title: 'ResourceLocator 屬性 (WSManDisp .h) '
description: 取得或設定 ResourceLocator 物件中的資源 URI。
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- ResourceURI 屬性 Windows 遠端管理
- ResourceURI 屬性 Windows 遠端管理，ResourceLocator 物件
- ResourceLocator 物件 Windows 遠端管理，ResourceURI 屬性
topic_type:
- apiref
api_name:
- ResourceLocator.ResourceURI
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f804835b5445c32f74094e8280a598785d1526
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465956"
---
# <a name="resourcelocatorresourceuri-property"></a><span data-ttu-id="af408-106">ResourceLocator 屬性</span><span class="sxs-lookup"><span data-stu-id="af408-106">ResourceLocator.ResourceURI property</span></span>

<span data-ttu-id="af408-107">取得或設定 [**ResourceLocator**](resourcelocator.md)物件中的 [*資源 URI*](windows-remote-management-glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="af408-107">Gets or sets the [*resource URI*](windows-remote-management-glossary.md) in a [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="af408-108">您可以提供 [**ResourceLocator**](resourcelocator.md) 物件，而不是在 [**會話**](session.md) 物件作業中指定資源 URI，例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**Session。列舉**](session-enumerate.md)。</span><span class="sxs-lookup"><span data-stu-id="af408-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="af408-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="af408-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="af408-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="af408-110">Syntax</span></span>


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a><span data-ttu-id="af408-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="af408-111">Property value</span></span>

<span data-ttu-id="af408-112">識別資源的字串。</span><span class="sxs-lookup"><span data-stu-id="af408-112">A string that identifies the resource.</span></span> <span data-ttu-id="af408-113">設定 [**ResourceLocator**](resourcelocator.md) 物件的資源 URI 時，URI 必須只包含路徑。</span><span class="sxs-lookup"><span data-stu-id="af408-113">When setting the resource URI for a [**ResourceLocator**](resourcelocator.md) object, the URI must contain only the path.</span></span>

## <a name="remarks"></a><span data-ttu-id="af408-114">備註</span><span class="sxs-lookup"><span data-stu-id="af408-114">Remarks</span></span>

<span data-ttu-id="af408-115">以下是適用于 [**ResourceURI**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri)的適當路徑範例。</span><span class="sxs-lookup"><span data-stu-id="af408-115">The following is an example of a proper path for [**ResourceURI**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).</span></span>

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

<span data-ttu-id="af408-116">下列路徑無法運作，因為它包含特定實例的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="af408-116">The following path does not work because it contains a key for a specific instance.</span></span> <span data-ttu-id="af408-117">使用 [**ResourceLocator. AddSelector**](resourcelocator-addselector.md) 方法來指定特定的實例。</span><span class="sxs-lookup"><span data-stu-id="af408-117">Use the [**ResourceLocator.AddSelector**](resourcelocator-addselector.md) method to specify a particular instance.</span></span>

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

<span data-ttu-id="af408-118">**IWSManResourceLocator：： ResourceURI** 是對應的 c + + 方法。</span><span class="sxs-lookup"><span data-stu-id="af408-118">**IWSManResourceLocator::ResourceURI** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="af408-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="af408-119">Requirements</span></span>



| <span data-ttu-id="af408-120">需求</span><span class="sxs-lookup"><span data-stu-id="af408-120">Requirement</span></span> | <span data-ttu-id="af408-121">值</span><span class="sxs-lookup"><span data-stu-id="af408-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="af408-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af408-122">Minimum supported client</span></span><br/> | <span data-ttu-id="af408-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af408-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="af408-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af408-124">Minimum supported server</span></span><br/> | <span data-ttu-id="af408-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af408-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="af408-126">標頭</span><span class="sxs-lookup"><span data-stu-id="af408-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="af408-127"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="af408-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="af408-128">Idl</span><span class="sxs-lookup"><span data-stu-id="af408-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="af408-129"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="af408-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="af408-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="af408-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="af408-131"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="af408-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="af408-132">DLL</span><span class="sxs-lookup"><span data-stu-id="af408-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af408-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af408-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="af408-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af408-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af408-135">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="af408-135">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





