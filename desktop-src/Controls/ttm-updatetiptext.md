---
title: 'TTM_UPDATETIPTEXT 訊息 (Commctrl .h) '
description: 設定工具的工具提示文字。
ms.assetid: 2a7432dd-76f9-42b4-b639-178dce1d89ef
keywords:
- TTM_UPDATETIPTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_UPDATETIPTEXT
- TTM_UPDATETIPTEXTA
- TTM_UPDATETIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c94b14ec83c190ce019ecba1413d2fa05f0103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104435"
---
# <a name="ttm_updatetiptext-message"></a><span data-ttu-id="091f9-104">TTM \_ UPDATETIPTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="091f9-104">TTM\_UPDATETIPTEXT message</span></span>

<span data-ttu-id="091f9-105">設定工具的工具提示文字。</span><span class="sxs-lookup"><span data-stu-id="091f9-105">Sets the tooltip text for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="091f9-106">參數</span><span class="sxs-lookup"><span data-stu-id="091f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="091f9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="091f9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="091f9-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="091f9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="091f9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="091f9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="091f9-110">[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="091f9-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="091f9-111">**Hinst** 和 **lpszText** 成員必須指定實例控制碼和文字的位址。</span><span class="sxs-lookup"><span data-stu-id="091f9-111">The **hinst** and **lpszText** members must specify the instance handle and the address of the text.</span></span> <span data-ttu-id="091f9-112">**Hwnd** 和 **uId** 成員會識別要更新的工具。</span><span class="sxs-lookup"><span data-stu-id="091f9-112">The **hwnd** and **uId** members identify the tool to update.</span></span> <span data-ttu-id="091f9-113">傳送此訊息之前，必須先填入此結構的 **cbSize** 成員。</span><span class="sxs-lookup"><span data-stu-id="091f9-113">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="091f9-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="091f9-114">Return value</span></span>

<span data-ttu-id="091f9-115">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="091f9-115">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="091f9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="091f9-116">Requirements</span></span>



| <span data-ttu-id="091f9-117">需求</span><span class="sxs-lookup"><span data-stu-id="091f9-117">Requirement</span></span> | <span data-ttu-id="091f9-118">值</span><span class="sxs-lookup"><span data-stu-id="091f9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="091f9-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="091f9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="091f9-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="091f9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="091f9-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="091f9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="091f9-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="091f9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="091f9-123">標頭</span><span class="sxs-lookup"><span data-stu-id="091f9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="091f9-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="091f9-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="091f9-125">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="091f9-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="091f9-126">**TTM \_UPDATETIPTEXTW** (Unicode) 和 **TTM \_ UPDATETIPTEXTA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="091f9-126">**TTM\_UPDATETIPTEXTW** (Unicode) and **TTM\_UPDATETIPTEXTA** (ANSI)</span></span><br/>       |



 

 





