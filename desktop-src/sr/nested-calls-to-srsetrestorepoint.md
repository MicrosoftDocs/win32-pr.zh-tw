---
title: SRSetRestorePoint 的嵌套呼叫
description: 本主題說明透過 BEGIN \_ nested \_ 系統 \_ 變更和結束 \_ 嵌套 \_ 系統 \_ 變更事件種類對 SRSetRestorePoint 進行的嵌套呼叫支援。
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5654dc7bb6e42ae55cbad18fc2418df3bdd942d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183608"
---
# <a name="nested-calls-to-srsetrestorepoint"></a><span data-ttu-id="34245-103">SRSetRestorePoint 的嵌套呼叫</span><span class="sxs-lookup"><span data-stu-id="34245-103">Nested Calls to SRSetRestorePoint</span></span>

<span data-ttu-id="34245-104">本主題說明透過 BEGIN [](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) \_ nested \_ 系統 \_ 變更和結束 \_ 嵌套 \_ 系統 \_ 變更事件種類對 SRSetRestorePoint 進行的嵌套呼叫支援。</span><span class="sxs-lookup"><span data-stu-id="34245-104">This topic describes support for nested calls to [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) through the BEGIN\_NESTED\_SYSTEM\_CHANGE and END\_NESTED\_SYSTEM\_CHANGE event types.</span></span>

<span data-ttu-id="34245-105">使用這些事件種類時，應用程式可以安全地呼叫 [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) 。</span><span class="sxs-lookup"><span data-stu-id="34245-105">Applications can safely call [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) when using these event types.</span></span> <span data-ttu-id="34245-106">函數的第一個呼叫會建立還原點。</span><span class="sxs-lookup"><span data-stu-id="34245-106">The first call to the function creates a restore point.</span></span> <span data-ttu-id="34245-107">對函式的後續嵌套呼叫不會建立還原點。</span><span class="sxs-lookup"><span data-stu-id="34245-107">Subsequent nested calls to the function do not create restore points.</span></span> <span data-ttu-id="34245-108">例如，假設應用程式會對 **SRSetRestorePoint** 進行下列呼叫：</span><span class="sxs-lookup"><span data-stu-id="34245-108">For example, suppose an application makes the following calls to **SRSetRestorePoint**:</span></span><dl> <span data-ttu-id="34245-109">針對具有 dwEventType = BEGIN \_ NESTED \_ SYSTEM \_ 變更的還原點 A</span><span class="sxs-lookup"><span data-stu-id="34245-109">For restore point A with dwEventType = BEGIN\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="34245-110">針對具有 dwEventType = BEGIN \_ NESTED \_ SYSTEM \_ 變更的還原點 B</span><span class="sxs-lookup"><span data-stu-id="34245-110">For restore point B with dwEventType = BEGIN\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="34245-111">針對具有 dwEventType = END \_ NESTED \_ SYSTEM \_ 變更的還原點 B</span><span class="sxs-lookup"><span data-stu-id="34245-111">For restore point B with dwEventType = END\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="34245-112">With dwEventType = END \_ NESTED \_ SYSTEM \_ CHANGE 的還原點 A</span><span class="sxs-lookup"><span data-stu-id="34245-112">For restore point A with dwEventType = END\_NESTED\_SYSTEM\_CHANGE</span></span>  
</dl>

<span data-ttu-id="34245-113">第二個呼叫不會建立新的還原點，因為呼叫是嵌套的。</span><span class="sxs-lookup"><span data-stu-id="34245-113">The second call does not create a new restore point because the call is nested.</span></span>

 

 




