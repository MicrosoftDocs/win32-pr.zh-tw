---
title: 正在抓取目錄資訊
description: 正在抓取目錄資訊
ms.assetid: f2ec795f-6e6f-4c0c-9332-f1e96524221a
keywords:
- Windows Media Player 線上商店，正在抓取目錄資訊
- 線上商店，正在抓取目錄資訊
- 輸入1個線上商店，正在抓取目錄資訊
- Windows Media Player 線上商店、目錄的診斷資訊
- 線上商店、目錄的診斷資訊
- 輸入1個線上商店、目錄的診斷資訊
- Windows Media Player 線上商店，catcomp.exe
- 線上商店、catcomp.exe
- 輸入1個線上商店，catcomp.exe
- catcomp.exe
- 目錄的診斷資訊
- 正在抓取目錄資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3b28da6d2d5f5143dab0664c10d0c906f971a6a60e4fdb502f4331fa71f408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570199"
---
# <a name="retrieving-catalog-information"></a>正在抓取目錄資訊

您可以使用下列語法來執行 catcomp，以顯示目錄的診斷資訊：


```C++
catcomp info <catalogpath> [track|artist|album] [ID]
```



例如，下列命令會顯示整個類別目錄的相關資訊，包括版本、地區設定以及類別目錄專案的內部資訊：


```C++
catcomp info C:\Catalog210\catalog.wmdb
```



以下顯示識別碼為3256的追蹤資訊：


```C++
catcomp info C:\Catalog210\catalog.wmdb track 3256
```



 

 




