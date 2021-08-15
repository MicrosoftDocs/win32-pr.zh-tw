---
description: 存取 COM + 類別目錄
ms.assetid: 1322a3fe-faee-4971-949f-5e0d2dfe469b
title: 存取 COM + 類別目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f05d85526cb6d82916aa48a49c7f97e581c01b7410530878a7f6e0fc69dac20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129409"
---
# <a name="accessing-the-com-catalog"></a>存取 COM + 類別目錄

COM + 類別目錄是保存所有 COM + 設定資料的基礎資料存放區。 當您進行任何類型的 COM + 管理時，您會讀取和寫入儲存在目錄中的資料。 您可以存取類別目錄的唯一方法是透過 [元件服務] 系統管理工具，或透過 COMAdmin 程式庫。

COM + 類別目錄提供抽象層，可瞭解如何儲存 COM + 設定資料的實際詳細資料。 大部分的資料都儲存在 COM + 註冊資料庫 (或 RegDB) ，其中包含安裝在 COM + 應用程式中所有已設定元件的資料。 此資料庫會在應用程式執行時間使用，以將設定資料提供給 COM +，以便在適當的內容中適當地啟用物件，並根據其設定為物件提供服務。 RegDB 本身是一種交易式資源管理員，可透過 [補償資源管理員](com--compensating-resource-manager.md)使用 DTC 交易;當您進行保存的設定變更時，它們會以交易方式認可。 存取 RegDB 的唯一方法是使用 COMAdmin 物件或元件服務系統管理工具，透過 COM + 類別目錄來存取。

在每部電腦上，都有一個在系統應用程式中以元件的形式執行的 COM + 類別目錄伺服器。 目錄伺服器可控制存取儲存在其電腦上的目錄資料。實際上，目錄伺服器是一種查詢引擎，可讓您在該電腦的目錄中讀取和寫入資料。 當您透過具現化 [**COMAdminCatalog**](comadmincatalog.md) 物件來起始程式設計管理時，此物件會開啟本機目錄伺服器的會話。 本機目錄伺服器會處理本機目錄上集合或集合專案的要求。 當您連線到遠端電腦時，您會與該電腦上的目錄伺服器進行通訊。

## <a name="security-considerations-in-administration"></a>管理中的安全性考慮

若要變更 COM + 類別目錄上的資料，您必須以系統管理員的身分擁有授權單位。 若要使用 [元件服務] 系統管理工具來變更任何設定資料，您必須是系統管理員角色的成員，且該角色已指派給您嘗試管理的電腦上的系統應用程式。 同樣地，若要使用 COMAdmin 物件變更任何資料，您的程式碼必須以系統管理員授權單位執行。 也就是說，使用 COMAdmin 物件的應用程式或腳本，必須在其嘗試管理的電腦上，于系統應用程式上指派為系統管理員角色的使用者帳戶下執行。 應用程式只能存取類別目錄上的資訊，並將其變更為其執行所在之帳戶所屬的範圍。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COMAdmin 物件的總覽](overview-of-the-comadmin-objects.md)
</dt> <dt>

[COMAdmin 類別的摘要描述](summary-description-of-the-comadmin-classes.md)
</dt> </dl>

 

 



