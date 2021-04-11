---
title: 'ResourceLocator. ClearSelectors 方法 (WSManDisp .h) '
description: 從 ResourceLocator 物件移除所有選取器。
ms.assetid: 759880e6-5026-45de-b7e1-a4f5a16c32a0
ms.tgt_platform: multiple
keywords:
- ClearSelectors 方法 Windows 遠端管理
- ClearSelectors 方法 Windows 遠端管理，ResourceLocator 物件
- ResourceLocator 物件 Windows 遠端管理，ClearSelectors 方法
topic_type:
- apiref
api_name:
- ResourceLocator.ClearSelectors
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd5dbf1322a5e0c36a1383581e2822fbd00a00e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105629"
---
# <a name="resourcelocatorclearselectors-method"></a><span data-ttu-id="fa6bd-106">ResourceLocator. ClearSelectors 方法</span><span class="sxs-lookup"><span data-stu-id="fa6bd-106">ResourceLocator.ClearSelectors method</span></span>

<span data-ttu-id="fa6bd-107">從 [**ResourceLocator**](resourcelocator.md)物件移除所有 [*選取器*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="fa6bd-107">Removes all of the [*selectors*](windows-remote-management-glossary.md) from a [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="fa6bd-108">您可以提供 [**ResourceLocator**](resourcelocator.md) 物件，而不是在 [**會話**](session.md) 物件作業中指定資源 URI，例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**Session。列舉**](session-enumerate.md)。</span><span class="sxs-lookup"><span data-stu-id="fa6bd-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa6bd-109">語法</span><span class="sxs-lookup"><span data-stu-id="fa6bd-109">Syntax</span></span>


```VB
ResourceLocator.ClearSelectors()
```



## <a name="parameters"></a><span data-ttu-id="fa6bd-110">參數</span><span class="sxs-lookup"><span data-stu-id="fa6bd-110">Parameters</span></span>

<span data-ttu-id="fa6bd-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fa6bd-111">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa6bd-112">備註</span><span class="sxs-lookup"><span data-stu-id="fa6bd-112">Remarks</span></span>

<span data-ttu-id="fa6bd-113">**IWSManResourceLocator：： ClearSelectors** 是對應的 c + + 方法。</span><span class="sxs-lookup"><span data-stu-id="fa6bd-113">**IWSManResourceLocator::ClearSelectors** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa6bd-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa6bd-114">Requirements</span></span>



| <span data-ttu-id="fa6bd-115">需求</span><span class="sxs-lookup"><span data-stu-id="fa6bd-115">Requirement</span></span> | <span data-ttu-id="fa6bd-116">值</span><span class="sxs-lookup"><span data-stu-id="fa6bd-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa6bd-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa6bd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fa6bd-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa6bd-118">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="fa6bd-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa6bd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fa6bd-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa6bd-120">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fa6bd-121">標頭</span><span class="sxs-lookup"><span data-stu-id="fa6bd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa6bd-122"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa6bd-122"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa6bd-123">Idl</span><span class="sxs-lookup"><span data-stu-id="fa6bd-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fa6bd-124"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa6bd-124"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="fa6bd-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="fa6bd-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa6bd-126"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fa6bd-126"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fa6bd-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fa6bd-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa6bd-128"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa6bd-128"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fa6bd-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa6bd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa6bd-130">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="fa6bd-130">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





