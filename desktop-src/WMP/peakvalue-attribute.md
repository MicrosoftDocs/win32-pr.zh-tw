---
title: PeakValue 屬性
description: PeakValue 屬性是16位的波幅值，表示尖峰磁片區層級。
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- PeakValue 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fde522e043adb8b11c25bede763bed6b252f2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997793"
---
# <a name="peakvalue-attribute"></a><span data-ttu-id="71339-104">PeakValue 屬性</span><span class="sxs-lookup"><span data-stu-id="71339-104">PeakValue Attribute</span></span>

<span data-ttu-id="71339-105">**PeakValue** 屬性是16位的波幅值，表示尖峰磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="71339-105">The **PeakValue** attribute is a 16-bit amplitude value indicating the peak volume level.</span></span>

## <a name="applies-to"></a><span data-ttu-id="71339-106">套用至</span><span class="sxs-lookup"><span data-stu-id="71339-106">Applies To</span></span>

-   [<span data-ttu-id="71339-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="71339-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="71339-108">常用的 Windows Media 檔案</span><span class="sxs-lookup"><span data-stu-id="71339-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="71339-109">備註</span><span class="sxs-lookup"><span data-stu-id="71339-109">Remarks</span></span>

<span data-ttu-id="71339-110">這個屬性會儲存在文件庫和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="71339-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="71339-111">Windows Media Player 會在下列其中一個實例中設定此值：</span><span class="sxs-lookup"><span data-stu-id="71339-111">Windows Media Player sets this value in either of the following instances:</span></span>

-   <span data-ttu-id="71339-112">完成檔案的翻錄之後。</span><span class="sxs-lookup"><span data-stu-id="71339-112">After it has ripped a file.</span></span>
-   <span data-ttu-id="71339-113">當已啟用自動磁片區調節增強功能時，它會在播放檔 () 。</span><span class="sxs-lookup"><span data-stu-id="71339-113">After it has played a file (when the Auto Volume Leveling enhancement is enabled).</span></span>

<span data-ttu-id="71339-114">這個屬性的 Windows Media Format SDK 常數是 g \_ wszPeakValue。</span><span class="sxs-lookup"><span data-stu-id="71339-114">The Windows Media Format SDK constant for this attribute is g\_wszPeakValue.</span></span>

<span data-ttu-id="71339-115">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="71339-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="71339-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="71339-116">Requirements</span></span>



| <span data-ttu-id="71339-117">需求</span><span class="sxs-lookup"><span data-stu-id="71339-117">Requirement</span></span> | <span data-ttu-id="71339-118">值</span><span class="sxs-lookup"><span data-stu-id="71339-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="71339-119">版本</span><span class="sxs-lookup"><span data-stu-id="71339-119">Version</span></span><br/> | <span data-ttu-id="71339-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="71339-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71339-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71339-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71339-122">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="71339-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





