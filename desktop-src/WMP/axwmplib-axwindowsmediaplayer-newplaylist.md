---
title: AxWindowsMediaPlayer. [] 方法
description: '[] 方法會傳回新播放清單的 IWMPPlaylist 介面。'
ms.assetid: caee8ee5-6201-474d-a4cb-80e574f84f0b
keywords:
- '[] 方法 Windows Media Player'
- '[] 方法 Windows Media Player，AxWindowsMediaPlayer 類別'
- AxWindowsMediaPlayer 類別 Windows Media Player，[] 方法
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc82be7aae37b4c1334b79f84e9d607b4f73cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984328"
---
# <a name="axwindowsmediaplayernewplaylist-method"></a><span data-ttu-id="460c8-106">AxWindowsMediaPlayer. [] 方法</span><span class="sxs-lookup"><span data-stu-id="460c8-106">AxWindowsMediaPlayer.newPlaylist method</span></span>

<span data-ttu-id="460c8-107">[] 方法會傳回新播放清單的 IWMPPlaylist 介面。</span><span class="sxs-lookup"><span data-stu-id="460c8-107">The newPlaylist method returns an IWMPPlaylist interface for a new playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="460c8-108">語法</span><span class="sxs-lookup"><span data-stu-id="460c8-108">Syntax</span></span>


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName,
  System.String bstrURL
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String, _
  ByVal bstrURL As System.String _
) As IWMPPlaylist
```





## <a name="parameters"></a><span data-ttu-id="460c8-109">參數</span><span class="sxs-lookup"><span data-stu-id="460c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="460c8-110">*bstrName*</span><span class="sxs-lookup"><span data-stu-id="460c8-110">*bstrName*</span></span> 
</dt> <dd>

<span data-ttu-id="460c8-111">**System.string** ，這是新播放清單的名稱。</span><span class="sxs-lookup"><span data-stu-id="460c8-111">The **System.String** that is the name of the new playlist.</span></span>

</dd> <dt>

<span data-ttu-id="460c8-112">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="460c8-112">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="460c8-113">**System.string** ，此為用來初始化新播放清單之 Windows Media 中繼檔播放清單的 URL。</span><span class="sxs-lookup"><span data-stu-id="460c8-113">The **System.String** that is the URL of the Windows Media metafile playlist that is used to initialize the new playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="460c8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="460c8-114">Return value</span></span>

<span data-ttu-id="460c8-115">WMPLib IWMPPlaylist 介面，代表新建立的播放清單。</span><span class="sxs-lookup"><span data-stu-id="460c8-115">A WMPLib.IWMPPlaylist interface that represents the newly created playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="460c8-116">備註</span><span class="sxs-lookup"><span data-stu-id="460c8-116">Remarks</span></span>

<span data-ttu-id="460c8-117">如果 *bstrURL* 參數為 null 或長度為零的字串 ( "" ) ，這個方法會建立空的 **播放清單**。</span><span class="sxs-lookup"><span data-stu-id="460c8-117">If the *bstrURL* parameter is a null or zero-length string (""), this method creates an empty **playlist**.</span></span> <span data-ttu-id="460c8-118">如果 *bstrName* 參數是長度為零的字串 ( "" ) ，這個方法會套用目前的中繼檔名稱。</span><span class="sxs-lookup"><span data-stu-id="460c8-118">If the *bstrName* parameter is a zero-length string (""), this method applies the current metafile name.</span></span>

<span data-ttu-id="460c8-119">使用這個方法建立的新播放清單，不會新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="460c8-119">The new playlist created with this method is not added to the library.</span></span> <span data-ttu-id="460c8-120">若要將新的播放清單新增至程式庫，請使用 IWMPPlaylistCollection。**importPlaylist** 或 IWMPPlaylistCollection。**[]**。</span><span class="sxs-lookup"><span data-stu-id="460c8-120">To add a new playlist to the library, use IWMPPlaylistCollection.**importPlaylist** or IWMPPlaylistCollection.**newPlaylist**.</span></span> <span data-ttu-id="460c8-121">新增至程式庫時，會自動移除播放清單名稱中的任何前置或尾端空格。</span><span class="sxs-lookup"><span data-stu-id="460c8-121">Any leading or trailing spaces in the playlist name are automatically removed when it is added to the library.</span></span>

<span data-ttu-id="460c8-122">由於程式庫允許多個具有相同名稱的播放清單，因此您可能會想要先檢查具有指定名稱的播放清單是否存在，然後再新增一個。</span><span class="sxs-lookup"><span data-stu-id="460c8-122">Because the library allows multiple playlists with the same name, you may want to check for the presence of a playlist with a given name before adding a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="460c8-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="460c8-123">Requirements</span></span>



| <span data-ttu-id="460c8-124">需求</span><span class="sxs-lookup"><span data-stu-id="460c8-124">Requirement</span></span> | <span data-ttu-id="460c8-125">值</span><span class="sxs-lookup"><span data-stu-id="460c8-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="460c8-126">版本</span><span class="sxs-lookup"><span data-stu-id="460c8-126">Version</span></span><br/>   | <span data-ttu-id="460c8-127">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="460c8-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="460c8-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="460c8-128">Namespace</span></span><br/> | <span data-ttu-id="460c8-129">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="460c8-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="460c8-130">組件</span><span class="sxs-lookup"><span data-stu-id="460c8-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="460c8-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="460c8-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="460c8-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="460c8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="460c8-133">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="460c8-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="460c8-134">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="460c8-134">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="460c8-135">**IWMPPlaylistCollection. importPlaylist (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="460c8-135">**IWMPPlaylistCollection.importPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> <dt>

<span data-ttu-id="460c8-136">[**IWMPPlaylistCollection. [] (VB 和 c # )**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)</span><span class="sxs-lookup"><span data-stu-id="460c8-136">[**IWMPPlaylistCollection.newPlaylist (VB and C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)</span></span>
</dt> </dl>

 

 





