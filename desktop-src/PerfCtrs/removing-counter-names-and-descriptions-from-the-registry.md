---
description: Unlodctr 工具會移除 lodctr 所建立的登錄專案。
ms.assetid: 83c0fb91-857c-40d9-8fb8-8734c1b573c4
title: 從登錄中移除計數器名稱和描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ea8c0a8efbe9a798f980a061c6cfc65745b89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977319"
---
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a><span data-ttu-id="6500b-103">從登錄中移除計數器名稱和描述</span><span class="sxs-lookup"><span data-stu-id="6500b-103">Removing Counter Names and Descriptions from the Registry</span></span>

<span data-ttu-id="6500b-104">**Unlodctr** 工具會移除 **lodctr** 所建立的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="6500b-104">The **unlodctr** tool removes the registry entries created by **lodctr**.</span></span> <span data-ttu-id="6500b-105">您傳遞給 **unlodctr** 的應用程式名稱必須與您在 **服務** 金鑰下建立的 [應用程式金鑰名稱](creating-the-applications-performance-key.md)相符。</span><span class="sxs-lookup"><span data-stu-id="6500b-105">The application name that you pass to **unlodctr** must match the [name of the application key](creating-the-applications-performance-key.md) that you created under the **Services** key.</span></span> <span data-ttu-id="6500b-106">如需執行 **unlodctr** 的詳細資訊，請參閱說明及支援中心。</span><span class="sxs-lookup"><span data-stu-id="6500b-106">For details on running **unlodctr** see, Help and Support Center.</span></span>

## <a name="using-unlodctr"></a><span data-ttu-id="6500b-107">使用 unlodctr</span><span class="sxs-lookup"><span data-stu-id="6500b-107">Using unlodctr</span></span>

<span data-ttu-id="6500b-108">**Unlodctr** 工具會查閱第一個和最後一個計數器，並在您的應用程式 **效能** 金鑰下使用類似的命名登錄值來協助索引值。</span><span class="sxs-lookup"><span data-stu-id="6500b-108">The **unlodctr** tool looks up the first and last counter and help index values using the like named registry values under your application's **Performance** key.</span></span> <span data-ttu-id="6500b-109">**Unlodctr** 工具會使用索引值的範圍來移除 **計數器** 的文字 **，以及每** 個語言識別項的說明值。</span><span class="sxs-lookup"><span data-stu-id="6500b-109">The **unlodctr** tool uses the range of index values to remove the text from **Counters** and **Help** values for each language identifier.</span></span>

<span data-ttu-id="6500b-110">**Unlodctr** 會使用索引值對登錄進行下列變更。</span><span class="sxs-lookup"><span data-stu-id="6500b-110">Using the index values, **unlodctr** makes the following changes to the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = updated if changed
                  Last Help = updated if changed
                  \009
                     Counters = application text removed
                     Help = application text removed
                  \supported language, other than English
                     Counters = application text removed
                     Help = application text removed
```

<span data-ttu-id="6500b-111">**Unlodctr** 工具也會從應用程式的 **效能** 索引鍵中移除 **第一個計數器**、**最後一個計數器**、**第一個** 說明、**最後** 一個說明和 **物件清單** 值，其位於 **HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ *應用程式名稱* \\ **效能**。</span><span class="sxs-lookup"><span data-stu-id="6500b-111">The **unlodctr** tool also removes the **First Counter**, **Last Counter**, **First Help**, **Last Help**, and **Object List** values from the application's **Performance** key located at **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\*application-name*\\**Performance**.</span></span>

> [!Note]  
> <span data-ttu-id="6500b-112">**Unlodctr**， [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)的卸載函式是在 Loadperf 中宣告，並且從 Loadperf.dll 匯出。</span><span class="sxs-lookup"><span data-stu-id="6500b-112">The unloading function of **unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), is declared in Loadperf.h and exported from Loadperf.dll.</span></span> <span data-ttu-id="6500b-113">這可讓您直接從卸載程式呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="6500b-113">This allows you to call this function directly from your uninstall program.</span></span>

 

 

 



