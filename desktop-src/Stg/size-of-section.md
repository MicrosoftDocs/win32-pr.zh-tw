---
title: 區段的大小
description: 區段大小資料類型表示區段的大小（以位元組為單位）。
ms.assetid: 6438fbce-42b9-4b16-a6b0-80c80246e546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b19df1c2f9a65f6952855a4ab325565c759af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184074"
---
# <a name="size-of-section"></a><span data-ttu-id="487eb-103">區段的大小</span><span class="sxs-lookup"><span data-stu-id="487eb-103">Size of Section</span></span>

<span data-ttu-id="487eb-104">區段大小資料類型表示區段的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="487eb-104">The section size data type indicates the size, in bytes, of the section.</span></span> <span data-ttu-id="487eb-105">由於區段大小是前4個位元組，因此可以將區段複製為位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="487eb-105">Because the section size is the first 4 bytes, sections can be copied as an array of bytes.</span></span> <span data-ttu-id="487eb-106">區段大小應一律為四的倍數。</span><span class="sxs-lookup"><span data-stu-id="487eb-106">The section size should always be a multiple of four.</span></span>

<span data-ttu-id="487eb-107">例如，空的區段，也就是其中有零屬性的區段，會有八個 (**DWORD** 位元組計數的位元組計數，以及) 屬性的 **dword** 計數。</span><span class="sxs-lookup"><span data-stu-id="487eb-107">For example, an empty section, that is, one with zero properties in it, would have a byte count of eight (the **DWORD** byte count and the **DWORD** count of properties).</span></span> <span data-ttu-id="487eb-108">區段本身會包含8個位元組： **08 00 00 00 00 00 00 00**。</span><span class="sxs-lookup"><span data-stu-id="487eb-108">The section itself would contain the 8 bytes: **08 00 00 00 00 00 00 00**.</span></span>

 

 




