---
title: 開啟多個 AVI 檔案
description: 開啟多個 AVI 檔案
ms.assetid: 982bcea1-77b0-4a38-893d-1f506ffb18f5
keywords:
- initAVI 函式
- termAVI 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac540d670b15eaf1befb1d2f253223e3571ecee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965844"
---
# <a name="opening-multiple-avi-files"></a><span data-ttu-id="aabfc-105">開啟多個 AVI 檔案</span><span class="sxs-lookup"><span data-stu-id="aabfc-105">Opening Multiple AVI Files</span></span>

<span data-ttu-id="aabfc-106">如果您的應用程式開啟多個檔案，它應該會包含下列程式，例如下列簡單的函式。</span><span class="sxs-lookup"><span data-stu-id="aabfc-106">If your application opens multiple files, it should include routines such as the following simple functions.</span></span> <span data-ttu-id="aabfc-107">應用程式會在其初始化期間使用 "initAVI" 函式，並在其終止期間使用 "termAVI" 函式。</span><span class="sxs-lookup"><span data-stu-id="aabfc-107">The application would use the "initAVI" function during its initialization and the "termAVI" function during its termination.</span></span> <span data-ttu-id="aabfc-108">這些函式只會包裝 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="aabfc-108">These functions simply wrap the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span>


```C++
// Initialize the MCIAVI driver. This returns TRUE if OK, 
// FALSE on error. 
 
BOOL initAVI(VOID) 
{ 
    // Perform additional initialization before loading first file. 
    return mciSendString("open digitalvideo", NULL, 0, NULL) == 0; 
} 
 
// Close the MCIAVI driver. 
void termAVI(VOID) 
{ 
    mciSendString("close digitalvideo", NULL, 0, NULL); 
} 
```



 

 