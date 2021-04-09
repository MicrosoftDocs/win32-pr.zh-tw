---
title: 'TDM_CLICK_RADIO_BUTTON 訊息 (Commctrl .h) '
description: 模擬選項按鈕在工作對話方塊中按一下的動作。
ms.assetid: ad1616fc-f64d-4575-8bd1-7ce63185d725
keywords:
- TDM_CLICK_RADIO_BUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_CLICK_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76d465b1b937359a3d312a401914d497f9c9b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935007"
---
# <a name="tdm_click_radio_button-message"></a><span data-ttu-id="a6649-104">TDM \_ 按一下 \_ 單選 \_ 按鈕訊息</span><span class="sxs-lookup"><span data-stu-id="a6649-104">TDM\_CLICK\_RADIO\_BUTTON message</span></span>

<span data-ttu-id="a6649-105">模擬選項按鈕在工作對話方塊中按一下的動作。</span><span class="sxs-lookup"><span data-stu-id="a6649-105">Simulates the action of a radio button click in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="a6649-106">參數</span><span class="sxs-lookup"><span data-stu-id="a6649-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6649-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6649-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6649-108">**Int** 值，指定要按一下之選項按鈕的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6649-108">An **int** value that specifies the ID of the radio button to be clicked.</span></span>

</dd> <dt>

<span data-ttu-id="a6649-109">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6649-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6649-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a6649-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6649-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a6649-111">Return value</span></span>

<span data-ttu-id="a6649-112">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="a6649-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6649-113">備註</span><span class="sxs-lookup"><span data-stu-id="a6649-113">Remarks</span></span>

<span data-ttu-id="a6649-114">指定的選項按鈕識別碼會傳送至 [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) 回呼函式，做為 [TDN \_ 單選 \_ 按鈕 \_](tdn-radio-button-clicked.md) 的按下通知程式碼的一部分。</span><span class="sxs-lookup"><span data-stu-id="a6649-114">The specified radio button ID is sent to the [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) callback function as part of a [TDN\_RADIO\_BUTTON\_CLICKED](tdn-radio-button-clicked.md) notification code.</span></span> <span data-ttu-id="a6649-115">回呼函數傳回之後，將會選取選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="a6649-115">After the callback function returns, the radio button will be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6649-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6649-116">Requirements</span></span>



| <span data-ttu-id="a6649-117">需求</span><span class="sxs-lookup"><span data-stu-id="a6649-117">Requirement</span></span> | <span data-ttu-id="a6649-118">值</span><span class="sxs-lookup"><span data-stu-id="a6649-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6649-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6649-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a6649-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6649-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6649-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6649-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a6649-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6649-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6649-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a6649-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6649-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a6649-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

