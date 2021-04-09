---
title: 'ResourceLocator. FragmentPath 屬性 (WSManDisp .h) '
description: 取得或設定在會話物件作業（例如 Session. Get、Session. Put 或 Session. 列舉）中使用 ResourceLocator 時，資源片段或屬性的路徑。
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- FragmentPath 屬性 Windows 遠端管理
- FragmentPath 屬性 Windows 遠端管理，ResourceLocator 物件
- ResourceLocator 物件 Windows 遠端管理、FragmentPath 屬性
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentPath
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e15fba102f9a7c8a2581271c575857b49bc5df1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025135"
---
# <a name="resourcelocatorfragmentpath-property"></a><span data-ttu-id="b94b5-106">ResourceLocator. FragmentPath 屬性</span><span class="sxs-lookup"><span data-stu-id="b94b5-106">ResourceLocator.FragmentPath property</span></span>

<span data-ttu-id="b94b5-107">取得或設定在 [**會話**](session.md)物件作業（例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**session. 列舉**](session-enumerate.md)）中使用 [**ResourceLocator**](resourcelocator.md)時，[*資源*](windows-remote-management-glossary.md)[*片段*](windows-remote-management-glossary.md)或屬性的路徑。</span><span class="sxs-lookup"><span data-stu-id="b94b5-107">Gets or sets the path for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) or property when [**ResourceLocator**](resourcelocator.md) is used in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="b94b5-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="b94b5-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b94b5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b94b5-109">Syntax</span></span>


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a><span data-ttu-id="b94b5-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="b94b5-110">Property value</span></span>

<span data-ttu-id="b94b5-111">識別資源之片段或屬性的字串。</span><span class="sxs-lookup"><span data-stu-id="b94b5-111">String that identifies the fragment or property of the resource.</span></span> <span data-ttu-id="b94b5-112">例如，如果資源是磁片磁碟機，而要求的屬性是製造商，則字串可能包含 `Diskdrive/Manufacturer` 。</span><span class="sxs-lookup"><span data-stu-id="b94b5-112">For example, if the resource is a disk drive and the requested property is Manufacturer, the string may contain `Diskdrive/Manufacturer`.</span></span> <span data-ttu-id="b94b5-113">片段文字會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b94b5-113">The fragment text is case-sensitive.</span></span> <span data-ttu-id="b94b5-114">在此情況下，您不能使用 `diskdrive/manufacturer` 。</span><span class="sxs-lookup"><span data-stu-id="b94b5-114">In this case, you cannot use `diskdrive/manufacturer`.</span></span>

## <a name="remarks"></a><span data-ttu-id="b94b5-115">備註</span><span class="sxs-lookup"><span data-stu-id="b94b5-115">Remarks</span></span>

<span data-ttu-id="b94b5-116">**IWSManResourceLocator：： FragmentPath** 是對應的 c + + 屬性。</span><span class="sxs-lookup"><span data-stu-id="b94b5-116">**IWSManResourceLocator::FragmentPath** is the corresponding C++ property.</span></span>

<span data-ttu-id="b94b5-117">您可以藉由提供陣列索引來指定陣列屬性的一個元素，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="b94b5-117">You can specify one element of an array property by supplying the array index as shown in the following example.</span></span> <span data-ttu-id="b94b5-118">請注意，陣列索引的開頭是1，而不是0。</span><span class="sxs-lookup"><span data-stu-id="b94b5-118">Be aware that array indexing starts with 1 rather than 0.</span></span>


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



<span data-ttu-id="b94b5-119">若要取得整個陣列，請指定陣列屬性名稱，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="b94b5-119">To get the whole array, specify the array property name as shown in the following example.</span></span>


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



## <a name="requirements"></a><span data-ttu-id="b94b5-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b94b5-120">Requirements</span></span>



| <span data-ttu-id="b94b5-121">需求</span><span class="sxs-lookup"><span data-stu-id="b94b5-121">Requirement</span></span> | <span data-ttu-id="b94b5-122">值</span><span class="sxs-lookup"><span data-stu-id="b94b5-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b94b5-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b94b5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b94b5-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b94b5-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b94b5-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b94b5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b94b5-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b94b5-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b94b5-127">標頭</span><span class="sxs-lookup"><span data-stu-id="b94b5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b94b5-128"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b94b5-128"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b94b5-129">Idl</span><span class="sxs-lookup"><span data-stu-id="b94b5-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b94b5-130"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b94b5-130"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b94b5-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="b94b5-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="b94b5-132"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b94b5-132"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b94b5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b94b5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b94b5-134"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b94b5-134"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b94b5-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b94b5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b94b5-136">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="b94b5-136">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





