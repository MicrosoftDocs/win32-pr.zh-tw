---
description: COM + CRM 疑難排解
ms.assetid: 4d2d9372-b540-4e08-9b57-8687802610b6
title: COM + CRM 疑難排解
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b04e37d183dbf3df8d017e780917f955e14a033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510627"
---
# <a name="troubleshooting-the-com-crm"></a>COM + CRM 疑難排解

以下是開發和使用 COM + CRM 時最常遇到的問題：

-   **事件記錄檔訊息。** 如果 CRM 伺服器應用程式遇到嚴重的內部錯誤，則會產生 failfast (終止 CRM 伺服器應用程式進程) 並將訊息寫入 Windows 事件記錄檔。 如果遇到任何問題，請參閱事件記錄檔。

-   **CRM 補償器的例外狀況。** CRM 基礎結構會建立 CRM 補償器，並將交易結果通知和 CRM 背景工作所寫入的記錄檔記錄傳遞給它。 如果 CRM 補償器傳回錯誤或擲回例外狀況，則會由 CRM 基礎結構攔截，並造成 failfast。 事件記錄檔中的訊息表示從 CRM 補償器收到例外狀況。 您可以強制忽略這些例外狀況。  (，請參閱 [Com + CRM 登錄設定](com--crm-registry-settings.md)。從 crm 補償器 ) 例外狀況，很可能表示特定 crm 補償器元件中的問題，而不是在 crm 基礎結構本身。

-   **復原追蹤。** 復原追蹤有助於判斷復原期間的問題。 如需啟用修復追蹤的詳細資訊，請參閱 [Com + CRM 登錄設定](com--crm-registry-settings.md)。

-   **嘗試在未啟用 CRM 的情況下執行。** 您只需將 CRM 工作者和 CRM 補償器元件放入 COM + 伺服器應用程式中即可。 使用 COM + 應用程式屬性頁之 [ **Advanced** ] 索引標籤上的 [**啟用補償資源管理員**] 選項，就必須特別針對特定的 com + 伺服器應用程式啟用 crm 的支援。  (如需詳細資訊，請參閱設定 [COM + CRM 元件](configuring-com--crm-components.md) 。 ) 如果嘗試在未啟用 crm 的伺服器應用程式內使用 crm，錯誤碼會傳回給 Crm 背景工作。

-   **嘗試在用戶端進程中執行 Crm。** Crm 不會在用戶端進程中執行;它們必須在 COM + 伺服器應用程式進程中執行。 CRM 元件可以放在程式庫封裝中，供多個 COM + 伺服器應用程式使用，但無法在用戶端進程中使用。 嘗試在用戶端進程內使用 CRM 介面，會將錯誤碼傳回給 CRM 背景工作。

-   **正在復原。** 當 CRM 伺服器應用程式啟動時，就會開始復原。 不過，復原是在 CRM 伺服器應用程式正常處理期間的背景進行。 您可以在復原完成之前建立 CRM 背景工作角色。 在成功完成復原之前，無法在 CRM 伺服器應用程式進程中使用 Crm。 在此情況下，當 CRM 工作者嘗試註冊 CRM 補償器時，會收到「正在復原」錯誤碼。 CRM 工作者應該輪詢或延遲，直到復原完成為止。 復原時間是特定類型的 CRM 專屬的，而且在設計 CRM 時應考慮這一點。 不需要長時間的復原。

-   **CRM 記錄檔的安全性。** 如果拒絕存取 CRM 記錄檔，請參閱 [Com + Crm 安全性考慮](com--crm-security-considerations.md) ，以取得在 crm 記錄檔上設定安全性的說明。

-   **不確定的交易。** 在罕見的情況下，DTC 交易可能會進入不確定狀態;也就是說，DTC 無法判斷交易結果。 在這些情況下，在復原期間，CRM 會在 CRM 記錄檔中維護該交易的記錄檔記錄。 當 DTC 解決了不確定的交易時，執行另一個 CRM 復原就會完成交易。

-   **CRM 補償器的建立和發行。** Crm 產生器第一次由 crm 工作者註冊時，它是由 CRM 基礎結構所建立，並會進行查詢以判斷其所支援的 CRM 補償器介面。 然後立即發行。 CRM Compensators 需要支援建立和發行的能力，而不需要任何中間的方法呼叫。 如果無法正確建立 CRM 補償器（可能是因為 COM 登錄不正確），或者如果它不支援至少一個正確的 CRM 補償器介面，則錯誤碼會傳回給 CRM 背景工作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 補償 Resource Manager 概念](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



