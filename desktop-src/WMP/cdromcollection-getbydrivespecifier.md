---
title: CdromCollection. getByDriveSpecifier 方法
description: GetByDriveSpecifier 方法會抓取與特定磁碟機號相關聯的 Cdrom 物件。
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- getByDriveSpecifier 方法 Windows Media Player
- getByDriveSpecifier 方法 Windows Media Player，CdromCollection 類別
- CdromCollection 類別 Windows Media Player，getByDriveSpecifier 方法
topic_type:
- apiref
api_name:
- CdromCollection.getByDriveSpecifier
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807b44a7be97ac93b5b0f270c2d1723404887c9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993660"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a><span data-ttu-id="0898e-106">CdromCollection. getByDriveSpecifier 方法</span><span class="sxs-lookup"><span data-stu-id="0898e-106">CdromCollection.getByDriveSpecifier method</span></span>

<span data-ttu-id="0898e-107">**GetByDriveSpecifier** 方法會抓取與特定磁碟機號相關聯的 **Cdrom** 物件。</span><span class="sxs-lookup"><span data-stu-id="0898e-107">The **getByDriveSpecifier** method retrieves the **Cdrom** object associated with a particular drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="0898e-108">語法</span><span class="sxs-lookup"><span data-stu-id="0898e-108">Syntax</span></span>


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a><span data-ttu-id="0898e-109">參數</span><span class="sxs-lookup"><span data-stu-id="0898e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0898e-110">*driveSpecifier* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0898e-110">*driveSpecifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0898e-111">**字串** ，包含後面接著冒號 ( "：" ) 字元的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="0898e-111">**String** containing the drive letter followed by a colon (":") character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0898e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0898e-112">Return value</span></span>

<span data-ttu-id="0898e-113">這個方法會傳回一個 **Cdrom** 物件。</span><span class="sxs-lookup"><span data-stu-id="0898e-113">This method returns a **Cdrom** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0898e-114">備註</span><span class="sxs-lookup"><span data-stu-id="0898e-114">Remarks</span></span>

<span data-ttu-id="0898e-115">磁碟機號必須以 *x*：形式提供，其中 *X* 代表磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="0898e-115">Drive letters must be given in the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="0898e-116">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="0898e-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="0898e-117">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="0898e-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="0898e-118">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0898e-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="0898e-119">範例</span><span class="sxs-lookup"><span data-stu-id="0898e-119">Examples</span></span>

<span data-ttu-id="0898e-120">下列 JScript 範例會使用 *CdromCollection*。**getByDriveSpecifier** ，以取得對應至使用者所提供之磁碟機號的 **Cdrom** 物件。</span><span class="sxs-lookup"><span data-stu-id="0898e-120">The following JScript example uses *CdromCollection*.**getByDriveSpecifier** to retrieve the **Cdrom** object that corresponds to a drive letter provided by the user.</span></span> <span data-ttu-id="0898e-121">已建立 HTML 文字元素，名稱 = "MyText"，用於使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="0898e-121">An HTML text element was created, with NAME = "MyText", for user input.</span></span> <span data-ttu-id="0898e-122">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="0898e-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the drive letter provided by the user.
var DriveLetter = MyText.value;

// Append a colon to the drive letter to create a valid drive specifier.
DriveLetter += ":";

// Get the Cdrom object using the drive specifier.
var Drive = Player.cdRomCollection.getByDriveSpecifier(DriveLetter);

// Use the Cdrom object to open the drive door.
Drive.eject();
```



## <a name="requirements"></a><span data-ttu-id="0898e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0898e-123">Requirements</span></span>



| <span data-ttu-id="0898e-124">需求</span><span class="sxs-lookup"><span data-stu-id="0898e-124">Requirement</span></span> | <span data-ttu-id="0898e-125">值</span><span class="sxs-lookup"><span data-stu-id="0898e-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0898e-126">版本</span><span class="sxs-lookup"><span data-stu-id="0898e-126">Version</span></span><br/> | <span data-ttu-id="0898e-127">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0898e-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0898e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0898e-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="0898e-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0898e-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0898e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0898e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0898e-131">**Cdrom 物件**</span><span class="sxs-lookup"><span data-stu-id="0898e-131">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="0898e-132">**Cdrom. 退出**</span><span class="sxs-lookup"><span data-stu-id="0898e-132">**Cdrom.eject**</span></span>](cdrom-eject.md)
</dt> <dt>

[<span data-ttu-id="0898e-133">**CdromCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="0898e-133">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="0898e-134">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="0898e-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="0898e-135">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="0898e-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





