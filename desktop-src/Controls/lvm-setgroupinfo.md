---
title: 'LVM_SETGROUPINFO 訊息 (Commctrl .h) '
description: 設定群組資訊。
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- LVM_SETGROUPINFO message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 688c5b56a57a579e5955fa62a9b44d88258b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024586"
---
# <a name="lvm_setgroupinfo-message"></a><span data-ttu-id="2e293-104">LVM \_ SETGROUPINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="2e293-104">LVM\_SETGROUPINFO message</span></span>

<span data-ttu-id="2e293-105">設定群組資訊。</span><span class="sxs-lookup"><span data-stu-id="2e293-105">Sets group information.</span></span> <span data-ttu-id="2e293-106">明確地傳送此訊息，或使用 [**ListView \_ SetGroupInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) 宏。</span><span class="sxs-lookup"><span data-stu-id="2e293-106">Send this message explicitly or by using the [**ListView\_SetGroupInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e293-107">參數</span><span class="sxs-lookup"><span data-stu-id="2e293-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e293-108">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e293-108">*wParam* \[in\]</span></span>
</dt> <dd><span data-ttu-id="2e293-109">指定要設定其資訊之群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2e293-109">ID that specifies the group whose information is to be set.</span></span></dd> <dt>

<span data-ttu-id="2e293-110">*lParam* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2e293-110">*lParam* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="2e293-111">[**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup)結構的指標，其中包含要設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="2e293-111">Pointer to a [**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e293-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e293-112">Return value</span></span>

<span data-ttu-id="2e293-113">如果成功，則傳回群組的識別碼，否則為-1。</span><span class="sxs-lookup"><span data-stu-id="2e293-113">Returns the ID of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e293-114">備註</span><span class="sxs-lookup"><span data-stu-id="2e293-114">Remarks</span></span>

<span data-ttu-id="2e293-115">若要變更現有群組的群組識別碼，請將 <b>LVGF_GROUPID</b> 新增至 <b>LVGROUP</b> ，並將 <b>LVGROUP IGROUPID</b> 設定為新的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2e293-115">To change a group ID of an existing group add <b>LVGF_GROUPID</b> to <b>LVGROUP.mask</b> and set <b>LVGROUP.iGroupId</b> to the new ID.</span></span> <span data-ttu-id="2e293-116">如果 <b>LVGROUP. iGroupId</b> 包含現有群組的識別碼，則呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="2e293-116">The call will fail if <b>LVGROUP.iGroupId</b> contains ID of an existing group.</span></span>

<span data-ttu-id="2e293-117">若要更新現有群組的其他屬性 (例如，更新群組的頁首或頁尾文字對齊方式， <b>uAlign</b>) <b>LVGROUP。 mask</b> 不得包含 <b>LVGF_GROUPID</b>，否則更新將會失敗。</span><span class="sxs-lookup"><span data-stu-id="2e293-117">To update other properties of an existing group (e.g. update an alignment of the header or footer text for the group, <b>uAlign</b>) <b>LVGROUP.mask</b> must not contain <b>LVGF_GROUPID</b>, else the update will fail.</span></span>

> [!Note]  
> <span data-ttu-id="2e293-118">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="2e293-118">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="2e293-119">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="2e293-119">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e293-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e293-120">Requirements</span></span>



| <span data-ttu-id="2e293-121">需求</span><span class="sxs-lookup"><span data-stu-id="2e293-121">Requirement</span></span> | <span data-ttu-id="2e293-122">值</span><span class="sxs-lookup"><span data-stu-id="2e293-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e293-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e293-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2e293-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e293-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e293-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e293-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2e293-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e293-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e293-127">標頭</span><span class="sxs-lookup"><span data-stu-id="2e293-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e293-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2e293-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





