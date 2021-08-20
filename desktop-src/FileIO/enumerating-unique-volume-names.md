---
description: 如何取得與目前正在電腦上使用之磁碟機號相關聯之每個本機磁片區的磁片區 GUID 路徑。
ms.assetid: f6590a46-2e09-472c-8231-bb24c9b0b5f6
title: 列舉磁片區 GUID 路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69831b2b6fa515335a8d9ec25836f91824035ce186023e97bce13b7c8f4a3ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117997505"
---
# <a name="enumerating-volume-guid-paths"></a>列舉磁片區 GUID 路徑

本主題中的程式碼範例會示範如何取得每個本機磁片區的磁片區 **GUID** 路徑，該路徑與電腦上目前正在使用的磁碟機號相關聯。

程式碼範例會使用 [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) 函數。


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define BUFSIZE MAX_PATH 

void main(void)
 {
  BOOL bFlag;
  TCHAR Buf[BUFSIZE];           // temporary buffer for volume name
  TCHAR Drive[] = TEXT("c:\\"); // template drive specifier
  TCHAR I;                      // generic loop counter

  // Walk through legal drive letters, skipping floppies.
  for (I = TEXT('c'); I < TEXT('z');  I++ ) 
   {
    // Stamp the drive for the appropriate letter.
    Drive[0] = I;

    bFlag = GetVolumeNameForVolumeMountPoint(
                Drive,     // input volume mount point or directory
                Buf,       // output volume name buffer
                BUFSIZE ); // size of volume name buffer

    if (bFlag) 
     {
      _tprintf (TEXT("The ID of drive \"%s\" is \"%s\"\n"), Drive, Buf);
     }
   }
 }
```



如需列舉所有本機連接的磁片區，並顯示裝置路徑、磁片區 **GUID** 路徑和掛接路徑 (包括磁碟機號) 的範例，請參閱 [顯示磁片區路徑](displaying-volume-paths.md)。

 

 



