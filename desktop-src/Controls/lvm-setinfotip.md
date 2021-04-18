---
title: 'LVM_SETINFOTIP 訊息 (Commctrl .h) '
description: 針對 LVN GETINFOTIP 通知，設定延遲回應中的工具提示文字 \_ 。
ms.assetid: 3dbf6a9a-52ec-4619-9c70-041e75942e20
keywords:
- LVM_SETINFOTIP message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90827766a6f1218dbbd631ed4eaf6b2989257944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965466"
---
# <a name="lvm_setinfotip-message"></a><span data-ttu-id="6868c-104">LVM \_ SETINFOTIP 訊息</span><span class="sxs-lookup"><span data-stu-id="6868c-104">LVM\_SETINFOTIP message</span></span>

<span data-ttu-id="6868c-105">針對 [LVN \_ GETINFOTIP](lvn-getinfotip.md) 通知，設定延遲回應中的工具提示文字。</span><span class="sxs-lookup"><span data-stu-id="6868c-105">Sets tooltip text in delayed response to the [LVN\_GETINFOTIP](lvn-getinfotip.md) notification.</span></span>

## <a name="parameters"></a><span data-ttu-id="6868c-106">參數</span><span class="sxs-lookup"><span data-stu-id="6868c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6868c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6868c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6868c-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6868c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6868c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6868c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6868c-110"><a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a>結構的指標，其中包含要設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="6868c-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6868c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6868c-111">Return value</span></span>

<span data-ttu-id="6868c-112">如果工具提示文字設定成功，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="6868c-112">Returns **TRUE** if the tooltip text is set successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6868c-113">備註</span><span class="sxs-lookup"><span data-stu-id="6868c-113">Remarks</span></span>

<span data-ttu-id="6868c-114">**LVM \_ SETINFOTIP** 訊息會透過執行下列步驟，讓應用程式在背景中計算提示：</span><span class="sxs-lookup"><span data-stu-id="6868c-114">The **LVM\_SETINFOTIP** message lets an application calculate infotips in the background by performing the following steps:</span></span>

1.  <span data-ttu-id="6868c-115">為了回應 [LVN \_ GETINFOTIP](lvn-getinfotip.md)通知，請將 [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa)結構的 **pszText** 成員設為空字串，並傳回0。</span><span class="sxs-lookup"><span data-stu-id="6868c-115">In response to the [LVN\_GETINFOTIP](lvn-getinfotip.md) notification, set the **pszText** member of the [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) structure to an empty string and return 0.</span></span>
2.  <span data-ttu-id="6868c-116">在背景中，計算提示。</span><span class="sxs-lookup"><span data-stu-id="6868c-116">In the background, compute the infotip.</span></span>
3.  <span data-ttu-id="6868c-117">計算資訊提示之後，傳送 **LVM \_ SETINFOTIP** 訊息，將 [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip)結構的 **pszText** 成員設定為資訊提示，並將 **iItem** 和 **iSubItem** 成員設定為資訊提示所套用的專案和子專案。</span><span class="sxs-lookup"><span data-stu-id="6868c-117">After computing the infotip, send the **LVM\_SETINFOTIP** message, setting the **pszText** member of the [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) structure to the infotip and the **iItem** and **iSubItem** members to the item and sub-item to which the infotip applies.</span></span>

<span data-ttu-id="6868c-118">只有當 [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip)結構所描述的專案和子專案仍處於需要資訊提示的狀態時，才會顯示傳遞至 **LVM \_ SETINFOTIP** 訊息的文字</span><span class="sxs-lookup"><span data-stu-id="6868c-118">The text passed to the **LVM\_SETINFOTIP** message appears only if the item and sub-item described by the [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) structure are still in a state that requires an infotip</span></span>

> [!Note]  
> <span data-ttu-id="6868c-119">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="6868c-119">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6868c-120">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="6868c-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6868c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6868c-121">Requirements</span></span>



| <span data-ttu-id="6868c-122">需求</span><span class="sxs-lookup"><span data-stu-id="6868c-122">Requirement</span></span> | <span data-ttu-id="6868c-123">值</span><span class="sxs-lookup"><span data-stu-id="6868c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6868c-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6868c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6868c-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6868c-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6868c-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6868c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6868c-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6868c-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6868c-128">標頭</span><span class="sxs-lookup"><span data-stu-id="6868c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6868c-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6868c-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





