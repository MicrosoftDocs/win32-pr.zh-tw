---
title: 'PSM_SETCURSEL 訊息 (Prsht.idl .h) '
description: 啟用屬性工作表中的指定頁面。 您可以使用 PropSheet SetCurSel 宏明確地傳送此訊息 \_ 。
ms.assetid: 800aadde-cabc-424e-8e63-60fc7ce952d7
keywords:
- PSM_SETCURSEL message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SETCURSEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f41f0ba2ec8d13a7bfc932b553b355399f76b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094419"
---
# <a name="psm_setcursel-message"></a><span data-ttu-id="0de87-105">PSM \_ SETCURSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="0de87-105">PSM\_SETCURSEL message</span></span>

<span data-ttu-id="0de87-106">啟用屬性工作表中的指定頁面。</span><span class="sxs-lookup"><span data-stu-id="0de87-106">Activates the specified page in a property sheet.</span></span> <span data-ttu-id="0de87-107">您可以使用 [**PropSheet \_ SetCurSel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="0de87-107">You can send this message explicitly or by using the [**PropSheet\_SetCurSel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0de87-108">參數</span><span class="sxs-lookup"><span data-stu-id="0de87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0de87-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0de87-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0de87-110">以零為基底的頁面索引。</span><span class="sxs-lookup"><span data-stu-id="0de87-110">The zero-based index of the page.</span></span> <span data-ttu-id="0de87-111">應用程式可以指定索引或控制碼或兩者。</span><span class="sxs-lookup"><span data-stu-id="0de87-111">An application can specify the index or the handle or both.</span></span> <span data-ttu-id="0de87-112">如果同時指定這兩者， *lParam* 會優先使用。</span><span class="sxs-lookup"><span data-stu-id="0de87-112">If both are specified, *lParam* takes precedence.</span></span>

</dd> <dt>

<span data-ttu-id="0de87-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0de87-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0de87-114">要啟用之頁面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0de87-114">The handle to the page to activate.</span></span> <span data-ttu-id="0de87-115">應用程式可以指定索引或控制碼或兩者。</span><span class="sxs-lookup"><span data-stu-id="0de87-115">An application can specify the index or the handle or both.</span></span> <span data-ttu-id="0de87-116">如果同時指定這兩者， *lParam* 會優先使用。</span><span class="sxs-lookup"><span data-stu-id="0de87-116">If both are specified, *lParam* takes precedence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0de87-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="0de87-117">Return value</span></span>

<span data-ttu-id="0de87-118">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="0de87-118">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0de87-119">備註</span><span class="sxs-lookup"><span data-stu-id="0de87-119">Remarks</span></span>

<span data-ttu-id="0de87-120">遺失啟用的視窗會收到 [PSN \_ KILLACTIVE](psn-killactive.md) 通知程式碼，而取得啟用的視窗則會接收 [PSN \_ advanced.field.setactive](psn-setactive.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="0de87-120">The window that is losing the activation receives the [PSN\_KILLACTIVE](psn-killactive.md) notification code, and the window that is gaining the activation receives the [PSN\_SETACTIVE](psn-setactive.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0de87-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="0de87-121">Requirements</span></span>



| <span data-ttu-id="0de87-122">需求</span><span class="sxs-lookup"><span data-stu-id="0de87-122">Requirement</span></span> | <span data-ttu-id="0de87-123">值</span><span class="sxs-lookup"><span data-stu-id="0de87-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0de87-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0de87-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0de87-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0de87-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0de87-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0de87-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0de87-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0de87-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0de87-128">標頭</span><span class="sxs-lookup"><span data-stu-id="0de87-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0de87-129"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0de87-129"><dt>Prsht.h</dt></span></span> </dl> |



 

 





