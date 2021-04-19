---
title: 'LVM_MAPIDTOINDEX 訊息 (Commctrl .h) '
description: 將專案的識別碼對應至索引。
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- LVM_MAPIDTOINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_MAPIDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb4cb8aa49b37186ef689ed8cb319bbb92b62d75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966136"
---
# <a name="lvm_mapidtoindex-message"></a><span data-ttu-id="711d5-104">LVM \_ MAPIDTOINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="711d5-104">LVM\_MAPIDTOINDEX message</span></span>

<span data-ttu-id="711d5-105">將專案的識別碼對應至索引。</span><span class="sxs-lookup"><span data-stu-id="711d5-105">Maps the ID of an item to an index.</span></span>

## <a name="parameters"></a><span data-ttu-id="711d5-106">參數</span><span class="sxs-lookup"><span data-stu-id="711d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="711d5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="711d5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="711d5-108">專案的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="711d5-108">The unique ID of an item.</span></span>

</dd> <dt>

<span data-ttu-id="711d5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="711d5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="711d5-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="711d5-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="711d5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="711d5-111">Return value</span></span>

<span data-ttu-id="711d5-112">傳回最新的索引。</span><span class="sxs-lookup"><span data-stu-id="711d5-112">Returns the most current index.</span></span>

## <a name="remarks"></a><span data-ttu-id="711d5-113">備註</span><span class="sxs-lookup"><span data-stu-id="711d5-113">Remarks</span></span>

<span data-ttu-id="711d5-114">清單視圖控制項會依索引在內部追蹤專案。</span><span class="sxs-lookup"><span data-stu-id="711d5-114">List-view controls internally track items by index.</span></span> <span data-ttu-id="711d5-115">這可能會造成問題，因為索引可能會在控制項的存留期間變更。</span><span class="sxs-lookup"><span data-stu-id="711d5-115">This can present problems because indexes can change during the control's lifetime.</span></span>

<span data-ttu-id="711d5-116">清單視圖控制項可以在建立專案時標記具有識別碼的專案。</span><span class="sxs-lookup"><span data-stu-id="711d5-116">The list-view control can tag an item with an ID when the item is created.</span></span> <span data-ttu-id="711d5-117">您可以使用這個識別碼，在清單視圖控制項的存留期內保證唯一性。</span><span class="sxs-lookup"><span data-stu-id="711d5-117">You can use this ID to guarantee uniqueness during the lifetime of the list-view control.</span></span>

<span data-ttu-id="711d5-118">若要唯一識別專案，請取得從呼叫傳回的索引，例如 [**IComponent：： GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) ，並呼叫 [**LVM \_ MAPINDEXTOID**](lvm-mapindextoid.md)。</span><span class="sxs-lookup"><span data-stu-id="711d5-118">To uniquely identify an item, take the index that is returned from a call such as [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) and call [**LVM\_MAPINDEXTOID**](lvm-mapindextoid.md).</span></span> <span data-ttu-id="711d5-119">傳回值是唯一的識別碼。</span><span class="sxs-lookup"><span data-stu-id="711d5-119">The return value is a unique ID.</span></span>

<span data-ttu-id="711d5-120">如果您在建立識別碼之後需要專案的索引，您可以使用唯一識別碼來呼叫 **LVM \_ MAPIDTOINDEX** ，它會傳回最新的索引。</span><span class="sxs-lookup"><span data-stu-id="711d5-120">If you need the index of an item after an ID is created you can call **LVM\_MAPIDTOINDEX** with the unique ID and it returns the most current index.</span></span>

<span data-ttu-id="711d5-121">**LVM \_** [**Lvs) \_ OWNERDATA**](list-view-window-styles.md)樣式下不支援 MAPIDTOINDEX。</span><span class="sxs-lookup"><span data-stu-id="711d5-121">**LVM\_MAPIDTOINDEX** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="711d5-122">在多執行緒環境中，只有裝載清單視圖控制項的執行緒（而不是背景執行緒）保證索引。</span><span class="sxs-lookup"><span data-stu-id="711d5-122">In a multithreaded environment, the index is only guaranteed on the thread that hosts the list-view control, not on background threads.</span></span>

 

> [!Note]  
> <span data-ttu-id="711d5-123">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="711d5-123">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="711d5-124">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="711d5-124">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="711d5-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="711d5-125">Requirements</span></span>



| <span data-ttu-id="711d5-126">需求</span><span class="sxs-lookup"><span data-stu-id="711d5-126">Requirement</span></span> | <span data-ttu-id="711d5-127">值</span><span class="sxs-lookup"><span data-stu-id="711d5-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="711d5-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="711d5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="711d5-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="711d5-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="711d5-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="711d5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="711d5-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="711d5-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="711d5-132">標頭</span><span class="sxs-lookup"><span data-stu-id="711d5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="711d5-133"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="711d5-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

