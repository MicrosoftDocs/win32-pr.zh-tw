---
title: 'TVM_SETLINECOLOR 訊息 (Commctrl .h) '
description: TVM \_ SETLINECOLOR 訊息會設定目前的線條色彩。
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- TVM_SETLINECOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70340ea0d2339055faa3fb473269f3b244f335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025207"
---
# <a name="tvm_setlinecolor-message"></a><span data-ttu-id="73cd2-104">TVM \_ SETLINECOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="73cd2-104">TVM\_SETLINECOLOR message</span></span>

<span data-ttu-id="73cd2-105">**TVM \_ SETLINECOLOR** 訊息會設定目前的線條色彩。</span><span class="sxs-lookup"><span data-stu-id="73cd2-105">The **TVM\_SETLINECOLOR** message sets the current line color.</span></span>

## <a name="parameters"></a><span data-ttu-id="73cd2-106">參數</span><span class="sxs-lookup"><span data-stu-id="73cd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73cd2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73cd2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="73cd2-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="73cd2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="73cd2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73cd2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73cd2-110">新的線條色彩。</span><span class="sxs-lookup"><span data-stu-id="73cd2-110">New line color.</span></span> <span data-ttu-id="73cd2-111">使用 CLR \_ 預設值來還原系統預設色彩。</span><span class="sxs-lookup"><span data-stu-id="73cd2-111">Use the CLR\_DEFAULT value to restore the system default colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73cd2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="73cd2-112">Return value</span></span>

<span data-ttu-id="73cd2-113">傳回先前的線條色彩。</span><span class="sxs-lookup"><span data-stu-id="73cd2-113">Returns the previous line color.</span></span>

## <a name="remarks"></a><span data-ttu-id="73cd2-114">備註</span><span class="sxs-lookup"><span data-stu-id="73cd2-114">Remarks</span></span>

<span data-ttu-id="73cd2-115">此訊息只會變更線條色彩。</span><span class="sxs-lookup"><span data-stu-id="73cd2-115">This message only changes line colors.</span></span> <span data-ttu-id="73cd2-116">若要變更按鈕內的 ' + ' 和 '-' 色彩，請使用 [**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="73cd2-116">To change the colors of the '+' and '-' inside the buttons, use the [**TVM\_SETTEXTCOLOR**](tvm-settextcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="73cd2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="73cd2-117">Requirements</span></span>



| <span data-ttu-id="73cd2-118">需求</span><span class="sxs-lookup"><span data-stu-id="73cd2-118">Requirement</span></span> | <span data-ttu-id="73cd2-119">值</span><span class="sxs-lookup"><span data-stu-id="73cd2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73cd2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73cd2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="73cd2-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73cd2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73cd2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73cd2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="73cd2-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73cd2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73cd2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="73cd2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="73cd2-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="73cd2-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73cd2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73cd2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73cd2-127">**TVM \_ GETLINECOLOR**</span><span class="sxs-lookup"><span data-stu-id="73cd2-127">**TVM\_GETLINECOLOR**</span></span>](tvm-getlinecolor.md)
</dt> </dl>

 

 





