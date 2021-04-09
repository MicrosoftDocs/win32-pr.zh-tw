---
title: '內容屬性 (命令物件) '
description: '[上下文] 屬性'
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ef0fcfb24aee7aed75f8eb794e81291207ea24
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093704"
---
# <a name="helpcontextid-property-command-object"></a><span data-ttu-id="e7b93-103">內容屬性 (命令物件) </span><span class="sxs-lookup"><span data-stu-id="e7b93-103">HelpContextID Property (Command Object)</span></span>

<span data-ttu-id="e7b93-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="e7b93-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e7b93-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="e7b93-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e7b93-106">傳回或設定 [**命令**](/windows/desktop/lwef/the-command-object) 物件的相關聯內容編號。</span><span class="sxs-lookup"><span data-stu-id="e7b93-106">Returns or sets an associated context number for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="e7b93-107">用來提供 **命令** 物件的即時線上說明。</span><span class="sxs-lookup"><span data-stu-id="e7b93-107">Used to provide context-sensitive Help for the **Command** object.</span></span>

</dd> <dt>

<span data-ttu-id="e7b93-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="e7b93-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e7b93-109">\*agent. \***字元 ( "**_CharacterID_\*_" ) . 命令 ( "" ) 。_ \*  \[  =  *值* 比\]</span><span class="sxs-lookup"><span data-stu-id="e7b93-109">*agent.\***Characters("**_CharacterID_*_").Commands("").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="e7b93-110">部分</span><span class="sxs-lookup"><span data-stu-id="e7b93-110">Part</span></span>     | <span data-ttu-id="e7b93-111">描述</span><span class="sxs-lookup"><span data-stu-id="e7b93-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="e7b93-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="e7b93-112">*Number*</span></span> | <span data-ttu-id="e7b93-113">指定有效內容編號的整數。</span><span class="sxs-lookup"><span data-stu-id="e7b93-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7b93-114">備註</span><span class="sxs-lookup"><span data-stu-id="e7b93-114">Remarks</span></span>

<span data-ttu-id="e7b93-115">如果您已建立應用程式的 Windows 說明檔，並將字元的 [ [**檔案説明] 屬性設定**](helpfile-property.md) 為檔案，則當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** 且使用者選取命令時，代理程式會自動呼叫說明。</span><span class="sxs-lookup"><span data-stu-id="e7b93-115">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property to the file, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="e7b93-116">如果您在 [協助工具] 中設定內容編號，Agent 會呼叫 [說明 [**]，並**](helpcontextid-property.md)搜尋目前內容編號所識別的主題。</span><span class="sxs-lookup"><span data-stu-id="e7b93-116">If you set a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="e7b93-117">目前的內容編號是 **命令的值** 為的值。</span><span class="sxs-lookup"><span data-stu-id="e7b93-117">The current context number is the value of **HelpContextID** for the command.</span></span>

<span data-ttu-id="e7b93-118">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="e7b93-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="e7b93-119">建立說明檔需要 Microsoft Windows 說明編譯器。</span><span class="sxs-lookup"><span data-stu-id="e7b93-119">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="e7b93-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7b93-120">See Also</span></span>

[<span data-ttu-id="e7b93-121">**內容説明屬性**</span><span class="sxs-lookup"><span data-stu-id="e7b93-121">**HelpFile property**</span></span>](helpfile-property.md)


 

 
