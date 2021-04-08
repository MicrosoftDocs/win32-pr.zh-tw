---
title: 開啟和關閉資料流程
description: 開啟和關閉資料流程
ms.assetid: 7dcaccbe-63d8-410a-ae00-16ce9e252ad0
keywords:
- AVIFileGetStream 函式
- AVIStreamRelease 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4462e261f1480129c073b70ddc61f91a422c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021164"
---
# <a name="opening-and-closing-streams"></a><span data-ttu-id="50ab1-105">開啟和關閉資料流程</span><span class="sxs-lookup"><span data-stu-id="50ab1-105">Opening and Closing Streams</span></span>

<span data-ttu-id="50ab1-106">開啟資料流程與開啟檔案類似。</span><span class="sxs-lookup"><span data-stu-id="50ab1-106">Opening data streams is similar to opening files.</span></span> <span data-ttu-id="50ab1-107">您可以使用 [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) 函數來開啟資料流程。</span><span class="sxs-lookup"><span data-stu-id="50ab1-107">You can open a stream by using the [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) function.</span></span> <span data-ttu-id="50ab1-108">此函式會建立資料流程介面、將資料流程的控制碼放在介面中，並將指標傳回至介面。</span><span class="sxs-lookup"><span data-stu-id="50ab1-108">This function creates a stream interface, places a handle of the stream in the interface, and returns a pointer to the interface.</span></span> <span data-ttu-id="50ab1-109">**AVIFileGetStream** 也會維護已開啟資料流程的應用程式參考計數，而不是已關閉它的應用程式的參考計數。</span><span class="sxs-lookup"><span data-stu-id="50ab1-109">**AVIFileGetStream** also maintains a reference count of the applications that have opened a stream, but not of those that have closed it.</span></span>

<span data-ttu-id="50ab1-110">如果您想要存取檔案中的單一資料流程，您可以使用 [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) 函數來開啟檔案和資料流程。</span><span class="sxs-lookup"><span data-stu-id="50ab1-110">If you want to access a single stream in a file, you can open the file and the stream by using the [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) function.</span></span> <span data-ttu-id="50ab1-111">此函數結合了 [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) 和 **AVIFileGetStream** 函數的作業和函式引數。</span><span class="sxs-lookup"><span data-stu-id="50ab1-111">This function combines the operations and function arguments of the [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) and **AVIFileGetStream** functions.</span></span>

<span data-ttu-id="50ab1-112">若要在檔案中存取一個以上的資料流程，請使用 **AVIFileOpen** 一次，然後再呼叫 **AVIFileGetStream** 的多個。</span><span class="sxs-lookup"><span data-stu-id="50ab1-112">To access more than one stream in a file, use **AVIFileOpen** once followed by multiple calls to **AVIFileGetStream**.</span></span>

<span data-ttu-id="50ab1-113">您可以使用 [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) 函式來遞增資料流程的參考計數，以在使用通常會關閉資料流程的函式時，讓資料流程保持開啟。</span><span class="sxs-lookup"><span data-stu-id="50ab1-113">You can increment the reference count of a stream by using the [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) function to keep a stream open when using a function that would normally close the stream.</span></span>

<span data-ttu-id="50ab1-114">您可以使用 [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) 函數來關閉資料流程。</span><span class="sxs-lookup"><span data-stu-id="50ab1-114">You can close a stream by using the [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) function.</span></span> <span data-ttu-id="50ab1-115">此函式會遞減資料流程的參考計數，並在參考計數到達零時將其關閉。</span><span class="sxs-lookup"><span data-stu-id="50ab1-115">This function decrements the reference count of the stream and closes it when the reference count reaches zero.</span></span> <span data-ttu-id="50ab1-116">您的應用程式應在每次使用 [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream)、 [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream)、 **AVIStreamAddRef** 或 **AVIStreamOpenFromFile** 函數時包含呼叫 **AVIStreamRelease** ，以平衡參考計數。</span><span class="sxs-lookup"><span data-stu-id="50ab1-116">Your applications should balance the reference count by including a call to **AVIStreamRelease** for each use of the [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef**, or **AVIStreamOpenFromFile** function.</span></span> <span data-ttu-id="50ab1-117">當您釋放使用 **AVIStreamOpenFromFile** 開啟的資料流程時，AVIFile 會關閉包含該資料流程的檔案。</span><span class="sxs-lookup"><span data-stu-id="50ab1-117">When you release a stream that has been opened by using **AVIStreamOpenFromFile**, AVIFile closes the file containing the stream.</span></span> <span data-ttu-id="50ab1-118">如果您的應用程式釋出具有開啟資料流程的檔案，則 AVIFile 會等到所有資料流程都釋出之後，才會關閉資料流程。</span><span class="sxs-lookup"><span data-stu-id="50ab1-118">If your application releases a file that has open data streams, AVIFile will not close the streams until all of the streams are released.</span></span>

 

 




