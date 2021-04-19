---
title: 'BM_SETDONTCLICK 訊息 (Winuser .h) '
description: 設定選項按鈕上的旗標，此旗標會在 \_ 按鈕取得焦點時，控制 BN 按一下訊息的產生。
ms.assetid: 91d98bce-abea-4afc-a995-0f426ba7a518
keywords:
- BM_SETDONTCLICK message Windows 控制項
topic_type:
- apiref
api_name:
- BM_SETDONTCLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8596ec679ff07b87b3433d5b5a7805698f56f84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969959"
---
# <a name="bm_setdontclick-message"></a><span data-ttu-id="6c1f7-104">BM \_ SETDONTCLICK 訊息</span><span class="sxs-lookup"><span data-stu-id="6c1f7-104">BM\_SETDONTCLICK message</span></span>

<span data-ttu-id="6c1f7-105">設定選項按鈕上的旗標，此旗標會在按鈕取得焦點時，控制 [BN \_ 按一下](bn-clicked.md) 訊息的產生。</span><span class="sxs-lookup"><span data-stu-id="6c1f7-105">Sets a flag on a radio button that controls the generation of [BN\_CLICKED](bn-clicked.md) messages when the button receives focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c1f7-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c1f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c1f7-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c1f7-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1f7-108">指定狀態的 **布林** 值。</span><span class="sxs-lookup"><span data-stu-id="6c1f7-108">A **BOOL** that specifies the state.</span></span> <span data-ttu-id="6c1f7-109">**TRUE** 表示設定旗標，否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6c1f7-109">**TRUE** to set the flag, otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6c1f7-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c1f7-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c1f7-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="6c1f7-111">Not used.</span></span> <span data-ttu-id="6c1f7-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6c1f7-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c1f7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c1f7-113">Return value</span></span>

<span data-ttu-id="6c1f7-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="6c1f7-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c1f7-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c1f7-115">Requirements</span></span>



| <span data-ttu-id="6c1f7-116">需求</span><span class="sxs-lookup"><span data-stu-id="6c1f7-116">Requirement</span></span> | <span data-ttu-id="6c1f7-117">值</span><span class="sxs-lookup"><span data-stu-id="6c1f7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c1f7-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c1f7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6c1f7-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c1f7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6c1f7-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c1f7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6c1f7-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c1f7-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6c1f7-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6c1f7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c1f7-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6c1f7-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





