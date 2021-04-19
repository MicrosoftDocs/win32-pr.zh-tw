---
description: 建立附件嵌入式管理單元擴充功能之後，您必須註冊它，MMC 和安全性設定嵌入式管理單元才能找到並使用它。
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: 註冊附件嵌入式管理單元延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7726131325433aa920ff22c9b71a4f7184000a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970789"
---
# <a name="registering-an-attachment-snap-in-extension"></a>註冊附件嵌入式管理單元延伸模組

建立附件嵌入式管理單元擴充功能之後，您必須註冊它，MMC 和安全性設定嵌入式管理單元才能找到並使用它。

您的附件嵌入式管理單元必須藉由新增自己的節點來擴充安全性設定嵌入式管理單元命名空間，如下列程式所述。

**安裝並註冊附件嵌入式管理單元延伸模組**

1.  在下列登錄機碼下註冊嵌入式管理單元延伸模組。 請勿在嵌入式管理單元下建立獨立金鑰;附件嵌入式管理單元延伸模組必須是延伸模組。

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             MMC
                SnapIns
    ```

2.  在下列子機碼下註冊附件嵌入式管理單元延伸模組。 這可做為 **DllRegisterServer** 和 **DllUnregisterServer** 函式執行的一部分。

    [安全性範本](security-templates.md) 命名空間：

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   24a7f717-1f0c-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

    [安全性設定與分析](security-configuration-and-analysis.md) 命名空間：

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   678050c7-1ff8-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

 

 



