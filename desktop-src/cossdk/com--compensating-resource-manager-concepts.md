---
description: 您可以使用 COM + 補償 Resource Manager (CRM) 輕鬆快速地整合應用程式資源與 Microsoft Distributed Transaction Coordinator (DTC) 交易。
ms.assetid: 8d1d034f-8a09-40ae-842a-5251135bd3c8
title: COM + 補償 Resource Manager 概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14206a54ffcb4f7e06ddf7362736a722393b0791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936267"
---
# <a name="com-compensating-resource-manager-concepts"></a>COM + 補償 Resource Manager 概念

您可以使用 COM + 補償 Resource Manager (CRM) 輕鬆快速地整合應用程式資源與 Microsoft Distributed Transaction Coordinator (DTC) 交易。 您的應用程式資源可以針對交易的結果投票，並可接收其結果的最終通知。 系統會產生持久的記錄檔，讓您的應用程式資源可以寫入存留失敗的記錄，而 CRM 會在應用程式重新開機時復原此記錄檔。

CRM 包含下列兩個元件：

-   CRM 背景工作角色。 此元件會執行特定 CRM 的主要工作，並針對需要執行的工作，執行特定的介面。 CRM 基礎結構為 crm 工作者提供了一個介面，CRM 工作者可以透過此介面將記錄寫入磁片上的持久記錄檔。 CRM 工作者必須將記錄寫入記錄檔，並使其在執行其工作之前保持持久，如此一來，萬一發生損毀時，就可以正確進行復原。 CRM 背景工作一律需要交易。
-   CRM 補償器。 在交易完成時，CRM 基礎結構會建立此元件。 它會執行已定義的介面，讓 CRM 基礎結構可以傳遞交易完成的通知，以及先前由 CRM 背景工作撰寫的記錄檔記錄。

COM + CRM 提供不可部分完成性的交易式通知，以及 CRM 記錄檔的持久性，但不提供資源的隔離。 在多執行緒環境中，CRM 開發人員必須負責確保在交易中同時序列化多個 CRM 工作者或外部應用程式的資源存取權。

交易通過準備階段之後，CRM 補償器和 CRM 工作者可以同時執行。 當先前交易的 CRM 補償器仍在處理先前的交易時，新交易的 CRM 背景工作元件可能會變成作用中狀態。

在 CRM 伺服器應用程式復原之前的失敗期間，應該將中斷的交易視為使用中且未完成。 在復原 CRM 伺服器進程之前，外部進程應該無法存取此特定交易所變更的資源。

CRM 定義了基本 CRM 函式的三種介面類別型：

-   [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) 會在 crm 員工上執行，並由 Crm 背景工作角色用來將記錄檔記錄寫入記錄檔。 CRM 補償器也可以使用它。
-   [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) 和 [**ICRMCOMPENSATORVARIANTS**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) 會在 CRM 補償器上執行。 這些介面是用來將交易結果通知及其相關聯的記錄檔記錄傳遞給 CRM 補償器。 通常，CRM 補償器只會根據它是否需要非結構化或結構化記錄檔記錄，來執行其中一個介面。 *結構化* 記錄是以 variant 集合的形式建立的記錄，通常可供 Microsoft Visual Basic 使用。 *非結構化記錄檔記錄* 只是位元組緩衝區，通常可供 Microsoft Visual C++ 使用。 CRM 補償器可以同時執行兩個補償器介面;不過，一次只能有一個用來傳遞記錄檔記錄。
-   COM + CRM 監視介面可用來監視特定伺服器應用程式內的 Crm。 如需監視介面的詳細資訊，請參閱 [Com + CRM 監視介面](com--crm-monitoring-interfaces.md)。

本節中的下列主題提供 COM + CRM 服務的更多詳細資料：

-   [COM + CRM 安全性考慮](com--crm-security-considerations.md)
-   [COM + CRM 操作進程](com--crm-operating-process.md)
-   [COM + CRM 啟動和復原](com--crm-startup-and-recovery.md)
-   [在叢集環境中使用 COM + CRM](using-the-com--crm-in-a-cluster-environment.md)
-   [COM + CRM 中的錯誤處理](error-handling-in-the-com--crm.md)
-   [COM + CRM 登錄設定](com--crm-registry-settings.md)
-   [COM + CRM 疑難排解](troubleshooting-the-com--crm.md)
-   [開發 COM + CRM 的設計建議](design-suggestions-for-developing-a-com--crm.md)
-   [COM + CRM 監視介面](com--crm-monitoring-interfaces.md)
-   [COM + CRM 介面](com--crm-interfaces.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 補償 Resource Manager 工作](com--compensating-resource-manager-tasks.md)
</dt> </dl>

 

 



