---
title: 'TB_SETROWS 訊息 (Commctrl .h) '
description: 設定工具列中的按鈕列數。
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- TB_SETROWS message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d0065a3f5f6a277713e368177886ebd064ea132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025500"
---
# <a name="tb_setrows-message"></a><span data-ttu-id="98524-104">TB \_ SETROWS 訊息</span><span class="sxs-lookup"><span data-stu-id="98524-104">TB\_SETROWS message</span></span>

<span data-ttu-id="98524-105">設定工具列中的按鈕列數。</span><span class="sxs-lookup"><span data-stu-id="98524-105">Sets the number of rows of buttons in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="98524-106">參數</span><span class="sxs-lookup"><span data-stu-id="98524-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98524-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98524-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98524-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定所要求的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="98524-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the number of rows requested.</span></span> <span data-ttu-id="98524-109">最小的資料列數目是1，而最大的資料列數目等於工具列中的按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="98524-109">The minimum number of rows is one, and the maximum number of rows is equal to the number of buttons in the toolbar.</span></span>

<span data-ttu-id="98524-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))是一個 **布林** 值，指出當系統無法建立 *wParam* 所指定的資料列數目時，是否要建立比所要求更多的資料列。</span><span class="sxs-lookup"><span data-stu-id="98524-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **BOOL** that indicates whether to create more rows than requested when the system cannot create the number of rows specified by *wParam*.</span></span> <span data-ttu-id="98524-111">若 **為 TRUE**，則系統會建立更多資料列。</span><span class="sxs-lookup"><span data-stu-id="98524-111">If **TRUE**, the system creates more rows.</span></span> <span data-ttu-id="98524-112">如果 **為 FALSE**，則系統會建立較少的資料列。</span><span class="sxs-lookup"><span data-stu-id="98524-112">If **FALSE**, the system creates fewer rows.</span></span>

</dd> <dt>

<span data-ttu-id="98524-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98524-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98524-114">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會在設定資料列之後接收工具列的周框。</span><span class="sxs-lookup"><span data-stu-id="98524-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle of the toolbar after the rows are set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98524-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="98524-115">Return value</span></span>

<span data-ttu-id="98524-116">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="98524-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98524-117">備註</span><span class="sxs-lookup"><span data-stu-id="98524-117">Remarks</span></span>

<span data-ttu-id="98524-118">因為在設定資料列數目時，系統不會分解按鈕群組，所以產生的資料列數目可能會與要求的數目不同。</span><span class="sxs-lookup"><span data-stu-id="98524-118">Because the system does not break up button groups when setting the number of rows, the resulting number of rows might differ from the number requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="98524-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="98524-119">Requirements</span></span>



| <span data-ttu-id="98524-120">需求</span><span class="sxs-lookup"><span data-stu-id="98524-120">Requirement</span></span> | <span data-ttu-id="98524-121">值</span><span class="sxs-lookup"><span data-stu-id="98524-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98524-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="98524-122">Minimum supported client</span></span><br/> | <span data-ttu-id="98524-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98524-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="98524-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="98524-124">Minimum supported server</span></span><br/> | <span data-ttu-id="98524-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98524-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="98524-126">標頭</span><span class="sxs-lookup"><span data-stu-id="98524-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="98524-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="98524-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

