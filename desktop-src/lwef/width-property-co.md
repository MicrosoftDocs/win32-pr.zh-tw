---
title: 'Width 屬性 (字元物件) '
description: Width 屬性
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a37a29bd8f50231bd44b6529a0c1ce13c0256d3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024446"
---
# <a name="width-property-characters-object"></a><span data-ttu-id="04f6b-103">Width 屬性 (字元物件) </span><span class="sxs-lookup"><span data-stu-id="04f6b-103">Width Property (Characters Object)</span></span>

<span data-ttu-id="04f6b-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="04f6b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="04f6b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="04f6b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="04f6b-106">傳回或設定指定字元的框架寬度。</span><span class="sxs-lookup"><span data-stu-id="04f6b-106">Returns or sets the width of the frame for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="04f6b-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="04f6b-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="04f6b-108">\*代理程式 \***。 ( "**_CharacterID_\*_" ) 的字元。寬度_ \*  \[ =  *值*\]</span><span class="sxs-lookup"><span data-stu-id="04f6b-108">*agent\***.Characters ("**_CharacterID_*_").Width_\* \[= *value*\]</span></span>



| <span data-ttu-id="04f6b-109">部分</span><span class="sxs-lookup"><span data-stu-id="04f6b-109">Part</span></span>    | <span data-ttu-id="04f6b-110">描述</span><span class="sxs-lookup"><span data-stu-id="04f6b-110">Description</span></span>                                                |
|---------|------------------------------------------------------------|
| <span data-ttu-id="04f6b-111">*value*</span><span class="sxs-lookup"><span data-stu-id="04f6b-111">*value*</span></span> | <span data-ttu-id="04f6b-112">指定字元框架寬度的長整數。</span><span class="sxs-lookup"><span data-stu-id="04f6b-112">A Long integer that specifies the character's frame width.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04f6b-113">備註</span><span class="sxs-lookup"><span data-stu-id="04f6b-113">Remarks</span></span>

<span data-ttu-id="04f6b-114">[**Width**](width-property.md)屬性一律以圖元表示。</span><span class="sxs-lookup"><span data-stu-id="04f6b-114">The [**Width**](width-property.md) property is always expressed in pixels.</span></span> <span data-ttu-id="04f6b-115">這個屬性的設定會套用到字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="04f6b-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="04f6b-116">雖然字元會出現在不規則的形狀區域視窗中，但字元的位置是以使用 Microsoft Agent 字元編輯器來編譯字元時所使用之矩形動畫框架的外部維度為基礎。</span><span class="sxs-lookup"><span data-stu-id="04f6b-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




