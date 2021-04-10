---
title: WMPCD 通訊協定
description: WMPCD 通訊協定
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Windows Media Player，通訊協定
- Windows Media Player 物件模型，通訊協定
- 物件模型，通訊協定
- Windows Media Player ActiveX 控制項，物件模型的通訊協定
- ActiveX 控制項，物件模型的通訊協定
- Windows Media Player 的行動 ActiveX 控制項、物件模型的通訊協定
- Windows Media Player 行動裝置、物件模型的通訊協定
- 通訊協定，Windows Media Player 物件模型
- 通訊協定，WMPCD
- WMPCD 通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78c591d0ba9605f1f63e3e152b974d112548d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183454"
---
# <a name="wmpcd-protocol"></a><span data-ttu-id="76b8e-113">WMPCD 通訊協定</span><span class="sxs-lookup"><span data-stu-id="76b8e-113">WMPCD Protocol</span></span>

<span data-ttu-id="76b8e-114">WMPCD 通訊協定可讓您使用 URL 語法來指定光碟片上的軌跡。</span><span class="sxs-lookup"><span data-stu-id="76b8e-114">The WMPCD protocol enables you to specify tracks on a compact disc using URL syntax.</span></span> <span data-ttu-id="76b8e-115">這是通訊協定的一般語法：</span><span class="sxs-lookup"><span data-stu-id="76b8e-115">This is the general syntax of the protocol:</span></span>


```C++
wmpcd://drive/track
```



<span data-ttu-id="76b8e-116">*磁片磁碟機* 區段是 CD 光碟機的索引。</span><span class="sxs-lookup"><span data-stu-id="76b8e-116">The *drive* segment is the index of the CD drive.</span></span> <span data-ttu-id="76b8e-117">*曲目* 區段是曲目的編號。下列範例將示範如何使用 WMPCD 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="76b8e-117">The *track* segment is the number of the track. The following example demonstrates using the WMPCD protocol.</span></span>


```C++
player.url = "wmpcd://0/4";
```



<span data-ttu-id="76b8e-118">此範例會在第一個 CD 光碟機的光碟上播放第四個曲目， (其索引為 0) 的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="76b8e-118">The example plays the fourth track on the disc in the first CD drive (the drive whose index is 0).</span></span>

## <a name="related-topics"></a><span data-ttu-id="76b8e-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="76b8e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76b8e-120">**支援的通訊協定和檔案類型**</span><span class="sxs-lookup"><span data-stu-id="76b8e-120">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




