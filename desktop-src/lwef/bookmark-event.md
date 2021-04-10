---
title: 書簽事件
description: 書簽事件
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0695ccd04f93eae46eaae66955c84fefb9e0c963
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183343"
---
# <a name="bookmark-event"></a><span data-ttu-id="0c985-103">書簽事件</span><span class="sxs-lookup"><span data-stu-id="0c985-103">Bookmark Event</span></span>

<span data-ttu-id="0c985-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="0c985-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0c985-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="0c985-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0c985-106">發生于已啟用您的應用程式所定義之語音文字字串中的書簽時。</span><span class="sxs-lookup"><span data-stu-id="0c985-106">Occurs when a bookmark in a speech text string that your application defined is activated.</span></span>

</dd> <dt>

<span data-ttu-id="0c985-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="0c985-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0c985-108">**子\*\*\*代理程式* \_ **書簽** **(ByVal** *BookmarkID \* \* \* )**</span><span class="sxs-lookup"><span data-stu-id="0c985-108">**Sub** *agent*\_**Bookmark** **(ByVal** *BookmarkID\*\*\*)*\*</span></span>



| <span data-ttu-id="0c985-109">部分</span><span class="sxs-lookup"><span data-stu-id="0c985-109">Part</span></span>         | <span data-ttu-id="0c985-110">描述</span><span class="sxs-lookup"><span data-stu-id="0c985-110">Description</span></span>                                     |
|--------------|-------------------------------------------------|
| <span data-ttu-id="0c985-111">*BookmarkID*</span><span class="sxs-lookup"><span data-stu-id="0c985-111">*BookmarkID*</span></span> | <span data-ttu-id="0c985-112">識別書簽編號的長整數。</span><span class="sxs-lookup"><span data-stu-id="0c985-112">A Long integer identifying the bookmark number.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="0c985-113">備註</span><span class="sxs-lookup"><span data-stu-id="0c985-113">Remarks</span></span>

<span data-ttu-id="0c985-114">若要指定書簽事件，請在提供的文字中使用 [**說話**](speak-method.md) 方法與 **Mrk** 標記。</span><span class="sxs-lookup"><span data-stu-id="0c985-114">To specify a bookmark event, use the [**Speak**](speak-method.md) method with a **Mrk** tag in your supplied text.</span></span> <span data-ttu-id="0c985-115">如需標記的詳細資訊，請參閱語音輸出標記。</span><span class="sxs-lookup"><span data-stu-id="0c985-115">For more information about tags, see Speech Output Tags.</span></span>

 

 




