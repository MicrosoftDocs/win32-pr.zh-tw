---
description: EXPERTSTATUSENUMERATION 列舉包含狀態值。 EXPERTSTATUS 結構的 Status 成員和 ExpertIndicateStatus 中的 Status 參數會使用它。
ms.assetid: 217dce5a-3698-45a9-bb13-8379bcbdd762
title: 'EXPERTSTATUSENUMERATION 列舉 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERT_STATUS_ENUMERATION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b634d4dad2e024c3c995216b5af7de23b14b7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991808"
---
# <a name="expertstatusenumeration-enumeration"></a><span data-ttu-id="f1e98-104">EXPERTSTATUSENUMERATION 列舉</span><span class="sxs-lookup"><span data-stu-id="f1e98-104">EXPERTSTATUSENUMERATION enumeration</span></span>

<span data-ttu-id="f1e98-105">**EXPERTSTATUSENUMERATION** 列舉包含狀態值。</span><span class="sxs-lookup"><span data-stu-id="f1e98-105">The **EXPERTSTATUSENUMERATION** enumeration contains status values.</span></span> <span data-ttu-id="f1e98-106">[EXPERTSTATUS](expertstatus.md)結構的 **Status** 成員和 [ExpertIndicateStatus](expertindicatestatus.md)中的 *status* 參數會使用它。</span><span class="sxs-lookup"><span data-stu-id="f1e98-106">It is used by the **Status** member of [EXPERTSTATUS](expertstatus.md) structure and the *Status* parameter in [ExpertIndicateStatus](expertindicatestatus.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f1e98-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1e98-107">Syntax</span></span>


```C++
typedef enum  { 
  EXPERTSTATUS_INACTIVE  = 0,
  EXPERTSTATUS_STARTING,
  EXPERTSTATUS_RUNNING,
  EXPERTSTATUS_PROBLEM,
  EXPERTSTATUS_ABORTED,
  EXPERTSTATUS_DONE
} EXPERT_STATUS_ENUMERATION;
```



## <a name="constants"></a><span data-ttu-id="f1e98-108">常數</span><span class="sxs-lookup"><span data-stu-id="f1e98-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f1e98-109"><span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS \_ 非使用中**</span><span class="sxs-lookup"><span data-stu-id="f1e98-109"><span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS\_INACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="f1e98-110">專家從未開始。</span><span class="sxs-lookup"><span data-stu-id="f1e98-110">The expert never started.</span></span>

</dd> <dt>

<span data-ttu-id="f1e98-111"><span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**EXPERTSTATUS \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="f1e98-111"><span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**EXPERTSTATUS\_STARTING**</span></span>
</dt> <dd>

<span data-ttu-id="f1e98-112">專家即將開始。</span><span class="sxs-lookup"><span data-stu-id="f1e98-112">The expert is starting.</span></span>

</dd> <dt>

<span data-ttu-id="f1e98-113"><span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS \_ 正在執行**</span><span class="sxs-lookup"><span data-stu-id="f1e98-113"><span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="f1e98-114">專家正在正常執行。</span><span class="sxs-lookup"><span data-stu-id="f1e98-114">The expert is running normally.</span></span>

</dd> <dt>

<span data-ttu-id="f1e98-115"><span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**EXPERTSTATUS \_ 問題**</span><span class="sxs-lookup"><span data-stu-id="f1e98-115"><span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**EXPERTSTATUS\_PROBLEM**</span></span>
</dt> <dd>

<span data-ttu-id="f1e98-116">在子 *狀態* 中指定的問題已停止專家。</span><span class="sxs-lookup"><span data-stu-id="f1e98-116">A problem specified in *SubStatus* stopped the expert.</span></span>

</dd> <dt>

<span data-ttu-id="f1e98-117"><span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS 已 \_ 中止**</span><span class="sxs-lookup"><span data-stu-id="f1e98-117"><span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="f1e98-118">網路監視器已停止專家。</span><span class="sxs-lookup"><span data-stu-id="f1e98-118">Network Monitor stopped the expert.</span></span>

</dd> <dt>

<span data-ttu-id="f1e98-119"><span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="f1e98-119"><span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS\_DONE**</span></span>
</dt> <dd>

<span data-ttu-id="f1e98-120">專家已順利完成。</span><span class="sxs-lookup"><span data-stu-id="f1e98-120">The expert finished successfully.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1e98-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1e98-121">Requirements</span></span>



| <span data-ttu-id="f1e98-122">需求</span><span class="sxs-lookup"><span data-stu-id="f1e98-122">Requirement</span></span> | <span data-ttu-id="f1e98-123">值</span><span class="sxs-lookup"><span data-stu-id="f1e98-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e98-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1e98-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f1e98-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1e98-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f1e98-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1e98-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f1e98-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1e98-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f1e98-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f1e98-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1e98-129"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="f1e98-129"><dt>Netmon.h</dt></span></span> </dl> |



 

 




