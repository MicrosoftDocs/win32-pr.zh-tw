---
title: 關於 IMFGetService
description: 關於 IMFGetService
ms.assetid: c71b1362-a596-42e5-b894-f8a3c0e70140
keywords:
- Windows Media Player 外掛程式，介面
- 外掛程式，介面
- 數位信號處理外掛程式，介面
- DSP 外掛程式，介面
- 介面、DSP 外掛程式
- Windows Media Player 外掛程式、IMFGetService 介面
- 外掛程式，IMFGetService 介面
- 數位信號處理外掛程式，IMFGetService 介面
- DSP 外掛程式，IMFGetService 介面
- IMFGetService 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235b616afe48db9ae772da1f1d74c4f7de1a74a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300212"
---
# <a name="about-imfgetservice"></a><span data-ttu-id="d9729-113">關於 IMFGetService</span><span class="sxs-lookup"><span data-stu-id="d9729-113">About IMFGetService</span></span>

<span data-ttu-id="d9729-114">**IMFGetService** 介面是必須由雙重模式的 DSP 外掛程式所執行的其中一個介面。</span><span class="sxs-lookup"><span data-stu-id="d9729-114">The **IMFGetService** interface is one of the interfaces that must be implemented by a dual-mode DSP plug-in.</span></span> <span data-ttu-id="d9729-115">它只有一個方法 **GetService**。</span><span class="sxs-lookup"><span data-stu-id="d9729-115">It has only one method, **GetService**.</span></span> <span data-ttu-id="d9729-116">DSP 外掛程式會執行 **GetService** 方法，讓用戶端可以在外掛程式于媒體基礎管線中以原生方式執行時，取得外掛程式所支援的介面指標。</span><span class="sxs-lookup"><span data-stu-id="d9729-116">A DSP plug-in implements the **GetService** method so that clients can obtain pointers to the interfaces supported by the plug-in when the plug-in is running natively in the Media Foundation pipeline.</span></span>

 

 




