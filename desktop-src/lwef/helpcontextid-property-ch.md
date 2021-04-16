---
title: '內容屬性 (字元物件) '
description: '[上下文] 屬性'
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42006f74cc3668f8df9af2c2ffcd2515614ec735
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383626"
---
# <a name="helpcontextid-property-characters-object"></a><span data-ttu-id="f67f2-103">內容屬性 (字元物件) </span><span class="sxs-lookup"><span data-stu-id="f67f2-103">HelpContextID Property (Characters Object)</span></span>

<span data-ttu-id="f67f2-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="f67f2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f67f2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="f67f2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f67f2-106">傳回或設定字元的相關聯內容編號。</span><span class="sxs-lookup"><span data-stu-id="f67f2-106">Returns or sets an associated context number for the character.</span></span> <span data-ttu-id="f67f2-107">用來為字元提供即時線上說明。</span><span class="sxs-lookup"><span data-stu-id="f67f2-107">Used to provide context-sensitive Help for the character.</span></span>

</dd> <dt>

<span data-ttu-id="f67f2-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="f67f2-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f67f2-109">\*agent. \***字元 ( "**_CharacterID_\*_" ) 。_ \*  \[  =  *值* 比\]</span><span class="sxs-lookup"><span data-stu-id="f67f2-109">*agent.\***Characters("**_CharacterID_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="f67f2-110">部分</span><span class="sxs-lookup"><span data-stu-id="f67f2-110">Part</span></span>     | <span data-ttu-id="f67f2-111">描述</span><span class="sxs-lookup"><span data-stu-id="f67f2-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="f67f2-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="f67f2-112">*Number*</span></span> | <span data-ttu-id="f67f2-113">指定有效內容編號的整數。</span><span class="sxs-lookup"><span data-stu-id="f67f2-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f67f2-114">備註</span><span class="sxs-lookup"><span data-stu-id="f67f2-114">Remarks</span></span>

<span data-ttu-id="f67f2-115">若要支援字元的即時線上說明，請在編譯說明檔時，將內容編號指派給您用於關聯說明主題的字元。</span><span class="sxs-lookup"><span data-stu-id="f67f2-115">To support context-sensitive Help for the character, assign the context number to the character you use for the associated Help topic when you compile your Help file.</span></span> <span data-ttu-id="f67f2-116">這個屬性只適用于字元的用戶端;此設定不會影響其他用戶端的字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="f67f2-116">This property applies only to the client of the character; the setting does not affect other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="f67f2-117">如果您已為您的應用程式建立 Windows 說明檔，並設定字元的 [協助工具 [**] 屬性，**](helpfile-property.md) 則當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** ，且使用者按一下該字元時，代理程式會自動呼叫說明。</span><span class="sxs-lookup"><span data-stu-id="f67f2-117">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character.</span></span> <span data-ttu-id="f67f2-118">如果 [提供者] 中有內容 [**編號，Agent**](helpcontextid-property.md)就會呼叫 [說明]，並搜尋目前內容編號所識別的主題。</span><span class="sxs-lookup"><span data-stu-id="f67f2-118">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="f67f2-119">目前的內容編號是 **字元的 [值] 的值** 。</span><span class="sxs-lookup"><span data-stu-id="f67f2-119">The current context number is the value of **HelpContextID** for the character.</span></span>

> [!Note]  
> <span data-ttu-id="f67f2-120">建立說明檔需要 Microsoft Windows 說明編譯器。</span><span class="sxs-lookup"><span data-stu-id="f67f2-120">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="f67f2-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f67f2-121">See Also</span></span>

[<span data-ttu-id="f67f2-122">**內容説明屬性**</span><span class="sxs-lookup"><span data-stu-id="f67f2-122">**HelpFile property**</span></span>](helpfile-property.md)


 

 




