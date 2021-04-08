---
title: 建立檔案或資料流程處理常式
description: 建立檔案或資料流程處理常式
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b2f118f4f5279cea1aacedd58b86f23afa9a9af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021313"
---
# <a name="creating-a-file-or-stream-handler"></a><span data-ttu-id="f73c9-103">建立檔案或資料流程處理常式</span><span class="sxs-lookup"><span data-stu-id="f73c9-103">Creating a File or Stream Handler</span></span>

<span data-ttu-id="f73c9-104">在以 C 程式設計語言撰寫的應用程式中，檔案或資料流程處理常式通常會建立每個方法的函式。</span><span class="sxs-lookup"><span data-stu-id="f73c9-104">In an application written in the C programming language, a file or stream handler usually creates a function for each method.</span></span> <span data-ttu-id="f73c9-105">您的應用程式會透過資料流程處理常式所建立的函式指標陣列來存取這些函式。</span><span class="sxs-lookup"><span data-stu-id="f73c9-105">Your application accesses these functions through an array of function pointers the stream handler creates.</span></span> <span data-ttu-id="f73c9-106">**IAVIStreamVtbl** 結構包含函式指標的陣列。</span><span class="sxs-lookup"><span data-stu-id="f73c9-106">An **IAVIStreamVtbl** structure contains the array of function pointers.</span></span> <span data-ttu-id="f73c9-107">資料流程處理常式可以指派它想要為方法建立之函式的任何名稱。</span><span class="sxs-lookup"><span data-stu-id="f73c9-107">A stream handler can assign any name it wants to functions it creates for the methods.</span></span> <span data-ttu-id="f73c9-108">結構中的函式指標位置表示函式與方法之間的對應。</span><span class="sxs-lookup"><span data-stu-id="f73c9-108">The position of the function pointer in the structure implies the correspondence of the function to the method.</span></span> <span data-ttu-id="f73c9-109">例如，結構中的第一個函式指標會與 **QueryInterface** 方法相對應。</span><span class="sxs-lookup"><span data-stu-id="f73c9-109">For example, the first function pointer in the structure corresponds to the **QueryInterface** method.</span></span> <span data-ttu-id="f73c9-110">您的資料流程處理常式必須提供介面的所有功能。</span><span class="sxs-lookup"><span data-stu-id="f73c9-110">Your stream handler must provide all the functions of an interface.</span></span>

 

 




