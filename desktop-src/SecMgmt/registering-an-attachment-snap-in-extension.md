---
description: 建立附件嵌入式管理單元擴充功能之後，您必須註冊它，MMC 和安全性設定嵌入式管理單元才能找到並使用它。
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: 註冊附件嵌入式管理單元延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7af8b586f0071a5718b420612fd552d578bf30bb083cca45a43f38198e1aee7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005016"
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

 

 



