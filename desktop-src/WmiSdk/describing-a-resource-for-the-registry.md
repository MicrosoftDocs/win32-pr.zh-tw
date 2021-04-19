---
description: 系統登錄包含與資源相關的資料。
ms.assetid: e66f1db8-a5f3-41d3-9835-34b81b9da5ed
ms.tgt_platform: multiple
title: 描述登錄的資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba175120b5abec238d1b9078010359effef8ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979276"
---
# <a name="describing-a-resource-for-the-registry"></a>描述登錄的資源

系統登錄包含與資源相關的資料。 這項資料位於下列登錄機碼底下，並保留在名為 **REG \_ RESOURCE \_ LIST** 的特殊登錄資料類型中。 應用程式可以透過系統登錄提供者取得與資源相關的資料。 您可以新增和修改登錄中的系統資源。

```
HKEY_LOCAL_MACHINE
   Hardware
      ResourceMap
```

下列程式說明如何在系統登錄中儲存與資源相關的資訊。

**在系統登錄中儲存與資源相關的資訊**

1.  建立包含下欄欄位的字串。

    

    <table>
    <thead>
    <tr class="header">
    <th>欄位</th>
    <th>包含</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>介面類型</td>
    <td>下列其中一個值：<br/> <dl> 內部<br />
    Isa<br />
    Eisa<br />
    MicroChannel<br />
    TurboChannel<br />
    PCIBus<br />
    VMEBus<br />
    NuBus<br />
    PCMCIABus<br />
    CBus<br />
    MPIBus<br />
    MPSABus<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>匯流排編號</td>
    <td>指定匯流排編號的整數。</td>
    </tr>
    <tr class="odd">
    <td>部分描述元編號</td>
    <td>指定描述項編號的整數。</td>
    </tr>
    <tr class="even">
    <td>Offset 或 union 類型</td>
    <td>下列其中一個值：<br/> <dl> 埠。啟動<br />
    Port. PhysicalAddress<br />
    埠。長度<br />
    中斷。層級<br />
    插斷向量<br />
    插斷的親和性<br />
    記憶體。開始<br />
    Memory. PhysicalAddress<br />
    記憶體。長度<br />
    Dma。通道<br />
    Dma。埠<br />
    Dma. Reserved1<br />
    DeviceSpecificData<br />
    DeviceSpecificData. Reserved1<br />
    DeviceSpecificData. Reserved2<br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  將字串放在登錄機碼底下的適當機碼中。

    ```
    HKEY_LOCAL_MACHINE
       Hardware
          ResourceMap
    ```

下列程式碼範例說明有效的資源描述項。

``` syntax
local|hkey_local_machine\hardware\resourcemap\
  hardware abstraction layer\
  pc compatible eisa/isa HAL|.raw("eisa",0,0,"interrupt.affinity")
```

下列程式碼範例顯示用於抓取資源描述項的有效 MOF 語法。

``` syntax
[DYNPROPS] 
class MyRegProp
{    
   [KEY]  
   STRING MyKey; 
   STRING MyReservedTranslated;
};

[DYNPROPS] 
instance of MyRegProp
{
   MyKey = "1";
   [PropertyContext("local|hkey_local_Machine\\hardware\\ResourceMap\\
                   System Resources\\Reserved|.Translated
                   (\"Internal\")(0)(1)(\"Memory.PhysicalAddress\")"),
   Dynamic, Provider("RegPropProv")] 
   MyReservedTranslated;
};
```

 

 




