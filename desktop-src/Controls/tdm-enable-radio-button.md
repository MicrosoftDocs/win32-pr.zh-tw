---
title: 'TDM_ENABLE_RADIO_BUTTON 訊息 (Commctrl .h) '
description: 啟用或停用工作對話方塊中的選項按鈕。
ms.assetid: da605ce0-b2d5-481a-a0e1-628ae5b65726
keywords:
- TDM_ENABLE_RADIO_BUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_ENABLE_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a78445158c5edc920eb329cdfc52d44f9cb7d6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935006"
---
# <a name="tdm_enable_radio_button-message"></a><span data-ttu-id="794fa-104">TDM \_ 啟用 \_ 單選 \_ 按鈕訊息</span><span class="sxs-lookup"><span data-stu-id="794fa-104">TDM\_ENABLE\_RADIO\_BUTTON message</span></span>

<span data-ttu-id="794fa-105">啟用或停用工作對話方塊中的選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="794fa-105">Enables or disables a radio button in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="794fa-106">參數</span><span class="sxs-lookup"><span data-stu-id="794fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="794fa-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="794fa-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="794fa-108">**Int** 值，指定要啟用或停用的選項按鈕的識別碼。</span><span class="sxs-lookup"><span data-stu-id="794fa-108">An **int** value that specifies the ID of the radio button to be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="794fa-109">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="794fa-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="794fa-110">指定按鈕狀態。</span><span class="sxs-lookup"><span data-stu-id="794fa-110">Specifies button state.</span></span> <span data-ttu-id="794fa-111">設定為0以停用按鈕;設定為非零以啟用按鈕。</span><span class="sxs-lookup"><span data-stu-id="794fa-111">Set to 0 to disable the button; set to nonzero to enable the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="794fa-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="794fa-112">Return value</span></span>

<span data-ttu-id="794fa-113">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="794fa-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="794fa-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="794fa-114">Requirements</span></span>



| <span data-ttu-id="794fa-115">需求</span><span class="sxs-lookup"><span data-stu-id="794fa-115">Requirement</span></span> | <span data-ttu-id="794fa-116">值</span><span class="sxs-lookup"><span data-stu-id="794fa-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="794fa-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="794fa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="794fa-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="794fa-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="794fa-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="794fa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="794fa-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="794fa-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="794fa-121">標頭</span><span class="sxs-lookup"><span data-stu-id="794fa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="794fa-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="794fa-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





