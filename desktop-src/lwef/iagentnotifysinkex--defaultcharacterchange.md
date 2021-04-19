---
title: IAgentNotifySinkEx DefaultCharacterChange
description: IAgentNotifySinkEx DefaultCharacterChange
ms.assetid: 13acb502-e247-433f-abf3-2d78a2d6a4a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ec212887d17d1aa59d942ece79b3e6928900ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966808"
---
# <a name="iagentnotifysinkexdefaultcharacterchange"></a><span data-ttu-id="5cc3c-103">IAgentNotifySinkEx：:D efaultCharacterChange</span><span class="sxs-lookup"><span data-stu-id="5cc3c-103">IAgentNotifySinkEx::DefaultCharacterChange</span></span>

<span data-ttu-id="5cc3c-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="5cc3c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DefaultCharacterChange(
   BSTR bszGUID  // character identifier
);
```

<span data-ttu-id="5cc3c-105">在預設字元變更時通知用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="5cc3c-105">Notifies a client application when the default character changes.</span></span>

-   <span data-ttu-id="5cc3c-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="5cc3c-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="5cc3c-107"><span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*</span><span class="sxs-lookup"><span data-stu-id="5cc3c-107"><span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*</span></span>
</dt> <dd>

<span data-ttu-id="5cc3c-108">字元的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5cc3c-108">The unique identifier for the character.</span></span>

</dd> </dl>

<span data-ttu-id="5cc3c-109">當使用者變更指派為使用者預設字元的字元時，伺服器會將此事件傳送給已載入預設字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="5cc3c-109">When the user changes the character assigned as the user's default character, the server sends this event to clients that have loaded the default character.</span></span> <span data-ttu-id="5cc3c-110">此事件會傳回字元的唯一識別碼 (GUID) 以大括弧和連字號格式格式化，這是在使用 Microsoft Agent 字元編輯器建立字元時所定義。</span><span class="sxs-lookup"><span data-stu-id="5cc3c-110">The event returns the character's unique identifier (GUID) formatted with braces and dashes, which is defined when the character is built with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="5cc3c-111">出現新的字元時，它會假設與任何已載入的字元實例或先前的預設字元相同的大小，) 的順序 (。</span><span class="sxs-lookup"><span data-stu-id="5cc3c-111">When the new character appears, it assumes the same size as any already loaded instance of the character or the previous default character (in that order).</span></span>

## <a name="see-also"></a><span data-ttu-id="5cc3c-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5cc3c-112">See Also</span></span>

[<span data-ttu-id="5cc3c-113">**IAgent：： Load**</span><span class="sxs-lookup"><span data-stu-id="5cc3c-113">**IAgent::Load**</span></span>](iagent--load.md)


 

 




