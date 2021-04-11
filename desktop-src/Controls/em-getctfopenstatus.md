---
title: 'EM_GETCTFOPENSTATUS 訊息 (Richedit .h) '
description: 決定文字服務架構 (TSF) 鍵盤是開啟或關閉。
ms.assetid: a50fedf4-b4e5-4b99-be46-1bbbf08e85a8
keywords:
- EM_GETCTFOPENSTATUS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce1bbf09af6c61a33c33c4172ff699fa5bd26f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934489"
---
# <a name="em_getctfopenstatus-message"></a><span data-ttu-id="c61f9-104">EM \_ GETCTFOPENSTATUS 訊息</span><span class="sxs-lookup"><span data-stu-id="c61f9-104">EM\_GETCTFOPENSTATUS message</span></span>

<span data-ttu-id="c61f9-105">決定文字服務架構 (TSF) 鍵盤是開啟或關閉。</span><span class="sxs-lookup"><span data-stu-id="c61f9-105">Determines if the Text Services Framework (TSF) keyboard is open or closed.</span></span>

## <a name="parameters"></a><span data-ttu-id="c61f9-106">參數</span><span class="sxs-lookup"><span data-stu-id="c61f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c61f9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c61f9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c61f9-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="c61f9-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c61f9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c61f9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c61f9-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="c61f9-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c61f9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c61f9-111">Return value</span></span>

<span data-ttu-id="c61f9-112">如果 TSF 鍵盤已開啟，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="c61f9-112">If the TSF keyboard is open, the return value is **TRUE**.</span></span> <span data-ttu-id="c61f9-113">否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c61f9-113">Otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c61f9-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c61f9-114">Requirements</span></span>



| <span data-ttu-id="c61f9-115">需求</span><span class="sxs-lookup"><span data-stu-id="c61f9-115">Requirement</span></span> | <span data-ttu-id="c61f9-116">值</span><span class="sxs-lookup"><span data-stu-id="c61f9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c61f9-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c61f9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c61f9-118">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c61f9-118">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c61f9-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c61f9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c61f9-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c61f9-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c61f9-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c61f9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c61f9-122"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="c61f9-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c61f9-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c61f9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c61f9-124">**EM \_ SETCTFOPENSTATUS**</span><span class="sxs-lookup"><span data-stu-id="c61f9-124">**EM\_SETCTFOPENSTATUS**</span></span>](em-setctfopenstatus.md)
</dt> </dl>

 

 





