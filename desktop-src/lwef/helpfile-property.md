---
title: 內容説明屬性
description: 內容説明屬性
ms.assetid: 18a5fd9b-4ca7-4701-9993-1e0c55f6e232
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d5307abfba0f884261f5b4a21131a75cf87224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673480"
---
# <a name="helpfile-property"></a><span data-ttu-id="32e4e-103">內容説明屬性</span><span class="sxs-lookup"><span data-stu-id="32e4e-103">HelpFile Property</span></span>

<span data-ttu-id="32e4e-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="32e4e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="32e4e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="32e4e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="32e4e-106">傳回或設定用戶端應用程式所提供之 Microsoft Windows 上下文相關說明檔的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="32e4e-106">Returns or sets the path and filename for a Microsoft Windows context-sensitive Help file supplied by the client application.</span></span>

</dd> <dt>

<span data-ttu-id="32e4e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="32e4e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="32e4e-108">*代理程式。\*\*\*字元 (*\*\* 」CharacterID \* \* \* ) 。\* \*  \[  =  *檔案名稱*\]</span><span class="sxs-lookup"><span data-stu-id="32e4e-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Helpfile** \[ = *Filename*\]</span></span>



| <span data-ttu-id="32e4e-109">部分</span><span class="sxs-lookup"><span data-stu-id="32e4e-109">Part</span></span>       | <span data-ttu-id="32e4e-110">描述</span><span class="sxs-lookup"><span data-stu-id="32e4e-110">Description</span></span>                                                                    |
|------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="32e4e-111">*檔案名稱*</span><span class="sxs-lookup"><span data-stu-id="32e4e-111">*Filename*</span></span> | <span data-ttu-id="32e4e-112">字串運算式，指定 Windows 說明檔的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="32e4e-112">A string expression specifying the path and filename of the Windows Help file.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32e4e-113">備註</span><span class="sxs-lookup"><span data-stu-id="32e4e-113">Remarks</span></span>

<span data-ttu-id="32e4e-114">如果您已為您的應用程式建立 Windows 說明檔，並設定字元的 [協助工具 **] 屬性，** 則當 [**HelpModeOn**](helpmodeon-property.md) 設定為 **True** ，且使用者按一下該字元或從快顯功能表中選取命令時，Agent 會自動呼叫說明。</span><span class="sxs-lookup"><span data-stu-id="32e4e-114">If you've created a Windows Help file for your application and set the character's **HelpFile** property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character or selects a command from its pop-up menu.</span></span> <span data-ttu-id="32e4e-115">如果您在所選 [**命令的 [屬性值**](helpcontextid-property.md) ] 屬性中指定內容編號，[說明] 會顯示對應于目前說明內容的主題;否則會顯示「沒有與這個專案相關聯的說明主題」。</span><span class="sxs-lookup"><span data-stu-id="32e4e-115">If you specified a context number in the [**HelpContextID**](helpcontextid-property.md) property of the selected command, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="32e4e-116">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="32e4e-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="32e4e-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32e4e-117">See Also</span></span>

<span data-ttu-id="32e4e-118">[**HelpModeOn 屬性**](helpmodeon-property.md)， [**屬性內容屬性**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="32e4e-118">[**HelpModeOn property**](helpmodeon-property.md), [**HelpContextID property**](helpcontextid-property.md)</span></span>


 

 




