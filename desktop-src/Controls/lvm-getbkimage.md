---
title: 'LVM_GETBKIMAGE 訊息 (Commctrl .h) '
description: 取得清單視圖控制項中的背景影像。 您可以明確地傳送此訊息，或使用 ListView \_ GetBkImage 宏來傳送。
ms.assetid: db0e8f31-746a-4a16-b689-68da696e3657
keywords:
- LVM_GETBKIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETBKIMAGE
- LVM_GETBKIMAGEA
- LVM_GETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e178bae10b9bed880213ca4a4ab2a1b4e07239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685522"
---
# <a name="lvm_getbkimage-message"></a><span data-ttu-id="8280e-105">LVM \_ GETBKIMAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="8280e-105">LVM\_GETBKIMAGE message</span></span>

<span data-ttu-id="8280e-106">取得清單視圖控制項中的背景影像。</span><span class="sxs-lookup"><span data-stu-id="8280e-106">Gets the background image in a list-view control.</span></span> <span data-ttu-id="8280e-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="8280e-107">You can send this message explicitly or by using the [**ListView\_GetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8280e-108">參數</span><span class="sxs-lookup"><span data-stu-id="8280e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8280e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8280e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8280e-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8280e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8280e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8280e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8280e-112">[**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea)結構的指標，此結構會接收背景影像資訊。</span><span class="sxs-lookup"><span data-stu-id="8280e-112">A pointer to an [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure that will receive the background image information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8280e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8280e-113">Return value</span></span>

<span data-ttu-id="8280e-114">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="8280e-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8280e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8280e-115">Requirements</span></span>



| <span data-ttu-id="8280e-116">需求</span><span class="sxs-lookup"><span data-stu-id="8280e-116">Requirement</span></span> | <span data-ttu-id="8280e-117">值</span><span class="sxs-lookup"><span data-stu-id="8280e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8280e-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8280e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8280e-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8280e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8280e-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8280e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8280e-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8280e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8280e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="8280e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8280e-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8280e-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8280e-124">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="8280e-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8280e-125">**LVM \_GETBKIMAGEW** (Unicode) 和 **LVM \_ GETBKIMAGEA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="8280e-125">**LVM\_GETBKIMAGEW** (Unicode) and **LVM\_GETBKIMAGEA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="8280e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8280e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8280e-127">**LVM \_ SETBKIMAGE**</span><span class="sxs-lookup"><span data-stu-id="8280e-127">**LVM\_SETBKIMAGE**</span></span>](lvm-setbkimage.md)
</dt> </dl>

 

 





