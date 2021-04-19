---
title: '>synconly 屬性'
description: '>synconly 屬性是布林值的字串表示，Windows Media Player 用來判斷播放清單是否僅適用于同步處理。'
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- '>synconly 屬性 Windows Media Player'
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0245ffac2c4c64717adf669fcc6ff8fd0768382
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983984"
---
# <a name="synconly-attribute"></a><span data-ttu-id="94244-104">>synconly 屬性</span><span class="sxs-lookup"><span data-stu-id="94244-104">SyncOnly Attribute</span></span>

<span data-ttu-id="94244-105">**>synconly** 屬性是 **布林** 值的字串表示，Windows Media Player 用來判斷播放清單是否僅適用于同步處理。</span><span class="sxs-lookup"><span data-stu-id="94244-105">The **SyncOnly** attribute is a string representation of a **Boolean** value that Windows Media Player uses to determine whether a playlist is available only for synchronization.</span></span>

## <a name="applies-to"></a><span data-ttu-id="94244-106">套用至</span><span class="sxs-lookup"><span data-stu-id="94244-106">Applies To</span></span>

-   [<span data-ttu-id="94244-107">播放清單</span><span class="sxs-lookup"><span data-stu-id="94244-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="94244-108">備註</span><span class="sxs-lookup"><span data-stu-id="94244-108">Remarks</span></span>

<span data-ttu-id="94244-109">值為1表示播放清單僅供同步處理使用，且不能出現在 [ **自動播放清單** ] 節點中。</span><span class="sxs-lookup"><span data-stu-id="94244-109">A value of 1 indicates that the playlist is available only for synchronization and cannot appear in the **Auto Playlist** node.</span></span> <span data-ttu-id="94244-110">值為零表示播放清單可以出現在 [ **自動播放清單** ] 節點中。</span><span class="sxs-lookup"><span data-stu-id="94244-110">A value of zero indicates that the playlist can appear in the **Auto Playlist** node.</span></span>

<span data-ttu-id="94244-111">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="94244-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="94244-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="94244-112">Requirements</span></span>



| <span data-ttu-id="94244-113">需求</span><span class="sxs-lookup"><span data-stu-id="94244-113">Requirement</span></span> | <span data-ttu-id="94244-114">值</span><span class="sxs-lookup"><span data-stu-id="94244-114">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="94244-115">版本</span><span class="sxs-lookup"><span data-stu-id="94244-115">Version</span></span><br/> | <span data-ttu-id="94244-116">Windows Media Player 10 或更新版本</span><span class="sxs-lookup"><span data-stu-id="94244-116">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94244-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94244-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94244-118">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="94244-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





