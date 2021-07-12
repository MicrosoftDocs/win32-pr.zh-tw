---
description: 您可以透過快捷方式檔案，將連接點的根目錄檢視啟動至該連接點。
title: 如何透過快捷方式檔案開啟連接點的根目錄檢視
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52096f0dbbcebadb60e2612f0304ed497199b2ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581606"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a>如何透過快捷方式檔案開啟連接點的根目錄檢視

您可以透過 [快捷方式](./links.md) 檔案，將連接點的根目錄檢視啟動至該連接點。

## <a name="instructions"></a>指示


使用/root 旗標，將快捷方式檔案的目標行設定為 Explorer.exe。 命令的確切形式取決於連接點的位置：

-   如果連接點是桌面的子資料夾，請使用：

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   如果連接點是檔系統資料夾，請使用：

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   如果連接點是系統虛擬資料夾的子資料夾，請使用：

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    可以包含連接點的系統虛擬資料夾具有下列類別識別碼 (Clsid) ：

    

    | 系統資料夾     | 類別識別碼                       |
    |-------------------|----------------------------------------|
    | 我的電腦       | {20D04FE0-3AEA-1069-A2D8-08002B30309D} |
    | 網路上的芳鄰 | {208D2C60-3AEA-1069-A2D7-08002B30309D} |
    | 控制台     | {21EC2020-3AEA-1069-A2DD-08002B30309D} |
    | Internet Explorer | {871C5380-42A0-1069-A2EA-08002B30309D} |

    

     

## <a name="related-topics"></a>相關主題

<dl> <dt>

[指定命名空間延伸模組的位置](nse-junction.md)
</dt> <dt>

[如何透過登錄開啟連接點的根目錄檢視](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 
