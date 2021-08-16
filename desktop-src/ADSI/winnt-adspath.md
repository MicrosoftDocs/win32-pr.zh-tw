---
title: WinNT ADsPath
description: 本主題包含用於 WinNT ADsPath 的字串範例。
ms.assetid: 0fad4b34-5287-43a0-a172-a08955b8b132
ms.tgt_platform: multiple
keywords:
- WinNT 服務提供者 ADSI，WinNT ADsPath
- ADsPath ADSI、WinNT、description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4971209a516d9e0c759e892322c99db1807a4bf88e771281299af30abc47d47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838368"
---
# <a name="winnt-adspath"></a>WinNT ADsPath

ADSI WinNT 提供者的 ADsPath 字串可以是下列其中一種形式：


```C++
WinNT:
WinNT://<domain name>
WinNT://<domain name>/<server>
WinNT://<domain name>/<path>
WinNT://<domain name>/<object name>
WinNT://<domain name>/<object name>,<object class>
WinNT://<server>
WinNT://<server>/<object name>
WinNT://<server>/<object name>,<object class>
```



功能變數名稱可以是 NETBIOS 名稱或 DNS 名稱。

伺服器是網域中特定伺服器的名稱。

路徑是物件的路徑，例如 "printserver1/printer2"。

物件名稱是特定物件的名稱。

物件類別是命名物件的類別名稱。 此使用方式的其中一個範例是 "WinNT://MyServer/JeffSmith,user"。 指定類別名稱可以改善系結作業的效能。

 

 




