---
title: 'ResourceLocator. MustUnderstandOptions 屬性 (WSManDisp .h) '
description: 取得或設定 ResourceLocator 物件的 MustUnderstandOptions 值。
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- MustUnderstandOptions 屬性 Windows 遠端管理
- MustUnderstandOptions 屬性 Windows 遠端管理，ResourceLocator 物件
- ResourceLocator 物件 Windows 遠端管理、MustUnderstandOptions 屬性
topic_type:
- apiref
api_name:
- ResourceLocator.MustUnderstandOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2945efd1a224c333f45956a29df779efc98e944f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934959"
---
# <a name="resourcelocatormustunderstandoptions-property"></a><span data-ttu-id="46471-106">ResourceLocator. MustUnderstandOptions 屬性</span><span class="sxs-lookup"><span data-stu-id="46471-106">ResourceLocator.MustUnderstandOptions property</span></span>

<span data-ttu-id="46471-107">取得或設定 [**ResourceLocator**](resourcelocator.md)物件的 **MustUnderstandOptions** 值。</span><span class="sxs-lookup"><span data-stu-id="46471-107">Gets or sets the **MustUnderstandOptions** value for the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="46471-108">您可以提供 [**ResourceLocator**](resourcelocator.md) 物件，而不是在 [**會話**](session.md) 物件作業中指定資源 URI，例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**Session。列舉**](session-enumerate.md)。</span><span class="sxs-lookup"><span data-stu-id="46471-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="46471-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="46471-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="46471-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="46471-110">Syntax</span></span>


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a><span data-ttu-id="46471-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="46471-111">Property value</span></span>

<span data-ttu-id="46471-112">指出若為 **True**，則如果執行 [WS-Management 通訊協定](ws-management-protocol.md) 的服務無法處理選項，則必須傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="46471-112">Indicates, when **True**, that the service which implements the [WS-Management Protocol](ws-management-protocol.md) must return an error if it is not capable of processing the option.</span></span>

## <a name="remarks"></a><span data-ttu-id="46471-113">備註</span><span class="sxs-lookup"><span data-stu-id="46471-113">Remarks</span></span>

<span data-ttu-id="46471-114">**IWSManResourceLocator：： MustUnderstandOptions** 是對應的 c + + 屬性。</span><span class="sxs-lookup"><span data-stu-id="46471-114">**IWSManResourceLocator::MustUnderstandOptions** is the corresponding C++ property.</span></span>

## <a name="requirements"></a><span data-ttu-id="46471-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="46471-115">Requirements</span></span>



| <span data-ttu-id="46471-116">需求</span><span class="sxs-lookup"><span data-stu-id="46471-116">Requirement</span></span> | <span data-ttu-id="46471-117">值</span><span class="sxs-lookup"><span data-stu-id="46471-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="46471-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46471-118">Minimum supported client</span></span><br/> | <span data-ttu-id="46471-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46471-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="46471-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46471-120">Minimum supported server</span></span><br/> | <span data-ttu-id="46471-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46471-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="46471-122">標頭</span><span class="sxs-lookup"><span data-stu-id="46471-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="46471-123"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="46471-123"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="46471-124">Idl</span><span class="sxs-lookup"><span data-stu-id="46471-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46471-125"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="46471-125"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="46471-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="46471-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="46471-127"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="46471-127"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="46471-128">DLL</span><span class="sxs-lookup"><span data-stu-id="46471-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46471-129"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46471-129"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="46471-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46471-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46471-131">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="46471-131">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





