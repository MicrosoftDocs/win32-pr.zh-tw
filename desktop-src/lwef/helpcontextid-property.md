---
title: '內容屬性 (命令集合物件) '
description: 瞭解命令集合物件的 [上下文] 屬性。 Microsoft Agent 已于 Windows 7 淘汰。
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ed6ccf40545e15b3603ce5abe80ef94ff4272a
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068234"
---
# <a name="helpcontextid-property-commands-collection-object"></a><span data-ttu-id="7175c-104">內容屬性 (命令集合物件) </span><span class="sxs-lookup"><span data-stu-id="7175c-104">HelpContextID Property (Commands Collection Object)</span></span>

<span data-ttu-id="7175c-105">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="7175c-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="7175c-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="7175c-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="7175c-107">傳回或設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 物件的相關聯內容編號。</span><span class="sxs-lookup"><span data-stu-id="7175c-107">Returns or sets an associated context number for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="7175c-108">用來提供 **命令** 物件的即時線上說明。</span><span class="sxs-lookup"><span data-stu-id="7175c-108">Used to provide context-sensitive Help for the **Commands** object.</span></span>

</dd> <dt>

<span data-ttu-id="7175c-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="7175c-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="7175c-110">\*agent. \***字元 ( "**_CharacterID_*_" ) . 命令 ( "_*_name_\*_" ) 。_ \*  \[  =  *值* 比\]</span><span class="sxs-lookup"><span data-stu-id="7175c-110">*agent.\***Characters("**_CharacterID_*_").Commands("_*_name_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="7175c-111">部分</span><span class="sxs-lookup"><span data-stu-id="7175c-111">Part</span></span>     | <span data-ttu-id="7175c-112">描述</span><span class="sxs-lookup"><span data-stu-id="7175c-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="7175c-113">*Number*</span><span class="sxs-lookup"><span data-stu-id="7175c-113">*Number*</span></span> | <span data-ttu-id="7175c-114">指定有效內容編號的整數。</span><span class="sxs-lookup"><span data-stu-id="7175c-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7175c-115">備註</span><span class="sxs-lookup"><span data-stu-id="7175c-115">Remarks</span></span>

<span data-ttu-id="7175c-116">如果您已為您的應用程式建立 Windows 說明檔，並設定字元的 [協助工具 [**] 屬性，**](helpfile-property.md) 則當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** 且使用者選取 [ [**命令**](/windows/desktop/lwef/the-commands-collection-object) ] 物件時，代理程式會自動呼叫說明。</span><span class="sxs-lookup"><span data-stu-id="7175c-116">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="7175c-117">如果您在 [協助工具] 中設定內容編號，Agent 會呼叫 [說明 **]，並** 搜尋該內容編號所識別的主題。</span><span class="sxs-lookup"><span data-stu-id="7175c-117">If you set a context number in the **HelpContextID**, Agent calls Help and searches for the topic identified by that context number.</span></span>

<span data-ttu-id="7175c-118">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="7175c-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="7175c-119">建立說明檔需要 Microsoft Windows 說明編譯器。</span><span class="sxs-lookup"><span data-stu-id="7175c-119">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="7175c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7175c-120">See Also</span></span>

[<span data-ttu-id="7175c-121">**內容説明屬性**</span><span class="sxs-lookup"><span data-stu-id="7175c-121">**HelpFile property**</span></span>](helpfile-property.md)


 

 
