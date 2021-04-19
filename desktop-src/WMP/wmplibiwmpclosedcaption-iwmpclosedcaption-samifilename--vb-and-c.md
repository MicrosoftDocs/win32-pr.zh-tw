---
title: IWMPClosedCaption SAMIFileName 屬性
description: SAMIFileName 屬性會取得或設定包含隱藏式輔助字幕所需資訊的檔案名。
ms.assetid: c3162c5f-9d66-41d4-920c-ed9840742d9d
keywords:
- SAMIFileName 屬性 Windows Media Player
- SAMIFileName 屬性 Windows Media Player，IWMPClosedCaption 介面
- IWMPClosedCaption 介面 Windows Media Player，SAMIFileName 屬性
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIFileName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251f2bbf0c8839ab9a0005c69e1869c47af16ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992962"
---
# <a name="iwmpclosedcaptionsamifilename-property"></a><span data-ttu-id="f4b78-106">IWMPClosedCaption：： SAMIFileName 屬性</span><span class="sxs-lookup"><span data-stu-id="f4b78-106">IWMPClosedCaption::SAMIFileName property</span></span>

<span data-ttu-id="f4b78-107">**SAMIFileName** 屬性會取得或設定包含隱藏式輔助字幕所需資訊的檔案名。</span><span class="sxs-lookup"><span data-stu-id="f4b78-107">The **SAMIFileName** property gets or sets the name of a file containing the information needed for closed captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4b78-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4b78-108">Syntax</span></span>


```CSharp
public System.String SAMIFileName {get; set;}
```


```VB

Public Property SAMIFileName As System.String
```





## <a name="property-value"></a><span data-ttu-id="f4b78-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="f4b78-109">Property value</span></span>

<span data-ttu-id="f4b78-110">表示 **已** 同步處理之可存取媒體的名稱 (薩米) 的檔案。</span><span class="sxs-lookup"><span data-stu-id="f4b78-110">The **System.String** that is the name of the Synchronized Accessible Media Interchange (SAMI) file.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4b78-111">備註</span><span class="sxs-lookup"><span data-stu-id="f4b78-111">Remarks</span></span>

<span data-ttu-id="f4b78-112">薩米文檔案必須使用 smi-s 或薩米的副檔名。</span><span class="sxs-lookup"><span data-stu-id="f4b78-112">The SAMI file must use an .smi or .sami file name extension.</span></span>

<span data-ttu-id="f4b78-113">如果您未使用 **SAMIFileName** 設定值，這個屬性會取得 **字串** ，其中包含與目前媒體專案相關聯的預設檔案名或 URL。</span><span class="sxs-lookup"><span data-stu-id="f4b78-113">If you do not set a value using **SAMIFileName**, this property gets a **string** containing the default file name or URL associated with the current media item.</span></span> <span data-ttu-id="f4b78-114">當您使用 *薩米* 文 URL 參數指定薩米文的檔案時，或當薩米文的檔案與數位媒體檔案的名稱相同時，就可能會發生此關聯 (但副檔名) 除外。</span><span class="sxs-lookup"><span data-stu-id="f4b78-114">This association can occur when a SAMI file is specified by using the *sami* URL parameter, or automatically when the SAMI file has the same name as the digital media file (except for the file name extension).</span></span> <span data-ttu-id="f4b78-115">如果目前媒體沒有相關聯的預設薩米文檔案，這個屬性會取得長度為零的字串 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="f4b78-115">If there is no default SAMI file associated with the current media, this property gets a zero-length string ("").</span></span>

<span data-ttu-id="f4b78-116">使用 **SAMIFileName** 設定值之後，該值會一直保留到您將新值設定 (或直到使用薩米文 URL 參數) 開啟新的媒體專案為止。</span><span class="sxs-lookup"><span data-stu-id="f4b78-116">Once you set a value using **SAMIFileName**, that value persists until you set a new value (or until a new media item is opened using the sami URL parameter).</span></span> <span data-ttu-id="f4b78-117">因此，在播放每個新媒體專案之前，您必須為這個屬性設定新的值。</span><span class="sxs-lookup"><span data-stu-id="f4b78-117">Therefore, you must set a new value for this property before you play each new media item.</span></span> <span data-ttu-id="f4b78-118">如此一來， **SAMIFileName** 的新值就會在下一個媒體專案開啟 (或) **AxWindowsMediaPlayer** 時才會生效。</span><span class="sxs-lookup"><span data-stu-id="f4b78-118">That way, the new value for **SAMIFileName** will take effect when the next media item is opened (or when **AxWindowsMediaPlayer.close** is called).</span></span> <span data-ttu-id="f4b78-119">為 **SAMIFileName** 指定新的值對目前的媒體沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="f4b78-119">Specifying a new value for **SAMIFileName** has no effect for the current media.</span></span>

<span data-ttu-id="f4b78-120">若要使 Windows Media Player 使用與特定媒體專案相關聯的預設薩米文檔案，請將 **SAMIFileName** 設定為零長度的字串 ( "" ) ，再播放下一個媒體專案。</span><span class="sxs-lookup"><span data-stu-id="f4b78-120">To cause Windows Media Player to use the default SAMI file associated with a particular media item, set **SAMIFileName** to a zero-length string ("") before you play the next media item.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4b78-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4b78-121">Requirements</span></span>



| <span data-ttu-id="f4b78-122">需求</span><span class="sxs-lookup"><span data-stu-id="f4b78-122">Requirement</span></span> | <span data-ttu-id="f4b78-123">值</span><span class="sxs-lookup"><span data-stu-id="f4b78-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4b78-124">版本</span><span class="sxs-lookup"><span data-stu-id="f4b78-124">Version</span></span><br/>   | <span data-ttu-id="f4b78-125">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="f4b78-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f4b78-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="f4b78-126">Namespace</span></span><br/> | <span data-ttu-id="f4b78-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f4b78-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f4b78-128">組件</span><span class="sxs-lookup"><span data-stu-id="f4b78-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f4b78-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="f4b78-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4b78-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4b78-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4b78-131">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="f4b78-131">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="f4b78-132">**AxWindowsMediaPlayer。關閉**</span><span class="sxs-lookup"><span data-stu-id="f4b78-132">**AxWindowsMediaPlayer.close**</span></span>](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[<span data-ttu-id="f4b78-133">**IWMPClosedCaption 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="f4b78-133">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f4b78-134">**IWMPClosedCaption2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="f4b78-134">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





