---
title: WM/WMContentID 屬性
description: WM/WMContentID 屬性是識別專案內容的 GUID。
ms.assetid: 1e741286-cdd8-4c2f-8fef-5d91d81d6387
keywords:
- WM/WMContentID 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04366991a37b727f2693bc42ce2050139ce5c211
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976134"
---
# <a name="wmwmcontentid-attribute"></a><span data-ttu-id="e021f-104">WM/WMContentID 屬性</span><span class="sxs-lookup"><span data-stu-id="e021f-104">WM/WMContentID Attribute</span></span>

<span data-ttu-id="e021f-105">**WM/WMContentID** 屬性是識別專案內容的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e021f-105">The **WM/WMContentID** attribute is a GUID identifying the content of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e021f-106">套用至</span><span class="sxs-lookup"><span data-stu-id="e021f-106">Applies To</span></span>

-   [<span data-ttu-id="e021f-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="e021f-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="e021f-108">CD 曲目</span><span class="sxs-lookup"><span data-stu-id="e021f-108">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="e021f-109">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="e021f-109">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="e021f-110">備註</span><span class="sxs-lookup"><span data-stu-id="e021f-110">Remarks</span></span>

<span data-ttu-id="e021f-111">這個屬性會儲存在程式庫 (或快取) 和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="e021f-111">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="e021f-112">**WMContentID** 是此屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="e021f-112">**WMContentID** is an alias for this attribute.</span></span>

<span data-ttu-id="e021f-113">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMContentID。</span><span class="sxs-lookup"><span data-stu-id="e021f-113">The Windows Media Format SDK constant for this attribute is g\_wszWMContentID.</span></span>

<span data-ttu-id="e021f-114">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="e021f-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e021f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e021f-115">Requirements</span></span>



| <span data-ttu-id="e021f-116">需求</span><span class="sxs-lookup"><span data-stu-id="e021f-116">Requirement</span></span> | <span data-ttu-id="e021f-117">值</span><span class="sxs-lookup"><span data-stu-id="e021f-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="e021f-118">版本</span><span class="sxs-lookup"><span data-stu-id="e021f-118">Version</span></span><br/> | <span data-ttu-id="e021f-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="e021f-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e021f-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e021f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e021f-121">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="e021f-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





