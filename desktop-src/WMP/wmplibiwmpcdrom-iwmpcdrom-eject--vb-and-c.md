---
title: IWMPCdrom 退出方法
description: 退出方法會從磁片磁碟機中取出 CD 或 DVD。 |IWMPCdrom 退出方法
ms.assetid: c0a69252-fd79-452c-bc61-3c3e8bcaaf48
keywords:
- 退出方法 Windows Media Player
- 退出方法 Windows Media Player，IWMPCdrom 介面
- IWMPCdrom 介面 Windows Media Player、退出方法
topic_type:
- apiref
api_name:
- IWMPCdrom.eject
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ca2403b86b648e98861d91a21db80ddb64aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984124"
---
# <a name="iwmpcdromeject-method"></a><span data-ttu-id="ebf89-107">IWMPCdrom：：退出方法</span><span class="sxs-lookup"><span data-stu-id="ebf89-107">IWMPCdrom::eject method</span></span>

<span data-ttu-id="ebf89-108">**退出** 方法會從磁片磁碟機中取出 CD 或 DVD。</span><span class="sxs-lookup"><span data-stu-id="ebf89-108">The **eject** method ejects the CD or DVD from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebf89-109">語法</span><span class="sxs-lookup"><span data-stu-id="ebf89-109">Syntax</span></span>


```CSharp
public void eject();
```


```VB

Public Sub eject()
Implements IWMPCdrom.eject
```





## <a name="parameters"></a><span data-ttu-id="ebf89-110">參數</span><span class="sxs-lookup"><span data-stu-id="ebf89-110">Parameters</span></span>

<span data-ttu-id="ebf89-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ebf89-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ebf89-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ebf89-112">Return value</span></span>

<span data-ttu-id="ebf89-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ebf89-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebf89-114">備註</span><span class="sxs-lookup"><span data-stu-id="ebf89-114">Remarks</span></span>

<span data-ttu-id="ebf89-115">如果磁片磁碟機門已開啟，這個方法會關閉門。</span><span class="sxs-lookup"><span data-stu-id="ebf89-115">If the drive door is open, this method closes the door.</span></span>

<span data-ttu-id="ebf89-116">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="ebf89-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="ebf89-117">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="ebf89-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ebf89-118">範例</span><span class="sxs-lookup"><span data-stu-id="ebf89-118">Examples</span></span>

<span data-ttu-id="ebf89-119">下列範例會使用「 **退出** 」來開啟索引為零的 CD 或 DVD 光碟機的門，以回應按鈕的 Click 事件。</span><span class="sxs-lookup"><span data-stu-id="ebf89-119">The following example uses **eject** to open the door of the CD or DVD drive that has the index of zero in response to the Click event of a button.</span></span> <span data-ttu-id="ebf89-120">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="ebf89-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void ejectButton_Click(object o, System.EventArgs args)
{
    player.cdromCollection.Item(0).eject();
}
```


```VB

Public Sub ejectButton_Click(ByVal o As Object, ByVal args As System.EventArgs) Handles ejectButton.Click

    player.cdromCollection.Item(0).eject()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="ebf89-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebf89-121">Requirements</span></span>



| <span data-ttu-id="ebf89-122">需求</span><span class="sxs-lookup"><span data-stu-id="ebf89-122">Requirement</span></span> | <span data-ttu-id="ebf89-123">值</span><span class="sxs-lookup"><span data-stu-id="ebf89-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf89-124">版本</span><span class="sxs-lookup"><span data-stu-id="ebf89-124">Version</span></span><br/>   | <span data-ttu-id="ebf89-125">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="ebf89-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ebf89-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="ebf89-126">Namespace</span></span><br/> | <span data-ttu-id="ebf89-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ebf89-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ebf89-128">組件</span><span class="sxs-lookup"><span data-stu-id="ebf89-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ebf89-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="ebf89-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebf89-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebf89-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf89-131">**AxWindowsMediaPlayer. playState (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ebf89-131">**AxWindowsMediaPlayer.playState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ebf89-132">**IWMPCdrom 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ebf89-132">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ebf89-133">**IWMPSettings2. mediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ebf89-133">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ebf89-134">**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ebf89-134">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





