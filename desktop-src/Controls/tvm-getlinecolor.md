---
title: 'TVM_GETLINECOLOR 訊息 (Commctrl .h) '
description: TVM \_ GETLINECOLOR 訊息會取得目前的線條色彩。
ms.assetid: e74441b3-5d4f-4454-b896-2e96ce649419
keywords:
- TVM_GETLINECOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd55149f38fb17238e13135e798ebbe55b15009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025245"
---
# <a name="tvm_getlinecolor-message"></a><span data-ttu-id="0501d-104">TVM \_ GETLINECOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="0501d-104">TVM\_GETLINECOLOR message</span></span>

<span data-ttu-id="0501d-105">**TVM \_ GETLINECOLOR** 訊息會取得目前的線條色彩。</span><span class="sxs-lookup"><span data-stu-id="0501d-105">The **TVM\_GETLINECOLOR** message gets the current line color.</span></span>

## <a name="parameters"></a><span data-ttu-id="0501d-106">參數</span><span class="sxs-lookup"><span data-stu-id="0501d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0501d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0501d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0501d-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0501d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0501d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0501d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0501d-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0501d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0501d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0501d-111">Return value</span></span>

<span data-ttu-id="0501d-112">傳回目前的線條色彩，如果未指定，則為 CLR \_ 預設值。</span><span class="sxs-lookup"><span data-stu-id="0501d-112">Returns the current line color, or the CLR\_DEFAULT value if none has been specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="0501d-113">備註</span><span class="sxs-lookup"><span data-stu-id="0501d-113">Remarks</span></span>

<span data-ttu-id="0501d-114">此訊息只會抓取線條色彩。</span><span class="sxs-lookup"><span data-stu-id="0501d-114">This message only retrieves line colors.</span></span> <span data-ttu-id="0501d-115">若要取出按鈕內的 ' + ' 和 '-' 色彩，請使用 [**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="0501d-115">To retrieve the colors of the '+' and '-' inside the buttons, use the [**TVM\_GETTEXTCOLOR**](tvm-gettextcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0501d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0501d-116">Requirements</span></span>



| <span data-ttu-id="0501d-117">需求</span><span class="sxs-lookup"><span data-stu-id="0501d-117">Requirement</span></span> | <span data-ttu-id="0501d-118">值</span><span class="sxs-lookup"><span data-stu-id="0501d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0501d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0501d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0501d-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0501d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0501d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0501d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0501d-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0501d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0501d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0501d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0501d-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0501d-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0501d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0501d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0501d-126">**TVM \_ SETLINECOLOR**</span><span class="sxs-lookup"><span data-stu-id="0501d-126">**TVM\_SETLINECOLOR**</span></span>](tvm-setlinecolor.md)
</dt> </dl>

 

 





