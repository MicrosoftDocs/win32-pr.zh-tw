---
description: 本主題說明應用程式如何在 Windows Vista 和更新版本或舊版作業系統上載入 Win32 PE 資源模組。 包含用於釋放資源模組的呼叫。
ms.assetid: c9f126a7-315a-4856-80b3-aec02402a80e
title: 載入 Win32 PE 資源模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c4c1906a4fc09dc39b805e8ad5a875d96fae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997266"
---
# <a name="loading-a-win32-pe-resource-module"></a>載入 Win32 PE 資源模組

本主題說明應用程式如何在 Windows Vista 和更新版本或舊版作業系統上載入 Win32 PE 資源模組。 包含用於釋放資源模組的呼叫。

## <a name="load-the-resource-module-on-windows-vista-and-later"></a>在 Windows Vista 和更新版本上載入資源模組

在 Windows Vista 和更新版本中，應用程式會使用對 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)的呼叫來載入資源模組。 建議的作業是呼叫此函式，並指定兩個旗標。 以下是根據系統語言設定載入模組的應用程式程式碼範例。


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ... insert code here to call resource loading functions ...
FreeLibrary(hResModule);
```



## <a name="load-the-resource-module-on-pre-windows-vista-operating-systems"></a>在 Windows Vista 之前的作業系統上載入資源模組

在 Windows Vista 之前版本的作業系統上，應用程式會根據與目標作業系統相容的語言設定，以及 Windows Vista 和更新版本來載入資源模組。 針對此類型的模組載入，應用程式必須呼叫 MUI 函式 [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) 和 [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary)。


```C++
#include "MuiLoad.h"
HMODULE hResModule = LoadMUILibrary(TEXT("Mymodule.dll"), MUI_LANGUAGE_NAME, 0);
// ... insert code here to call resource loading functions ...
FreeMUILibrary(hResModule);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[尋找 Win32 PE 資源](locating-win32-pe-resources.md)
</dt> <dt>

[MUI： (Windows Vista) 的 Application-Specific 設定範例 ](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[MUI： (Windows Vista 之前的 Application-Specific 設定範例) ](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 
