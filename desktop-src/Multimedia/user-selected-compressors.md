---
title: User-Selected 壓縮機
description: User-Selected 壓縮機
ms.assetid: 38569f9c-2df3-4959-990b-5c33203ff916
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，使用者選取的壓縮機
- BC-VCM-LVM-HYPERV (video 壓縮管理員) ，使用者選取的壓縮機
- ICCompressorChoose 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbba48b919265ea6e0bab2c3d891f628c4e660a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932377"
---
# <a name="user-selected-compressors"></a><span data-ttu-id="430be-106">User-Selected 壓縮機</span><span class="sxs-lookup"><span data-stu-id="430be-106">User-Selected Compressors</span></span>

<span data-ttu-id="430be-107">壓縮資料時，您的應用程式可以使用 [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) 函式來建立對話方塊，讓使用者可以在其中選取壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="430be-107">When compressing data, your application can use the [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) function to create a dialog box in which the user can select the compressor.</span></span> <span data-ttu-id="430be-108">您可以指定此函式的旗標，讓使用者指定主要畫面格頻率和電影資料速率，或顯示預覽視窗。</span><span class="sxs-lookup"><span data-stu-id="430be-108">You can specify flags for this function to allow the user to specify the key-frame frequency and the movie-data rate, or to display a preview window.</span></span>

<span data-ttu-id="430be-109">系統會自動開啟使用者所選取的壓縮程式，並在 **ICCompressorChoose** 中指定之 [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars)結構的 .hic .hid 成員傳回其控制碼。</span><span class="sxs-lookup"><span data-stu-id="430be-109">The compressor selected by the user is automatically opened and its handle is returned in the hic member of the [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) structure specified in **ICCompressorChoose**.</span></span>

<span data-ttu-id="430be-110">如果您使用 **ICCompressorChoose**，請使用 [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) 函式來關閉壓縮功能，並釋放與 **COMPVARS** 結構相關聯的任何資源。</span><span class="sxs-lookup"><span data-stu-id="430be-110">If you use **ICCompressorChoose**, use the [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) function to close the compressor and free any resources associated with the **COMPVARS** structure.</span></span>

 

 




