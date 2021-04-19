---
title: IBackgroundCopyCallback3 方法
description: IBackgroundCopyCallback3 介面會公開下列方法。
ms.assetid: FF0BA13F-63DA-46A4-ACC6-DE72AC20EAA2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f13aa1c97006084007e747f2766868c25e5b998
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "107001063"
---
# <a name="ibackgroundcopycallback3-methods"></a><span data-ttu-id="da2dc-103">IBackgroundCopyCallback3 方法</span><span class="sxs-lookup"><span data-stu-id="da2dc-103">IBackgroundCopyCallback3 Methods</span></span>

<span data-ttu-id="da2dc-104">[**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3)介面會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="da2dc-104">The [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="da2dc-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="da2dc-105">In this section</span></span>



| <span data-ttu-id="da2dc-106">主題</span><span class="sxs-lookup"><span data-stu-id="da2dc-106">Topic</span></span>                                                                                             | <span data-ttu-id="da2dc-107">描述</span><span class="sxs-lookup"><span data-stu-id="da2dc-107">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da2dc-108">**FileRangesTransferred 方法**</span><span class="sxs-lookup"><span data-stu-id="da2dc-108">**FileRangesTransferred method**</span></span>](/windows/desktop/api/Bits10_1/nf-bits10_1-ibackgroundcopycallback3-filerangestransferred)<br/> | <span data-ttu-id="da2dc-109">當您下載一或多個檔案範圍時，BITS 會呼叫 [**FileRangesTransferred**](/windows/desktop/api/Bits10_1/nf-bits10_1-ibackgroundcopycallback3-filerangestransferred) 方法的執行。</span><span class="sxs-lookup"><span data-stu-id="da2dc-109">BITS calls your implementation of the [**FileRangesTransferred**](/windows/desktop/api/Bits10_1/nf-bits10_1-ibackgroundcopycallback3-filerangestransferred) method when one or more file ranges have been downloaded.</span></span> <span data-ttu-id="da2dc-110">使用 [**IBackgroundCopyFile6：： RequestFileRanges**](/windows/desktop/api/Bits10_1/nf-bits10_1-ibackgroundcopyfile6-requestfileranges) 方法，將檔案範圍新增至作業。</span><span class="sxs-lookup"><span data-stu-id="da2dc-110">File ranges are added to the job using the [**IBackgroundCopyFile6::RequestFileRanges**](/windows/desktop/api/Bits10_1/nf-bits10_1-ibackgroundcopyfile6-requestfileranges) method.</span></span><br/> |



 

 

 





