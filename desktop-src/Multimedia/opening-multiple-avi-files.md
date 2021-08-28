---
title: 開啟多個 AVI 檔案
description: 開啟多個 AVI 檔案
ms.assetid: 982bcea1-77b0-4a38-893d-1f506ffb18f5
keywords:
- initAVI 函式
- termAVI 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22045e23c3dcc6f05279fe9ddf999586923e0bf828757cd14a490f10c045c715
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806228"
---
# <a name="opening-multiple-avi-files"></a>開啟多個 AVI 檔案

如果您的應用程式開啟多個檔案，它應該會包含下列程式，例如下列簡單的函式。 應用程式會在其初始化期間使用 "initAVI" 函式，並在其終止期間使用 "termAVI" 函式。 這些函式只會包裝 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函數。


```C++
// Initialize the MCIAVI driver. This returns TRUE if OK, 
// FALSE on error. 
 
BOOL initAVI(VOID) 
{ 
    // Perform additional initialization before loading first file. 
    return mciSendString("open digitalvideo", NULL, 0, NULL) == 0; 
} 
 
// Close the MCIAVI driver. 
void termAVI(VOID) 
{ 
    mciSendString("close digitalvideo", NULL, 0, NULL); 
} 
```



 

 