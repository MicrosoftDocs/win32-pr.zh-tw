---
title: 'TDM_SET_BUTTON_ELE加值稅ION_REQUIRED_STATE 訊息 (Commctrl .h) '
description: 指定指定的工作對話方塊按鈕或命令連結是否應該有 (UAC) 盾牌圖示的使用者帳戶控制;亦即，按鈕叫用的動作是否需要提高許可權。
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- TDM_SET_BUTTON_ELE加值稅ION_REQUIRED_STATE message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5f8479e88a3b63cbd5fab6a5686913864fd9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105972"
---
# <a name="tdm_set_button_elevation_required_state-message"></a><span data-ttu-id="9560b-104">TDM \_ 設定 \_ 按鈕提高 \_ 許可權的 \_ 必要 \_ 狀態訊息</span><span class="sxs-lookup"><span data-stu-id="9560b-104">TDM\_SET\_BUTTON\_ELEVATION\_REQUIRED\_STATE message</span></span>

<span data-ttu-id="9560b-105">指定指定的工作對話方塊按鈕或命令連結是否應該有 (UAC) 盾牌圖示的使用者帳戶控制;亦即，按鈕叫用的動作是否需要提高許可權。</span><span class="sxs-lookup"><span data-stu-id="9560b-105">Specifies whether a given task dialog button or command link should have a User Account Control (UAC) shield icon; that is, whether the action invoked by the button requires elevation.</span></span>

## <a name="parameters"></a><span data-ttu-id="9560b-106">參數</span><span class="sxs-lookup"><span data-stu-id="9560b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9560b-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9560b-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9560b-108">要更新之推播按鈕或命令連結的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9560b-108">The ID of the push button or command link to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="9560b-109">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9560b-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9560b-110">設定為0，以指定按鈕叫用的動作不需要提高許可權。</span><span class="sxs-lookup"><span data-stu-id="9560b-110">Set to 0 to designate that the action invoked by the button does not require elevation.</span></span> <span data-ttu-id="9560b-111">設定為非零，以指定動作需要提高許可權。</span><span class="sxs-lookup"><span data-stu-id="9560b-111">Set to nonzero to designate that the action requires elevation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9560b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9560b-112">Return value</span></span>

<span data-ttu-id="9560b-113">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="9560b-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="9560b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9560b-114">Requirements</span></span>



| <span data-ttu-id="9560b-115">需求</span><span class="sxs-lookup"><span data-stu-id="9560b-115">Requirement</span></span> | <span data-ttu-id="9560b-116">值</span><span class="sxs-lookup"><span data-stu-id="9560b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9560b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9560b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9560b-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9560b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9560b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9560b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9560b-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9560b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9560b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="9560b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9560b-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9560b-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





