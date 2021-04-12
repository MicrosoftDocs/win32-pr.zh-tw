---
description: 開發人員會產生修補程式建立檔案，並使用 Msimsp.exe 在 Patchwiz.dll 中呼叫 UiCreatePatchPackageEx 函式，藉以建立修補程式套件。
ms.assetid: 8a163653-6ba1-46ea-9832-f998749d29ae
title: 建立修補程式套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2561cb6729dc7b4e0e48acd13b6338f08a8ba943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193123"
---
# <a name="creating-a-patch-package"></a>建立修補程式套件

開發人員會產生修補程式建立檔案，並使用[Msimsp.exe](msimsp-exe.md)在[Patchwiz.dll](patchwiz-dll.md)中呼叫[UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md)函式，藉以建立修補程式套件。 Windows Installer SDK 中提供 Msimsp.exe 和 Patchwiz.dll。 如需詳細資訊，請參閱 [小型更新修補範例](a-small-update-patching-example.md)。

由於 Windows Installer 套件的修補程式會導致使用新的 .msi 檔案安裝原始來源，因此新的 .msi 檔案必須與原始來源的配置保持相容。

當您撰寫修補程式套件時，您必須使用未壓縮的安裝映射來建立修補程式，例如，系統管理映射或從 CD-ROM 的未壓縮安裝映射。 您也必須遵守下列限制：

-   請勿將檔案從某個資料夾移至另一個資料夾。
-   請勿將檔案從一個封包移至另一個。
-   請勿變更封包中的檔案順序。
-   請勿變更現有檔案的序號。 序號是在 [File 資料表](file-table.md)的 sequence 資料行中指定的值。
-   修補程式所加入的任何新檔案都必須放在現有檔案順序的結尾。 升級映射中任何新檔案的序號都必須大於目標映射中現有檔案的最大序號。
-   請勿在原始和新的 .msi 檔案版本之間變更檔案 [資料表](file-table.md) 中的主鍵。
    > [!Note]  
    > 檔案在目標映射和更新的映射的檔案 [資料表](file-table.md) 中必須有相同的索引鍵。 這兩個數據表的 File 資料行中的字串值必須相同，包括大小寫。

     

-   請勿使用只有大小寫不同的檔案 [資料表](file-table.md) 索引鍵來撰寫套件，例如，避免使用下表範例。

    

    | 檔案       | 元件\_ | FileName   |
    |------------|-------------|------------|
    | readme.txt | Comp1       | readme.txt |
    | ReadMe.txt | Comp2       | readme.txt |

    

     

    當 Comp1 和 Comp2 安裝在不同的目錄，但您無法使用 [Msimsp.exe](msimsp-exe.md) 或 [Patchwiz.dll](patchwiz-dll.md) 產生封裝的修補程式時，Windows Installer 可以允許上一個資料表範例。 Msimsp.exe 和 Patchwiz.dll 呼叫 Makecab.exe，不區分大小寫且失敗。

    在安裝程式中使用合併模組時，請確定檔案序號和配置符合上述指導方針。

 

 



