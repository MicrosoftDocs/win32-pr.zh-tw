---
title: 'Left 屬性 (字元物件) '
description: 深入瞭解 [左字元] 物件屬性。 Microsoft Agent 已于 Windows 7 淘汰。
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e2f860e6827a9c96c42014456e43b791ab70ed4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988934"
---
# <a name="left-property-characters-object"></a><span data-ttu-id="a18cc-104">Left 屬性 (字元物件) </span><span class="sxs-lookup"><span data-stu-id="a18cc-104">Left Property (Characters Object)</span></span>

<span data-ttu-id="a18cc-105">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a18cc-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a18cc-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="a18cc-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a18cc-107">傳回或設定指定之字元框架的左邊緣。</span><span class="sxs-lookup"><span data-stu-id="a18cc-107">Returns or sets the left edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="a18cc-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="a18cc-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a18cc-109">\*代理程式 \***。 ( "**_CharacterID_\*_" ) 的字元。左_ \*  \[  =  *值*\]</span><span class="sxs-lookup"><span data-stu-id="a18cc-109">*agent\***.Characters ("**_CharacterID_*_").Left_\* \[ = *value*\]</span></span>



| <span data-ttu-id="a18cc-110">部分</span><span class="sxs-lookup"><span data-stu-id="a18cc-110">Part</span></span>    | <span data-ttu-id="a18cc-111">描述</span><span class="sxs-lookup"><span data-stu-id="a18cc-111">Description</span></span>                                                           |
|---------|-----------------------------------------------------------------------|
| <span data-ttu-id="a18cc-112">*value*</span><span class="sxs-lookup"><span data-stu-id="a18cc-112">*value*</span></span> | <span data-ttu-id="a18cc-113">指定字元框架左邊緣的長整數。</span><span class="sxs-lookup"><span data-stu-id="a18cc-113">A Long integer that specifies the left edge of the character's frame.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a18cc-114">備註</span><span class="sxs-lookup"><span data-stu-id="a18cc-114">Remarks</span></span>

<span data-ttu-id="a18cc-115">**左邊** 的屬性一律以圖元表示，相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="a18cc-115">The **Left** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="a18cc-116">這個屬性的設定會套用到字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="a18cc-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="a18cc-117">雖然字元會出現在不規則的形狀區域視窗中，但字元的位置是以使用 Microsoft Agent 字元編輯器來編譯字元時所使用之矩形動畫框架的外部維度為基礎。</span><span class="sxs-lookup"><span data-stu-id="a18cc-117">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




