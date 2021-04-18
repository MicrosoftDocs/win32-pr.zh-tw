---
title: 'TTM_DELTOOL 訊息 (Commctrl .h) '
description: 從工具提示控制項移除工具。
ms.assetid: 433b6f1c-3e9f-4e3a-9834-d447a3f9e6a5
keywords:
- TTM_DELTOOL message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_DELTOOL
- TTM_DELTOOLA
- TTM_DELTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943259c5496757c0f15ca4127d0a5e6a4237fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965493"
---
# <a name="ttm_deltool-message"></a><span data-ttu-id="1efdb-104">TTM \_ DELTOOL 訊息</span><span class="sxs-lookup"><span data-stu-id="1efdb-104">TTM\_DELTOOL message</span></span>

<span data-ttu-id="1efdb-105">從工具提示控制項移除工具。</span><span class="sxs-lookup"><span data-stu-id="1efdb-105">Removes a tool from a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1efdb-106">參數</span><span class="sxs-lookup"><span data-stu-id="1efdb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1efdb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1efdb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1efdb-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="1efdb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1efdb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1efdb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1efdb-110">[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1efdb-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="1efdb-111">**Hwnd** 和 **uId** 成員會識別要移除的工具，而 **cbSize** 成員必須指定結構的大小。</span><span class="sxs-lookup"><span data-stu-id="1efdb-111">The **hwnd** and **uId** members identify the tool to remove, and the **cbSize** member must specify the size of the structure.</span></span> <span data-ttu-id="1efdb-112">所有其他成員都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="1efdb-112">All other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1efdb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1efdb-113">Return value</span></span>

<span data-ttu-id="1efdb-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="1efdb-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1efdb-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1efdb-115">Requirements</span></span>



| <span data-ttu-id="1efdb-116">需求</span><span class="sxs-lookup"><span data-stu-id="1efdb-116">Requirement</span></span> | <span data-ttu-id="1efdb-117">值</span><span class="sxs-lookup"><span data-stu-id="1efdb-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1efdb-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1efdb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1efdb-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1efdb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1efdb-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1efdb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1efdb-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1efdb-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1efdb-122">標頭</span><span class="sxs-lookup"><span data-stu-id="1efdb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1efdb-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1efdb-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1efdb-124">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="1efdb-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1efdb-125">**TTM \_DELTOOLW** (Unicode) 和 **TTM \_ DELTOOLA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="1efdb-125">**TTM\_DELTOOLW** (Unicode) and **TTM\_DELTOOLA** (ANSI)</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="1efdb-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1efdb-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="1efdb-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="1efdb-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1efdb-128">**TTM \_ ADDTOOL**</span><span class="sxs-lookup"><span data-stu-id="1efdb-128">**TTM\_ADDTOOL**</span></span>](ttm-addtool.md)
</dt> <dt>

<span data-ttu-id="1efdb-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="1efdb-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1efdb-130">關於工具提示控制項</span><span class="sxs-lookup"><span data-stu-id="1efdb-130">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





