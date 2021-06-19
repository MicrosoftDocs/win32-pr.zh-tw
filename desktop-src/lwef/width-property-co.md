---
title: 'Width 屬性 (字元物件) '
description: 深入瞭解字元物件的 Width 屬性，它會針對指定的字元傳回或設定框架的寬度。
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17f11412774fcf34e887a2f00479ab7d96369de
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395124"
---
# <a name="width-property-characters-object"></a><span data-ttu-id="d0252-103">Width 屬性 (字元物件) </span><span class="sxs-lookup"><span data-stu-id="d0252-103">Width Property (Characters Object)</span></span>

<span data-ttu-id="d0252-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="d0252-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d0252-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="d0252-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d0252-106">傳回或設定指定字元的框架寬度。</span><span class="sxs-lookup"><span data-stu-id="d0252-106">Returns or sets the width of the frame for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="d0252-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="d0252-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="d0252-108">\*代理程式 \***。 ( "**_CharacterID_\*_" ) 的字元。寬度_ \*  \[ =  *值*\]</span><span class="sxs-lookup"><span data-stu-id="d0252-108">*agent\***.Characters ("**_CharacterID_*_").Width_\* \[= *value*\]</span></span>



| <span data-ttu-id="d0252-109">部分</span><span class="sxs-lookup"><span data-stu-id="d0252-109">Part</span></span>    | <span data-ttu-id="d0252-110">描述</span><span class="sxs-lookup"><span data-stu-id="d0252-110">Description</span></span>                                                |
|---------|------------------------------------------------------------|
| <span data-ttu-id="d0252-111">*value*</span><span class="sxs-lookup"><span data-stu-id="d0252-111">*value*</span></span> | <span data-ttu-id="d0252-112">指定字元框架寬度的長整數。</span><span class="sxs-lookup"><span data-stu-id="d0252-112">A Long integer that specifies the character's frame width.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0252-113">備註</span><span class="sxs-lookup"><span data-stu-id="d0252-113">Remarks</span></span>

<span data-ttu-id="d0252-114">[**Width**](width-property.md)屬性一律以圖元表示。</span><span class="sxs-lookup"><span data-stu-id="d0252-114">The [**Width**](width-property.md) property is always expressed in pixels.</span></span> <span data-ttu-id="d0252-115">這個屬性的設定會套用到字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="d0252-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="d0252-116">雖然字元會出現在不規則的形狀區域視窗中，但字元的位置是以使用 Microsoft Agent 字元編輯器來編譯字元時所使用之矩形動畫框架的外部維度為基礎。</span><span class="sxs-lookup"><span data-stu-id="d0252-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




