---
description: Windows 通訊端中的命名空間組織 (Winsock) SPI。
ms.assetid: c369a476-23e4-48a1-912b-2d876deb0b88
title: SPI 中的命名空間組織
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a572ad86299f0bf5ba3e7f95662e1616da520608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973843"
---
# <a name="namespace-organization-in-the-spi"></a><span data-ttu-id="6b79c-103">SPI 中的命名空間組織</span><span class="sxs-lookup"><span data-stu-id="6b79c-103">Namespace Organization in the SPI</span></span>

<span data-ttu-id="6b79c-104">許多命名空間會以階層方式排列。</span><span class="sxs-lookup"><span data-stu-id="6b79c-104">Many namespaces are arranged hierarchically.</span></span> <span data-ttu-id="6b79c-105">有些（例如，X. 500 和 NDS）允許無限制的嵌套。</span><span class="sxs-lookup"><span data-stu-id="6b79c-105">Some, such as X.500 and NDS, allow unlimited nesting.</span></span> <span data-ttu-id="6b79c-106">其他則允許將服務合併為單一層級的階層或群組。</span><span class="sxs-lookup"><span data-stu-id="6b79c-106">Others allow services to be combined into a single level of hierarchy or group.</span></span> <span data-ttu-id="6b79c-107">這通常稱為工作組。</span><span class="sxs-lookup"><span data-stu-id="6b79c-107">This is typically referred to as a workgroup.</span></span> <span data-ttu-id="6b79c-108">當您建立查詢時，通常必須在命名空間階層內建立搜尋開始的內容點。</span><span class="sxs-lookup"><span data-stu-id="6b79c-108">When constructing a query, it is often necessary to establish a context point within a namespace hierarchy from which the search will begin.</span></span>

 

 



