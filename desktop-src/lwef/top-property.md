---
title: 'Top 屬性 (字元物件) '
description: 深入瞭解 Top property (字元物件) 。 Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a5e26d2ef578a98447d47eb2a3fae3613760a9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396343"
---
# <a name="top-property-characters-object"></a><span data-ttu-id="b9aa2-104">Top 屬性 (字元物件) </span><span class="sxs-lookup"><span data-stu-id="b9aa2-104">Top Property (Characters Object)</span></span>

<span data-ttu-id="b9aa2-105">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b9aa2-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b9aa2-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="b9aa2-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b9aa2-107">傳回或設定指定之字元框架的上邊緣。</span><span class="sxs-lookup"><span data-stu-id="b9aa2-107">Returns or sets the top edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="b9aa2-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="b9aa2-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b9aa2-109">\*代理程式 \***。 ( "**_CharacterID_\*_" ) 的字元。Top_ \*  \[  =  *值*\]</span><span class="sxs-lookup"><span data-stu-id="b9aa2-109">*agent\***.Characters ("**_CharacterID_*_").Top_\* \[ = *value*\]</span></span>



| <span data-ttu-id="b9aa2-110">部分</span><span class="sxs-lookup"><span data-stu-id="b9aa2-110">Part</span></span>    | <span data-ttu-id="b9aa2-111">描述</span><span class="sxs-lookup"><span data-stu-id="b9aa2-111">Description</span></span>                                             |
|---------|---------------------------------------------------------|
| <span data-ttu-id="b9aa2-112">*value*</span><span class="sxs-lookup"><span data-stu-id="b9aa2-112">*value*</span></span> | <span data-ttu-id="b9aa2-113">指定字元上邊緣的長整數。</span><span class="sxs-lookup"><span data-stu-id="b9aa2-113">A Long integer that specifies the character's top edge.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9aa2-114">備註</span><span class="sxs-lookup"><span data-stu-id="b9aa2-114">Remarks</span></span>

<span data-ttu-id="b9aa2-115">**Top** 屬性一律以圖元表示，相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="b9aa2-115">The **Top** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="b9aa2-116">這個屬性的設定會套用到字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="b9aa2-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="b9aa2-117">雖然字元會出現在不規則的形狀區域視窗中，但字元的位置是以使用 Microsoft Agent 字元編輯器來編譯字元時所使用之矩形動畫框架的外部維度為基礎。</span><span class="sxs-lookup"><span data-stu-id="b9aa2-117">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="b9aa2-118">使用 [**MoveTo**](moveto-method.md) 方法來變更字元的位置。</span><span class="sxs-lookup"><span data-stu-id="b9aa2-118">Use the [**MoveTo**](moveto-method.md) method to change the character's location.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9aa2-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9aa2-119">See Also</span></span>

<span data-ttu-id="b9aa2-120">[**左屬性**](left-property.md)、 [ **MoveTo 方法**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="b9aa2-120">[**Left property**](left-property.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




