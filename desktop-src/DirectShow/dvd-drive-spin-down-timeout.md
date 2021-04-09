---
description: DVD 光碟機調低時間
ms.assetid: 2295253d-0199-41b4-95a8-cda049ca93c7
title: DVD 光碟機調低時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda6853830ee7289e529d029c78fe4e56e4a0e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846607"
---
# <a name="dvd-drive-spin-down-timeout"></a>DVD 光碟機調低時間

在膝上型電腦上，為了節省電池壽命，您可能會想要縮短 DVD 光碟機在使用者暫停播放後會繼續旋轉的時間長度。 根據預設，DVD 導覽器會保留光碟旋轉兩分鐘。 此值可以在 Windows 登錄的下列機碼底下修改：


```C++
DWORD HKLM\SOFTWARE\Microsoft\DVDNavigator\DriveSpindown 
[Sec]
```



其中


```
Sec
```



這是微調時間（以秒為單位）。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[附錄](appendixes.md)
</dt> </dl>

 

 



