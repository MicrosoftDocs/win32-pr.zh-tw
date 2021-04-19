---
title: IWMPCdrom driveSpecifier 屬性
description: DriveSpecifier 屬性會取得 CD 或 DVD 光碟機號。
ms.assetid: 8865232a-08a3-447b-a6d6-2bfda3a689e1
keywords:
- driveSpecifier 屬性 Windows Media Player
- driveSpecifier 屬性 Windows Media Player，IWMPCdrom 介面
- IWMPCdrom 介面 Windows Media Player，driveSpecifier 屬性
topic_type:
- apiref
api_name:
- IWMPCdrom.driveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a6c439523d90824da708700d48274f5a2e5ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978770"
---
# <a name="iwmpcdromdrivespecifier-property"></a><span data-ttu-id="48f94-106">IWMPCdrom：:d riveSpecifier 屬性</span><span class="sxs-lookup"><span data-stu-id="48f94-106">IWMPCdrom::driveSpecifier property</span></span>

<span data-ttu-id="48f94-107">**DriveSpecifier** 屬性會取得 CD 或 DVD 光碟機號。</span><span class="sxs-lookup"><span data-stu-id="48f94-107">The **driveSpecifier** property gets the CD or DVD drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="48f94-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="48f94-108">Syntax</span></span>


```CSharp
public System.String driveSpecifier {get; set;}
```


```VB

Public ReadOnly Property driveSpecifier As System.String
```





## <a name="property-value"></a><span data-ttu-id="48f94-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="48f94-109">Property value</span></span>

<span data-ttu-id="48f94-110">**System.string** ，表示磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="48f94-110">A **System.String** that is the drive letter.</span></span>

## <a name="remarks"></a><span data-ttu-id="48f94-111">備註</span><span class="sxs-lookup"><span data-stu-id="48f94-111">Remarks</span></span>

<span data-ttu-id="48f94-112">DVD 光碟機通常可以播放 CD 媒體，但 CD 光碟機無法播放 DVD 媒體。</span><span class="sxs-lookup"><span data-stu-id="48f94-112">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

<span data-ttu-id="48f94-113">這個屬性會在使用 **IWMPCdromCollection** 抓取的範圍內取得以零為基底之磁片磁碟機索引的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="48f94-113">This property gets a drive letter for a zero-based drive index within the range retrieved using **IWMPCdromCollection.count**.</span></span> <span data-ttu-id="48f94-114">抓取的值採用 *x*：形式，其中 *X* 代表磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="48f94-114">The value retrieved takes the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="48f94-115">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="48f94-115">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="48f94-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="48f94-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="48f94-117">範例</span><span class="sxs-lookup"><span data-stu-id="48f94-117">Examples</span></span>

<span data-ttu-id="48f94-118">下列範例會使用 **driveSpecifier** 來建立包含可用 CD 和 DVD 光碟機清單的字串，並在訊息方塊中顯示該字串。</span><span class="sxs-lookup"><span data-stu-id="48f94-118">The following example uses **driveSpecifier** to build a string that contains a list of available CD and DVD drives and displays that string in a message box.</span></span> <span data-ttu-id="48f94-119">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="48f94-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String that will contain the list of drive specifiers.
string MyDriveSpecifiers = "Drive letters found:  ";

// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives. 
for (int i = 0; i < numDrives; i++)
{
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier;
    MyDriveSpecifiers += " ";
}

// Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers);
```


```VB

'  String that will contain the list of drive specifiers.
Dim MyDriveSpecifiers As String = &quot;Drive letters found:  &quot;

&#39;  Store the number of available drives.
Dim numDrives = player.cdromCollection.count

&#39;  Loop through the available drives. 
For i As Integer = 0 To (numDrives - 1)
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier
    MyDriveSpecifiers += &quot; &quot;
Next i

&#39;  Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers)
```





## <a name="requirements"></a><span data-ttu-id="48f94-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="48f94-120">Requirements</span></span>



| <span data-ttu-id="48f94-121">需求</span><span class="sxs-lookup"><span data-stu-id="48f94-121">Requirement</span></span> | <span data-ttu-id="48f94-122">值</span><span class="sxs-lookup"><span data-stu-id="48f94-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48f94-123">版本</span><span class="sxs-lookup"><span data-stu-id="48f94-123">Version</span></span><br/>   | <span data-ttu-id="48f94-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="48f94-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="48f94-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="48f94-125">Namespace</span></span><br/> | <span data-ttu-id="48f94-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="48f94-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="48f94-127">組件</span><span class="sxs-lookup"><span data-stu-id="48f94-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="48f94-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="48f94-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48f94-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48f94-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48f94-130">**IWMPCdrom 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="48f94-130">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="48f94-131">**IWMPCdromCollection (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="48f94-131">**IWMPCdromCollection.count (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="48f94-132">**IWMPSettings2. mediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="48f94-132">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="48f94-133">**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="48f94-133">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





