---
description: 正在載入語言資源
ms.assetid: 2655b2a3-2926-43f6-aef4-8b756c02a162
title: 正在載入語言資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eebf027476658872fe392fe60699da1a586f9297f39a191898b1e132439962c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106928"
---
# <a name="loading-language-resources"></a>正在載入語言資源

您的應用程式會使用標準資源載入函式的呼叫（例如， [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)、 [**loadstring 時**](/windows/win32/api/winuser/nf-winuser-loadstringa)和 [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)）載入所有使用者介面語言資源，而非特定重新導向的登錄字串。 許多資源載入函式已經過修改，可自動從特定語言的資源檔載入資源，將資源視為包含在 LN 檔案中。 下列範例說明如何使用 **loadstring 時** ，為遵循系統語言設定的應用程式載入語言字串。


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ...
LoadString(hResModule, myID, lpBuffer, cbBufferSize);
// ...
FreeLibrary(hResModule);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[尋找 Win32 PE 資源](locating-win32-pe-resources.md)
</dt> </dl>

 

 
