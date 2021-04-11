---
title: 關於 AVIFile 函式和宏
description: 關於 AVIFile 函式和宏
ms.assetid: 877f6759-8271-47eb-8a7f-540393e5ae89
keywords:
- AVIFileInit 函式
- AVIFileExit 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f66bbac900b69841fd7cba814aad339731b75727
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022060"
---
# <a name="about-avifile-functions-and-macros"></a><span data-ttu-id="da48b-105">關於 AVIFile 函式和宏</span><span class="sxs-lookup"><span data-stu-id="da48b-105">About AVIFile Functions and Macros</span></span>

<span data-ttu-id="da48b-106">AVIFile 函式和宏會將以時間為基礎的檔案中的資訊當作一或多個 *資料流程* 來處理，而不是以標記的資料區塊（稱為區塊）來處理。</span><span class="sxs-lookup"><span data-stu-id="da48b-106">The AVIFile functions and macros handle the information in time-based files as one or more *data streams* instead of tagged blocks of data called chunks.</span></span> <span data-ttu-id="da48b-107">資料流程指的是以時間為基礎之檔案的元件。</span><span class="sxs-lookup"><span data-stu-id="da48b-107">Data streams refer to the components of a time-based file.</span></span> <span data-ttu-id="da48b-108">AVI 檔案可以包含數種不同類型的資料，例如影片順序、英文的聲帶和法文的聲帶。</span><span class="sxs-lookup"><span data-stu-id="da48b-108">An AVI file can contain several different types of data, such as a video sequence, an English soundtrack, and a French soundtrack.</span></span> <span data-ttu-id="da48b-109">使用 AVIFile，應用程式可以個別存取每個元件。</span><span class="sxs-lookup"><span data-stu-id="da48b-109">Using AVIFile, an application can access each of these components separately.</span></span>

> [!Note]  
> <span data-ttu-id="da48b-110">雖然 AVIFile 函式和宏適用于任何 RIFF 檔案，但此總覽只會示範其僅搭配 AVI 檔案使用的功能。</span><span class="sxs-lookup"><span data-stu-id="da48b-110">Although the AVIFile functions and macros work with any RIFF file, this overview demonstrates their use with AVI files only.</span></span> <span data-ttu-id="da48b-111">AVI 檔案通常是搭配 AVIFile 宏和函式使用的以時間為基礎的檔案。</span><span class="sxs-lookup"><span data-stu-id="da48b-111">AVI files are typically the time-based files used with the AVIFile macros and functions.</span></span>

 

<span data-ttu-id="da48b-112">AVIFile 函式和宏都包含在動態連結程式庫中。</span><span class="sxs-lookup"><span data-stu-id="da48b-112">AVIFile functions and macros are contained in a dynamic-link library.</span></span> <span data-ttu-id="da48b-113">若要初始化程式庫，請使用 [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) 函數。</span><span class="sxs-lookup"><span data-stu-id="da48b-113">To initialize the library, use the [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) function.</span></span> <span data-ttu-id="da48b-114">初始化程式庫之後，您可以使用任何 AVIFile 函數或宏。</span><span class="sxs-lookup"><span data-stu-id="da48b-114">After you initialize the library, you can use any of the AVIFile functions or macros.</span></span> <span data-ttu-id="da48b-115">若要釋放程式庫，請使用 [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) 函數。</span><span class="sxs-lookup"><span data-stu-id="da48b-115">To release the library, use the [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) function.</span></span> <span data-ttu-id="da48b-116">AVIFile 會維護使用程式庫之應用程式的參考計數，但不會維護已發行的應用程式的參考計數。</span><span class="sxs-lookup"><span data-stu-id="da48b-116">AVIFile maintains a reference count of the applications that are using the library, but not those that have released it.</span></span> <span data-ttu-id="da48b-117">您的應用程式應該使用 **AVIFileExit** 的呼叫來平衡 **AVIFileInit** 的每個使用，以在每個應用程式完成使用後完全釋放程式庫。</span><span class="sxs-lookup"><span data-stu-id="da48b-117">Your applications should balance each use of **AVIFileInit** with a call to **AVIFileExit** to completely release the library after each application finishes using it.</span></span>

 

 




