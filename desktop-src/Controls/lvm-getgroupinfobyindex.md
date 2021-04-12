---
title: 'LVM_GETGROUPINFOBYINDEX 訊息 (Commctrl .h) '
description: 取得指定群組的資訊。 明確地傳送此訊息，或使用 ListView \_ GetGroupInfoByIndex 宏。
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- LVM_GETGROUPINFOBYINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFOBYINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff801eae55ab4b4194ef23e624ff6eff75fbc25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104459"
---
# <a name="lvm_getgroupinfobyindex-message"></a><span data-ttu-id="c56f5-105">LVM \_ GETGROUPINFOBYINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="c56f5-105">LVM\_GETGROUPINFOBYINDEX message</span></span>

<span data-ttu-id="c56f5-106">取得指定群組的資訊。</span><span class="sxs-lookup"><span data-stu-id="c56f5-106">Gets information on a specified group.</span></span> <span data-ttu-id="c56f5-107">明確地傳送此訊息，或使用 [**ListView \_ GetGroupInfoByIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) 宏。</span><span class="sxs-lookup"><span data-stu-id="c56f5-107">Send this message explicitly or by using the [**ListView\_GetGroupInfoByIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c56f5-108">參數</span><span class="sxs-lookup"><span data-stu-id="c56f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c56f5-109">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c56f5-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c56f5-110">群組的索引。</span><span class="sxs-lookup"><span data-stu-id="c56f5-110">The index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="c56f5-111">*lParam* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c56f5-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c56f5-112">[**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)結構的指標，用來接收 *wParam* 所指定之群組的資訊。</span><span class="sxs-lookup"><span data-stu-id="c56f5-112">A pointer to an [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure to receive information on the group specified by *wParam*.</span></span> <span data-ttu-id="c56f5-113">呼叫進程負責為結構和結構中的任何緩衝區（例如 **pszHeader** 成員所指向的緩衝區）配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="c56f5-113">The calling process is responsible for allocating memory for the structure and any buffers in the structure, such as the one pointed to by the **pszHeader** member.</span></span> <span data-ttu-id="c56f5-114">設定結構的任何有的成員，例如 **CchHeader** **pszHeader** 在 **WCHARs** 中所指向的緩衝區大小，包括終止的 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c56f5-114">Set any contingent members of the structure, such as **cchHeader** the size of the buffer pointed to by **pszHeader** in **WCHARs** including the terminating **NULL**.</span></span> <span data-ttu-id="c56f5-115">將 **cbSize** 設定為 SIZEOF (LVGROUP) 。</span><span class="sxs-lookup"><span data-stu-id="c56f5-115">Set **cbSize** to sizeof(LVGROUP).</span></span>

<span data-ttu-id="c56f5-116">訊息接收者負責為結構成員設定 *wParam* 所指定之群組的資訊。</span><span class="sxs-lookup"><span data-stu-id="c56f5-116">The message receiver is responsible for setting the structure members with information for the group specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c56f5-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="c56f5-117">Return value</span></span>

<span data-ttu-id="c56f5-118">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c56f5-118">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c56f5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c56f5-119">Requirements</span></span>



| <span data-ttu-id="c56f5-120">需求</span><span class="sxs-lookup"><span data-stu-id="c56f5-120">Requirement</span></span> | <span data-ttu-id="c56f5-121">值</span><span class="sxs-lookup"><span data-stu-id="c56f5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c56f5-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c56f5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c56f5-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c56f5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c56f5-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c56f5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c56f5-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c56f5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c56f5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c56f5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c56f5-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c56f5-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





