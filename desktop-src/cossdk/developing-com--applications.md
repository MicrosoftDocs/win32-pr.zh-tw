---
description: 開發 COM + 應用程式時，主要工作包括設計 COM 元件來封裝應用程式邏輯，並將這些元件整合至 COM + 應用程式中、建立 COM + 應用程式，以及透過部署和維護來管理應用程式。
ms.assetid: 8c6ec901-1eeb-46b0-8a3a-26d8eff99f6d
title: 開發 COM + 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee6495b7d8f7b2cc059b113f4250042cfd59b99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510472"
---
# <a name="developing-com-applications"></a>開發 COM + 應用程式

開發 COM + 應用程式時，主要工作包括設計 COM 元件來封裝應用程式邏輯，並將這些元件整合至 COM + 應用程式中、建立 COM + 應用程式，以及透過部署和維護來管理應用程式。

## <a name="designing-com-components"></a>設計 COM 元件

下列步驟描述良好元件設計的一般程式：

1.  定義 COM 類別和實類別。
2.  將類別群組為元件。
3.  針對您的元件選取 COM + 服務集合，即使您未在開發元件時指定所有服務。 您稍後可以使用 [元件服務] 系統管理工具或 COM + 系統管理物件模型來指定這些服務 (如需 COM + 系統管理物件模型的詳細資訊，請參閱 [自動化 COM + 管理](automating-com--administration.md) 。 ) 

## <a name="creating-the-com-application"></a>建立 COM + 應用程式

設計 COM 元件之後，開發人員會將元件整合至 COM + 應用程式，並設定應用程式。 下列步驟說明此程序：

1.  將元件整合至 COM + 應用程式。 您可以將元件整合至現有的 COM + 應用程式，或為元件建立新的 (空白) 應用程式。  (參閱 [建立 COM + 應用程式](creating-com--applications.md)。 ) 
2.  針對每個類別 (指定一組正確的屬性（如果有的話），如果未在開發工具) 中指定，則為。 這些屬性 (會表達任何 COM + 服務的元件相依性，例如，交易、佇列元件、安全性、物件共用和及時啟用) 。
3.  將安全性架構 (角色和角色指派指派給) 的類別、介面和方法。
4.  在類別和應用程式上設定環境特定屬性 (預設物件集區大小，例如) 。 這些環境特定屬性之後可以 (或修改) 由系統管理員設定。
5.  匯出應用程式以轉散發和部署。

如需設計分散式應用程式之步驟的詳細資訊，請參閱 [設計 COM + 應用程式](designing-com--applications.md)。

## <a name="administering-com-applications"></a>管理 COM + 應用程式

一般來說，開發人員會將部分設定的 COM + 應用程式提供給系統管理員。 然後系統管理員可以自訂一個或多個特定環境的應用程式 (例如，將使用者帳戶新增至應用程式叢集中的角色和伺服器名稱) 。 系統管理員的工作包括下列各項：

-   在系統管理電腦上安裝部分設定的 COM + 應用程式。
-   提供環境特定的屬性，例如角色成員和物件集區大小。
-   重新匯出完整設定的 COM + 應用程式。
-   建立應用程式 proxy (如果要從遠端存取應用程式) 。

針對特定環境完整設定應用程式之後，系統管理員就可以將它部署在測試或實際執行機器上。 這牽涉到在一或多部電腦上安裝完整設定的 COM + 應用程式。

如需 COM + 系統管理程式的詳細資訊，請參閱「元件服務」系統管理工具。

 

 



