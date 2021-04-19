---
title: DurationString
description: DurationString 屬性會抓取字串值，指出目前媒體專案的持續時間（以 HH MM SS 格式表示）。
ms.assetid: dfcb4c2e-c62c-4c3e-a9f4-fd147fb5b28c
keywords:
- DurationString Windows Media Player
topic_type:
- apiref
api_name:
- Media.durationString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1bbb89716ab1d06b176754396611ab22980659
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983154"
---
# <a name="mediadurationstring"></a><span data-ttu-id="22824-104">DurationString</span><span class="sxs-lookup"><span data-stu-id="22824-104">Media.durationString</span></span>

<span data-ttu-id="22824-105">**DurationString** 屬性會抓取 **字串** 值，以 HH： MM： SS 格式指出目前媒體專案的持續時間。</span><span class="sxs-lookup"><span data-stu-id="22824-105">The **durationString** property retrieves a **String** value indicating the duration of the current media item in HH:MM:SS format.</span></span>

## <a name="syntax"></a><span data-ttu-id="22824-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="22824-106">Syntax</span></span>

<span data-ttu-id="22824-107">*玩家*。*currentMedia*。**durationString**</span><span class="sxs-lookup"><span data-stu-id="22824-107">*player*.*currentMedia*.**durationString**</span></span>

## <a name="possible-values"></a><span data-ttu-id="22824-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="22824-108">Possible Values</span></span>

<span data-ttu-id="22824-109">這個屬性是唯讀 **字串**。</span><span class="sxs-lookup"><span data-stu-id="22824-109">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="22824-110">備註</span><span class="sxs-lookup"><span data-stu-id="22824-110">Remarks</span></span>

<span data-ttu-id="22824-111">如果這個屬性與 media 專案一起使用，而不是 *播放* 程式中指定的媒體專案。**currentMedia**，它可能不包含有效的值。</span><span class="sxs-lookup"><span data-stu-id="22824-111">If this property is used with a media item other than the one specified in *Player*.**currentMedia**, it may not contain a valid value.</span></span> <span data-ttu-id="22824-112">如果媒體專案的長度不到一小時，則會省略傳回值的 HH：部分。</span><span class="sxs-lookup"><span data-stu-id="22824-112">If the media item is less than an hour long, the HH: portion of the return value is omitted.</span></span>

<span data-ttu-id="22824-113">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="22824-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="22824-114">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="22824-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="22824-115">範例</span><span class="sxs-lookup"><span data-stu-id="22824-115">Examples</span></span>

<span data-ttu-id="22824-116">下列 JScript 範例會使用 *媒體*。**durationString** ，以格式化的文字顯示目前媒體專案的持續時間。</span><span class="sxs-lookup"><span data-stu-id="22824-116">The following JScript example uses *Media*.**durationString** to display the duration of the current media item as formatted text.</span></span> <span data-ttu-id="22824-117">名為 Mediainfo.xml 的 HTML DIV 元素會顯示持續時間資訊。</span><span class="sxs-lookup"><span data-stu-id="22824-117">An HTML DIV element named MediaInfo displays the duration information.</span></span> <span data-ttu-id="22824-118">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="22824-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler to update the display when
 the current media item changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Write the formatted duration string to the DIV region.
   MediaInfo.innerHTML = "Duration: " + Player.currentMedia.durationString;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="22824-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="22824-119">Requirements</span></span>



| <span data-ttu-id="22824-120">需求</span><span class="sxs-lookup"><span data-stu-id="22824-120">Requirement</span></span> | <span data-ttu-id="22824-121">值</span><span class="sxs-lookup"><span data-stu-id="22824-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="22824-122">版本</span><span class="sxs-lookup"><span data-stu-id="22824-122">Version</span></span><br/> | <span data-ttu-id="22824-123">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="22824-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="22824-124">DLL</span><span class="sxs-lookup"><span data-stu-id="22824-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="22824-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22824-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22824-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22824-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22824-127">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="22824-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="22824-128">**Media. duration**</span><span class="sxs-lookup"><span data-stu-id="22824-128">**Media.duration**</span></span>](media-duration.md)
</dt> <dt>

[<span data-ttu-id="22824-129">**CurrentMedia**</span><span class="sxs-lookup"><span data-stu-id="22824-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="22824-130">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="22824-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="22824-131">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="22824-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





