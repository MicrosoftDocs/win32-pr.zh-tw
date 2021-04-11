---
title: 'PSM_SETCURSELID 訊息 (Prsht.idl .h) '
description: 根據頁面的資源識別碼，啟用屬性工作表中的指定頁面。 您可以使用 PropSheet SetCurSelByID 宏明確地傳送此訊息 \_ 。
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- PSM_SETCURSELID message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SETCURSELID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da6ec827bbf3b9bade0af649f124d25c420d299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105084"
---
# <a name="psm_setcurselid-message"></a><span data-ttu-id="ca0fa-105">PSM \_ SETCURSELID 訊息</span><span class="sxs-lookup"><span data-stu-id="ca0fa-105">PSM\_SETCURSELID message</span></span>

<span data-ttu-id="ca0fa-106">根據頁面的資源識別碼，啟用屬性工作表中的指定頁面。</span><span class="sxs-lookup"><span data-stu-id="ca0fa-106">Activates the given page in a property sheet based on the resource identifier of the page.</span></span> <span data-ttu-id="ca0fa-107">您可以使用 [**PropSheet \_ SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ca0fa-107">You can send this message explicitly or by using the [**PropSheet\_SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ca0fa-108">參數</span><span class="sxs-lookup"><span data-stu-id="ca0fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca0fa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca0fa-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca0fa-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ca0fa-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ca0fa-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca0fa-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca0fa-112">要啟動之頁面的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ca0fa-112">Resource identifier of the page to activate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca0fa-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ca0fa-113">Return value</span></span>

<span data-ttu-id="ca0fa-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ca0fa-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca0fa-115">備註</span><span class="sxs-lookup"><span data-stu-id="ca0fa-115">Remarks</span></span>

<span data-ttu-id="ca0fa-116">遺失啟用的視窗會收到 [PSN \_ KILLACTIVE](psn-killactive.md) 通知程式碼，而取得啟用的視窗則會接收 [PSN \_ advanced.field.setactive](psn-setactive.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="ca0fa-116">The window that is losing the activation receives the [PSN\_KILLACTIVE](psn-killactive.md) notification code, and the window that is gaining the activation receives the [PSN\_SETACTIVE](psn-setactive.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca0fa-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca0fa-117">Requirements</span></span>



| <span data-ttu-id="ca0fa-118">需求</span><span class="sxs-lookup"><span data-stu-id="ca0fa-118">Requirement</span></span> | <span data-ttu-id="ca0fa-119">值</span><span class="sxs-lookup"><span data-stu-id="ca0fa-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ca0fa-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ca0fa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ca0fa-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca0fa-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ca0fa-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ca0fa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ca0fa-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca0fa-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ca0fa-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ca0fa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca0fa-125"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ca0fa-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





