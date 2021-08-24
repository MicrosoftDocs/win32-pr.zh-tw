---
description: 下列程式碼範例顯示 mutex 物件的使用方式，以判斷是否已登入 MSN Explorer。
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: 判斷 MSN 是否處於登入狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da0abffc1735d2bf7af6ee6f9a68bf0d71ca1a2fda44176a0905c3e8faec6d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654188"
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



 

 
