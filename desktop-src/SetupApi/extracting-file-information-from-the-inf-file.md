---
description: 開啟 INF 檔案之後，您可以從該檔案收集資訊以建立使用者介面，或指示安裝程式。 安裝函式提供數個層級的功能，可從 INF 檔案收集資訊。
ms.assetid: 3ef2768b-8c73-4258-937c-77a40963ffe4
title: 從 INF 檔案解壓縮檔案資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b404f44ca7d1d92fe0ce8eab08b73012ff144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848231"
---
# <a name="extracting-file-information-from-the-inf-file"></a>從 INF 檔案解壓縮檔案資訊

開啟 INF 檔案之後，您可以從該檔案收集資訊以建立使用者介面，或指示安裝程式。 安裝函式提供數個層級的功能，可從 INF 檔案收集資訊。



| 若要收集資訊 .。。                | 使用這些函數 .。。                                                        |
|---------------------------------------|-----------------------------------------------------------------------------|
| 關於 INF 檔案                    | [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                    |
|                                       | [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)        |
|                                       | [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa)。 |
| 關於來源和目標檔案         | [**SetupGetSourceFileLocation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)            |
|                                       | [**SetupGetSourceFileSize**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                    |
|                                       | [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                            |
|                                       | [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                            |
| 從 INF 檔案中的一行            | [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                |
|                                       | [**SetupFindNextLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                              |
|                                       | [**SetupFindNextMatchLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                    |
|                                       | [**SetupGetLineByIndex**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                          |
|                                       | [**SetupFindFirstLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                            |
| 從 INF 檔案中的列欄位 | [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                          |
|                                       | [**SetupGetIntField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                |
|                                       | [**SetupGetBinaryField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                          |
|                                       | [**SetupGetMultiSzField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                        |



 

下列範例會使用 [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) 函式，從 INF 檔案取出來源媒體的人們可讀取描述。


```C++
#include <windows.h>
#include <setupapi.h>

BOOL test;  
HINF MyInf;
UINT SourceId;
PTSTR Buffer;
DWORD MaxBufSize;
DWORD BufSize;

int main()  
{ 

test = SetupGetSourceInfo (
     MyInf,   //Handle to the INF file to access                
     SourceId, //Id of the source media                 
     SRCINFO_DESCRIPTION, //which information to retrieve     
     Buffer, //a pointer to the buffer to receive the information                     
     MaxBufSize,  //the size allocated for the buffer 
     &BufSize    //buffer size actually needed
);
  
return 0;
}
```



在此範例中，MyInf 是開啟的 INF 檔案的控制碼。 SourceId 是特定來源媒體的識別碼。 值 SRCINFO \_ 描述指定 [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) 函式應該取出來源媒體描述。 緩衝區指向將接收描述的字串，MaxBufSize 表示配置給緩衝區的資源，而 BufSize 指出儲存緩衝區所需的資源。

如果 BufSize 大於 MaxBufSize，則函式會傳回 **FALSE**，而後續對 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 的呼叫將會傳回錯誤 \_ 的 \_ 緩衝區。

 

 
