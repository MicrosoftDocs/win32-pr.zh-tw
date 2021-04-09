---
title: 'PSM_SETTITLE 訊息 (Prsht.idl .h) '
description: 設定屬性工作表的標題。 您可以使用 PropSheet SetTitle 宏明確地傳送此訊息 \_ 。
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- PSM_SETTITLE message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SETTITLE
- PSM_SETTITLEA
- PSM_SETTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a848a5bdaeaae64b6f1825740d1e8ade07a5a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933955"
---
# <a name="psm_settitle-message"></a><span data-ttu-id="4cc54-105">PSM \_ SETTITLE 訊息</span><span class="sxs-lookup"><span data-stu-id="4cc54-105">PSM\_SETTITLE message</span></span>

<span data-ttu-id="4cc54-106">設定屬性工作表的標題。</span><span class="sxs-lookup"><span data-stu-id="4cc54-106">Sets the title of a property sheet.</span></span> <span data-ttu-id="4cc54-107">您可以使用 [**PropSheet \_ SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="4cc54-107">You can send this message explicitly or by using the [**PropSheet\_SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4cc54-108">參數</span><span class="sxs-lookup"><span data-stu-id="4cc54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cc54-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4cc54-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cc54-110">旗標，指出是否要包含前置詞 "Properties" 或後置詞 "Properties" (視具有指定之標題字串的版本) 而定。</span><span class="sxs-lookup"><span data-stu-id="4cc54-110">Flag that indicates whether to include the prefix "Properties for" or the suffix "Properties" (depending on the version) with the specified title string.</span></span> <span data-ttu-id="4cc54-111">如果此值為 PSH \_ PROPTITLE，則會包含前置詞或尾碼。</span><span class="sxs-lookup"><span data-stu-id="4cc54-111">If this value is PSH\_PROPTITLE, the prefix or suffix is included.</span></span>

</dd> <dt>

<span data-ttu-id="4cc54-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4cc54-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cc54-113">包含標題字串的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="4cc54-113">Pointer to a buffer that contains the title string.</span></span> <span data-ttu-id="4cc54-114">如果此參數的 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 為 **Null**，則屬性工作表會載入 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))中指定的字串資源。</span><span class="sxs-lookup"><span data-stu-id="4cc54-114">If the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of this parameter is **NULL**, the property sheet loads the string resource specified in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cc54-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4cc54-115">Return value</span></span>

<span data-ttu-id="4cc54-116">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="4cc54-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cc54-117">備註</span><span class="sxs-lookup"><span data-stu-id="4cc54-117">Remarks</span></span>

<span data-ttu-id="4cc54-118">在 Aero Wizard 中，此訊息可以用來動態變更內部頁面的標題;例如，在處理 [PSN \_ advanced.field.setactive](psn-setactive.md) 通知時。</span><span class="sxs-lookup"><span data-stu-id="4cc54-118">In an Aero Wizard, this message can be used to change the title of an interior page dynamically; for example, when handling the [PSN\_SETACTIVE](psn-setactive.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cc54-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4cc54-119">Requirements</span></span>



| <span data-ttu-id="4cc54-120">需求</span><span class="sxs-lookup"><span data-stu-id="4cc54-120">Requirement</span></span> | <span data-ttu-id="4cc54-121">值</span><span class="sxs-lookup"><span data-stu-id="4cc54-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4cc54-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4cc54-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4cc54-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4cc54-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4cc54-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4cc54-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4cc54-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4cc54-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4cc54-126">標頭</span><span class="sxs-lookup"><span data-stu-id="4cc54-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cc54-127"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4cc54-127"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="4cc54-128">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="4cc54-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4cc54-129">**PSM \_SETTITLEW** (Unicode) 和 **PSM \_ SETTITLEA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="4cc54-129">**PSM\_SETTITLEW** (Unicode) and **PSM\_SETTITLEA** (ANSI)</span></span><br/>              |



 

