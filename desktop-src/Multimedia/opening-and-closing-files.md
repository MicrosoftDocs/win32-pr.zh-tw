---
title: 開啟和關閉檔案
description: 開啟和關閉檔案
ms.assetid: 72655d33-f685-4205-a982-f7cd20c59f22
keywords:
- AVIFileOpen 函式
- AVIFileRelease 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e1c51c4747e03bf4f18a8e6c560e45798e1c8c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106992659"
---
# <a name="opening-and-closing-files"></a><span data-ttu-id="a0ab0-105">開啟和關閉檔案</span><span class="sxs-lookup"><span data-stu-id="a0ab0-105">Opening and Closing Files</span></span>

<span data-ttu-id="a0ab0-106">應用程式必須在讀取或寫入之前開啟 AVI 檔案。</span><span class="sxs-lookup"><span data-stu-id="a0ab0-106">An application must open an AVI file before reading or writing.</span></span> <span data-ttu-id="a0ab0-107">若要開啟 AVI 檔案，請使用 [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) 函數。</span><span class="sxs-lookup"><span data-stu-id="a0ab0-107">To open an AVI file, use the [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) function.</span></span> <span data-ttu-id="a0ab0-108">**AVIFileOpen** 會傳回 AVI 檔案介面的位址，其中包含開啟檔案的控制碼，並遞增檔案的參考計數。</span><span class="sxs-lookup"><span data-stu-id="a0ab0-108">**AVIFileOpen** returns the address of an AVI file interface that contains the handle of the open file and increments the reference count of the file.</span></span>

<span data-ttu-id="a0ab0-109">**AVIFileOpen** 函式支援搭配 [OPENFILE](/documentation/)函數使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="a0ab0-109">The **AVIFileOpen** function supports the OF flags used with the [OpenFile](/documentation/) function.</span></span> <span data-ttu-id="a0ab0-110">如果應用程式寫入至現有的檔案，則必須 \_ 在 **AVIFileOpen** 中包含寫入旗標的。</span><span class="sxs-lookup"><span data-stu-id="a0ab0-110">If an application writes to an existing file, it must include the OF\_WRITE flag in **AVIFileOpen**.</span></span> <span data-ttu-id="a0ab0-111">同樣地，如果您的應用程式會建立並寫入至新的檔案，您就必須 \_ \_ 在 **AVIFileOpen** 中包含 CREATE 和 WRITE 旗標的。</span><span class="sxs-lookup"><span data-stu-id="a0ab0-111">Similarly, if your application creates and writes to a new file, you must include the OF\_CREATE and OF\_WRITE flags in **AVIFileOpen**.</span></span>

<span data-ttu-id="a0ab0-112">當您使用 **AVIFileOpen** 開啟檔案時，可以使用預設的檔案處理常式，也可以指定自訂的檔案處理常式，以讀取和寫入檔案和其資料流程。</span><span class="sxs-lookup"><span data-stu-id="a0ab0-112">When you open a file using **AVIFileOpen**, you can use a default file handler or you can specify a custom file handler to read and write to the file and its data streams.</span></span> <span data-ttu-id="a0ab0-113">在任何一種情況下，AVIFile 都會搜尋登錄，以取得正確的檔案處理常式來使用。</span><span class="sxs-lookup"><span data-stu-id="a0ab0-113">In either case, AVIFile searches the registry for the correct file handler to use.</span></span> <span data-ttu-id="a0ab0-114">您必須確保自訂檔案處理常式位於登錄中，應用程式才能存取它們。</span><span class="sxs-lookup"><span data-stu-id="a0ab0-114">You must ensure custom file handlers are in the registry before an application can access them.</span></span>

<span data-ttu-id="a0ab0-115">您可以使用 [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) 函數來遞增檔案的參考計數。</span><span class="sxs-lookup"><span data-stu-id="a0ab0-115">You can increment the reference count of a file by using the [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) function.</span></span> <span data-ttu-id="a0ab0-116">例如，您可能會想要在將檔案介面的控制碼傳遞給另一個應用程式時，或當您使用通常會關閉檔案的函式時，將檔案保持開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="a0ab0-116">For example, you might want to do this when passing a handle of the file interface to another application, or when you want to keep a file open while using a function that would normally close the file.</span></span>

<span data-ttu-id="a0ab0-117">您可以使用 [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) 函數來關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="a0ab0-117">You can close a file by using the [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) function.</span></span> <span data-ttu-id="a0ab0-118">**AVIFileRelease** 函式會遞減 AVI 檔案的參考計數、儲存對檔案所做的變更，以及當參考計數到達零時，關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="a0ab0-118">The **AVIFileRelease** function decrements the reference count of an AVI file, saves changes made to the file, and when the reference count reaches zero, closes the file.</span></span> <span data-ttu-id="a0ab0-119">您的應用程式應在每次使用 [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen)和 **AVIFileAddRef** 的情況中包含呼叫 **AVIFileRelease** ，以平衡參考計數。</span><span class="sxs-lookup"><span data-stu-id="a0ab0-119">Your applications should balance the reference count by including a call to **AVIFileRelease** for each use of [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) and **AVIFileAddRef**.</span></span>

> [!Note]  
> <span data-ttu-id="a0ab0-120">應用程式可以使用一或多個程式執行緒來開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="a0ab0-120">An application can open a file with one or more program threads.</span></span> <span data-ttu-id="a0ab0-121">不過，為了獲得最佳效能，每次只能有一個執行緒存取檔案。</span><span class="sxs-lookup"><span data-stu-id="a0ab0-121">However, for the best possible performance, only one thread should access the file at any one time.</span></span>

 

 

 