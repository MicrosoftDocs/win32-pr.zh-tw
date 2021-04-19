---
description: 如何取得與目前正在電腦上使用之磁碟機號相關聯之每個本機磁片區的磁片區 GUID 路徑。
ms.assetid: f6590a46-2e09-472c-8231-bb24c9b0b5f6
title: 列舉磁片區 GUID 路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e363369d3ea26abb054c8b9321c0147ace7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996802"
---
# <a name="enumerating-volume-guid-paths"></a><span data-ttu-id="6dabf-103">列舉磁片區 GUID 路徑</span><span class="sxs-lookup"><span data-stu-id="6dabf-103">Enumerating Volume GUID Paths</span></span>

<span data-ttu-id="6dabf-104">本主題中的程式碼範例會示範如何取得每個本機磁片區的磁片區 **GUID** 路徑，該路徑與電腦上目前正在使用的磁碟機號相關聯。</span><span class="sxs-lookup"><span data-stu-id="6dabf-104">The code example in this topic shows you how to obtain a volume **GUID** path for each local volume associated with a drive letter that is currently in use on the computer.</span></span>

<span data-ttu-id="6dabf-105">程式碼範例會使用 [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) 函數。</span><span class="sxs-lookup"><span data-stu-id="6dabf-105">The code example uses the [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) function.</span></span>


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



<span data-ttu-id="6dabf-106">如需列舉所有本機連接的磁片區，並顯示裝置路徑、磁片區 **GUID** 路徑和掛接路徑 (包括磁碟機號) 的範例，請參閱 [顯示磁片區路徑](displaying-volume-paths.md)。</span><span class="sxs-lookup"><span data-stu-id="6dabf-106">For an example that enumerates all locally attached volumes and displays the device path, volume **GUID** path, and mounted paths (including drive letters), see [Displaying Volume Paths](displaying-volume-paths.md).</span></span>

 

 



