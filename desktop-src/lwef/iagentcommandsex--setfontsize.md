---
title: IAgentCommandsEx SetFontSize
description: IAgentCommandsEx SetFontSize
ms.assetid: 095f78d2-ef91-4880-ad49-dd9a94f02891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19bb9a638141dc3cebe683748500510ea848a664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463016"
---
# <a name="iagentcommandsexsetfontsize"></a><span data-ttu-id="66f16-103">IAgentCommandsEx::SetFontSize</span><span class="sxs-lookup"><span data-stu-id="66f16-103">IAgentCommandsEx::SetFontSize</span></span>

<span data-ttu-id="66f16-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="66f16-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in character's pop-up menu
);
```

<span data-ttu-id="66f16-105">設定在字元的快顯功能表中所顯示字型的大小。</span><span class="sxs-lookup"><span data-stu-id="66f16-105">Sets the size of the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="66f16-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="66f16-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="66f16-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span><span class="sxs-lookup"><span data-stu-id="66f16-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="66f16-108">字型的大小。</span><span class="sxs-lookup"><span data-stu-id="66f16-108">The size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="66f16-109">當您的用戶端應用程式為輸入-主動時，這個屬性會決定用來在字元的快顯功能表中顯示文字的字型的點大小。</span><span class="sxs-lookup"><span data-stu-id="66f16-109">This property determines the point size of the font used to display text in the character's pop-up menu when your client application is input-active.</span></span> <span data-ttu-id="66f16-110">字型設定的預設值是以字元語言識別項設定的功能表字型設定為基礎，如果未設定則為-使用者預設語言設定。</span><span class="sxs-lookup"><span data-stu-id="66f16-110">The default value for the font setting is based on the menu font setting for the character's language ID setting-or if that's not set-the user default language setting.</span></span> <span data-ttu-id="66f16-111">如果不是輸入-主動，用戶端應用程式的 [**命令**](/windows/desktop/lwef/the-command-object)[**標題**](caption-property.md)文字會出現在針對輸入-主動用戶端指定的點大小。</span><span class="sxs-lookup"><span data-stu-id="66f16-111">If not input-active, your client application's [**Command**](/windows/desktop/lwef/the-command-object) [**Caption**](caption-property.md) text appears in the point size specified for the input-active client.</span></span>

<span data-ttu-id="66f16-112">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="66f16-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="66f16-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66f16-113">See Also</span></span>

<span data-ttu-id="66f16-114">[**IAgentCommandsEx：： GetFontSize**](iagentcommandsex--getfontsize.md)、 [**IAgentCommandsEx：： GetFontName**](iagentcommandsex--getfontname.md)、 [**IAgentCommandsEx：： SetFontName**](iagentcommandsex--setfontname.md)</span><span class="sxs-lookup"><span data-stu-id="66f16-114">[**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)</span></span>


 

 