---
title: 'LVM_GETEMPTYTEXT 訊息 (Commctrl .h) '
description: 取得當清單視圖控制項顯示為空白時，所要顯示的文字。 明確地傳送此訊息，或使用 ListView \_ GetEmptyText 宏。
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- LVM_GETEMPTYTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETEMPTYTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7549081ef7f158a6a6a061bcee9669ea62d52f68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464276"
---
# <a name="lvm_getemptytext-message"></a><span data-ttu-id="1ff9f-105">LVM \_ GETEMPTYTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="1ff9f-105">LVM\_GETEMPTYTEXT message</span></span>

<span data-ttu-id="1ff9f-106">取得當清單視圖控制項顯示為空白時，所要顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="1ff9f-106">Gets the text meant for display when the list-view control appears empty.</span></span> <span data-ttu-id="1ff9f-107">明確地傳送此訊息，或使用 [**ListView \_ GetEmptyText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) 宏。</span><span class="sxs-lookup"><span data-stu-id="1ff9f-107">Send this message explicitly or by using the [**ListView\_GetEmptyText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ff9f-108">參數</span><span class="sxs-lookup"><span data-stu-id="1ff9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ff9f-109">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1ff9f-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff9f-110">*LParam* 所指向的緩衝區大小，包括終止的 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1ff9f-110">The size of the buffer pointed to by *lParam*, including the terminating **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1ff9f-111">*lParam* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1ff9f-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff9f-112">以 null 終止的 Unicode 緩衝區指標， *wParam* 指定的大小，以接收文字。</span><span class="sxs-lookup"><span data-stu-id="1ff9f-112">A pointer to a null-terminated, Unicode buffer of size specified by *wParam* to receive the text.</span></span> <span data-ttu-id="1ff9f-113">呼叫端負責配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1ff9f-113">The caller is responsible for allocating the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ff9f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ff9f-114">Return value</span></span>

<span data-ttu-id="1ff9f-115">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="1ff9f-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ff9f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ff9f-116">Requirements</span></span>



| <span data-ttu-id="1ff9f-117">需求</span><span class="sxs-lookup"><span data-stu-id="1ff9f-117">Requirement</span></span> | <span data-ttu-id="1ff9f-118">值</span><span class="sxs-lookup"><span data-stu-id="1ff9f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff9f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ff9f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1ff9f-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ff9f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ff9f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ff9f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1ff9f-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ff9f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ff9f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="1ff9f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ff9f-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1ff9f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





