---
description: C 執行時間中包含的時間函數會使用 time \_ t 類型來代表自1970年1月1日午夜起經過的秒數。 下列範例會使用 Int32x32To64 函式，將 time \_ t 值轉換為檔案時間。
ms.assetid: f626c0b2-a5a1-475d-9a24-64e7b0407278
title: 將 time_t 值轉換為檔案時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee866efaed716fb12d2501337236afdb7cf641b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998921"
---
# <a name="converting-a-time_t-value-to-a-file-time"></a>將時間 \_ t 值轉換為檔案時間

C 執行時間中包含的時間函數會使用 time \_ t 類型來代表自1970年1月1日午夜起經過的秒數。 下列範例會使用 Int32x32To64 函式，將 time \_ t 值轉換為檔案[](/windows/desktop/api/winnt/nf-winnt-int32x32to64)時間。


```C++
#include <windows.h>
#include <time.h>

void TimetToFileTime( time_t t, LPFILETIME pft )
{
    LONGLONG ll = Int32x32To64(t, 10000000) + 116444736000000000;
    pft->dwLowDateTime = (DWORD) ll;
    pft->dwHighDateTime = ll >>32;
}
```



取得檔案時間之後，您可以使用 [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) 函數將此值轉換為系統時間。

 

 
