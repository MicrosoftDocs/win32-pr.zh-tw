---
description: 當使用密碼編譯服務提供者 Csp 時，請記住下列慣例。
ms.assetid: 70053b89-4d39-4a86-985a-0e8f05fbc9c0
title: 使用 Csp：一般進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f067ef0e3cd837b1b347daac3e3da21543047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992009"
---
# <a name="using-csps-general-processes"></a><span data-ttu-id="e4e03-103">使用 Csp：一般進程</span><span class="sxs-lookup"><span data-stu-id="e4e03-103">Using CSPs: General Processes</span></span>

<span data-ttu-id="e4e03-104">當使用 [*密碼編譯服務提供者*](../secgloss/c-gly.md) csp 時，請記住下列慣例。</span><span class="sxs-lookup"><span data-stu-id="e4e03-104">When using [*cryptographic service providers*](../secgloss/c-gly.md) CSPs, keep the following conventions in mind.</span></span>

## <a name="private-key-caching"></a><span data-ttu-id="e4e03-105">私密金鑰快取</span><span class="sxs-lookup"><span data-stu-id="e4e03-105">Private Key Caching</span></span>

<span data-ttu-id="e4e03-106">CSP 可以快取部分 [*私密金鑰*](../secgloss/p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e03-106">A CSP can cache some [*private keys*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="e4e03-107">您可以在全域上控制這個私密金鑰快取，但不能在應用程式特定的基礎上進行控制。</span><span class="sxs-lookup"><span data-stu-id="e4e03-107">It is possible to control this private key caching on a global, but not an application-specific, basis.</span></span> <span data-ttu-id="e4e03-108">您可以藉由修改特定的登錄設定來進行快取變更。</span><span class="sxs-lookup"><span data-stu-id="e4e03-108">Caching changes are made by modifying certain registry settings.</span></span> <span data-ttu-id="e4e03-109">如需詳細資訊，請參閱私密金鑰快取 [**常數**](private-key-caching-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e03-109">For more information, see [**Private Key Caching Constants**](private-key-caching-constants.md).</span></span>

## <a name="example-code-conventions"></a><span data-ttu-id="e4e03-110">範例程式碼慣例</span><span class="sxs-lookup"><span data-stu-id="e4e03-110">Example Code Conventions</span></span>

<span data-ttu-id="e4e03-111">為了提供更簡潔、更容易閱讀的程式碼，範例中不一定會有良好程式設計實務的部分原則。</span><span class="sxs-lookup"><span data-stu-id="e4e03-111">To provide more concise, more readable code, some principles of good programming practice are not always followed in the examples.</span></span> <span data-ttu-id="e4e03-112">尤其是：</span><span class="sxs-lookup"><span data-stu-id="e4e03-112">In particular:</span></span>

-   <span data-ttu-id="e4e03-113">只會顯示有限的錯誤回應。</span><span class="sxs-lookup"><span data-stu-id="e4e03-113">Only limited error responses are shown.</span></span> <span data-ttu-id="e4e03-114">妥善撰寫的完整程式會檢查傳回的錯誤碼，並在發生錯誤時執行適當的動作。</span><span class="sxs-lookup"><span data-stu-id="e4e03-114">Well-written, complete programs check returned error codes and perform appropriate actions when an error is encountered.</span></span>
-   <span data-ttu-id="e4e03-115">只會執行有限的記憶體和資源管理。</span><span class="sxs-lookup"><span data-stu-id="e4e03-115">Only limited memory and resource management is done.</span></span> <span data-ttu-id="e4e03-116">撰寫完善的程式會摧毀所有的金鑰和 [*雜湊*](../secgloss/h-gly.md)、釋放所有配置的記憶體、關閉所有檔案，以及釋放所有控制碼。</span><span class="sxs-lookup"><span data-stu-id="e4e03-116">Well-written, complete programs destroy all keys and [*hashes*](../secgloss/h-gly.md), free all allocated memory, close all files, and release all handles.</span></span> <span data-ttu-id="e4e03-117">這些範例僅提供使用執行這些工作的函式的有限示範。</span><span class="sxs-lookup"><span data-stu-id="e4e03-117">These examples provide only limited demonstrations of the use of functions that perform these tasks.</span></span> <span data-ttu-id="e4e03-118">這些範例在程式終止時，不會執行任何記憶體或資源管理工作，因為發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="e4e03-118">These examples perform no memory or resource management tasks in the case of program termination due to errors.</span></span>

<span data-ttu-id="e4e03-119">下列主題提供有關程式範例和範例程式碼的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="e4e03-119">The following topics present general information about procedure examples as well as sample code.</span></span>

-   [<span data-ttu-id="e4e03-120">正在抓取未知長度的資料</span><span class="sxs-lookup"><span data-stu-id="e4e03-120">Retrieving Data of Unknown Length</span></span>](retrieving-data-of-unknown-length.md)
-   [<span data-ttu-id="e4e03-121">列舉支援的通訊協定</span><span class="sxs-lookup"><span data-stu-id="e4e03-121">Enumerating Supported Protocols</span></span>](enumerating-supported-protocols.md)

 

 
