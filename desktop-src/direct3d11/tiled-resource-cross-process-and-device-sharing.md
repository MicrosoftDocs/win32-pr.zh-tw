---
title: 磚資源跨進程和裝置共用
description: 磚集區可以與其他處理序共用，就像傳統資源一樣。
ms.assetid: CADE009E-A71E-4ACA-A549-EFCE81F8EAD1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f69c88ec7e56a0ad3f67ca7d219352261af9d60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183111"
---
# <a name="tiled-resource-cross-process-and-device-sharing"></a><span data-ttu-id="64e8e-103">磚資源跨進程和裝置共用</span><span class="sxs-lookup"><span data-stu-id="64e8e-103">Tiled resource cross process and device sharing</span></span>

<span data-ttu-id="64e8e-104">磚集區可以與其他處理序共用，就像傳統資源一樣。</span><span class="sxs-lookup"><span data-stu-id="64e8e-104">Tile pools can be shared with other processes just like traditional resources.</span></span> <span data-ttu-id="64e8e-105">參考磚集區的並排資源無法跨裝置和進程共用。</span><span class="sxs-lookup"><span data-stu-id="64e8e-105">Tiled resources that reference tile pools can't be shared across devices and processes.</span></span> <span data-ttu-id="64e8e-106">但是，個別的進程可以建立自己的磚資源，對應至這些已並排資源之間共用的磚集區。</span><span class="sxs-lookup"><span data-stu-id="64e8e-106">But separate processes can create their own tiled resources that map to tile pools that are shared between those tiled resources.</span></span>

<span data-ttu-id="64e8e-107">共用的磚集區無法調整大小。</span><span class="sxs-lookup"><span data-stu-id="64e8e-107">Shared tile pools can't be resized.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="64e8e-108">本節內容</span><span class="sxs-lookup"><span data-stu-id="64e8e-108">In this section</span></span>



| <span data-ttu-id="64e8e-109">主題</span><span class="sxs-lookup"><span data-stu-id="64e8e-109">Topic</span></span>                                                                                                                   | <span data-ttu-id="64e8e-110">描述</span><span class="sxs-lookup"><span data-stu-id="64e8e-110">Description</span></span>                                                                     |
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="64e8e-111">磚的資源不支援樣板格式</span><span class="sxs-lookup"><span data-stu-id="64e8e-111">Stencil formats not supported with tiled resources</span></span>](stencil-formats-not-supported-with-tiled-resources.md)<br/> | <span data-ttu-id="64e8e-112">磚的資源不支援包含樣板的格式。</span><span class="sxs-lookup"><span data-stu-id="64e8e-112">Formats that contain stencil aren't supported with tiled resources.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="64e8e-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="64e8e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64e8e-114">建立磚資源</span><span class="sxs-lookup"><span data-stu-id="64e8e-114">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 





