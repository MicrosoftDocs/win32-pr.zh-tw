---
title: 'LVM_GETHOTCURSOR 訊息 (Commctrl .h) '
description: 在啟用熱追蹤時，抓取指標在專案上方時所使用的 HCURSOR 值。 您可以明確地傳送此訊息，或使用 ListView \_ GetHotCursor 宏。
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- LVM_GETHOTCURSOR message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd8fa4c038bf2fb1c10816319504dd9de32c0e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686284"
---
# <a name="lvm_gethotcursor-message"></a><span data-ttu-id="3330c-105">LVM \_ GETHOTCURSOR 訊息</span><span class="sxs-lookup"><span data-stu-id="3330c-105">LVM\_GETHOTCURSOR message</span></span>

<span data-ttu-id="3330c-106">在啟用熱追蹤時，抓取指標在專案上方時所使用的 HCURSOR 值。</span><span class="sxs-lookup"><span data-stu-id="3330c-106">Retrieves the HCURSOR value used when the pointer is over an item while hot tracking is enabled.</span></span> <span data-ttu-id="3330c-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) 宏。</span><span class="sxs-lookup"><span data-stu-id="3330c-107">You can send this message explicitly or use the [**ListView\_GetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3330c-108">參數</span><span class="sxs-lookup"><span data-stu-id="3330c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3330c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3330c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3330c-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3330c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3330c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3330c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3330c-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3330c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3330c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3330c-113">Return value</span></span>

<span data-ttu-id="3330c-114">傳回 HCURSOR 值，此值是當啟用熱追蹤時，清單視圖控制項所使用之游標的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3330c-114">Returns an HCURSOR value that is the handle to the cursor that the list-view control uses when hot tracking is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="3330c-115">備註</span><span class="sxs-lookup"><span data-stu-id="3330c-115">Remarks</span></span>

<span data-ttu-id="3330c-116">當設定 [**lvs) \_ EX \_ TRACKSELECT**](extended-list-view-styles.md) 樣式時，清單視圖控制項會使用熱追蹤和暫留選取專案。</span><span class="sxs-lookup"><span data-stu-id="3330c-116">A list-view control uses hot tracking and hover selection when the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) style is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="3330c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3330c-117">Requirements</span></span>



| <span data-ttu-id="3330c-118">需求</span><span class="sxs-lookup"><span data-stu-id="3330c-118">Requirement</span></span> | <span data-ttu-id="3330c-119">值</span><span class="sxs-lookup"><span data-stu-id="3330c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3330c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3330c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3330c-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3330c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3330c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3330c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3330c-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3330c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3330c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3330c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3330c-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3330c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





