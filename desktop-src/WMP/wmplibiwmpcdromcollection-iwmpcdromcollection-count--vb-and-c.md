---
title: IWMPCdromCollection count 屬性
description: Count 屬性會取得系統上的可用 CD 和 DVD 光碟機數目。
ms.assetid: 1359ab7e-fbe3-461c-801b-7c986f6e5687
keywords:
- count 屬性 Windows Media Player
- count 屬性 Windows Media Player，IWMPCdromCollection 介面
- IWMPCdromCollection 介面 Windows Media Player，count 屬性
topic_type:
- apiref
api_name:
- IWMPCdromCollection.count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2da4d4d443c730d19c791a486fed4be0241b8c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992977"
---
# <a name="iwmpcdromcollectioncount-property"></a><span data-ttu-id="c638c-106">IWMPCdromCollection：： count 屬性</span><span class="sxs-lookup"><span data-stu-id="c638c-106">IWMPCdromCollection::count property</span></span>

<span data-ttu-id="c638c-107">**Count** 屬性會取得系統上的可用 CD 和 DVD 光碟機數目。</span><span class="sxs-lookup"><span data-stu-id="c638c-107">The **count** property gets the number of available CD and DVD drives on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="c638c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c638c-108">Syntax</span></span>


```CSharp
public System.Int32 count {get; set;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="c638c-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="c638c-109">Property value</span></span>

<span data-ttu-id="c638c-110">是可用磁片磁碟機計數的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="c638c-110">A **System.Int32** that is the count of available drives.</span></span>

## <a name="remarks"></a><span data-ttu-id="c638c-111">備註</span><span class="sxs-lookup"><span data-stu-id="c638c-111">Remarks</span></span>

<span data-ttu-id="c638c-112">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="c638c-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="c638c-113">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="c638c-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="c638c-114">DVD 磁片磁碟機的計算方式與 CD 光碟機完全一樣。</span><span class="sxs-lookup"><span data-stu-id="c638c-114">DVD drives are counted exactly like CD drives.</span></span> <span data-ttu-id="c638c-115">不過，Windows Media Player ActiveX 控制項只支援 Windows XP 或更新版本的 DVD 功能。</span><span class="sxs-lookup"><span data-stu-id="c638c-115">However, the Windows Media Player ActiveX control only supports DVD functionality for Windows XP or later.</span></span> <span data-ttu-id="c638c-116">DVD 光碟機通常可以播放 CD 媒體，但 CD 光碟機無法播放 DVD 媒體。</span><span class="sxs-lookup"><span data-stu-id="c638c-116">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

## <a name="examples"></a><span data-ttu-id="c638c-117">範例</span><span class="sxs-lookup"><span data-stu-id="c638c-117">Examples</span></span>

<span data-ttu-id="c638c-118">下列範例會使用 count 來顯示訊息方塊中可用 CD 和 DVD 光碟機的數目。</span><span class="sxs-lookup"><span data-stu-id="c638c-118">The following example uses count to display the number of available CD and DVD drives in a message box.</span></span> <span data-ttu-id="c638c-119">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="c638c-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show("Number of available CD and DVD drives:  " + numDrives.ToString());
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show(&quot;Number of available CD and DVD drives:  &quot; + numDrives.ToString())
```





## <a name="requirements"></a><span data-ttu-id="c638c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c638c-120">Requirements</span></span>



| <span data-ttu-id="c638c-121">需求</span><span class="sxs-lookup"><span data-stu-id="c638c-121">Requirement</span></span> | <span data-ttu-id="c638c-122">值</span><span class="sxs-lookup"><span data-stu-id="c638c-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c638c-123">版本</span><span class="sxs-lookup"><span data-stu-id="c638c-123">Version</span></span><br/>   | <span data-ttu-id="c638c-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="c638c-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c638c-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="c638c-125">Namespace</span></span><br/> | <span data-ttu-id="c638c-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c638c-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c638c-127">組件</span><span class="sxs-lookup"><span data-stu-id="c638c-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c638c-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="c638c-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c638c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c638c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c638c-130">**IWMPCdromCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="c638c-130">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c638c-131">**IWMPSettings2. mediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="c638c-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c638c-132">**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="c638c-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





