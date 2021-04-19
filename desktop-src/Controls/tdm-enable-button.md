---
title: 'TDM_ENABLE_BUTTON 訊息 (Commctrl .h) '
description: 啟用或停用工作對話方塊中的 [推送] 按鈕。
ms.assetid: 133fe4ac-4e2d-4826-8510-c0d9f88b5b37
keywords:
- TDM_ENABLE_BUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_ENABLE_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db10d616b4d07adcdc8c97495f7d12c89e603a7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106997046"
---
# <a name="tdm_enable_button-message"></a><span data-ttu-id="c07f2-104">TDM \_ 啟用 \_ 按鈕訊息</span><span class="sxs-lookup"><span data-stu-id="c07f2-104">TDM\_ENABLE\_BUTTON message</span></span>

<span data-ttu-id="c07f2-105">啟用或停用工作對話方塊中的 [推送] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="c07f2-105">Enables or disables a push button in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="c07f2-106">參數</span><span class="sxs-lookup"><span data-stu-id="c07f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c07f2-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c07f2-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c07f2-108">**Int** 值，指定要啟用或停用之推送按鈕的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c07f2-108">An **int** value that specifies the ID of the push button to be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="c07f2-109">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c07f2-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c07f2-110">指定按鈕狀態。</span><span class="sxs-lookup"><span data-stu-id="c07f2-110">Specifies button state.</span></span> <span data-ttu-id="c07f2-111">設定為0以停用按鈕;設定為非零以啟用按鈕。</span><span class="sxs-lookup"><span data-stu-id="c07f2-111">Set to 0 to disable the button; set to nonzero to enable the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c07f2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c07f2-112">Return value</span></span>

<span data-ttu-id="c07f2-113">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="c07f2-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c07f2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c07f2-114">Requirements</span></span>



| <span data-ttu-id="c07f2-115">需求</span><span class="sxs-lookup"><span data-stu-id="c07f2-115">Requirement</span></span> | <span data-ttu-id="c07f2-116">值</span><span class="sxs-lookup"><span data-stu-id="c07f2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c07f2-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c07f2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c07f2-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c07f2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c07f2-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c07f2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c07f2-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c07f2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c07f2-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c07f2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c07f2-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c07f2-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





