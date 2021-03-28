---
description: 抓取 Windows 工作列的自動隱藏和 alwayson 最上層狀態。
title: 'ABM_GETSTATE 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 18e16752-16be-492b-a4fa-c951e18dc86c
api_name:
- ABM_GETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 71225cd8d93de09a07cb0049066e52be08c18a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318124"
---
# <a name="abm_getstate-message"></a><span data-ttu-id="c9c87-103">ABM \_ >getstate 訊息</span><span class="sxs-lookup"><span data-stu-id="c9c87-103">ABM\_GETSTATE message</span></span>

<span data-ttu-id="c9c87-104">抓取 Windows 工作列的自動隱藏和 alwayson 最上層狀態。</span><span class="sxs-lookup"><span data-stu-id="c9c87-104">Retrieves the autohide and always-on-top states of the Windows taskbar.</span></span>


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a><span data-ttu-id="c9c87-105">參數</span><span class="sxs-lookup"><span data-stu-id="c9c87-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9c87-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="c9c87-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c87-107">[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c9c87-107">Pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="c9c87-108">傳送此訊息時，您必須指定 **cbSize** 成員;所有其他成員都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="c9c87-108">You must specify the **cbSize** member when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9c87-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9c87-109">Return value</span></span>

<span data-ttu-id="c9c87-110">如果工作列不是自動隱藏或不在最上層狀態，則傳回零。</span><span class="sxs-lookup"><span data-stu-id="c9c87-110">Returns zero if the taskbar is neither in the autohide nor always-on-top state.</span></span> <span data-ttu-id="c9c87-111">否則，傳回值是下列其中一項或兩項：</span><span class="sxs-lookup"><span data-stu-id="c9c87-111">Otherwise, the return value is one or both of the following:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9c87-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c9c87-112">Return code</span></span></th>
<th><span data-ttu-id="c9c87-113">Description</span><span class="sxs-lookup"><span data-stu-id="c9c87-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="c9c87-114"><dt><strong>ABS_ALWAYSONTOP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c9c87-114"><dt><strong>ABS_ALWAYSONTOP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c9c87-115">工作列處於 always on 最上層狀態。</span><span class="sxs-lookup"><span data-stu-id="c9c87-115">The taskbar is in the always-on-top state.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c9c87-116">從 Windows 7，因為工作列永遠處于該狀態，所以不會再傳回 ABS_ALWAYSONTOP。</span><span class="sxs-lookup"><span data-stu-id="c9c87-116">As of Windows 7, ABS_ALWAYSONTOP is no longer returned because the taskbar is always in that state.</span></span> <span data-ttu-id="c9c87-117">您應該更新較舊的程式碼，以忽略此值不存在的情況下，不假設該傳回值表示工作列不是處於最新狀態。</span><span class="sxs-lookup"><span data-stu-id="c9c87-117">Older code should be updated to ignore the absence of this value in not assume that return value to mean that the taskbar is not in the always-on-top state.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c9c87-118"><dt><strong>ABS_AUTOHIDE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c9c87-118"><dt><strong>ABS_AUTOHIDE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c9c87-119">工作列處於 [自動隱藏] 狀態。</span><span class="sxs-lookup"><span data-stu-id="c9c87-119">The taskbar is in the autohide state.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="c9c87-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9c87-120">Requirements</span></span>



| <span data-ttu-id="c9c87-121">需求</span><span class="sxs-lookup"><span data-stu-id="c9c87-121">Requirement</span></span> | <span data-ttu-id="c9c87-122">值</span><span class="sxs-lookup"><span data-stu-id="c9c87-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9c87-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9c87-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c9c87-124">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9c87-124">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c9c87-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9c87-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c9c87-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9c87-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9c87-127">標頭</span><span class="sxs-lookup"><span data-stu-id="c9c87-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9c87-128"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9c87-128"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




