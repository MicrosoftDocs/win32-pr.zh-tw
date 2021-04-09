---
title: 'RB_SETBARINFO 訊息 (Commctrl .h) '
description: 設定 Rebar 控制項的特性。
ms.assetid: e4413d46-574f-4ccd-b5fd-3ba6c1e3924b
keywords:
- RB_SETBARINFO message Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b360bc0b4d14963619aad8f769634d7dd0ad17e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024650"
---
# <a name="rb_setbarinfo-message"></a><span data-ttu-id="354bb-104">RB \_ SETBARINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="354bb-104">RB\_SETBARINFO message</span></span>

<span data-ttu-id="354bb-105">設定 Rebar 控制項的特性。</span><span class="sxs-lookup"><span data-stu-id="354bb-105">Sets the characteristics of a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="354bb-106">參數</span><span class="sxs-lookup"><span data-stu-id="354bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="354bb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="354bb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="354bb-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="354bb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="354bb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="354bb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="354bb-110">[**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo)結構的指標，其中包含要設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="354bb-110">Pointer to a [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) structure that contains the information to be set.</span></span> <span data-ttu-id="354bb-111">在傳送此訊息之前，您必須將此結構的 **cbSize** 成員設定為 **sizeof** (REBARINFO) 。</span><span class="sxs-lookup"><span data-stu-id="354bb-111">You must set the **cbSize** member of this structure to **sizeof**(REBARINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="354bb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="354bb-112">Return value</span></span>

<span data-ttu-id="354bb-113">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="354bb-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="354bb-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="354bb-114">Requirements</span></span>



| <span data-ttu-id="354bb-115">需求</span><span class="sxs-lookup"><span data-stu-id="354bb-115">Requirement</span></span> | <span data-ttu-id="354bb-116">值</span><span class="sxs-lookup"><span data-stu-id="354bb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="354bb-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="354bb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="354bb-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="354bb-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="354bb-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="354bb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="354bb-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="354bb-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="354bb-121">標頭</span><span class="sxs-lookup"><span data-stu-id="354bb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="354bb-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="354bb-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





