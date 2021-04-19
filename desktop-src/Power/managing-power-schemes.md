---
description: 電源配置管理
ms.assetid: b79e7b64-be56-4165-af59-a8251284d029
title: 電源配置管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867d7509e9a04e948818ff7a3a13638a5c9933b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975093"
---
# <a name="power-scheme-management"></a><span data-ttu-id="6541e-103">電源配置管理</span><span class="sxs-lookup"><span data-stu-id="6541e-103">Power Scheme Management</span></span>

<span data-ttu-id="6541e-104">每個電源配置都是由 **GUID** 來唯一識別。</span><span class="sxs-lookup"><span data-stu-id="6541e-104">Each power scheme is uniquely identified by a **GUID**.</span></span> <span data-ttu-id="6541e-105">若要列舉所有可用的電源配置，請使用 [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) 函數。</span><span class="sxs-lookup"><span data-stu-id="6541e-105">To enumerate all available power schemes, use the [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) function.</span></span> <span data-ttu-id="6541e-106">**PowerEnumerate** 也可用來取得指定配置的所有電源設定。</span><span class="sxs-lookup"><span data-stu-id="6541e-106">**PowerEnumerate** can also be used to retrieve all of the power settings for a specified scheme.</span></span>

<span data-ttu-id="6541e-107">目前正在系統上使用的電源配置稱為「使用中」電源配置或方案。</span><span class="sxs-lookup"><span data-stu-id="6541e-107">The power scheme that is currently in use on the system is called the active power scheme or plan.</span></span> <span data-ttu-id="6541e-108">若要取得使用中計畫的 **GUID** ，請呼叫 [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) 函數。</span><span class="sxs-lookup"><span data-stu-id="6541e-108">To retrieve the **GUID** of the active plan, call the [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) function.</span></span> <span data-ttu-id="6541e-109">若要變更作用中的電源計劃，請呼叫 [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) 函式。</span><span class="sxs-lookup"><span data-stu-id="6541e-109">To change the active power plan, call the [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) function.</span></span>

<span data-ttu-id="6541e-110">若要建立電源配置，您必須先使用 [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) 函式來複製現有的配置，並指定您想要作為新配置基礎之配置的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="6541e-110">To create a power scheme, you need to first duplicate an existing scheme by using the [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) function, specifying the **GUID** of the scheme you wish to base your new scheme upon.</span></span> <span data-ttu-id="6541e-111">您應該複製其中一個內建的配置，並依據您的需求修改電源設定。</span><span class="sxs-lookup"><span data-stu-id="6541e-111">You should copy one of the built-in schemes and modify the power settings to your needs.</span></span> <span data-ttu-id="6541e-112">請注意，建立電源計劃不會自動更新主動式電源計劃。</span><span class="sxs-lookup"><span data-stu-id="6541e-112">Note that creating a power plan does not automatically update the active power plan.</span></span> <span data-ttu-id="6541e-113">您必須一律呼叫 [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) 來更新使用中的電源計劃。</span><span class="sxs-lookup"><span data-stu-id="6541e-113">You must always call [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) to update the active power plan.</span></span> <span data-ttu-id="6541e-114">您可以修改現有的電源計劃，然後以同樣的方式套用。</span><span class="sxs-lookup"><span data-stu-id="6541e-114">Existing power plans can be modified and then applied in the same manner.</span></span>

<span data-ttu-id="6541e-115">若要移除電源計劃，請呼叫 [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) 函數。</span><span class="sxs-lookup"><span data-stu-id="6541e-115">To remove a power plan, call the [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) function.</span></span>

> [!Note]  
> <span data-ttu-id="6541e-116">若要取出系統電源狀態的其他資訊，請呼叫 [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) 函數。</span><span class="sxs-lookup"><span data-stu-id="6541e-116">To retrieve additional information about the system power state, call the [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6541e-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="6541e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6541e-118">電源配置</span><span class="sxs-lookup"><span data-stu-id="6541e-118">Power Schemes</span></span>](power-schemes.md)
</dt> </dl>

 

 



