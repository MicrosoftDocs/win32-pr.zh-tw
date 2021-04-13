---
title: 結構化儲存體 API 函數
description: 結構化儲存體的某些 API 函式是協助程式函式，可對其他 API 函式和介面方法執行一連串的呼叫。 您可以使用這些 helper 函式作為簡短的剪下。
ms.assetid: 99ac66bc-db73-4811-9a39-fc49bb90ada8
keywords:
- 結構化儲存體 Strctd Stg.，基礎，API 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df87e8c5910c6da23ca518d05541a69e7070f8bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300259"
---
# <a name="structured-storage-api-functions"></a><span data-ttu-id="a7fce-105">結構化儲存體 API 函數</span><span class="sxs-lookup"><span data-stu-id="a7fce-105">Structured Storage API Functions</span></span>

<span data-ttu-id="a7fce-106">結構化儲存體的某些 API 函式是協助程式函式，可對其他 API 函式和介面方法執行一連串的呼叫。</span><span class="sxs-lookup"><span data-stu-id="a7fce-106">Some of the API functions for structured storage are helper functions that perform a sequence of calls to other API functions and interface methods.</span></span> <span data-ttu-id="a7fce-107">您可以使用這些 helper 函式作為簡短的剪下。</span><span class="sxs-lookup"><span data-stu-id="a7fce-107">You can use these helper functions as short cuts.</span></span>

<span data-ttu-id="a7fce-108">其他 API 函式可讓您存取 COM 的結構化儲存體、複合檔案的執行。</span><span class="sxs-lookup"><span data-stu-id="a7fce-108">Other API functions provide access to COM's implementation of structured storage, Compound Files.</span></span>

<span data-ttu-id="a7fce-109">另外還有另一組 API 函數可讓您將 OLE 1 物件轉換成結構化儲存區。</span><span class="sxs-lookup"><span data-stu-id="a7fce-109">Still another set of API functions enable you to convert OLE 1 objects to structured storage.</span></span> <span data-ttu-id="a7fce-110">您可以使用這些函式來判斷物件類別是否來自 OLE 1，以及轉換 OLE 1 和目前 COM 儲存格式之間的物件。</span><span class="sxs-lookup"><span data-stu-id="a7fce-110">You can use these functions to determine whether an object class is from OLE 1 and to convert objects between OLE 1 and current COM storage formats.</span></span>

<span data-ttu-id="a7fce-111">最後，有 API 函式可用於轉換和模擬其他物件。</span><span class="sxs-lookup"><span data-stu-id="a7fce-111">Finally, there are API functions for converting and emulating other objects.</span></span> <span data-ttu-id="a7fce-112">這些函式會為一個伺服器應用程式提供服務，以處理來自另一個應用程式的資料。</span><span class="sxs-lookup"><span data-stu-id="a7fce-112">These functions provide services for one server application to work with data from another application.</span></span> <span data-ttu-id="a7fce-113">資料可以轉換成原生格式的伺服器應用程式，方法是從其原始格式讀取資料，但以物件應用程式的原生格式寫入資料。</span><span class="sxs-lookup"><span data-stu-id="a7fce-113">The data can be converted to the native format of the server application by reading the data from its original format but writing it in the native format of the object application.</span></span> <span data-ttu-id="a7fce-114">或者，資料可以維持原始格式，而伺服器應用程式會以其原始格式讀取和寫入資料。</span><span class="sxs-lookup"><span data-stu-id="a7fce-114">Or the data can remain in its original format while the server application both reads and writes the data in its original format.</span></span>

<span data-ttu-id="a7fce-115">如需詳細資訊，請參閱下一節的 [結構化儲存體存取模式](structured-storage-access-modes.md)。</span><span class="sxs-lookup"><span data-stu-id="a7fce-115">For more information, see the following section [Structured Storage Access Modes](structured-storage-access-modes.md).</span></span>

 

 




