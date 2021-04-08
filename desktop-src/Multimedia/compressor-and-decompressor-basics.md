---
title: 壓縮和解壓縮的基本概念
description: 壓縮和解壓縮的基本概念
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，開啟壓縮機
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，開啟壓縮機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b51e0221c495d5e2d0782f4e56e0778c0d2462
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839936"
---
# <a name="compressor-and-decompressor-basics"></a><span data-ttu-id="161d0-105">壓縮和解壓縮的基本概念</span><span class="sxs-lookup"><span data-stu-id="161d0-105">Compressor and Decompressor Basics</span></span>

<span data-ttu-id="161d0-106">若要開啟並尋找壓縮的功能，您可以使用 [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) 和 [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) 函式。</span><span class="sxs-lookup"><span data-stu-id="161d0-106">To open and locate a compressor, you can use the [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) and [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) functions.</span></span> <span data-ttu-id="161d0-107">您可以使用 **ICLocate** 來尋找特定類型的壓縮程式，並取得它的控制碼，以便在其他 bc-vcm-lvm-hyperv 函式中使用。</span><span class="sxs-lookup"><span data-stu-id="161d0-107">You can use **ICLocate** to find a compressor of a specific type and to obtain a handle of it for use in other VCM functions.</span></span> <span data-ttu-id="161d0-108">若要開啟壓縮壓縮，您可以使用 **ICOpen**。</span><span class="sxs-lookup"><span data-stu-id="161d0-108">To open a compressor, you can use **ICOpen**.</span></span> <span data-ttu-id="161d0-109">當應用程式使用其他 BC-VCM-LVM-HYPERV 函式時，您的應用程式會使用這個函數所傳回的控制碼來識別開啟的壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="161d0-109">Your application uses the handle returned by this function to identify the opened compressor when it uses other VCM functions.</span></span>

<span data-ttu-id="161d0-110">若要開啟並尋找解壓縮程式，應用程式可以使用 [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) 和 [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) 宏。</span><span class="sxs-lookup"><span data-stu-id="161d0-110">To open and locate a decompressor, applications can use the [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) and [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) macros.</span></span> <span data-ttu-id="161d0-111">這些宏會使用 **ICLocate** 來進行操作。</span><span class="sxs-lookup"><span data-stu-id="161d0-111">These macros use **ICLocate** for operation.</span></span>

<span data-ttu-id="161d0-112">當您的應用程式已完成使用壓縮程式或解壓縮程式時，必須將其關閉，以釋放用於壓縮或解壓縮的任何資源。</span><span class="sxs-lookup"><span data-stu-id="161d0-112">When your application has finished using a compressor or decompressor, it must close it to free any resources used for compression or decompression.</span></span> <span data-ttu-id="161d0-113">您的應用程式可以使用 [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) 函數來關閉壓縮程式或解壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="161d0-113">Your application can use the [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) function to close the compressor or decompressor.</span></span>

<span data-ttu-id="161d0-114">此外，您的應用程式也可以使用 [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) 函數來列舉系統上的壓縮機或 decompressors。</span><span class="sxs-lookup"><span data-stu-id="161d0-114">Also, your application can enumerate the compressors or decompressors on a system by using the [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) function.</span></span>

> [!Note]  
> <span data-ttu-id="161d0-115">AVI 檔案中的資料流程標頭包含資料流程類型的相關資訊，以及該資料流程的特定處理常式。</span><span class="sxs-lookup"><span data-stu-id="161d0-115">The stream header in an AVI file contains information about the stream type and the specific handler for that stream.</span></span> <span data-ttu-id="161d0-116">在資料流程標頭中， **fccType** 和 **fccHandler** 成員會識別資料流程類型以及為數據流指定的資料流程處理常式。</span><span class="sxs-lookup"><span data-stu-id="161d0-116">Within the stream header, the **fccType** and **fccHandler** members identify the stream type and the stream handler specified for the stream.</span></span>

 

 

 




