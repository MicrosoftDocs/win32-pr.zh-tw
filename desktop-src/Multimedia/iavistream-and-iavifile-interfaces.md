---
title: IAVIStream 和 IAVIFile 介面
description: IAVIStream 和 IAVIFile 介面
ms.assetid: 3ab602da-239f-44ff-b43d-e0c380619d99
keywords:
- IAVIStream 介面
- IAVIFile 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cdd72a034f2c380638979e656c84a173331fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840243"
---
# <a name="iavistream-and-iavifile-interfaces"></a><span data-ttu-id="8009b-105">IAVIStream 和 IAVIFile 介面</span><span class="sxs-lookup"><span data-stu-id="8009b-105">IAVIStream and IAVIFile Interfaces</span></span>

<span data-ttu-id="8009b-106">[**IAVIStream**](/windows/desktop/api/Vfw/nn-vfw-iavistream)和 [**IAVIFile**](/windows/desktop/api/Vfw/nn-vfw-iavifile)介面包含檔案和資料流程處理常式所使用的方法。</span><span class="sxs-lookup"><span data-stu-id="8009b-106">The [**IAVIStream**](/windows/desktop/api/Vfw/nn-vfw-iavistream) and [**IAVIFile**](/windows/desktop/api/Vfw/nn-vfw-iavifile) interfaces contain the methods used by file and stream handlers.</span></span> <span data-ttu-id="8009b-107">**PAVISTREAM** 資料型別是 avi 資料流程物件的指標， (透過 **IAVIStream**) 介面，而 **PAVIFILE** 資料類型則是透過 **IAVIFile** 介面)  (之 avi 檔案物件的指標。</span><span class="sxs-lookup"><span data-stu-id="8009b-107">The **PAVISTREAM** data type is a pointer to an AVI stream object (through the **IAVIStream** interface) and the **PAVIFILE** data type is a pointer to an AVI file object (through the **IAVIFile** interface).</span></span>

<span data-ttu-id="8009b-108">若要在 C 中建立物件指標，請先為夠大的結構配置空間，以包含虛擬函式資料表和其他資料成員的指標。</span><span class="sxs-lookup"><span data-stu-id="8009b-108">To create an object pointer in C, first allocate space for a structure that is large enough to contain the pointer to the virtual function table and the other data members.</span></span> <span data-ttu-id="8009b-109">為您的資料流程類型建立方法的虛擬函式資料表，然後將虛擬函式資料表的指標設定為虛擬函式資料表的位址。</span><span class="sxs-lookup"><span data-stu-id="8009b-109">Create a virtual function table for the methods for your type of stream, then set the pointer to the virtual function table to the address of the virtual function table.</span></span>

 

 




