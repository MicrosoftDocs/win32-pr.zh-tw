---
title: 'LVM_GETFOOTERINFO 訊息 (Commctrl .h) '
description: 取得清單視圖控制項頁尾的相關資訊。 明確地傳送此訊息，或使用 ListView \_ GetFooterInfo 宏。
ms.assetid: 5734e151-50c0-46df-8f2c-220c4910a590
keywords:
- LVM_GETFOOTERINFO message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETFOOTERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718e6c165985981190b5a1d4c52e851d1a2d504d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933923"
---
# <a name="lvm_getfooterinfo-message"></a><span data-ttu-id="98182-105">LVM \_ GETFOOTERINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="98182-105">LVM\_GETFOOTERINFO message</span></span>

<span data-ttu-id="98182-106">取得清單視圖控制項頁尾的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="98182-106">Gets information about the footer of a list-view control.</span></span> <span data-ttu-id="98182-107">明確地傳送此訊息，或使用 [**ListView \_ GetFooterInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) 宏。</span><span class="sxs-lookup"><span data-stu-id="98182-107">Send this message explicitly or by using the [**ListView\_GetFooterInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="98182-108">參數</span><span class="sxs-lookup"><span data-stu-id="98182-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98182-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98182-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98182-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="98182-110">Not used.</span></span> <span data-ttu-id="98182-111">必須是 0。</span><span class="sxs-lookup"><span data-stu-id="98182-111">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="98182-112">*lParam* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="98182-112">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98182-113">[**LVFOOTERINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo)結構的指標，用來接收資訊，視 **遮罩** 成員的值而定。</span><span class="sxs-lookup"><span data-stu-id="98182-113">A pointer to a [**LVFOOTERINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) structure to receive information depending on the value of the **mask** member.</span></span> <span data-ttu-id="98182-114">呼叫進程負責配置此結構及設定 **遮罩** 成員。</span><span class="sxs-lookup"><span data-stu-id="98182-114">The calling process is responsible for allocating this structure and setting the **mask** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98182-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="98182-115">Return value</span></span>

<span data-ttu-id="98182-116">傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="98182-116">Returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="98182-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="98182-117">Requirements</span></span>



| <span data-ttu-id="98182-118">需求</span><span class="sxs-lookup"><span data-stu-id="98182-118">Requirement</span></span> | <span data-ttu-id="98182-119">值</span><span class="sxs-lookup"><span data-stu-id="98182-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98182-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="98182-120">Minimum supported client</span></span><br/> | <span data-ttu-id="98182-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98182-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="98182-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="98182-122">Minimum supported server</span></span><br/> | <span data-ttu-id="98182-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98182-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="98182-124">標頭</span><span class="sxs-lookup"><span data-stu-id="98182-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="98182-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="98182-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





