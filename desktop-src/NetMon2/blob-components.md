---
description: BLOB 元件
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: BLOB 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfdb9c1f336ad0cddc1798cc98083890096dd39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193918"
---
# <a name="blob-components"></a><span data-ttu-id="33f4f-103">BLOB 元件</span><span class="sxs-lookup"><span data-stu-id="33f4f-103">BLOB Components</span></span>

<span data-ttu-id="33f4f-104">二進位大型物件 (BLOB) 包含下列階層式元件：</span><span class="sxs-lookup"><span data-stu-id="33f4f-104">A binary large object (BLOB) includes the following hierarchical components:</span></span>

-   <span data-ttu-id="33f4f-105">擁有者</span><span class="sxs-lookup"><span data-stu-id="33f4f-105">Owners</span></span>
-   <span data-ttu-id="33f4f-106">類別</span><span class="sxs-lookup"><span data-stu-id="33f4f-106">Categories</span></span>
-   <span data-ttu-id="33f4f-107">標籤</span><span class="sxs-lookup"><span data-stu-id="33f4f-107">Tags</span></span>
-   <span data-ttu-id="33f4f-108">值</span><span class="sxs-lookup"><span data-stu-id="33f4f-108">Values</span></span>

## <a name="textual-representation"></a><span data-ttu-id="33f4f-109">文字標記法</span><span class="sxs-lookup"><span data-stu-id="33f4f-109">Textual Representation</span></span>

<span data-ttu-id="33f4f-110">為了方便起見，Blob 會在儲存至檔案時出現在「擁有者：類別：標記：值」格式中。</span><span class="sxs-lookup"><span data-stu-id="33f4f-110">For convenience, BLOBs appear in the Owner:Category:Tag:Value format that they appear in when saved to a file.</span></span> <span data-ttu-id="33f4f-111">BLOB 的內部結構是不透明的，因為它代表指標和資料表。</span><span class="sxs-lookup"><span data-stu-id="33f4f-111">The internal structure of the BLOB is opaque because it represents pointers and tables.</span></span> <span data-ttu-id="33f4f-112">例如，以下是可用於設定 NPP 的 BLOB 專案：</span><span class="sxs-lookup"><span data-stu-id="33f4f-112">For example, here is an entry from a BLOB that can be used to configure an NPP:</span></span>

``` syntax
NPP:Configure:BufferSize=32768
```

<span data-ttu-id="33f4f-113">擁有者為 NPP。</span><span class="sxs-lookup"><span data-stu-id="33f4f-113">The Owner is NPP.</span></span> <span data-ttu-id="33f4f-114">此類別為 [設定]，標記為 [BufferSize]，而值為32768。</span><span class="sxs-lookup"><span data-stu-id="33f4f-114">The Category is Configure, the Tag is BufferSize, and the Value is 32768.</span></span>

 

 



