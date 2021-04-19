---
title: IWMPCdromCollection getByDriveSpecifier 方法
description: GetByDriveSpecifier 方法會傳回與特定磁碟機號相關聯的 IWMPCdrom 介面。
ms.assetid: 4a550eb1-a37e-43fd-9e08-801c4fd64e68
keywords:
- getByDriveSpecifier 方法 Windows Media Player
- getByDriveSpecifier 方法 Windows Media Player，IWMPCdromCollection 介面
- IWMPCdromCollection 介面 Windows Media Player，getByDriveSpecifier 方法
topic_type:
- apiref
api_name:
- IWMPCdromCollection.getByDriveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe771fc893d4bf43b82dc825a2d33724926e8151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997005"
---
# <a name="iwmpcdromcollectiongetbydrivespecifier-method"></a><span data-ttu-id="5de92-106">IWMPCdromCollection：： getByDriveSpecifier 方法</span><span class="sxs-lookup"><span data-stu-id="5de92-106">IWMPCdromCollection::getByDriveSpecifier method</span></span>

<span data-ttu-id="5de92-107">**GetByDriveSpecifier** 方法會傳回與特定磁碟機號相關聯的 **IWMPCdrom** 介面。</span><span class="sxs-lookup"><span data-stu-id="5de92-107">The **getByDriveSpecifier** method returns an **IWMPCdrom** interface associated with a particular drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="5de92-108">語法</span><span class="sxs-lookup"><span data-stu-id="5de92-108">Syntax</span></span>


```CSharp
public IWMPCdrom getByDriveSpecifier(
  System.String bstrDriveSpecifier
);
```


```VB

Public Function getByDriveSpecifier( _
  ByVal bstrDriveSpecifier As System.String _
) As IWMPCdrom
Implements IWMPCdromCollection.getByDriveSpecifier
```





## <a name="parameters"></a><span data-ttu-id="5de92-109">參數</span><span class="sxs-lookup"><span data-stu-id="5de92-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5de92-110">*bstrDriveSpecifier* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5de92-110">*bstrDriveSpecifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5de92-111">**System.string** ，後面接著冒號 ( "：" ) 字元的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="5de92-111">A **System.String** that is the drive letter followed by a colon (":") character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5de92-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5de92-112">Return value</span></span>

<span data-ttu-id="5de92-113">**WMPLib IWMPCdrom** 介面。</span><span class="sxs-lookup"><span data-stu-id="5de92-113">A **WMPLib.IWMPCdrom** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="5de92-114">備註</span><span class="sxs-lookup"><span data-stu-id="5de92-114">Remarks</span></span>

<span data-ttu-id="5de92-115">磁碟機號必須以 *x*：形式提供，其中 *X* 代表磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="5de92-115">Drive letters must be given in the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="5de92-116">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="5de92-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="5de92-117">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="5de92-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5de92-118">範例</span><span class="sxs-lookup"><span data-stu-id="5de92-118">Examples</span></span>

<span data-ttu-id="5de92-119">下列範例會使用 **getByDriveSpecifier** 來取得對應至使用者在文字方塊中所提供之磁碟機號的 **IWMPCdrom** 介面。</span><span class="sxs-lookup"><span data-stu-id="5de92-119">The following example uses **getByDriveSpecifier** to get the **IWMPCdrom** interface that corresponds to a drive letter provided by the user in a text box.</span></span> <span data-ttu-id="5de92-120">接著會呼叫 **IWMPCdrom 取出** 方法來退出指定的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="5de92-120">The **IWMPCdrom.eject** method is then called to eject the specified drive.</span></span> <span data-ttu-id="5de92-121">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="5de92-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store the drive letter provided by the user.
string driveLetter = myText.Text;

// Append a colon to the drive letter to create a valid drive specifier.
driveLetter += ":";

// Get an IWMPCdrom interface for the drive.
WMPLib.IWMPCdrom drive = player.cdromCollection.getByDriveSpecifier(driveLetter);

// Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject();
```


```VB

' Store the drive letter provided by the user.
Dim driveLetter As String = myText.Text

&#39; Append a colon to the drive letter to create a valid drive specifier.
driveLetter += &quot;:&quot;

&#39; Get an IWMPCdrom interface for the drive.
Dim drive As WMPLib.IWMPCdrom = player.cdromCollection.getByDriveSpecifier(driveLetter)

&#39; Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject()
```





## <a name="requirements"></a><span data-ttu-id="5de92-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5de92-122">Requirements</span></span>



| <span data-ttu-id="5de92-123">需求</span><span class="sxs-lookup"><span data-stu-id="5de92-123">Requirement</span></span> | <span data-ttu-id="5de92-124">值</span><span class="sxs-lookup"><span data-stu-id="5de92-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5de92-125">版本</span><span class="sxs-lookup"><span data-stu-id="5de92-125">Version</span></span><br/>   | <span data-ttu-id="5de92-126">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="5de92-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5de92-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="5de92-127">Namespace</span></span><br/> | <span data-ttu-id="5de92-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5de92-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5de92-129">組件</span><span class="sxs-lookup"><span data-stu-id="5de92-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5de92-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="5de92-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5de92-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5de92-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5de92-132">**IWMPCdrom 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5de92-132">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5de92-133">**IWMPCdrom (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5de92-133">**IWMPCdrom.eject (VB and C#)**</span></span>](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5de92-134">**IWMPCdromCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5de92-134">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5de92-135">**IWMPSettings2. mediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5de92-135">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5de92-136">**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5de92-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





