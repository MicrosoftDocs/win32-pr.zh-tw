---
title: 登錄值範例
description: 下列範例顯示某些驗證通訊協定登錄值的可能資料。
ms.assetid: 07772af0-db56-4cc6-ad72-cf79d3813883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bcbc3d4ca10a3e9298177a5eea240d0d34ade04
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104022886"
---
# <a name="registry-values-example"></a>登錄值範例

下列範例顯示某些驗證通訊協定登錄值的可能資料。

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               PPP
                  EAP
                     40
                        Path
                        FriendlyName
                        ConfigUIPath
                        IdentityPath
                        InteractiveUIPath
                        RequireConfigUI
                        ConfigCLSID
                        StandaloneSupported
```



| 金鑰名稱            | Datatype        | 值                                  |
|---------------------|-----------------|----------------------------------------|
| 路徑                | REG \_ EXPAND \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| FriendlyName        | REG \_ SZ         | EAP 通訊協定範例                    |
| ConfigUIPath        | REG \_ EXPAND \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| IdentityPath        | REG \_ EXPAND \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| InteractiveUIPath   | REG \_ EXPAND \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| RequireConfigUI     | REG \_ DWORD      | 1                                      |
| ConfigCLSID         | REG \_ SZ         | {0000031A-0000-0000-C000-000000000046} |
| StandaloneSupported | REG \_ DWORD      | 1                                      |



 

 

 




