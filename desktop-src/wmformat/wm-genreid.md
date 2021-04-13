---
title: WM/GenreID
description: WM/GenreID 屬性包含與 ID3v2 中 TCON 標記內容相容的內容類型識別碼。
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- WM/GenreID windows Media 格式
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a3b25dffe69471f47eaf20124af48141835540f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373401"
---
# <a name="wmgenreid"></a><span data-ttu-id="f415c-104">WM/GenreID</span><span class="sxs-lookup"><span data-stu-id="f415c-104">WM/GenreID</span></span>

<span data-ttu-id="f415c-105">**WM/GenreID** 屬性包含與 ID3V2 中 TCON 標記內容相容的內容類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="f415c-105">The **WM/GenreID** attribute contains a genre identifier compliant with the contents of the TCON tag in ID3v2.</span></span> <span data-ttu-id="f415c-106">這應該會在括弧中包含內容類型識別碼，並選擇性地接著進一步描述內容類型。</span><span class="sxs-lookup"><span data-stu-id="f415c-106">This should contain the genre ID in parentheses, optionally followed by a refinement further describing the genre.</span></span> <span data-ttu-id="f415c-107">如需詳細資訊，請參閱 ID3v2 規格。</span><span class="sxs-lookup"><span data-stu-id="f415c-107">For more information, refer to the ID3v2 specification.</span></span>

## <a name="global-constant"></a><span data-ttu-id="f415c-108">全域常數</span><span class="sxs-lookup"><span data-stu-id="f415c-108">Global Constant</span></span>

<span data-ttu-id="f415c-109">g \_ wszWMGenreID</span><span class="sxs-lookup"><span data-stu-id="f415c-109">g\_wszWMGenreID</span></span>

## <a name="data-type"></a><span data-ttu-id="f415c-110">資料類型</span><span class="sxs-lookup"><span data-stu-id="f415c-110">Data Type</span></span>

<span data-ttu-id="f415c-111">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="f415c-111">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="f415c-112">備註</span><span class="sxs-lookup"><span data-stu-id="f415c-112">Remarks</span></span>

<span data-ttu-id="f415c-113">用來指定類型的慣用屬性為 [**WM/**](wm-genre.md)內容類型。</span><span class="sxs-lookup"><span data-stu-id="f415c-113">The preferred attribute for specifying a genre is [**WM/Genre**](wm-genre.md).</span></span> <span data-ttu-id="f415c-114">將其用於此屬性的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="f415c-114">Use it in preference to this attribute.</span></span>

<span data-ttu-id="f415c-115">如果您變更了 MP3 檔中的 **wm/** 內容類型或 **wm/GenreID** ，其他屬性將會變更為 [符合]。</span><span class="sxs-lookup"><span data-stu-id="f415c-115">If you change either **WM/Genre** or **WM/GenreID** in an MP3 file, the other attribute will be changed to match.</span></span>

### <a name="example"></a><span data-ttu-id="f415c-116">範例</span><span class="sxs-lookup"><span data-stu-id="f415c-116">Example</span></span>



| <span data-ttu-id="f415c-117">檔案類型</span><span class="sxs-lookup"><span data-stu-id="f415c-117">File type</span></span> | <span data-ttu-id="f415c-118">範例值</span><span class="sxs-lookup"><span data-stu-id="f415c-118">Example value</span></span>   |
|-----------|-----------------|
| <span data-ttu-id="f415c-119">音訊</span><span class="sxs-lookup"><span data-stu-id="f415c-119">Audio</span></span>     | <span data-ttu-id="f415c-120">" (4) Eurodisco"</span><span class="sxs-lookup"><span data-stu-id="f415c-120">"(4) Eurodisco"</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="f415c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f415c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f415c-122">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="f415c-122">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




