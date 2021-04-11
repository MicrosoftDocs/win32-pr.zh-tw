---
title: 'ResourceLocator. ClearOptions 方法 (WSManDisp .h) '
description: 從 ResourceLocator 物件移除任何選項。
ms.assetid: 1b4d7f15-c56f-4b0d-9614-8376012abca7
ms.tgt_platform: multiple
keywords:
- ClearOptions 方法 Windows 遠端管理
- ClearOptions 方法 Windows 遠端管理，ResourceLocator 物件
- ResourceLocator 物件 Windows 遠端管理，ClearOptions 方法
topic_type:
- apiref
api_name:
- ResourceLocator.ClearOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda4be766b65756a9bcf8de02a4417fd15a3e7f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843216"
---
# <a name="resourcelocatorclearoptions-method"></a><span data-ttu-id="2fcd0-106">ResourceLocator. ClearOptions 方法</span><span class="sxs-lookup"><span data-stu-id="2fcd0-106">ResourceLocator.ClearOptions method</span></span>

<span data-ttu-id="2fcd0-107">從 [**ResourceLocator**](resourcelocator.md)物件移除任何 [*選項*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="2fcd0-107">Removes any [*options*](windows-remote-management-glossary.md) from the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="2fcd0-108">您可以提供 [**ResourceLocator**](resourcelocator.md) 物件，而不是在 [**會話**](session.md) 物件作業中指定資源 URI，例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**Session。列舉**](session-enumerate.md)。</span><span class="sxs-lookup"><span data-stu-id="2fcd0-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2fcd0-109">語法</span><span class="sxs-lookup"><span data-stu-id="2fcd0-109">Syntax</span></span>


```VB
ResourceLocator.ClearOptions()
```



## <a name="parameters"></a><span data-ttu-id="2fcd0-110">參數</span><span class="sxs-lookup"><span data-stu-id="2fcd0-110">Parameters</span></span>

<span data-ttu-id="2fcd0-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2fcd0-111">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fcd0-112">備註</span><span class="sxs-lookup"><span data-stu-id="2fcd0-112">Remarks</span></span>

<span data-ttu-id="2fcd0-113">**IWSManResourceLocator：： ClearOptions** 是對應的 c + + 方法。</span><span class="sxs-lookup"><span data-stu-id="2fcd0-113">**IWSManResourceLocator::ClearOptions** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fcd0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fcd0-114">Requirements</span></span>



| <span data-ttu-id="2fcd0-115">需求</span><span class="sxs-lookup"><span data-stu-id="2fcd0-115">Requirement</span></span> | <span data-ttu-id="2fcd0-116">值</span><span class="sxs-lookup"><span data-stu-id="2fcd0-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fcd0-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2fcd0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2fcd0-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fcd0-118">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2fcd0-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2fcd0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2fcd0-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fcd0-120">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2fcd0-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2fcd0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fcd0-122"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="2fcd0-122"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2fcd0-123">Idl</span><span class="sxs-lookup"><span data-stu-id="2fcd0-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2fcd0-124"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2fcd0-124"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="2fcd0-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="2fcd0-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="2fcd0-126"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2fcd0-126"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2fcd0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2fcd0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fcd0-128"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fcd0-128"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2fcd0-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fcd0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fcd0-130">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="2fcd0-130">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





