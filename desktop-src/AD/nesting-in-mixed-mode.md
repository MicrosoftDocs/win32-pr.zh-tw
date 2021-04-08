---
title: 在混合模式中進行嵌套
description: 本主題列出混合模式網域中安全性群組的限制。
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- 混合模式 AD 中的嵌套
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d63d475edf77398a69a519a08f3803f69d67d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839284"
---
# <a name="nesting-in-mixed-mode"></a><span data-ttu-id="0a325-104">在混合模式中進行嵌套</span><span class="sxs-lookup"><span data-stu-id="0a325-104">Nesting in Mixed Mode</span></span>

<span data-ttu-id="0a325-105">本主題列出混合模式網域中安全性群組的限制。</span><span class="sxs-lookup"><span data-stu-id="0a325-105">This topic lists the restrictions of security groups in a mixed-mode domain.</span></span>

<span data-ttu-id="0a325-106">混合模式網域中的安全性群組有下列限制：</span><span class="sxs-lookup"><span data-stu-id="0a325-106">Security groups in a mixed-mode domain have the following restrictions:</span></span>

-   <span data-ttu-id="0a325-107">無法在混合模式網域中建立萬用群組，因為只有在 Windows 2000 原生模式網域中才支援通用範圍。</span><span class="sxs-lookup"><span data-stu-id="0a325-107">Universal groups cannot be created in mixed-mode domains because the universal scope is supported only in Windows 2000 native-mode domains.</span></span>
-   <span data-ttu-id="0a325-108">全域群組可以包含群組所屬的相同網域中的帳戶。</span><span class="sxs-lookup"><span data-stu-id="0a325-108">A global group can contain accounts from the same domain to which the group belongs.</span></span> <span data-ttu-id="0a325-109">全域群組不能包含任何萬用群組、任何全域群組或其他網域中的帳戶。</span><span class="sxs-lookup"><span data-stu-id="0a325-109">A global group cannot contain any universal groups, any global group, or an account from another domain.</span></span>
-   <span data-ttu-id="0a325-110">網域本機群組可以包含來自任何網域或樹系的全域群組和帳戶。</span><span class="sxs-lookup"><span data-stu-id="0a325-110">A domain local group can contain global groups and accounts from any domain or forest.</span></span> <span data-ttu-id="0a325-111">網域本機群組不能包含任何其他的網域本機群組。</span><span class="sxs-lookup"><span data-stu-id="0a325-111">A domain local group cannot contain any other domain local group.</span></span>

<span data-ttu-id="0a325-112">請注意，您可以根據原生模式的嵌套規則來嵌套通訊群組。</span><span class="sxs-lookup"><span data-stu-id="0a325-112">Be aware that distribution groups can be nested according to the nesting rules for native mode.</span></span>

 

 




