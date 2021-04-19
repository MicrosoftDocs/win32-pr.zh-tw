---
description: '\_ \_ 當安裝程式提示使用者插入 cd-rom 時，就會有 MsiPromptForCD Mutex。'
ms.assetid: f6319cda-48ac-4351-8eb5-f326490e3aff
title: __MsiPromptForCD Mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e646b23a003d10cce29807297e56abaebf3d935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975054"
---
# <a name="__msipromptforcd-mutex"></a><span data-ttu-id="ab036-103">\_\_MsiPromptForCD Mutex</span><span class="sxs-lookup"><span data-stu-id="ab036-103">\_\_MsiPromptForCD Mutex</span></span>

<span data-ttu-id="ab036-104">\_ \_ 當安裝程式提示使用者插入 cd-rom 時，就會有 MsiPromptForCD Mutex。</span><span class="sxs-lookup"><span data-stu-id="ab036-104">The \_\_MsiPromptForCD Mutex exists when the installer prompts the user to insert a CD-ROM.</span></span> <span data-ttu-id="ab036-105">自動播放程式應該會在 \_ \_ 開始之前，檢查 MsiPromptForCD mutex 目前未設定。</span><span class="sxs-lookup"><span data-stu-id="ab036-105">Autoplay programs should check that the \_\_MsiPromptForCD mutex is not currently set before starting.</span></span> <span data-ttu-id="ab036-106">請注意，在進行 InProgress 按鍵或 MSIExecute Mutex 之前，可能會出現 CD-ROM 提示 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ab036-106">Note that it is possible for a CD-ROM prompt to occur before either the InProgress key or the \_MSIExecute Mutex exist.</span></span>

 

 



