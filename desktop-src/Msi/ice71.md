---
description: ICE71 會確認媒體資料表是否包含 DiskId 等於1的專案。
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c6e136362caa13da2b6305e3d8c3ca9c3a5c7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944978"
---
# <a name="ice71"></a><span data-ttu-id="d7c5c-103">ICE71</span><span class="sxs-lookup"><span data-stu-id="d7c5c-103">ICE71</span></span>

<span data-ttu-id="d7c5c-104">ICE71 會確認 [媒體資料表](media-table.md) 是否包含 DiskId 等於1的專案。</span><span class="sxs-lookup"><span data-stu-id="d7c5c-104">ICE71 verifies that the [Media table](media-table.md) contains an entry with DiskId equal to 1.</span></span> <span data-ttu-id="d7c5c-105"> (Windows Installer 會假設 .msi 封裝位於磁片1上。 ) </span><span class="sxs-lookup"><span data-stu-id="d7c5c-105">(Windows Installer assumes that the .msi package is on disk 1.)</span></span>

## <a name="result"></a><span data-ttu-id="d7c5c-106">結果</span><span class="sxs-lookup"><span data-stu-id="d7c5c-106">Result</span></span>

<span data-ttu-id="d7c5c-107">如果媒體資料表未包含 DiskId 等於1的專案，ICE71 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d7c5c-107">ICE71 returns an error if the Media table does not contain an entry with DiskId equal to 1.</span></span>

## <a name="example"></a><span data-ttu-id="d7c5c-108">範例</span><span class="sxs-lookup"><span data-stu-id="d7c5c-108">Example</span></span>

<span data-ttu-id="d7c5c-109">ICE71 會針對所顯示的範例報告下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="d7c5c-109">ICE71 reports the following error for the example shown.</span></span>

``` syntax
The Media table requires an entry with DiskId=1. First DiskId is '2'.
```

<span data-ttu-id="d7c5c-110">T0 修正這個錯誤，請變更將封裝儲存至1之專案的 DiskId。</span><span class="sxs-lookup"><span data-stu-id="d7c5c-110">T0 fix this error, change the DiskId of the entry where the package is stored to 1.</span></span>

<span data-ttu-id="d7c5c-111">[媒體資料表](media-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="d7c5c-111">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="d7c5c-112">DiskId</span><span class="sxs-lookup"><span data-stu-id="d7c5c-112">DiskId</span></span> |
|--------|
| <span data-ttu-id="d7c5c-113">2</span><span class="sxs-lookup"><span data-stu-id="d7c5c-113">2</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="d7c5c-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="d7c5c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7c5c-115">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="d7c5c-115">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



