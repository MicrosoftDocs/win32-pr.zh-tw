---
title: 'Session.BatchItems 屬性 (WSManDisp) '
description: 設定並取得每個列舉批次中的專案數。
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- BatchItems 屬性 Windows 遠端管理
- BatchItems 屬性 Windows 遠端管理，Session 物件
- Session 物件 Windows 遠端管理，BatchItems 屬性
topic_type:
- apiref
api_name:
- Session.BatchItems
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb668b80a2fea8ec5c8683a7a85a20cfbb217a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965110"
---
# <a name="sessionbatchitems-property"></a><span data-ttu-id="54a95-106">Session.BatchItems 屬性</span><span class="sxs-lookup"><span data-stu-id="54a95-106">Session.BatchItems property</span></span>

<span data-ttu-id="54a95-107">設定並取得每個列舉批次中的專案數。</span><span class="sxs-lookup"><span data-stu-id="54a95-107">Sets and gets the number of items in each enumeration batch.</span></span> <span data-ttu-id="54a95-108">列舉期間無法變更此值。</span><span class="sxs-lookup"><span data-stu-id="54a95-108">This value cannot be changed during an enumeration.</span></span> <span data-ttu-id="54a95-109">資源提供者可能會設定限制。</span><span class="sxs-lookup"><span data-stu-id="54a95-109">The resource provider may set a limit.</span></span>

<span data-ttu-id="54a95-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="54a95-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="54a95-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="54a95-111">Syntax</span></span>


```VB
Session.BatchItems As long
```



## <a name="property-value"></a><span data-ttu-id="54a95-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="54a95-112">Property value</span></span>

<span data-ttu-id="54a95-113">指定對服務的每個基礎網路呼叫傳回的專案數目上限。</span><span class="sxs-lookup"><span data-stu-id="54a95-113">Specifies the maximum number of elements returned for each underlying network call to the service.</span></span> <span data-ttu-id="54a95-114">預設值為 20。</span><span class="sxs-lookup"><span data-stu-id="54a95-114">The default is 20.</span></span>

## <a name="remarks"></a><span data-ttu-id="54a95-115">備註</span><span class="sxs-lookup"><span data-stu-id="54a95-115">Remarks</span></span>

<span data-ttu-id="54a95-116">這是一項優化功能，可控制在用戶端與伺服器之間進行網路呼叫的頻率。</span><span class="sxs-lookup"><span data-stu-id="54a95-116">This is an optimization feature that controls how often network calls are made between the client and the server.</span></span> <span data-ttu-id="54a95-117">目前，它僅用於列舉。</span><span class="sxs-lookup"><span data-stu-id="54a95-117">Currently, it is used only for enumerations.</span></span> <span data-ttu-id="54a95-118">如需列舉資源的詳細資訊，請參閱 [**列舉**](session-enumerate.md)。</span><span class="sxs-lookup"><span data-stu-id="54a95-118">For more information about enumerating resources, see [**Enumerate**](session-enumerate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54a95-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="54a95-119">Requirements</span></span>



| <span data-ttu-id="54a95-120">需求</span><span class="sxs-lookup"><span data-stu-id="54a95-120">Requirement</span></span> | <span data-ttu-id="54a95-121">值</span><span class="sxs-lookup"><span data-stu-id="54a95-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="54a95-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54a95-122">Minimum supported client</span></span><br/> | <span data-ttu-id="54a95-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54a95-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="54a95-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54a95-124">Minimum supported server</span></span><br/> | <span data-ttu-id="54a95-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54a95-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="54a95-126">標頭</span><span class="sxs-lookup"><span data-stu-id="54a95-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="54a95-127"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="54a95-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="54a95-128">Idl</span><span class="sxs-lookup"><span data-stu-id="54a95-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="54a95-129"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="54a95-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="54a95-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="54a95-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="54a95-131"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="54a95-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="54a95-132">DLL</span><span class="sxs-lookup"><span data-stu-id="54a95-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54a95-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54a95-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="54a95-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54a95-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54a95-135">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="54a95-135">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="54a95-136">**列舉**</span><span class="sxs-lookup"><span data-stu-id="54a95-136">**Enumerate**</span></span>](session-enumerate.md)
</dt> <dt>

[<span data-ttu-id="54a95-137">**列舉值. ReadItem**</span><span class="sxs-lookup"><span data-stu-id="54a95-137">**Enumerator.ReadItem**</span></span>](enumerator-readitem.md)
</dt> </dl>

 

 





