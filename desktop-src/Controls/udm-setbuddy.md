---
title: 'UDM_SETBUDDY 訊息 (Commctrl .h) '
description: 設定上下按鈕控制項的合作者視窗。
ms.assetid: 66e35acc-95f6-4bc5-b654-690abf2188ba
keywords:
- UDM_SETBUDDY message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e8bd57727d730c67fe09a52c0bedf121eac982
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104765"
---
# <a name="udm_setbuddy-message"></a><span data-ttu-id="0acc6-104">UDM \_ SETBUDDY 訊息</span><span class="sxs-lookup"><span data-stu-id="0acc6-104">UDM\_SETBUDDY message</span></span>

<span data-ttu-id="0acc6-105">設定上下按鈕控制項的合作者視窗。</span><span class="sxs-lookup"><span data-stu-id="0acc6-105">Sets the buddy window for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0acc6-106">參數</span><span class="sxs-lookup"><span data-stu-id="0acc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0acc6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0acc6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0acc6-108">新好友視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0acc6-108">Handle to the new buddy window.</span></span>

</dd> <dt>

<span data-ttu-id="0acc6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0acc6-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0acc6-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0acc6-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0acc6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0acc6-111">Return value</span></span>

<span data-ttu-id="0acc6-112">傳回值是上一個好友視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0acc6-112">The return value is the handle to the previous buddy window.</span></span>

## <a name="requirements"></a><span data-ttu-id="0acc6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0acc6-113">Requirements</span></span>



| <span data-ttu-id="0acc6-114">需求</span><span class="sxs-lookup"><span data-stu-id="0acc6-114">Requirement</span></span> | <span data-ttu-id="0acc6-115">值</span><span class="sxs-lookup"><span data-stu-id="0acc6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0acc6-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0acc6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0acc6-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0acc6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0acc6-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0acc6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0acc6-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0acc6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0acc6-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0acc6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0acc6-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0acc6-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





