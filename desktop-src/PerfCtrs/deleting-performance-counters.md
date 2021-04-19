---
description: 若要從系統移除您的應用程式效能計數器，請執行下列步驟。
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: 正在刪除效能計數器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba257a1a44b5272543b7e61dcdc4b4e96225c160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977321"
---
# <a name="deleting-performance-counters"></a><span data-ttu-id="9bff9-103">正在刪除效能計數器</span><span class="sxs-lookup"><span data-stu-id="9bff9-103">Deleting Performance Counters</span></span>

<span data-ttu-id="9bff9-104">若要從系統移除您應用程式的效能計數器，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="9bff9-104">To remove your application's performance counters from the system, perform the following steps.</span></span>

1.  <span data-ttu-id="9bff9-105">使用電腦隨附的 **unlodctr** 工具，從登錄中移除計數器相關資料。</span><span class="sxs-lookup"><span data-stu-id="9bff9-105">Use the **unlodctr** tool included with the computer to remove the counter related data from the registry.</span></span> <span data-ttu-id="9bff9-106">請注意， **unlodctr** 工具必須要有應用程式的 **效能** 金鑰才能成功。</span><span class="sxs-lookup"><span data-stu-id="9bff9-106">Note that the application's **Performance** key must exist for the **unlodctr** tool to succeed.</span></span> <span data-ttu-id="9bff9-107">如需詳細資訊，請參閱 [從登錄中移除計數器名稱和描述](removing-counter-names-and-descriptions-from-the-registry.md)。</span><span class="sxs-lookup"><span data-stu-id="9bff9-107">For details, see [Removing Counter Names and Descriptions from the Registry](removing-counter-names-and-descriptions-from-the-registry.md).</span></span>
2.  <span data-ttu-id="9bff9-108">刪除應用程式 **服務** 金鑰下的 **效能** 和 **連結** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9bff9-108">Delete the **Performance** and **Linkage** keys under the application's **Services** key.</span></span> <span data-ttu-id="9bff9-109">若要刪除這些金鑰，請使用 Regedt32.exe 公用程式或呼叫 [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)。</span><span class="sxs-lookup"><span data-stu-id="9bff9-109">To delete these keys, use either the Regedt32.exe utility or call [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).</span></span>

 

 
