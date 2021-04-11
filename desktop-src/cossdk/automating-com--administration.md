---
description: COM + 提供的系統管理物件模型會公開 [元件服務] 系統管理工具的所有功能，它本身是以系統管理物件為基礎所撰寫的圖形前端。
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: 自動化 COM + 管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ef3f56da64e442594a7685a77efb9a06e3fe08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111048"
---
# <a name="automating-com-administration"></a>自動化 COM + 管理

COM + 提供的系統管理物件模型會公開 [元件服務] 系統管理工具的所有功能，它本身是以系統管理物件為基礎所撰寫的圖形前端。 您可以使用元件服務管理 (COMAdmin) 程式庫所提供的這些物件，將 COM + 應用程式和服務管理中的所有工作自動化。

COMAdmin 物件可讓您讀取和寫入儲存在 COM + 目錄中的資訊，這是保存所有 COM + 設定資料的基礎資料存放區。

您可以使用這些物件來執行下列作業：

-   建立和設定 COM + 應用程式。
-   安裝和匯出現有的 COM + 應用程式。
-   管理已安裝的 COM + 應用程式。
-   管理和設定服務。
-   在不同的電腦上遠端系統管理元件服務。

您可以使用可編寫腳本的 COMAdmin 物件搭配任何自動化相容語言，例如 Microsoft Visual Basic 和 Visual Basic 腳本。 您可以開發輕量腳本或一般用途的管理工具。 例如，您可以：

-   撰寫腳本來執行例行的系統管理工作。
-   撰寫腳本，以在開發 COM + 應用程式的過程中自動執行程式。
-   開發用來管理和監視元件服務的一般用途工具。
-   開發安裝程式可執行檔，以安裝及部署您的 COM + 應用程式。

COMAdmin 程式庫提供與 MTS 2.0 管理程式庫的回溯相容性。 雖然有一些例外狀況，但大部分現有的 MTS 2.0 管理程式碼仍可運作。  (參閱 [MTS 管理程式庫](mts-administration-library.md)。 ) 

若要有效率地自動化管理，您應該熟悉使用 [元件服務] 系統管理工具執行的系統管理工作。

如需 COMAdmin 物件和對應介面的完整說明，請參閱下列類別和介面的 COM + 參考檔：

-   [**COMAdminCatalog**](comadmincatalog.md)
-   [**COMAdminCatalogCollection**](comadmincatalogcollection.md)
-   [**COMAdminCatalogObject**](comadmincatalogobject.md)
-   [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
-   [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
-   [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
-   [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

本節中的下列主題提供使用 COMAdmin 物件自動化管理的總覽：

-   [COMAdmin 物件的總覽](overview-of-the-comadmin-objects.md)
-   [在 COM + 類別目錄上取出集合](retrieving-collections-on-the-com--catalog.md)
-   [設定屬性並將變更儲存至 COM + 類別目錄](setting-properties-and-saving-changes-to-the-com--catalog.md)
-   [處理 COM + 管理錯誤](handling-com--administration-errors.md)
-   [交易內的 COM + 管理作業](com--administration-operations-within-transactions.md)
-   [使用 COM + 系統管理目錄的簡介範例](introductory-example-using-the-com--administration-catalog.md)

 

 



