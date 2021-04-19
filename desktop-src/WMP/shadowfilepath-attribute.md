---
title: ShadowFilePath 屬性
description: ShadowFilePath 屬性是陰影檔案的完整路徑。
ms.assetid: dd00d53c-8a95-450c-a65b-1763e9112941
keywords:
- ShadowFilePath 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- ShadowFilePath
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef79271995e9817315fb918049fc22491e232a5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987091"
---
# <a name="shadowfilepath-attribute"></a><span data-ttu-id="2501f-104">ShadowFilePath 屬性</span><span class="sxs-lookup"><span data-stu-id="2501f-104">ShadowFilePath Attribute</span></span>

<span data-ttu-id="2501f-105">**ShadowFilePath** 屬性是陰影檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="2501f-105">The **ShadowFilePath** attribute is the fully qualified path to a shadow file.</span></span>

## <a name="applies-to"></a><span data-ttu-id="2501f-106">套用至</span><span class="sxs-lookup"><span data-stu-id="2501f-106">Applies To</span></span>

-   [<span data-ttu-id="2501f-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="2501f-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="2501f-108">備註</span><span class="sxs-lookup"><span data-stu-id="2501f-108">Remarks</span></span>

<span data-ttu-id="2501f-109">在檔案格式轉換過程中，會建立一個 *陰影* 檔。</span><span class="sxs-lookup"><span data-stu-id="2501f-109">A *shadow file* is created as part of a file format conversion.</span></span> <span data-ttu-id="2501f-110">這是播放程式在使用者將內容從電腦同步處理到需要內容為原始檔案格式的裝置時，所使用的檔案複本。</span><span class="sxs-lookup"><span data-stu-id="2501f-110">It is the copy of a file that the Player uses when the user syncs content from the computer to a device that requires the content to be in the original file format.</span></span> <span data-ttu-id="2501f-111">已轉換的檔案會設定這個屬性，以指向陰影檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="2501f-111">This attribute is set for the converted file to point to the location of the shadow file.</span></span>

<span data-ttu-id="2501f-112">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="2501f-112">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2501f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2501f-113">Requirements</span></span>



| <span data-ttu-id="2501f-114">需求</span><span class="sxs-lookup"><span data-stu-id="2501f-114">Requirement</span></span> | <span data-ttu-id="2501f-115">值</span><span class="sxs-lookup"><span data-stu-id="2501f-115">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="2501f-116">版本</span><span class="sxs-lookup"><span data-stu-id="2501f-116">Version</span></span><br/> | <span data-ttu-id="2501f-117">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="2501f-117">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2501f-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2501f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2501f-119">**關於轉換流程**</span><span class="sxs-lookup"><span data-stu-id="2501f-119">**About the Conversion Process**</span></span>](about-the-conversion-process.md)
</dt> <dt>

[<span data-ttu-id="2501f-120">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="2501f-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





