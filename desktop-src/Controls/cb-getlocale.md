---
title: 'CB_GETLOCALE 訊息 (Winuser .h) '
description: 取得下拉式方塊的目前地區設定。 地區設定是用來判斷下拉式方塊中顯示的文字， \_ 以及使用 CB ADDSTRING 訊息加入之 CBS 排序樣式和文字的正確排序次序 \_ 。
ms.assetid: 57c77ce2-bad0-43f3-8325-f2a7227994ec
keywords:
- CB_GETLOCALE message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847d9f73e8bf0b1d533d0b79ba86d939bee0e9b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025087"
---
# <a name="cb_getlocale-message"></a><span data-ttu-id="74dc3-105">CB \_ GETLOCALE 訊息</span><span class="sxs-lookup"><span data-stu-id="74dc3-105">CB\_GETLOCALE message</span></span>

<span data-ttu-id="74dc3-106">取得下拉式方塊的目前地區設定。</span><span class="sxs-lookup"><span data-stu-id="74dc3-106">Gets the current locale of the combo box.</span></span> <span data-ttu-id="74dc3-107">地區設定是用來判斷下拉式方塊中顯示的文字，以及使用 [**CB \_ ADDSTRING**](cb-addstring.md)訊息加入之 [**CBS \_ 排序**](combo-box-styles.md)樣式和文字的正確排序次序。</span><span class="sxs-lookup"><span data-stu-id="74dc3-107">The locale is used to determine the correct sorting order of displayed text for combo boxes with the [**CBS\_SORT**](combo-box-styles.md) style and text added by using the [**CB\_ADDSTRING**](cb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="74dc3-108">參數</span><span class="sxs-lookup"><span data-stu-id="74dc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74dc3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74dc3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74dc3-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="74dc3-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="74dc3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74dc3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74dc3-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="74dc3-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74dc3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="74dc3-113">Return value</span></span>

<span data-ttu-id="74dc3-114">傳回值會指定下拉式方塊的目前地區設定。</span><span class="sxs-lookup"><span data-stu-id="74dc3-114">The return value specifies the current locale of the combo box.</span></span> <span data-ttu-id="74dc3-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))包含國家/地區代碼，而 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含語言識別項。</span><span class="sxs-lookup"><span data-stu-id="74dc3-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the country/region code and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the language identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="74dc3-116">備註</span><span class="sxs-lookup"><span data-stu-id="74dc3-116">Remarks</span></span>

<span data-ttu-id="74dc3-117">語言識別項是由多語系識別碼和主要語言識別項所組成。</span><span class="sxs-lookup"><span data-stu-id="74dc3-117">The language identifier is made up of a sublanguage identifier and a primary language identifier.</span></span> <span data-ttu-id="74dc3-118">[**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid)宏會取得主要語言識別項，而 [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid)宏會取得子語言識別項。</span><span class="sxs-lookup"><span data-stu-id="74dc3-118">The [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) macro obtains the primary language identifier and the [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) macro obtains the sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="74dc3-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="74dc3-119">Requirements</span></span>



| <span data-ttu-id="74dc3-120">需求</span><span class="sxs-lookup"><span data-stu-id="74dc3-120">Requirement</span></span> | <span data-ttu-id="74dc3-121">值</span><span class="sxs-lookup"><span data-stu-id="74dc3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74dc3-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74dc3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="74dc3-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74dc3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="74dc3-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74dc3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="74dc3-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74dc3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="74dc3-126">標頭</span><span class="sxs-lookup"><span data-stu-id="74dc3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="74dc3-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="74dc3-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74dc3-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74dc3-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="74dc3-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="74dc3-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="74dc3-130">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="74dc3-130">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="74dc3-131">**CB \_ SETLOCALE**</span><span class="sxs-lookup"><span data-stu-id="74dc3-131">**CB\_SETLOCALE**</span></span>](cb-setlocale.md)
</dt> <dt>

<span data-ttu-id="74dc3-132">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="74dc3-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="74dc3-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="74dc3-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="74dc3-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="74dc3-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="74dc3-135">**PRIMARYLANGID**</span><span class="sxs-lookup"><span data-stu-id="74dc3-135">**PRIMARYLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[<span data-ttu-id="74dc3-136">**SUBLANGID**</span><span class="sxs-lookup"><span data-stu-id="74dc3-136">**SUBLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

