---
title: 'Height 屬性 (字元物件) '
description: Height 屬性
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e504dcbbfd470c62b4102d86f25a1d2b3c4c25e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685363"
---
# <a name="height-property-characters-object"></a><span data-ttu-id="eec62-103">Height 屬性 (字元物件) </span><span class="sxs-lookup"><span data-stu-id="eec62-103">Height Property (Characters Object)</span></span>

<span data-ttu-id="eec62-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="eec62-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="eec62-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="eec62-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="eec62-106">傳回或設定指定之字元框架的高度。</span><span class="sxs-lookup"><span data-stu-id="eec62-106">Returns or sets the height of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="eec62-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="eec62-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="eec62-108">\*代理程式 \***。 ( "**_CharacterID_\*_" ) 的字元。高度_ \*  \[ =  *值*\]</span><span class="sxs-lookup"><span data-stu-id="eec62-108">*agent\***.Characters ("**_CharacterID_*_").Height_\* \[= *value*\]</span></span>



| <span data-ttu-id="eec62-109">部分</span><span class="sxs-lookup"><span data-stu-id="eec62-109">Part</span></span>    | <span data-ttu-id="eec62-110">描述</span><span class="sxs-lookup"><span data-stu-id="eec62-110">Description</span></span>                                                 |
|---------|-------------------------------------------------------------|
| <span data-ttu-id="eec62-111">*value*</span><span class="sxs-lookup"><span data-stu-id="eec62-111">*value*</span></span> | <span data-ttu-id="eec62-112">指定字元之框架高度的長整數。</span><span class="sxs-lookup"><span data-stu-id="eec62-112">A Long integer that specifies the character's frame height.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eec62-113">備註</span><span class="sxs-lookup"><span data-stu-id="eec62-113">Remarks</span></span>

<span data-ttu-id="eec62-114">**Height** 屬性一律會以圖元表示（相對於螢幕座標 (左上) ）。</span><span class="sxs-lookup"><span data-stu-id="eec62-114">The **Height** property is always expressed in pixels, relative to screen coordinates (upper left).</span></span> <span data-ttu-id="eec62-115">這個屬性的設定會套用到字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="eec62-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="eec62-116">雖然字元會出現在不規則形狀的區域視窗中，但字元的高度是以使用 Microsoft Agent 字元編輯器來編譯字元時所使用之矩形動畫框架的外部維度為基礎。</span><span class="sxs-lookup"><span data-stu-id="eec62-116">Even though the character appears in an irregularly shaped region window, the height of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




