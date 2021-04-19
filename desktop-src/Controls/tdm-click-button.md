---
title: 'TDM_CLICK_BUTTON 訊息 (Commctrl .h) '
description: 模擬按鈕在工作對話方塊中按一下的動作。
ms.assetid: cc8a8252-3418-4a28-bfb7-11d6e3fee903
keywords:
- TDM_CLICK_BUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_CLICK_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5933668eca907f36414113091b8901bfb9c110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001105"
---
# <a name="tdm_click_button-message"></a><span data-ttu-id="09e5b-104">TDM \_ CLICK \_ 按鈕訊息</span><span class="sxs-lookup"><span data-stu-id="09e5b-104">TDM\_CLICK\_BUTTON message</span></span>

<span data-ttu-id="09e5b-105">模擬按鈕在工作對話方塊中按一下的動作。</span><span class="sxs-lookup"><span data-stu-id="09e5b-105">Simulates the action of a button click in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="09e5b-106">參數</span><span class="sxs-lookup"><span data-stu-id="09e5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09e5b-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="09e5b-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09e5b-108">**整數**，指定要按一下之按鈕的識別碼。</span><span class="sxs-lookup"><span data-stu-id="09e5b-108">An **int** that specifies the ID of the button to be clicked.</span></span>

</dd> <dt>

<span data-ttu-id="09e5b-109">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="09e5b-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09e5b-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="09e5b-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09e5b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="09e5b-111">Return value</span></span>

<span data-ttu-id="09e5b-112">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="09e5b-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="09e5b-113">備註</span><span class="sxs-lookup"><span data-stu-id="09e5b-113">Remarks</span></span>

<span data-ttu-id="09e5b-114">*WParam* 所指定的按鈕識別碼會傳送至 [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)回呼函式，作為 [TDN \_ 按鈕 \_](tdn-button-clicked.md)按下通知程式碼的一部分。</span><span class="sxs-lookup"><span data-stu-id="09e5b-114">The button ID specified by *wParam* is sent to the [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) callback function as part of a [TDN\_BUTTON\_CLICKED](tdn-button-clicked.md) notification code.</span></span> <span data-ttu-id="09e5b-115">回呼函式傳回之後，如果 \_ 從回呼函數傳回 S OK，工作對話方塊就會關閉。</span><span class="sxs-lookup"><span data-stu-id="09e5b-115">After the callback function returns, the task dialog is closed if S\_OK was returned from the callback function.</span></span> <span data-ttu-id="09e5b-116">如果 \_ 從回呼函式傳回 FALSE，工作對話方塊會維持使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="09e5b-116">If S\_FALSE was returned from the callback function, the task dialog remains active.</span></span>

## <a name="requirements"></a><span data-ttu-id="09e5b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="09e5b-117">Requirements</span></span>



| <span data-ttu-id="09e5b-118">需求</span><span class="sxs-lookup"><span data-stu-id="09e5b-118">Requirement</span></span> | <span data-ttu-id="09e5b-119">值</span><span class="sxs-lookup"><span data-stu-id="09e5b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09e5b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09e5b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="09e5b-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09e5b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09e5b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09e5b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="09e5b-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09e5b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09e5b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="09e5b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="09e5b-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="09e5b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

