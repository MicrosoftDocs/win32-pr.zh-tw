---
title: 'LVM_SETBKIMAGE 訊息 (Commctrl .h) '
description: 在清單視圖控制項中設定背景影像。 您可以明確地傳送此訊息，或使用 ListView \_ SetBkImage 宏來傳送。
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- LVM_SETBKIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETBKIMAGE
- LVM_SETBKIMAGEA
- LVM_SETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e22bebdcb36faff56dfabab721731acb55fdec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465873"
---
# <a name="lvm_setbkimage-message"></a><span data-ttu-id="d1206-105">LVM \_ SETBKIMAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="d1206-105">LVM\_SETBKIMAGE message</span></span>

<span data-ttu-id="d1206-106">在清單視圖控制項中設定背景影像。</span><span class="sxs-lookup"><span data-stu-id="d1206-106">Sets the background image in a list-view control.</span></span> <span data-ttu-id="d1206-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="d1206-107">You can send this message explicitly or by using the [**ListView\_SetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1206-108">參數</span><span class="sxs-lookup"><span data-stu-id="d1206-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1206-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1206-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1206-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="d1206-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d1206-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1206-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1206-112">[**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea)結構的指標，其中包含新的背景影像資訊。</span><span class="sxs-lookup"><span data-stu-id="d1206-112">Pointer to a [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure that contains the new background image information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1206-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1206-113">Return value</span></span>

<span data-ttu-id="d1206-114">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="d1206-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="d1206-115">如果 [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea)結構的 **UlFlags** 成員是 **LVBKIF \_ 來源 \_ NONE**，則傳回零。</span><span class="sxs-lookup"><span data-stu-id="d1206-115">Returns zero if the **ulFlags** member of the [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure is **LVBKIF\_SOURCE\_NONE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1206-116">備註</span><span class="sxs-lookup"><span data-stu-id="d1206-116">Remarks</span></span>

<span data-ttu-id="d1206-117">由於清單視圖控制項會使用 OLE COM 來操作背景影像，因此呼叫端應用程式必須呼叫 [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) 或 [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) ，才能傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="d1206-117">Because the list-view control uses OLE COM to manipulate the background images, the calling application must call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) before sending this message.</span></span> <span data-ttu-id="d1206-118">最好是在應用程式初始化時呼叫其中一個函式，並在應用程式終止時呼叫 [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) 或 [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) 。</span><span class="sxs-lookup"><span data-stu-id="d1206-118">It is best to call one of these functions when the application is initialized and call either [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) or [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) when the application is terminating.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1206-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1206-119">Requirements</span></span>



| <span data-ttu-id="d1206-120">需求</span><span class="sxs-lookup"><span data-stu-id="d1206-120">Requirement</span></span> | <span data-ttu-id="d1206-121">值</span><span class="sxs-lookup"><span data-stu-id="d1206-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1206-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1206-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d1206-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1206-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1206-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1206-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d1206-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1206-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1206-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d1206-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1206-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d1206-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d1206-128">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="d1206-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d1206-129">**LVM \_SETBKIMAGEW** (Unicode) 和 **LVM \_ SETBKIMAGEA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="d1206-129">**LVM\_SETBKIMAGEW** (Unicode) and **LVM\_SETBKIMAGEA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d1206-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1206-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1206-131">**LVM \_ GETBKIMAGE**</span><span class="sxs-lookup"><span data-stu-id="d1206-131">**LVM\_GETBKIMAGE**</span></span>](lvm-getbkimage.md)
</dt> </dl>

 

