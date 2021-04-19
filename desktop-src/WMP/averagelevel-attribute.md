---
title: AverageLevel 屬性
description: AverageLevel 屬性是16位的波幅值，表示平均音量層級。
ms.assetid: 04ff19f1-a9a5-4e47-86a6-50c6f08b0d7d
keywords:
- AverageLevel 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594612f3675d818f94270b1952d2a9ca7bed15d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998600"
---
# <a name="averagelevel-attribute"></a><span data-ttu-id="203b6-104">AverageLevel 屬性</span><span class="sxs-lookup"><span data-stu-id="203b6-104">AverageLevel Attribute</span></span>

<span data-ttu-id="203b6-105">**AverageLevel** 屬性是16位的波幅值，表示平均音量層級。</span><span class="sxs-lookup"><span data-stu-id="203b6-105">The **AverageLevel** attribute is a 16-bit amplitude value indicating the average volume level.</span></span>

## <a name="applies-to"></a><span data-ttu-id="203b6-106">套用至</span><span class="sxs-lookup"><span data-stu-id="203b6-106">Applies To</span></span>

-   [<span data-ttu-id="203b6-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="203b6-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="203b6-108">常用的 Windows Media 檔案</span><span class="sxs-lookup"><span data-stu-id="203b6-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="203b6-109">備註</span><span class="sxs-lookup"><span data-stu-id="203b6-109">Remarks</span></span>

<span data-ttu-id="203b6-110">這個屬性會儲存在文件庫和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="203b6-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="203b6-111">Windows Media Player 會在下列其中一個實例中設定此值：</span><span class="sxs-lookup"><span data-stu-id="203b6-111">Windows Media Player sets this value in either of the following instances:</span></span>

-   <span data-ttu-id="203b6-112">完成檔案的翻錄之後。</span><span class="sxs-lookup"><span data-stu-id="203b6-112">After it has ripped a file.</span></span>
-   <span data-ttu-id="203b6-113">當已啟用自動磁片區調節增強功能時，它會在播放檔 () 。</span><span class="sxs-lookup"><span data-stu-id="203b6-113">After it has played a file (when the Auto Volume Leveling enhancement is enabled).</span></span>

<span data-ttu-id="203b6-114">這個屬性的 Windows Media Format SDK 常數是 g \_ wszAverageLevel。</span><span class="sxs-lookup"><span data-stu-id="203b6-114">The Windows Media Format SDK constant for this attribute is g\_wszAverageLevel.</span></span>

<span data-ttu-id="203b6-115">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="203b6-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="203b6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="203b6-116">Requirements</span></span>



| <span data-ttu-id="203b6-117">需求</span><span class="sxs-lookup"><span data-stu-id="203b6-117">Requirement</span></span> | <span data-ttu-id="203b6-118">值</span><span class="sxs-lookup"><span data-stu-id="203b6-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="203b6-119">版本</span><span class="sxs-lookup"><span data-stu-id="203b6-119">Version</span></span><br/> | <span data-ttu-id="203b6-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="203b6-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="203b6-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="203b6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="203b6-122">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="203b6-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





