---
description: 下列範例說明如何在安裝結束時啟動 HTML 檔案。
ms.assetid: 6b082559-bcfa-4098-b072-27ee78092833
title: 使用自訂動作在安裝結束時啟動已安裝的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108ae06dae331660fe5c4f1ff8740a5fdb7e76f5eab27794fafcd7a4495296ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141471"
---
# <a name="using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation"></a>使用自訂動作在安裝結束時啟動已安裝的檔案

下列範例說明如何在安裝結束時啟動 HTML 檔案。 安裝程式會安裝包含該檔案的元件，然後在安裝結束時發佈控制項事件，以執行可開啟檔案的自訂動作。 這種方法可用來在應用程式第一次安裝結束時啟動說明教學課程。

範例必須符合下列規格。

-   只有在使用 [*完整的 UI*](f-gly.md) 層級來安裝應用程式時，安裝程式才會執行自訂動作。
-   只有當包含 HTML 檔案的元件安裝在本機電腦上執行時，安裝程式才會執行自訂動作。
-   自訂動作只會在第一次安裝應用程式時執行。
-   如果自訂動作失敗，安裝將不會失敗。

此範例包含名為「教學課程」的假想元件，它會控制至少一個資源，一個名為 tutorial.htm 的檔案。 在檔案資料表的 [檔案] 資料行中，這個檔案的識別碼是教學課程。 下列討論假設您已經建立教學課程所需的資源，並已在[功能](feature-table.md)、[元件](component-table.md) [、檔案、](file-table.md)[目錄](directory-table.md)和[FeatureComponents](featurecomponents-table.md)資料表中完成所有必要的專案，以安裝此元件。 如需詳細資訊，請參閱 [安裝範例](an-installation-example.md)。

下列主題包含有關如何建立必要的自訂動作，並將其新增至安裝套件的資訊。

-   [撰寫啟動自訂動作](authoring-the-launch-custom-action.md)
-   [將啟動新增至 CustomAction 和二進位資料表](adding-launch-to-the-customaction-and-binary-tables.md)
-   [在安裝結束時新增控制項事件以執行啟動](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)

 

 



