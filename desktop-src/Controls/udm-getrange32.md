---
title: 'UDM_GETRANGE32 訊息 (Commctrl .h) '
description: 抓取上下按鈕控制項的32位範圍。
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- UDM_GETRANGE32 message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca418cd08dc4c81b3ff734d74f3ca9deeef7d848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465024"
---
# <a name="udm_getrange32-message"></a><span data-ttu-id="4146f-104">UDM \_ GETRANGE32 訊息</span><span class="sxs-lookup"><span data-stu-id="4146f-104">UDM\_GETRANGE32 message</span></span>

<span data-ttu-id="4146f-105">抓取上下按鈕控制項的32位範圍。</span><span class="sxs-lookup"><span data-stu-id="4146f-105">Retrieves the 32-bit range of an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4146f-106">參數</span><span class="sxs-lookup"><span data-stu-id="4146f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4146f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4146f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4146f-108">帶正負號之整數的指標，該整數會接收最小的最小值控制項範圍。</span><span class="sxs-lookup"><span data-stu-id="4146f-108">Pointer to a signed integer that receives the lower limit of the up-down control range.</span></span> <span data-ttu-id="4146f-109">這個參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4146f-109">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4146f-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4146f-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4146f-111">帶正負號之整數的指標，該整數會接收上下按鈕控制項範圍的上限。</span><span class="sxs-lookup"><span data-stu-id="4146f-111">Pointer to a signed integer that receives the upper limit of the up-down control range.</span></span> <span data-ttu-id="4146f-112">這個參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4146f-112">This parameter may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4146f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4146f-113">Return value</span></span>

<span data-ttu-id="4146f-114">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="4146f-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4146f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4146f-115">Requirements</span></span>



| <span data-ttu-id="4146f-116">需求</span><span class="sxs-lookup"><span data-stu-id="4146f-116">Requirement</span></span> | <span data-ttu-id="4146f-117">值</span><span class="sxs-lookup"><span data-stu-id="4146f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4146f-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4146f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4146f-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4146f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4146f-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4146f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4146f-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4146f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4146f-122">標頭</span><span class="sxs-lookup"><span data-stu-id="4146f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4146f-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4146f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





