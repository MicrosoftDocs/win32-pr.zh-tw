---
description: 下列程式碼範例顯示 mutex 物件的使用方式，以判斷是否已登入 MSN Explorer。
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: 判斷 MSN 是否處於登入狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d7af3511035c997493f0439a8635c1a928a75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510651"
---
# <a name="determining-if-msn-is-in-the-sign-in-state"></a><span data-ttu-id="01797-103">判斷 MSN 是否處於登入狀態</span><span class="sxs-lookup"><span data-stu-id="01797-103">Determining if MSN Is in the Sign-in State</span></span>

<span data-ttu-id="01797-104">下列程式碼範例顯示 mutex 物件的使用方式，以判斷是否已登入 MSN Explorer。</span><span class="sxs-lookup"><span data-stu-id="01797-104">The following code example shows the usage of a mutex object to determine if MSN Explorer is signed in.</span></span> <span data-ttu-id="01797-105">當您完成使用控制碼時，請務必呼叫 [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) 函數。</span><span class="sxs-lookup"><span data-stu-id="01797-105">When you have finished using the handle, be sure to call the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span>

> [!Note]  
> <span data-ttu-id="01797-106">此 mutex 物件可用於檢查 MSN Explorer 7。*x* 登入狀態。</span><span class="sxs-lookup"><span data-stu-id="01797-106">This mutex object is available for use in checking MSN Explorer 7.*x* sign-in status.</span></span> <span data-ttu-id="01797-107">它可能在後續版本中無法使用。</span><span class="sxs-lookup"><span data-stu-id="01797-107">It may be unavailable in subsequent versions.</span></span>

 


```C++
    HANDLE hMSNSignedInMutex;

    hMSNSignedInMutex = OpenMutex(SYNCHRONIZE, FALSE, 
        "{ECCC50B5-064B-4693-B104-925714A4C74B}");

    if (hMSNSignedInMutex != NULL)
    {
        // MSN Explorer is signed in
    }
```



 

 
