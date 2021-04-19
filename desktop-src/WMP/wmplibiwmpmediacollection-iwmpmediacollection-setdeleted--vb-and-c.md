---
title: IWMPMediaCollection setDeleted 方法
description: SetDeleted 方法會將指定的媒體專案移到 [刪除的專案] 資料夾。 |IWMPMediaCollection setDeleted 方法
ms.assetid: 3fa7989e-8b98-44e1-93ca-8136aba358ea
keywords:
- setDeleted 方法 Windows Media Player
- setDeleted 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，setDeleted 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.setDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ccf8cf2d36ab7e4aaf76fdbe5c28582650fcda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999399"
---
# <a name="iwmpmediacollectionsetdeleted-method"></a><span data-ttu-id="4d7cc-107">IWMPMediaCollection：： setDeleted 方法</span><span class="sxs-lookup"><span data-stu-id="4d7cc-107">IWMPMediaCollection::setDeleted method</span></span>

<span data-ttu-id="4d7cc-108">`setDeleted`方法會將指定的媒體專案移到 [刪除的專案] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="4d7cc-108">The `setDeleted` method moves the specified media item to the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d7cc-109">語法</span><span class="sxs-lookup"><span data-stu-id="4d7cc-109">Syntax</span></span>


```CSharp
public void setDeleted(
  IWMPMedia pItem,
  System.Boolean varfIsDeleted
);
```


```VB

Public Sub setDeleted( _
  ByVal pItem As IWMPMedia, _
  ByVal varfIsDeleted As System.Boolean _
)
Implements IWMPMediaCollection.setDeleted
```





## <a name="parameters"></a><span data-ttu-id="4d7cc-110">參數</span><span class="sxs-lookup"><span data-stu-id="4d7cc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d7cc-111">*pItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d7cc-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d7cc-112">要移動之專案的 **WMPLib IWMPMedia** 介面。</span><span class="sxs-lookup"><span data-stu-id="4d7cc-112">A **WMPLib.IWMPMedia** interface for the item to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="4d7cc-113">*varfIsDeleted* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d7cc-113">*varfIsDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d7cc-114">指定是否應將專案移至 [已刪除的專案] 資料夾的 [system.string] （ **布林** 值）值。</span><span class="sxs-lookup"><span data-stu-id="4d7cc-114">A **System.Boolean** value that specifies whether the item should be moved to the deleted items folder.</span></span> <span data-ttu-id="4d7cc-115">此值必須一律為 **true**。</span><span class="sxs-lookup"><span data-stu-id="4d7cc-115">This value must always be **true**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d7cc-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d7cc-116">Return value</span></span>

<span data-ttu-id="4d7cc-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4d7cc-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d7cc-118">備註</span><span class="sxs-lookup"><span data-stu-id="4d7cc-118">Remarks</span></span>

<span data-ttu-id="4d7cc-119">這個方法不會從使用者的電腦移除檔案，而是將它們移到 [刪除的專案] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="4d7cc-119">This method does not remove files from the user's computer, it just moves them to the deleted items folder.</span></span>

<span data-ttu-id="4d7cc-120">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="4d7cc-120">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="4d7cc-121">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="4d7cc-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4d7cc-122">範例</span><span class="sxs-lookup"><span data-stu-id="4d7cc-122">Examples</span></span>

<span data-ttu-id="4d7cc-123">下列範例會使用 `setDeleted` 將特定媒體專案移至 [已刪除的專案] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="4d7cc-123">The following example uses `setDeleted` to move a particular media item to the deleted items folder.</span></span> <span data-ttu-id="4d7cc-124">**IsDeleted** 方法會先測試是否已刪除專案。</span><span class="sxs-lookup"><span data-stu-id="4d7cc-124">The **isDeleted** method first tests whether the item has already been deleted.</span></span> <span data-ttu-id="4d7cc-125">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="4d7cc-125">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Test whether the media item has already been deleted.
if (!player.mediaCollection.isDeleted(media))
{
    // The item is available to be deleted; move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, true);

    // Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show("Item moved to deleted items folder.");
}
else
{
    // Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show("Item is already deleted!");
}
```


```VB

' Test whether the media item has already been deleted.
If (Not player.mediaCollection.isDeleted(media)) Then

    &#39; The item is available to be deleted move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, True)

    &#39; Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show(&quot;Item moved to deleted items folder.&quot;)

Else

    &#39; Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show(&quot;Item is already deleted!&quot;)

End If
```





## <a name="requirements"></a><span data-ttu-id="4d7cc-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d7cc-126">Requirements</span></span>



| <span data-ttu-id="4d7cc-127">需求</span><span class="sxs-lookup"><span data-stu-id="4d7cc-127">Requirement</span></span> | <span data-ttu-id="4d7cc-128">值</span><span class="sxs-lookup"><span data-stu-id="4d7cc-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7cc-129">版本</span><span class="sxs-lookup"><span data-stu-id="4d7cc-129">Version</span></span><br/>   | <span data-ttu-id="4d7cc-130">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="4d7cc-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4d7cc-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="4d7cc-131">Namespace</span></span><br/> | <span data-ttu-id="4d7cc-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4d7cc-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4d7cc-133">組件</span><span class="sxs-lookup"><span data-stu-id="4d7cc-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4d7cc-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="4d7cc-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d7cc-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d7cc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d7cc-136">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4d7cc-136">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4d7cc-137">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4d7cc-137">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





