---
title: 'SB_SETTIPTEXT 訊息 (Commctrl .h) '
description: 設定狀態列中某部分的工具提示文字。 您必須使用 SBT \_ 工具提示樣式來建立狀態列，才能啟用工具提示。
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- SB_SETTIPTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- SB_SETTIPTEXT
- SB_SETTIPTEXTA
- SB_SETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d5ddb3f4fdfe18525e2b444438295f8a926180
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466228"
---
# <a name="sb_settiptext-message"></a><span data-ttu-id="da78b-105">SB \_ SETTIPTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="da78b-105">SB\_SETTIPTEXT message</span></span>

<span data-ttu-id="da78b-106">設定狀態列中某部分的工具提示文字。</span><span class="sxs-lookup"><span data-stu-id="da78b-106">Sets the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="da78b-107">您必須使用 [**SBT \_ 工具提示**](status-bar-styles.md) 樣式來建立狀態列，才能啟用工具提示。</span><span class="sxs-lookup"><span data-stu-id="da78b-107">The status bar must have been created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="da78b-108">參數</span><span class="sxs-lookup"><span data-stu-id="da78b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da78b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da78b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da78b-110">將接收工具提示文字之部分的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="da78b-110">Zero-based index of the part that will receive the tooltip text.</span></span>

</dd> <dt>

<span data-ttu-id="da78b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da78b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da78b-112">字元緩衝區的指標，其中包含新的工具提示文字。</span><span class="sxs-lookup"><span data-stu-id="da78b-112">Pointer to a character buffer that contains the new tooltip text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da78b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="da78b-113">Return value</span></span>

<span data-ttu-id="da78b-114">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="da78b-114">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="da78b-115">備註</span><span class="sxs-lookup"><span data-stu-id="da78b-115">Remarks</span></span>

<span data-ttu-id="da78b-116">在兩種情況下，會顯示此工具提示文字：</span><span class="sxs-lookup"><span data-stu-id="da78b-116">This tooltip text is displayed in two situations:</span></span>

-   <span data-ttu-id="da78b-117">當狀態列中的對應窗格只包含一個圖示時。</span><span class="sxs-lookup"><span data-stu-id="da78b-117">When the corresponding pane in the status bar contains only an icon.</span></span>
-   <span data-ttu-id="da78b-118">當狀態列中的對應窗格包含由於窗格大小而截斷的文字時。</span><span class="sxs-lookup"><span data-stu-id="da78b-118">When the corresponding pane in the status bar contains text that is truncated due to the size of the pane.</span></span>

## <a name="requirements"></a><span data-ttu-id="da78b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="da78b-119">Requirements</span></span>



| <span data-ttu-id="da78b-120">需求</span><span class="sxs-lookup"><span data-stu-id="da78b-120">Requirement</span></span> | <span data-ttu-id="da78b-121">值</span><span class="sxs-lookup"><span data-stu-id="da78b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da78b-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da78b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="da78b-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da78b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="da78b-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da78b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="da78b-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da78b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da78b-126">標頭</span><span class="sxs-lookup"><span data-stu-id="da78b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="da78b-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="da78b-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="da78b-128">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="da78b-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="da78b-129">**SB \_SETTIPTEXTW** (Unicode) 和 **SB \_ SETTIPTEXTA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="da78b-129">**SB\_SETTIPTEXTW** (Unicode) and **SB\_SETTIPTEXTA** (ANSI)</span></span><br/>               |



 

 





