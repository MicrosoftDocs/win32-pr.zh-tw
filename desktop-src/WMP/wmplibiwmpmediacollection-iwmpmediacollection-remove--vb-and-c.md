---
title: IWMPMediaCollection remove 方法
description: Remove 方法會從媒體集合中移除指定的專案。
ms.assetid: 2ed45159-0a92-4353-8bf1-1d20de404bf7
keywords:
- 移除方法 Windows Media Player
- remove 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player、remove 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d341f8974255dab5e3cdce356a9b221eddff193c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999536"
---
# <a name="iwmpmediacollectionremove-method"></a><span data-ttu-id="ff7fa-106">IWMPMediaCollection：： remove 方法</span><span class="sxs-lookup"><span data-stu-id="ff7fa-106">IWMPMediaCollection::remove method</span></span>

<span data-ttu-id="ff7fa-107">`remove`方法會從媒體集合中移除指定的專案。</span><span class="sxs-lookup"><span data-stu-id="ff7fa-107">The `remove` method removes a specified item from the media collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff7fa-108">語法</span><span class="sxs-lookup"><span data-stu-id="ff7fa-108">Syntax</span></span>


```CSharp
public void remove(
  IWMPMedia pItem,
  System.Boolean varfDeleteFile
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPMedia, _
  ByVal varfDeleteFile As System.Boolean _
)
Implements IWMPMediaCollection.remove
```





## <a name="parameters"></a><span data-ttu-id="ff7fa-109">參數</span><span class="sxs-lookup"><span data-stu-id="ff7fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff7fa-110">*pItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff7fa-110">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff7fa-111">識別要移除之專案的 **WMPLib IWMPMedia** 介面。</span><span class="sxs-lookup"><span data-stu-id="ff7fa-111">A **WMPLib.IWMPMedia** interface that identifies the item to remove.</span></span>

</dd> <dt>

<span data-ttu-id="ff7fa-112">*varfDeleteFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff7fa-112">*varfDeleteFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff7fa-113">指定方法是否應從程式庫移除指定專案的 **布林** 值。</span><span class="sxs-lookup"><span data-stu-id="ff7fa-113">A **System.Boolean** value that specifies whether the method should remove the specified item from the library.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff7fa-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff7fa-114">Return value</span></span>

<span data-ttu-id="ff7fa-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ff7fa-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff7fa-116">備註</span><span class="sxs-lookup"><span data-stu-id="ff7fa-116">Remarks</span></span>

<span data-ttu-id="ff7fa-117">這個方法會從程式庫中刪除專案。</span><span class="sxs-lookup"><span data-stu-id="ff7fa-117">This method deletes an item from the library.</span></span> <span data-ttu-id="ff7fa-118">這個方法不會刪除使用者電腦中的檔案。</span><span class="sxs-lookup"><span data-stu-id="ff7fa-118">This method does not delete files from the user's computer.</span></span>

<span data-ttu-id="ff7fa-119">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="ff7fa-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="ff7fa-120">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="ff7fa-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ff7fa-121">範例</span><span class="sxs-lookup"><span data-stu-id="ff7fa-121">Examples</span></span>

<span data-ttu-id="ff7fa-122">下列範例會在提示使用者之後，使用來永久刪除媒體集合中的第一個媒體專案 `remove` 。</span><span class="sxs-lookup"><span data-stu-id="ff7fa-122">The following example, after prompting the user, permanently deletes the first media item in the media collection by using `remove`.</span></span> <span data-ttu-id="ff7fa-123">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="ff7fa-123">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first item from the media collection. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Store the name of the retrieved media item.
string mediaName = media.name;

// Prepare a message, a caption and buttons for the user prompt.
string message = ("OK to permanently delete " + mediaName + "?");
string caption = "Confirm deletion";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.OKCancel;

// Prompt the user for permission to delete the object.
System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

// Check the user response.
if (result == System.Windows.Forms.DialogResult.OK)
{
    // Permanently delete the item.
    player.mediaCollection.remove(media, true);

    // Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show("Deleted item " + mediaName);
}
```


```VB

' Get an interface to the first item from the media collection. 
Dim media As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Store the name of the retrieved media item.
Dim mediaName As String = media.name

&#39; Prepare a message, a caption and buttons for the user prompt.
Dim message As String = (&quot;OK to permanently delete &quot; + mediaName + &quot;?&quot;)
Dim caption As String = &quot;Confirm deletion&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.OKCancel

&#39; Prompt the user for permission to delete the object.
Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

&#39; Check the user response.
If (result = System.Windows.Forms.DialogResult.OK) Then

    &#39; Permanently delete the item.
    player.mediaCollection.remove(media, True)

    &#39; Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show(&quot;Deleted item &quot; + mediaName)

End If
```





## <a name="requirements"></a><span data-ttu-id="ff7fa-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff7fa-124">Requirements</span></span>



| <span data-ttu-id="ff7fa-125">需求</span><span class="sxs-lookup"><span data-stu-id="ff7fa-125">Requirement</span></span> | <span data-ttu-id="ff7fa-126">值</span><span class="sxs-lookup"><span data-stu-id="ff7fa-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff7fa-127">版本</span><span class="sxs-lookup"><span data-stu-id="ff7fa-127">Version</span></span><br/>   | <span data-ttu-id="ff7fa-128">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="ff7fa-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ff7fa-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="ff7fa-129">Namespace</span></span><br/> | <span data-ttu-id="ff7fa-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ff7fa-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ff7fa-131">組件</span><span class="sxs-lookup"><span data-stu-id="ff7fa-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ff7fa-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="ff7fa-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff7fa-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff7fa-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff7fa-134">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ff7fa-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ff7fa-135">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ff7fa-135">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ff7fa-136">**IWMPMediaCollection：新增 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ff7fa-136">**IWMPMediaCollection.add (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> </dl>

 

 





