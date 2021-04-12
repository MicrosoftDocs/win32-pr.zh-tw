---
title: 'LVM_SORTGROUPS 訊息 (Commctrl .h) '
description: 使用應用程式定義的比較函式，在清單視圖控制項內依識別碼排序群組。
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- LVM_SORTGROUPS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SORTGROUPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c70fd0f343c9efe0215c87f430e5ed1c89a3aed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105461"
---
# <a name="lvm_sortgroups-message"></a><span data-ttu-id="dbc7d-104">LVM \_ SORTGROUPS 訊息</span><span class="sxs-lookup"><span data-stu-id="dbc7d-104">LVM\_SORTGROUPS message</span></span>

<span data-ttu-id="dbc7d-105">使用應用程式定義的比較函式，在清單視圖控制項內依識別碼排序群組。</span><span class="sxs-lookup"><span data-stu-id="dbc7d-105">Uses an application-defined comparison function to sort groups by ID within a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dbc7d-106">參數</span><span class="sxs-lookup"><span data-stu-id="dbc7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbc7d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dbc7d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dbc7d-108">應用程式定義的比較函式 <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>的指標。</span><span class="sxs-lookup"><span data-stu-id="dbc7d-108">Pointer to an application-defined comparison function, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>.</span></span></dd> <dt>

<span data-ttu-id="dbc7d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dbc7d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dbc7d-110">應用程式定義資訊的 Void 指標。</span><span class="sxs-lookup"><span data-stu-id="dbc7d-110">Void pointer to the application-defined information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbc7d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="dbc7d-111">Return value</span></span>

<span data-ttu-id="dbc7d-112">如果成功，則傳回1，否則傳回0。</span><span class="sxs-lookup"><span data-stu-id="dbc7d-112">Returns 1 if successful, or 0 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbc7d-113">備註</span><span class="sxs-lookup"><span data-stu-id="dbc7d-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dbc7d-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="dbc7d-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="dbc7d-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="dbc7d-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dbc7d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbc7d-116">Requirements</span></span>



| <span data-ttu-id="dbc7d-117">需求</span><span class="sxs-lookup"><span data-stu-id="dbc7d-117">Requirement</span></span> | <span data-ttu-id="dbc7d-118">值</span><span class="sxs-lookup"><span data-stu-id="dbc7d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc7d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dbc7d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dbc7d-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbc7d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dbc7d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dbc7d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dbc7d-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbc7d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dbc7d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="dbc7d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbc7d-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="dbc7d-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbc7d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbc7d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc7d-126">**LVGroupCompare**</span><span class="sxs-lookup"><span data-stu-id="dbc7d-126">**LVGroupCompare**</span></span>](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>

