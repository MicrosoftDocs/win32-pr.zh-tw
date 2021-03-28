---
description: ExcludeUpdateRgn 函式會從顯示裝置內容的裁剪區域中排除更新區域。
ms.assetid: e652122b-a3b7-4d1b-8afd-9648d5ee3d42
title: 排除更新區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7be39b948e61fc06c7f7005d15c1163cef0068f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026458"
---
# <a name="excluding-the-update-region"></a><span data-ttu-id="749db-103">排除更新區域</span><span class="sxs-lookup"><span data-stu-id="749db-103">Excluding the Update Region</span></span>

<span data-ttu-id="749db-104">[**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn)函式會從顯示裝置內容的裁剪區域中排除更新區域。</span><span class="sxs-lookup"><span data-stu-id="749db-104">The [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) function excludes the update region from the clipping region for the display device context.</span></span> <span data-ttu-id="749db-105">當您在非 WM \_ 油漆訊息正在處理的視窗中繪製時，此函式很有用。</span><span class="sxs-lookup"><span data-stu-id="749db-105">This function is useful when drawing in a window other than when a WM\_PAINT message is processing.</span></span> <span data-ttu-id="749db-106">它會防止在下一個 WM 油漆訊息期間更新的區域中進行繪圖 \_ 。</span><span class="sxs-lookup"><span data-stu-id="749db-106">It prevents drawing in the areas that will be updated during the next WM\_PAINT message.</span></span>

 

 



