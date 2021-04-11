---
description: Windows Installer 可以修復、取代和驗證應用程式中包含的檔案。 如果任何與任何功能相關聯的檔案或登錄專案遺失或損毀，可能需要重新安裝部分或完整的應用程式。
ms.assetid: fab23ab9-f1ab-4743-b883-cffc29b0124b
title: 重新安裝功能或應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f7dbf95204d96202c71a120eafb6e6e054ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115497"
---
# <a name="reinstalling-a-feature-or-application"></a>重新安裝功能或應用程式

Windows Installer 可以修復、取代和驗證應用程式中包含的檔案。 如果任何與任何功能相關聯的檔案或登錄專案遺失或損毀，可能需要重新安裝部分或完整的應用程式。

重新安裝功能或應用程式時，也會重新安裝屬於功能或應用程式的所有服務、環境變數和自訂動作。 請注意，這表示在原始安裝和重新安裝之間對環境變數所做的任何變更都會遺失。

下列清單包含重新安裝功能或產品的方法。 前兩個方法已由安裝程式自動化：

-   藉由呼叫 [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) 函數來修復、取代或驗證檔案。
-   藉由呼叫 [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) 函數來重新安裝整個產品。
-   透過 [重新安裝 ControlEvent](reinstall-controlevent.md)，重新安裝、取代或確認具有安裝程式 UI 控制項按鈕的檔案。
-   藉由設定 [**重新安裝**](reinstall.md) 屬性和 [**REINSTALLMODE**](reinstallmode.md) 屬性，從命令列重新安裝、取代或驗證檔案。

如需重新安裝功能或應用程式的詳細資訊，請參閱 [復原](resiliency.md)。

**使用安裝程式重新安裝產品**

-   呼叫 [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)。

**使用安裝程式重新安裝功能**

-   呼叫 [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)。

**使用安裝程式使用者介面重新安裝產品或功能**

1.  將專案加入至 [控制項資料表](control-table.md)，以將按鈕加入至指定的對話方塊。
2.  將 [ReinstallMode ControlEvent](reinstallmode-controlevent.md) 加入至 ControlEvent 資料表，而對話方塊 \_ 和控制項欄位則 \_ 參考在步驟1中建立的按鈕控制項。 在 [引數] 欄位中，輸入字串，其中包含與您想要的重新安裝模式相對應的字母 (此欄位可接受的值與 [**REINSTALLMODE**](reinstallmode.md) 屬性) 所接受的值相同。 此事件之排序資料行中的值應該是1。
3.  將 [重新安裝 ControlEvent](reinstall-controlevent.md) 事件新增至 [ControlEvent 資料表](controlevent-table.md)，並再次參考相同的按鈕控制項。 此事件的 [引數] 欄位通常都是 [全部]，以強制重新安裝所有功能，但您可以在此放置特定功能的名稱。 此事件之排序資料行中的值應該是2。
4.  再新增一個系結至相同按鈕控制項的事件，以實際起始重新安裝。 這可以是 EndDialog 事件 (具有傳回) 的引數。 不過，NewDialog 事件通常是在這裡用來跳到 **您確定要重新安裝？** 確認對話方塊。 此事件之排序資料行中的值應為3。

    如有需要，可以為單一對話方塊建立數個 [**重新安裝**](reinstall.md) 按鈕，讓使用者選取執行的重新安裝類型。 在此情況下，每個按鈕都會依照上述程式中的說明來撰寫，每個按鈕都有不同的 [ReinstallMode ControlEvent](reinstallmode-controlevent.md) 參數。

一旦將特定產品安裝 (與部分或所有產品功能) ，就可以在命令列執行重新安裝：

**從命令列重新安裝產品或功能**

1.  從命令提示字元中，指定 [**重新安裝**](reinstall.md) 屬性。
2.  從命令提示字元中，指定 [**REINSTALLMODE**](reinstallmode.md) 屬性。

    指定這些屬性可讓使用者重新安裝產品的任何或所有功能。 您也可以指定重新安裝類型。 例如，您可以指定只重新安裝完全遺失的檔案，或是只有損毀的檔案 (例如，總和檢查碼不符合實際檔案內容的任何可執行檔) 被取代。

 

 



