---
title: 清除可讀寫 CD
description: 清除可讀寫 CD
ms.assetid: 272fdd2b-c174-4bde-b05e-839d547532a6
keywords:
- Windows Media Player、CD 燒錄
- Windows Media Player 物件模型，CD 燒錄
- 物件模型，CD 燒錄
- Windows Media Player ActiveX 控制項、CD 燒錄
- ActiveX 控制項，CD 燒錄
- Windows Media Player 的行動 ActiveX 控制項、CD 燒錄
- Windows Media Player Mobile、CD 燒錄
- CD 燒錄，抹除可讀寫 Cd
- 燒錄 Cd，抹除可讀寫 Cd
- 清除可讀寫 Cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7025b7cd70c86c0b832aa792e50a8a2c64e7f45
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023042"
---
# <a name="erasing-a-rewritable-cd"></a><span data-ttu-id="164cf-113">清除可讀寫 CD</span><span class="sxs-lookup"><span data-stu-id="164cf-113">Erasing a Rewritable CD</span></span>

<span data-ttu-id="164cf-114">[IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)介面提供清除 cd-rw 光碟的方法。</span><span class="sxs-lookup"><span data-stu-id="164cf-114">The [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface provides a method for erasing CD-RW discs.</span></span> <span data-ttu-id="164cf-115">清除 CD 之前，您必須先確定已支援此作業。</span><span class="sxs-lookup"><span data-stu-id="164cf-115">Before erasing a CD, you must first ensure that the operation is supported.</span></span> <span data-ttu-id="164cf-116">如需詳細資訊，請參閱 [取出磁片磁碟機和光碟狀態](retrieving-the-drive-and-disc-status.md)。</span><span class="sxs-lookup"><span data-stu-id="164cf-116">For more information, see [Retrieving the Drive and Disc Status](retrieving-the-drive-and-disc-status.md).</span></span>

<span data-ttu-id="164cf-117">若要開始清除可讀寫 CD 的內容，請呼叫 [IWMPCdromBurn：： erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase)。</span><span class="sxs-lookup"><span data-stu-id="164cf-117">To begin erasing the contents of a rewritable CD, call [IWMPCdromBurn::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span></span>


```C++

    HRESULT hr = m_spCdromBurn->erase();
    

```



## <a name="related-topics"></a><span data-ttu-id="164cf-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="164cf-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="164cf-119">**燒錄 CD**</span><span class="sxs-lookup"><span data-stu-id="164cf-119">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="164cf-120">**擷取 CD 燒錄介面**</span><span class="sxs-lookup"><span data-stu-id="164cf-120">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="164cf-121">**啟動燒錄流程**</span><span class="sxs-lookup"><span data-stu-id="164cf-121">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="164cf-122">**正在抓取磁片磁碟機和光碟狀態**</span><span class="sxs-lookup"><span data-stu-id="164cf-122">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="164cf-123">**正在取出燒錄狀態**</span><span class="sxs-lookup"><span data-stu-id="164cf-123">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




