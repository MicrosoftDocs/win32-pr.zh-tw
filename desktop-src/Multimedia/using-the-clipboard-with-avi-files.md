---
title: 使用具有 AVI 檔案的剪貼簿
description: 使用具有 AVI 檔案的剪貼簿
ms.assetid: 76ef7cc9-9afd-462a-b9fe-2b62f8113a9a
keywords:
- AVIPutFileOnClipboard 函式
- AVIGetFromClipboard 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe46f463f22aa2d015d4ffd8496eb95c37053a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673280"
---
# <a name="using-the-clipboard-with-avi-files"></a><span data-ttu-id="900dc-105">使用具有 AVI 檔案的剪貼簿</span><span class="sxs-lookup"><span data-stu-id="900dc-105">Using the Clipboard with AVI Files</span></span>

<span data-ttu-id="900dc-106">剪貼簿可提供方便的暫存儲存體，讓應用程式用來複製或傳輸 AVI 檔案。</span><span class="sxs-lookup"><span data-stu-id="900dc-106">The clipboard provides convenient, temporary storage that an application can use to copy or transfer AVI files.</span></span> <span data-ttu-id="900dc-107">AVIFile 包含可用於磁片或記憶體檔案的剪貼簿函數。</span><span class="sxs-lookup"><span data-stu-id="900dc-107">AVIFile includes clipboard functions that you can use with disk or memory files.</span></span>

<span data-ttu-id="900dc-108">您可以使用 [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) 函式，將檔案複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="900dc-108">You can copy a file to the clipboard by using the [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) function.</span></span> <span data-ttu-id="900dc-109">若要將剪貼簿上的檔案寫入記憶體或磁片，請使用 [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) 函數。</span><span class="sxs-lookup"><span data-stu-id="900dc-109">To write a file that is on the clipboard to memory or disk, use the [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) function.</span></span>

<span data-ttu-id="900dc-110">您可以使用 [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) 函式清除剪貼簿中的檔案。</span><span class="sxs-lookup"><span data-stu-id="900dc-110">You can clear a file from the clipboard by using the [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) function.</span></span> <span data-ttu-id="900dc-111">此函式不會清除剪貼簿中其他類型的資訊，例如文字。</span><span class="sxs-lookup"><span data-stu-id="900dc-111">This function does not clear other types of information, such as text, from the clipboard.</span></span> <span data-ttu-id="900dc-112">如果您在應用程式中使用剪貼簿功能，請在關閉應用程式或關閉剪貼簿上的檔案之前，使用 **AVIClearClipboard** 清除剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="900dc-112">If you use clipboard functions in your application, clear the clipboard with **AVIClearClipboard** before closing the application or closing the file on the clipboard.</span></span> <span data-ttu-id="900dc-113">無論是否已使用 **AVIPutFileOnClipboard** ，您都可以在應用程式中呼叫 **AVIClearClipboard** 。</span><span class="sxs-lookup"><span data-stu-id="900dc-113">You can call **AVIClearClipboard** in your application whether or not **AVIPutFileOnClipboard** has been used.</span></span>

> [!Note]  
> <span data-ttu-id="900dc-114">如果您的應用程式將檔案複製到剪貼簿，而檔案中包含可能變更的資料流程資料，您可以使用 [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) 函式來建立複製資料流程的記憶體檔。</span><span class="sxs-lookup"><span data-stu-id="900dc-114">If your application copies a file to the clipboard and the file contains stream data that might change, you can create a memory file of cloned streams by using the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function.</span></span> <span data-ttu-id="900dc-115">然後，您可以將檔案放在剪貼簿上，然後釋出原始檔案而不使它失效。</span><span class="sxs-lookup"><span data-stu-id="900dc-115">You can then place the file on the clipboard and then release the original file without invalidating it.</span></span>

 

 

 




