---
description: 程式限制範例
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: 程式限制範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1fde65fa1870ac3ed118bd7c9f95c6add5192f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984997"
---
# <a name="example-program-limitations"></a><span data-ttu-id="6472b-103">程式限制範例</span><span class="sxs-lookup"><span data-stu-id="6472b-103">Example Program Limitations</span></span>

<span data-ttu-id="6472b-104">在這些範例程式中，不一定會遵循良好的程式設計實務準則，以提供更簡潔、更容易閱讀的程式碼。</span><span class="sxs-lookup"><span data-stu-id="6472b-104">Principles of good programming practice are not always followed in these sample programs in order to provide more concise, more readable code.</span></span> <span data-ttu-id="6472b-105">尤其是：</span><span class="sxs-lookup"><span data-stu-id="6472b-105">In particular:</span></span>

-   <span data-ttu-id="6472b-106">只會顯示有限的錯誤回應。</span><span class="sxs-lookup"><span data-stu-id="6472b-106">Only limited error responses are shown.</span></span> <span data-ttu-id="6472b-107">工作程式應一律檢查傳回的錯誤碼，並在發生錯誤時執行適當的動作。</span><span class="sxs-lookup"><span data-stu-id="6472b-107">Working programs should always check returned error codes and perform appropriate actions when an error is encountered.</span></span>
-   <span data-ttu-id="6472b-108">只會執行有限的記憶體和資源管理。</span><span class="sxs-lookup"><span data-stu-id="6472b-108">Only limited memory and resource management is done.</span></span> <span data-ttu-id="6472b-109">在工作程式中，所有的金鑰和 [*雜湊*](../secgloss/h-gly.md) 都應該終結、所有配置的記憶體都應該釋出、所有的檔案都應該關閉，而且所有的控制碼都應該釋放出來。</span><span class="sxs-lookup"><span data-stu-id="6472b-109">In working programs, all keys and [*hashes*](../secgloss/h-gly.md) should be destroyed, all allocated memory should be freed, all files should be closed, and all handles should be released.</span></span> <span data-ttu-id="6472b-110">這些範例程式只提供使用執行這些工作的函式的有限示範。</span><span class="sxs-lookup"><span data-stu-id="6472b-110">These example programs provide only limited demonstrations of the use of functions that perform these tasks.</span></span> <span data-ttu-id="6472b-111">這些範例程式在程式終止時，不會執行任何記憶體或資源管理工作，因為發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="6472b-111">These example programs perform no memory or resource management tasks in the case of program termination due to errors.</span></span>

 

 
