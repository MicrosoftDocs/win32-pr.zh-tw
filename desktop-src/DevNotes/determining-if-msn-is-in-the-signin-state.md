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
# <a name="determining-if-msn-is-in-the-sign-in-state"></a>判斷 MSN 是否處於登入狀態

下列程式碼範例顯示 mutex 物件的使用方式，以判斷是否已登入 MSN Explorer。 當您完成使用控制碼時，請務必呼叫 [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) 函數。

> [!Note]  
> 此 mutex 物件可用於檢查 MSN Explorer 7。*x* 登入狀態。 它可能在後續版本中無法使用。

 


```C++
    HANDLE hMSNSignedInMutex;

    hMSNSignedInMutex = OpenMutex(SYNCHRONIZE, FALSE, 
        "{ECCC50B5-064B-4693-B104-925714A4C74B}");

    if (hMSNSignedInMutex != NULL)
    {
        // MSN Explorer is signed in
    }
```



 

 
