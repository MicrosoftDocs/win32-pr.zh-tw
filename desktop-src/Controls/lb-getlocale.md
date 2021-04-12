---
title: 'LB_GETLOCALE 訊息 (Winuser .h) '
description: 取得清單方塊的目前地區設定。 您可以使用地區設定來決定所顯示文字的正確排序次序 (針對具有磅 \_ 排序樣式) 的清單方塊，以及 LB ADDSTRING 訊息所加入的文字 \_ 。
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- LB_GETLOCALE message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57620b62011dba234710caf1b5d1c429da37ace9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465689"
---
# <a name="lb_getlocale-message"></a><span data-ttu-id="31997-105">LB \_ GETLOCALE 訊息</span><span class="sxs-lookup"><span data-stu-id="31997-105">LB\_GETLOCALE message</span></span>

<span data-ttu-id="31997-106">取得清單方塊的目前地區設定。</span><span class="sxs-lookup"><span data-stu-id="31997-106">Gets the current locale of the list box.</span></span> <span data-ttu-id="31997-107">您可以使用地區設定來決定所顯示文字的正確排序次序 (針對具有 [**磅 \_ 排序**](list-box-styles.md) 樣式) 的清單方塊，以及 [**LB \_ ADDSTRING**](lb-addstring.md) 訊息所加入的文字。</span><span class="sxs-lookup"><span data-stu-id="31997-107">You can use the locale to determine the correct sorting order of displayed text (for list boxes with the [**LBS\_SORT**](list-box-styles.md) style) and of text added by the [**LB\_ADDSTRING**](lb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="31997-108">參數</span><span class="sxs-lookup"><span data-stu-id="31997-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31997-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31997-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31997-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="31997-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="31997-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31997-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31997-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="31997-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31997-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="31997-113">Return value</span></span>

<span data-ttu-id="31997-114">傳回值會指定清單方塊的目前地區設定。</span><span class="sxs-lookup"><span data-stu-id="31997-114">The return value specifies the current locale of the list box.</span></span> <span data-ttu-id="31997-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))包含國家/地區代碼，而 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含語言識別項。</span><span class="sxs-lookup"><span data-stu-id="31997-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the country/region code and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the language identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="31997-116">備註</span><span class="sxs-lookup"><span data-stu-id="31997-116">Remarks</span></span>

<span data-ttu-id="31997-117">語言識別項包含子語言識別項和主要語言識別項。</span><span class="sxs-lookup"><span data-stu-id="31997-117">The language identifier consists of a sublanguage identifier and a primary language identifier.</span></span> <span data-ttu-id="31997-118">使用 [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) 宏將主要語言識別項從傳回值的 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 中解壓縮，並使用 [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) 宏來解壓縮語言識別項。</span><span class="sxs-lookup"><span data-stu-id="31997-118">Use the [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) macro to extract the primary language identifier from the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the return value, and the [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) macro to extract the sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="31997-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="31997-119">Requirements</span></span>



| <span data-ttu-id="31997-120">需求</span><span class="sxs-lookup"><span data-stu-id="31997-120">Requirement</span></span> | <span data-ttu-id="31997-121">值</span><span class="sxs-lookup"><span data-stu-id="31997-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31997-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31997-122">Minimum supported client</span></span><br/> | <span data-ttu-id="31997-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31997-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="31997-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31997-124">Minimum supported server</span></span><br/> | <span data-ttu-id="31997-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31997-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="31997-126">標頭</span><span class="sxs-lookup"><span data-stu-id="31997-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="31997-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="31997-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31997-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31997-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="31997-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="31997-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="31997-130">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="31997-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="31997-131">**LB \_ SETLOCALE**</span><span class="sxs-lookup"><span data-stu-id="31997-131">**LB\_SETLOCALE**</span></span>](lb-setlocale.md)
</dt> <dt>

<span data-ttu-id="31997-132">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="31997-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="31997-133">**PRIMARYLANGID**</span><span class="sxs-lookup"><span data-stu-id="31997-133">**PRIMARYLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[<span data-ttu-id="31997-134">**SUBLANGID**</span><span class="sxs-lookup"><span data-stu-id="31997-134">**SUBLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

