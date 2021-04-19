---
title: MetadataText。文字
description: Text 屬性會捕獲中繼資料文字。
ms.assetid: e6963df8-6c83-40c5-a442-5307850d15cf
keywords:
- MetadataText Windows Media Player 文字
topic_type:
- apiref
api_name:
- MetadataText.text
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60aebaf8df3328d9263e7416f6fa2dfaae6e7826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996326"
---
# <a name="metadatatexttext"></a><span data-ttu-id="32a33-104">MetadataText。文字</span><span class="sxs-lookup"><span data-stu-id="32a33-104">MetadataText.text</span></span>

<span data-ttu-id="32a33-105">**Text** 屬性會捕獲中繼資料文字。</span><span class="sxs-lookup"><span data-stu-id="32a33-105">The **text** property retrieves the metadata text.</span></span>

## <a name="syntax"></a><span data-ttu-id="32a33-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="32a33-106">Syntax</span></span>

<span data-ttu-id="32a33-107">*玩家*。*currentMedia*。**getItemInfoByType** ( *name*、 *language*、 *index*) 。**文字**</span><span class="sxs-lookup"><span data-stu-id="32a33-107">*player*.*currentMedia*.**getItemInfoByType**( *name*, *language*, *index*).**text**</span></span>

## <a name="possible-values"></a><span data-ttu-id="32a33-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="32a33-108">Possible Values</span></span>

<span data-ttu-id="32a33-109">這個屬性是唯讀 **字串**。</span><span class="sxs-lookup"><span data-stu-id="32a33-109">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="32a33-110">備註</span><span class="sxs-lookup"><span data-stu-id="32a33-110">Remarks</span></span>

<span data-ttu-id="32a33-111">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="32a33-111">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="32a33-112">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="32a33-112">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="32a33-113">**Windows Media Player 10** 行動裝置版：不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="32a33-113">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="32a33-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="32a33-114">Requirements</span></span>



| <span data-ttu-id="32a33-115">需求</span><span class="sxs-lookup"><span data-stu-id="32a33-115">Requirement</span></span> | <span data-ttu-id="32a33-116">值</span><span class="sxs-lookup"><span data-stu-id="32a33-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="32a33-117">版本</span><span class="sxs-lookup"><span data-stu-id="32a33-117">Version</span></span><br/> | <span data-ttu-id="32a33-118">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="32a33-118">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="32a33-119">DLL</span><span class="sxs-lookup"><span data-stu-id="32a33-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="32a33-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32a33-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32a33-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32a33-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32a33-122">**MetadataText 物件**</span><span class="sxs-lookup"><span data-stu-id="32a33-122">**MetadataText Object**</span></span>](metadatatext-object.md)
</dt> <dt>

[<span data-ttu-id="32a33-123">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="32a33-123">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="32a33-124">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="32a33-124">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





