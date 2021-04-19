---
title: ClosedCaption.SAMIFileName
description: SAMIFileName 屬性會指定或抓取包含隱藏式輔助字幕所需資訊的檔案名。
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- ClosedCaption. SAMIFileName Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIFileName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd748076eec80b5b7d97e7c041f454c4f9193f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984012"
---
# <a name="closedcaptionsamifilename"></a><span data-ttu-id="8a109-104">ClosedCaption.SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="8a109-104">ClosedCaption.SAMIFileName</span></span>

<span data-ttu-id="8a109-105">**SAMIFileName** 屬性會指定或抓取包含隱藏式輔助字幕所需資訊的檔案名。</span><span class="sxs-lookup"><span data-stu-id="8a109-105">The **SAMIFileName** property specifies or retrieves the name of the file containing the information needed for closed captioning.</span></span>

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a><span data-ttu-id="8a109-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="8a109-106">Possible Values</span></span>

<span data-ttu-id="8a109-107">這個屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="8a109-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a109-108">備註</span><span class="sxs-lookup"><span data-stu-id="8a109-108">Remarks</span></span>

<span data-ttu-id="8a109-109">已同步處理的可存取媒體交換 (薩米) 檔案必須使用 smi-s 或薩米文的副檔名。</span><span class="sxs-lookup"><span data-stu-id="8a109-109">The Synchronized Accessible Media Interchange (SAMI) file must use an .smi or .sami file name extension.</span></span>

<span data-ttu-id="8a109-110">如果您未指定 **SAMIFileName** 的值，此屬性會抓取包含與目前媒體專案相關聯之檔案名或 URL 的字串。</span><span class="sxs-lookup"><span data-stu-id="8a109-110">If you don't specify a value for **SAMIFileName**, this property retrieves a string containing the file name or URL associated with the current media item.</span></span> <span data-ttu-id="8a109-111">當您使用 *薩米* 文 URL 參數指定薩米文的檔案時，或當薩米文的檔案與數位媒體檔案名 (（副檔名) 除外）時，就可能會發生此關聯。</span><span class="sxs-lookup"><span data-stu-id="8a109-111">This association can occur when a SAMI file is specified using the *sami* URL parameter, or automatically when the SAMI file has the same name as the digital media file name (except for the file name extension).</span></span> <span data-ttu-id="8a109-112">如果目前的媒體沒有相關聯的薩米文檔案，這個屬性會 )  ( 的空字串。</span><span class="sxs-lookup"><span data-stu-id="8a109-112">If there is no SAMI file associated with the current media, this property retrieves an empty string ("").</span></span>

<span data-ttu-id="8a109-113">一旦您指定 **SAMIFileName** 的值，該值就會持續，直到您指定新值為止 (或直到使用 *薩米* 文 URL 參數) 開啟新的媒體專案為止。</span><span class="sxs-lookup"><span data-stu-id="8a109-113">Once you specify a value for **SAMIFileName**, that value persists until you specify a new value (or until a new media item is opened using the *sami* URL parameter).</span></span> <span data-ttu-id="8a109-114">因此，在播放每個新媒體專案之前，您必須為這個屬性指定新的值。</span><span class="sxs-lookup"><span data-stu-id="8a109-114">Therefore, you must specify a new value for this property before you play each new media item.</span></span> <span data-ttu-id="8a109-115">如此一來，當下一個媒體專案 (或 *播放* 程式開啟時， **SAMIFileName** 的新值就會生效。**close** 稱為) 。</span><span class="sxs-lookup"><span data-stu-id="8a109-115">That way, the new value for **SAMIFileName** will take effect when the next media item is opened (or when *Player*.**close** is called).</span></span> <span data-ttu-id="8a109-116">為 **SAMIFileName** 指定新的值對目前的媒體沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="8a109-116">Specifying a new value for **SAMIFileName** has no effect for the current media.</span></span>

<span data-ttu-id="8a109-117">若要使 Windows Media Player 使用與特定媒體專案相關聯的薩米文檔案傳回，請在播放下一個媒體專案之前，指定 **SAMIFileName** 等於空字串 ( "" ) 的值。</span><span class="sxs-lookup"><span data-stu-id="8a109-117">To cause Windows Media Player to return to using the SAMI file associated with a particular media item, specify a value for **SAMIFileName** equal to an empty string ("") before you play the next media item.</span></span>

<span data-ttu-id="8a109-118">**Windows Media Player 10** 行動裝置版：這個屬性是唯讀的，而且一律會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="8a109-118">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="8a109-119">範例</span><span class="sxs-lookup"><span data-stu-id="8a109-119">Examples</span></span>

<span data-ttu-id="8a109-120">下列三個 JScript 範例使用 *ClosedCaption*。**SAMIFileName** 指定隱藏式輔助字幕文字檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a109-120">The following three JScript examples use *ClosedCaption*.**SAMIFileName** to specify the name of a closed caption text file.</span></span> <span data-ttu-id="8a109-121">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="8a109-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Display the closed captions from a website.
Player.closedCaption.SAMIFileName="https://www.proseware.com/ccsample.smi";

// Display the closed captions from a local network.
// You must add an escape sequence of a backslash for every original backslash.
Player.closedCaption.SAMIFileName="\\\\yourservername\\Public\\ccsample.smi";

// Display the closed captions from a file on a local drive.
// Be sure to add the appropriate escape sequences.
Player.closedCaption.SAMIFileName="C:\\WMSDK\\WMPSDK9\\samples\\media\\ccsample.smi";

```



## <a name="requirements"></a><span data-ttu-id="8a109-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a109-122">Requirements</span></span>



| <span data-ttu-id="8a109-123">需求</span><span class="sxs-lookup"><span data-stu-id="8a109-123">Requirement</span></span> | <span data-ttu-id="8a109-124">值</span><span class="sxs-lookup"><span data-stu-id="8a109-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8a109-125">版本</span><span class="sxs-lookup"><span data-stu-id="8a109-125">Version</span></span><br/> | <span data-ttu-id="8a109-126">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8a109-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8a109-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8a109-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="8a109-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a109-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a109-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a109-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a109-130">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="8a109-130">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="8a109-131">**ClosedCaption 物件**</span><span class="sxs-lookup"><span data-stu-id="8a109-131">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="8a109-132">**Player. 關閉**</span><span class="sxs-lookup"><span data-stu-id="8a109-132">**Player.close**</span></span>](player-close.md)
</dt> </dl>

 

 





