---
title: IWMPCdromCollection Item 方法
description: Item 方法會傳回指定索引處的 IWMPCdrom 介面。
ms.assetid: 66e51aa9-39c8-4b79-9cc7-d7125516e87e
keywords:
- Item 方法 Windows Media Player
- Item 方法 Windows Media Player，IWMPCdromCollection 介面
- IWMPCdromCollection 介面 Windows Media Player，Item 方法
topic_type:
- apiref
api_name:
- IWMPCdromCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf0c4a0c79a17b1e6956ba640daec74f0cbb2825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992963"
---
# <a name="iwmpcdromcollectionitem-method"></a><span data-ttu-id="d37f2-106">IWMPCdromCollection：： Item 方法</span><span class="sxs-lookup"><span data-stu-id="d37f2-106">IWMPCdromCollection::Item method</span></span>

<span data-ttu-id="d37f2-107">**Item** 方法會傳回指定索引處的 **IWMPCdrom** 介面。</span><span class="sxs-lookup"><span data-stu-id="d37f2-107">The **Item** method returns an **IWMPCdrom** interface at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="d37f2-108">語法</span><span class="sxs-lookup"><span data-stu-id="d37f2-108">Syntax</span></span>


```CSharp
public IWMPCdrom Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPCdrom
Implements IWMPCdromCollection.Item
```





## <a name="parameters"></a><span data-ttu-id="d37f2-109">參數</span><span class="sxs-lookup"><span data-stu-id="d37f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d37f2-110">*lIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d37f2-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d37f2-111">作為索引的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="d37f2-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d37f2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d37f2-112">Return value</span></span>

<span data-ttu-id="d37f2-113">**WMPLib IWMPCdrom** 介面。</span><span class="sxs-lookup"><span data-stu-id="d37f2-113">A **WMPLib.IWMPCdrom** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="d37f2-114">備註</span><span class="sxs-lookup"><span data-stu-id="d37f2-114">Remarks</span></span>

<span data-ttu-id="d37f2-115">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="d37f2-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="d37f2-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="d37f2-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d37f2-117">範例</span><span class="sxs-lookup"><span data-stu-id="d37f2-117">Examples</span></span>

<span data-ttu-id="d37f2-118">下列範例會使用 **專案** ，在清單方塊中顯示電腦上每個可用 CD 的磁片磁碟機規範和播放清單名稱。</span><span class="sxs-lookup"><span data-stu-id="d37f2-118">The following example uses **Item** to display the drive specifier and playlist name from each CD available on the computer in a list box.</span></span> <span data-ttu-id="d37f2-119">如果磁片磁碟機實際包含 DVD 內容，則需要 Windows XP 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d37f2-119">If the drive actually contains DVD content, Windows XP or later is required.</span></span> <span data-ttu-id="d37f2-120">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="d37f2-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives.
for (int i = 0; i < numDrives; i++)
{
    // Store the drive specifier and playlist name for this drive in a string.
    string pl = player.cdromCollection.Item(i).driveSpecifier + " ";
    pl += player.cdromCollection.Item(i).Playlist.name;

    // Add the string to a list box.
    myPlaylists.Items.Add(pl);
}
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Loop through the available drives.
For i As Integer = 0 To (numDrives - 1)

    &#39; Store the drive specifier and playlist name for this drive in a string.
    Dim pl As String = player.cdromCollection.Item(i).driveSpecifier + &quot; &quot;
    pl += player.cdromCollection.Item(i).Playlist.name

    &#39; Add the string to a list box.
    myPlaylists.Items.Add(pl)

Next i
```





## <a name="requirements"></a><span data-ttu-id="d37f2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d37f2-121">Requirements</span></span>



| <span data-ttu-id="d37f2-122">需求</span><span class="sxs-lookup"><span data-stu-id="d37f2-122">Requirement</span></span> | <span data-ttu-id="d37f2-123">值</span><span class="sxs-lookup"><span data-stu-id="d37f2-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d37f2-124">版本</span><span class="sxs-lookup"><span data-stu-id="d37f2-124">Version</span></span><br/>   | <span data-ttu-id="d37f2-125">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="d37f2-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d37f2-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="d37f2-126">Namespace</span></span><br/> | <span data-ttu-id="d37f2-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d37f2-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d37f2-128">組件</span><span class="sxs-lookup"><span data-stu-id="d37f2-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d37f2-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="d37f2-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d37f2-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d37f2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d37f2-131">**IWMPCdrom 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d37f2-131">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d37f2-132">**IWMPCdromCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d37f2-132">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d37f2-133">**IWMPCdromCollection (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d37f2-133">**IWMPCdromCollection.count (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d37f2-134">**IWMPCdromCollection. getByDriveSpecifier (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d37f2-134">**IWMPCdromCollection.getByDriveSpecifier (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d37f2-135">**IWMPPlaylist.name (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d37f2-135">**IWMPPlaylist.name (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d37f2-136">**IWMPSettings2. mediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d37f2-136">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d37f2-137">**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d37f2-137">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





