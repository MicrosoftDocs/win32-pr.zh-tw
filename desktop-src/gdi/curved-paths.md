---
description: 曲線路徑
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: 曲線路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe27e20d7c5c3f59ea4bd38b46049088ae9d409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848569"
---
# <a name="curved-paths"></a><span data-ttu-id="fac02-103">曲線路徑</span><span class="sxs-lookup"><span data-stu-id="fac02-103">Curved Paths</span></span>

<span data-ttu-id="fac02-104">應用程式可以藉由呼叫 [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) 函式來壓平合併路徑中的曲線。</span><span class="sxs-lookup"><span data-stu-id="fac02-104">An application can flatten the curves in a path by calling the [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) function.</span></span> <span data-ttu-id="fac02-105">此函式特別適用于將文字放在包含曲線的路徑輪廓上的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fac02-105">This function is especially useful for applications that fit text onto the contour of a path which contains curves.</span></span> <span data-ttu-id="fac02-106">為了符合文字，應用程式必須執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="fac02-106">To fit the text, the application must perform the following steps:</span></span>

1.  <span data-ttu-id="fac02-107">建立文字出現的路徑。</span><span class="sxs-lookup"><span data-stu-id="fac02-107">Create the path where the text appears.</span></span>
2.  <span data-ttu-id="fac02-108">呼叫 [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) 函數，將路徑中的曲線轉換成線段。</span><span class="sxs-lookup"><span data-stu-id="fac02-108">Call the [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) function to convert the curves in a path into line segments.</span></span>
3.  <span data-ttu-id="fac02-109">呼叫 [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) 函式來取出這些線段。</span><span class="sxs-lookup"><span data-stu-id="fac02-109">Call the [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) function to retrieve those line segments.</span></span>
4.  <span data-ttu-id="fac02-110">計算每一行的長度，以及字串中每個字元的寬度。</span><span class="sxs-lookup"><span data-stu-id="fac02-110">Calculate the length of each line and the width of each character in the string.</span></span>
5.  <span data-ttu-id="fac02-111">使用線條寬度和字元寬度資料，沿著曲線放置每個字元。</span><span class="sxs-lookup"><span data-stu-id="fac02-111">Use line-width and character-width data to position each character along the curve.</span></span>

 

 



