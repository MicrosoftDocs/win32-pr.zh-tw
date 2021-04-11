---
title: 可安裝的磁片磁碟機 Module-Definition 檔案
description: 可安裝的磁片磁碟機 Module-Definition 檔案
ms.assetid: d8d8d32e-18ac-47a5-a923-48b94b75e11d
keywords:
- 可安裝的驅動程式、模組定義檔
- 可安裝的驅動程式、DEF 檔案
- nstallable 驅動程式，DriverProc 函式
- DriverProc 函式
- 模組定義檔
- DEF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700931c91bfb3c17a36a1e3a1bbc4833097b4b38
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023365"
---
# <a name="installable-drive-module-definition-file"></a>可安裝的磁片磁碟機 Module-Definition 檔案

模組定義 (。DEF) 可安裝驅動程式的檔案會將驅動程式命名為驅動程式、匯出 [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) 函式，並定義驅動程式描述。 下列範例顯示可安裝驅動程式的典型模組定義檔：


```C++
LIBRARY OSCI 
DESCRIPTION 'FREQ,AMPL:Oscilloscope frequency and amplitude drivers.'
EXPORTS
    DriverProc
 
```



某些安裝應用程式可能會開啟驅動程式，並取得安裝驅動程式時所要使用的描述行。 為了與這些安裝應用程式保持相容，描述行的格式應該如下：

**DESCRIPTION**  *alias* \[ ，*alias* \] ... **:* * * text*

*別名* 會指定應用程式可用來開啟驅動程式之驅動程式的唯一名稱。 別名也可作為與登錄中驅動程式相關聯的值名稱。 多個別名會以逗號分隔。 此 *文字* 描述驅動程式的用途。

 

 