---
title: 'TDM_CLICK_VERIFICATION 訊息 (Commctrl .h) '
description: 模擬工作對話方塊的 [驗證] 核取方塊（如果有的話）。
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- TDM_CLICK_VERIFICATION message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_CLICK_VERIFICATION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df61676104169e3084e7cde09439c218f2237e60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093800"
---
# <a name="tdm_click_verification-message"></a><span data-ttu-id="5b4d6-104">TDM \_ CLICK \_ 驗證訊息</span><span class="sxs-lookup"><span data-stu-id="5b4d6-104">TDM\_CLICK\_VERIFICATION message</span></span>

<span data-ttu-id="5b4d6-105">模擬工作對話方塊的 [驗證] 核取方塊（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="5b4d6-105">Simulates a click of the verification checkbox of a task dialog, if it exists.</span></span>

## <a name="parameters"></a><span data-ttu-id="5b4d6-106">參數</span><span class="sxs-lookup"><span data-stu-id="5b4d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b4d6-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b4d6-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b4d6-108">**TRUE** 表示設定要檢查之核取方塊的狀態。 **FALSE** 表示將它設定為未核取。</span><span class="sxs-lookup"><span data-stu-id="5b4d6-108">**TRUE** to set the state of the checkbox to be checked; **FALSE** to set it to be unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="5b4d6-109">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b4d6-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b4d6-110">**TRUE** 表示將鍵盤焦點設定為核取方塊;否則 **為 FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="5b4d6-110">**TRUE** to set the keyboard focus to the checkbox; **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b4d6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b4d6-111">Return value</span></span>

<span data-ttu-id="5b4d6-112">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="5b4d6-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b4d6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b4d6-113">Requirements</span></span>



| <span data-ttu-id="5b4d6-114">需求</span><span class="sxs-lookup"><span data-stu-id="5b4d6-114">Requirement</span></span> | <span data-ttu-id="5b4d6-115">值</span><span class="sxs-lookup"><span data-stu-id="5b4d6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b4d6-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b4d6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5b4d6-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b4d6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b4d6-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b4d6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5b4d6-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b4d6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b4d6-120">標頭</span><span class="sxs-lookup"><span data-stu-id="5b4d6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b4d6-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5b4d6-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





