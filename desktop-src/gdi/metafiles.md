---
description: 中繼檔是結構的集合，會以與裝置無關的格式儲存圖片。
ms.assetid: 309ee4cf-111b-4f09-a722-4823cb3d26b0
title: " (Windows GDI) 的中繼檔"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6eba952989215ac284dbae0642d30363c49088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972652"
---
# <a name="metafiles-windows-gdi"></a><span data-ttu-id="efebb-103"> (Windows GDI) 的中繼檔</span><span class="sxs-lookup"><span data-stu-id="efebb-103">Metafiles (Windows GDI)</span></span>

<span data-ttu-id="efebb-104">*中繼檔* 是結構的集合，會以與裝置無關的格式儲存圖片。</span><span class="sxs-lookup"><span data-stu-id="efebb-104">A *metafile* is a collection of structures that store a picture in a device-independent format.</span></span> <span data-ttu-id="efebb-105">裝置獨立性是設定點陣圖以外的中繼檔的一項功能。</span><span class="sxs-lookup"><span data-stu-id="efebb-105">Device independence is the one feature that sets metafiles apart from bitmaps.</span></span> <span data-ttu-id="efebb-106">與點陣圖不同的是，中繼檔可保證裝置獨立性。</span><span class="sxs-lookup"><span data-stu-id="efebb-106">Unlike a bitmap, a metafile guarantees device independence.</span></span> <span data-ttu-id="efebb-107">不過，中繼檔有一個缺點，通常繪製的速度比點陣圖更慢。</span><span class="sxs-lookup"><span data-stu-id="efebb-107">There is a drawback to metafiles however, they are generally drawn more slowly than bitmaps.</span></span> <span data-ttu-id="efebb-108">因此，如果應用程式需要快速繪圖，且裝置獨立性不是問題，則應該使用點陣圖而非中繼檔。</span><span class="sxs-lookup"><span data-stu-id="efebb-108">Therefore, if an application requires fast drawing and device independence is not an issue, it should use bitmaps instead of metafiles.</span></span>

-   [<span data-ttu-id="efebb-109">關於中繼檔</span><span class="sxs-lookup"><span data-stu-id="efebb-109">About Metafiles</span></span>](about-metafiles.md)
-   [<span data-ttu-id="efebb-110">使用中繼檔</span><span class="sxs-lookup"><span data-stu-id="efebb-110">Using Metafiles</span></span>](using-metafiles.md)
-   [<span data-ttu-id="efebb-111">中繼檔參考</span><span class="sxs-lookup"><span data-stu-id="efebb-111">Metafile Reference</span></span>](metafile-reference.md)

<span data-ttu-id="efebb-112">如需點陣圖的詳細資訊，請參閱 [點陣圖](bitmaps.md)。</span><span class="sxs-lookup"><span data-stu-id="efebb-112">For information about bitmaps, see [Bitmaps](bitmaps.md).</span></span>

 

 



