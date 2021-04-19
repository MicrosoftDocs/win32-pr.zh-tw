---
title: Cdrom. 退出方法
description: 退出方法會從磁片磁碟機中取出 CD 或 DVD。 |Cdrom. 退出方法
ms.assetid: f43c7f10-7de2-488c-833a-ecd3ac21744b
keywords:
- 退出方法 Windows Media Player
- 退出方法 Windows Media Player、Cdrom 類別
- Cdrom 類別 Windows Media Player、退出方法
topic_type:
- apiref
api_name:
- Cdrom.eject
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78326ca57dcf097344fc073681fae772222ea9ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106989153"
---
# <a name="cdromeject-method"></a><span data-ttu-id="5977c-107">Cdrom. 退出方法</span><span class="sxs-lookup"><span data-stu-id="5977c-107">Cdrom.eject method</span></span>

<span data-ttu-id="5977c-108">**退出** 方法會從磁片磁碟機中取出 CD 或 DVD。</span><span class="sxs-lookup"><span data-stu-id="5977c-108">The **eject** method ejects the CD or DVD from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="5977c-109">語法</span><span class="sxs-lookup"><span data-stu-id="5977c-109">Syntax</span></span>


```JScript
Cdrom.eject()
```



## <a name="parameters"></a><span data-ttu-id="5977c-110">參數</span><span class="sxs-lookup"><span data-stu-id="5977c-110">Parameters</span></span>

<span data-ttu-id="5977c-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5977c-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5977c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5977c-112">Return value</span></span>

<span data-ttu-id="5977c-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5977c-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5977c-114">備註</span><span class="sxs-lookup"><span data-stu-id="5977c-114">Remarks</span></span>

<span data-ttu-id="5977c-115">如果磁片磁碟機門已開啟，這個方法會關閉門。</span><span class="sxs-lookup"><span data-stu-id="5977c-115">If the drive door is open, this method closes the door.</span></span>

<span data-ttu-id="5977c-116">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="5977c-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="5977c-117">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="5977c-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="5977c-118">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="5977c-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="5977c-119">範例</span><span class="sxs-lookup"><span data-stu-id="5977c-119">Examples</span></span>

<span data-ttu-id="5977c-120">下列範例會建立使用 *Cdrom* 的 HTML button 專案。**退出** 以開啟磁片磁碟機規範索引為零之磁片磁碟機的門。</span><span class="sxs-lookup"><span data-stu-id="5977c-120">The following example creates an HTML button element that uses *Cdrom*.**eject** to open the door of the drive that has drive specifier index zero.</span></span> <span data-ttu-id="5977c-121">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="5977c-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"
       NAME = "EJECTBUTTON"
       VALUE = "EJECT"
       OnClick =  "Player.cdromCollection.item(0).eject()"
>
```



## <a name="requirements"></a><span data-ttu-id="5977c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5977c-122">Requirements</span></span>



| <span data-ttu-id="5977c-123">需求</span><span class="sxs-lookup"><span data-stu-id="5977c-123">Requirement</span></span> | <span data-ttu-id="5977c-124">值</span><span class="sxs-lookup"><span data-stu-id="5977c-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5977c-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5977c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5977c-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5977c-126">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5977c-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5977c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5977c-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5977c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5977c-129">版本</span><span class="sxs-lookup"><span data-stu-id="5977c-129">Version</span></span><br/>                  | <span data-ttu-id="5977c-130">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="5977c-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5977c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5977c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5977c-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5977c-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5977c-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5977c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5977c-134">**Cdrom 物件**</span><span class="sxs-lookup"><span data-stu-id="5977c-134">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="5977c-135">**PlayState**</span><span class="sxs-lookup"><span data-stu-id="5977c-135">**Player.playState**</span></span>](player-playstate.md)
</dt> <dt>

[<span data-ttu-id="5977c-136">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5977c-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5977c-137">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5977c-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





