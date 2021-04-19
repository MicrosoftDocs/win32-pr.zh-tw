---
title: 'Left 屬性 (字元物件) '
description: 左方屬性
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a318e659405883c56f296a9371eba7e9423662b1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106967944"
---
# <a name="left-property-characters-object"></a><span data-ttu-id="79b54-103">Left 屬性 (字元物件) </span><span class="sxs-lookup"><span data-stu-id="79b54-103">Left Property (Characters Object)</span></span>

<span data-ttu-id="79b54-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="79b54-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="79b54-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="79b54-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="79b54-106">傳回或設定指定之字元框架的左邊緣。</span><span class="sxs-lookup"><span data-stu-id="79b54-106">Returns or sets the left edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="79b54-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="79b54-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="79b54-108">\*代理程式 \***。 ( "**_CharacterID_\*_" ) 的字元。左_ \*  \[  =  *值*\]</span><span class="sxs-lookup"><span data-stu-id="79b54-108">*agent\***.Characters ("**_CharacterID_*_").Left_\* \[ = *value*\]</span></span>



| <span data-ttu-id="79b54-109">部分</span><span class="sxs-lookup"><span data-stu-id="79b54-109">Part</span></span>    | <span data-ttu-id="79b54-110">描述</span><span class="sxs-lookup"><span data-stu-id="79b54-110">Description</span></span>                                                           |
|---------|-----------------------------------------------------------------------|
| <span data-ttu-id="79b54-111">*value*</span><span class="sxs-lookup"><span data-stu-id="79b54-111">*value*</span></span> | <span data-ttu-id="79b54-112">指定字元框架左邊緣的長整數。</span><span class="sxs-lookup"><span data-stu-id="79b54-112">A Long integer that specifies the left edge of the character's frame.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79b54-113">備註</span><span class="sxs-lookup"><span data-stu-id="79b54-113">Remarks</span></span>

<span data-ttu-id="79b54-114">**左邊** 的屬性一律以圖元表示，相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="79b54-114">The **Left** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="79b54-115">這個屬性的設定會套用到字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="79b54-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="79b54-116">雖然字元會出現在不規則的形狀區域視窗中，但字元的位置是以使用 Microsoft Agent 字元編輯器來編譯字元時所使用之矩形動畫框架的外部維度為基礎。</span><span class="sxs-lookup"><span data-stu-id="79b54-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




