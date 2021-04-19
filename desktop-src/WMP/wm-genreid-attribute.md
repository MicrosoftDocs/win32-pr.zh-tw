---
title: WM/GenreID 屬性
description: WM/GenreID 屬性是符合 ID3v2 中 TCON 標記的內容類型識別碼。
ms.assetid: 9b68f9be-1f02-4b14-b052-90657b8800e3
keywords:
- WM/GenreID 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d31e54805f778a51f345c84654056391ec4052e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000765"
---
# <a name="wmgenreid-attribute"></a><span data-ttu-id="1723b-104">WM/GenreID 屬性</span><span class="sxs-lookup"><span data-stu-id="1723b-104">WM/GenreID Attribute</span></span>

<span data-ttu-id="1723b-105">**WM/GenreID** 屬性是符合 ID3V2 中 TCON 標記的內容類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="1723b-105">The **WM/GenreID** attribute is a genre identifier compliant with the TCON tag in ID3v2.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1723b-106">套用至</span><span class="sxs-lookup"><span data-stu-id="1723b-106">Applies To</span></span>

-   [<span data-ttu-id="1723b-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="1723b-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="1723b-108">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="1723b-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="1723b-109">備註</span><span class="sxs-lookup"><span data-stu-id="1723b-109">Remarks</span></span>

<span data-ttu-id="1723b-110">這個屬性只會儲存在數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="1723b-110">This attribute is stored only in the digital media file.</span></span>

<span data-ttu-id="1723b-111">ID3 第2版是一種標記慣例，原本是針對 MP3 所設計。</span><span class="sxs-lookup"><span data-stu-id="1723b-111">ID3 version 2 is a tagging convention that was originally designed for MP3.</span></span> <span data-ttu-id="1723b-112">如需詳細資訊，請參閱 [ID3 組織的網站](https://id3.org/)。</span><span class="sxs-lookup"><span data-stu-id="1723b-112">For more information, see the [ID3 organization's website](https://id3.org/).</span></span>

<span data-ttu-id="1723b-113">這個屬性的 Windows Media Format SDK 常數是 g \_ wszGenreID。</span><span class="sxs-lookup"><span data-stu-id="1723b-113">The Windows Media Format SDK constant for this attribute is g\_wszGenreID.</span></span>

<span data-ttu-id="1723b-114">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="1723b-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1723b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1723b-115">Requirements</span></span>



| <span data-ttu-id="1723b-116">需求</span><span class="sxs-lookup"><span data-stu-id="1723b-116">Requirement</span></span> | <span data-ttu-id="1723b-117">值</span><span class="sxs-lookup"><span data-stu-id="1723b-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1723b-118">版本</span><span class="sxs-lookup"><span data-stu-id="1723b-118">Version</span></span><br/> | <span data-ttu-id="1723b-119">Windows Media Player 9 系列 Windows Media Player 10 或更新版本不支援此屬性</span><span class="sxs-lookup"><span data-stu-id="1723b-119">Windows Media Player 9 Series Windows Media Player 10 or later does not support this attribute</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1723b-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1723b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1723b-121">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="1723b-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





