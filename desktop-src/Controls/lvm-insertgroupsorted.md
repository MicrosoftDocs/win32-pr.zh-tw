---
title: 'LVM_INSERTGROUPSORTED 訊息 (Commctrl .h) '
description: 將群組插入排序的群組清單中。
ms.assetid: 8ad1660b-8b64-4f02-ac1b-b7edeeea38ab
keywords:
- LVM_INSERTGROUPSORTED message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_INSERTGROUPSORTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 485941f803fd5af565d8b40524a9e15968e387cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844083"
---
# <a name="lvm_insertgroupsorted-message"></a><span data-ttu-id="b85bf-104">LVM \_ INSERTGROUPSORTED 訊息</span><span class="sxs-lookup"><span data-stu-id="b85bf-104">LVM\_INSERTGROUPSORTED message</span></span>

<span data-ttu-id="b85bf-105">將群組插入排序的群組清單中。</span><span class="sxs-lookup"><span data-stu-id="b85bf-105">Inserts a group into an ordered list of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="b85bf-106">參數</span><span class="sxs-lookup"><span data-stu-id="b85bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b85bf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b85bf-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b85bf-108"><a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">LVINSERTGROUPSORTED</a>結構的指標，其中包含要插入的群組。</span><span class="sxs-lookup"><span data-stu-id="b85bf-108">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">LVINSERTGROUPSORTED</a> structure that contains the group to insert.</span></span></dd> <dt>

<span data-ttu-id="b85bf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b85bf-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b85bf-110">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b85bf-110">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b85bf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b85bf-111">Return value</span></span>

<span data-ttu-id="b85bf-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="b85bf-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="b85bf-113">備註</span><span class="sxs-lookup"><span data-stu-id="b85bf-113">Remarks</span></span>

<span data-ttu-id="b85bf-114">清單的順序是根據群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b85bf-114">The ordering of the list is based on the ID of the group.</span></span> <span data-ttu-id="b85bf-115">順序是由應用程式定義的順序函式 [**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)所定義，該函式是由 *WParam* 參數在 [**LVINSERTGROUPSORTED**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted)結構中傳遞。</span><span class="sxs-lookup"><span data-stu-id="b85bf-115">The order is defined by the application-defined ordering function, [**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare), that is passed in the [**LVINSERTGROUPSORTED**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted) structure by the *wParam* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="b85bf-116">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="b85bf-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="b85bf-117">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="b85bf-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b85bf-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b85bf-118">Requirements</span></span>



| <span data-ttu-id="b85bf-119">需求</span><span class="sxs-lookup"><span data-stu-id="b85bf-119">Requirement</span></span> | <span data-ttu-id="b85bf-120">值</span><span class="sxs-lookup"><span data-stu-id="b85bf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b85bf-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b85bf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b85bf-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b85bf-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b85bf-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b85bf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b85bf-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b85bf-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b85bf-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b85bf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b85bf-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b85bf-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b85bf-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b85bf-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="b85bf-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="b85bf-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b85bf-129">**LVGroupCompare**</span><span class="sxs-lookup"><span data-stu-id="b85bf-129">**LVGroupCompare**</span></span>](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> <dt>

[<span data-ttu-id="b85bf-130">**LVINSERTGROUPSORTED**</span><span class="sxs-lookup"><span data-stu-id="b85bf-130">**LVINSERTGROUPSORTED**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted)
</dt> </dl>

 

