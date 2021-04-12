---
description: CRM 基礎結構提供一組介面，可用來監視特定伺服器應用程式內的 Crm。
ms.assetid: b8f40c91-001b-4003-b377-57a918988100
title: COM + CRM 監視介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c893040c46810c980c647cbacdc808200e8d5f5e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187662"
---
# <a name="com-crm-monitoring-interfaces"></a>COM + CRM 監視介面

CRM 基礎結構提供一組介面，可用來監視特定伺服器應用程式內的 Crm。 若要存取監視介面，在伺服器應用程式內執行的元件必須先建立一個稱為 CRM 復原員的特製化 CRM 職員。

在 Crm 的正常使用方式下，交易預期會存留期很短，因此 CRM 工作者和 CRM Compensators 的存在時間很短，通常只需要幾秒鐘的時間。 因此，監視介面的設計目的是在特定時間點提供執行中 Crm 狀態的快照集。 如果有任何 Crm 發生問題，監視介面可以在有問題的 CRM 上用於零，以檢查其記錄檔記錄，並在必要時中止其交易。

以下是三個 CRM 監視介面，以及其運作方式的說明。



| 介面                                                         | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICrmMonitor**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)<br/>                     | 您可以使用 [**ICrmMonitor：： GetClerks**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmmonitor-getclerks)，在伺服器應用程式內取得目前作用中 CRM clerk 集的快照集。 如此一來，就可以找到和查詢感興趣的特定 CRM 職員集合物件，包括其交易的目前狀態，以及 CRM 所寫入的記錄檔記錄。<br/> 當監視工具判定有興趣的職員時，它會呼叫 [**ICrmMonitor：： HoldClerk**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmmonitor-holdclerk) 來取得該特定人員的 [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) 介面。 此時，監視工具會保存該職員的參考，而如果交易完成，則會將該職員保留在記憶體中，而且在監視工具完成之前，不會釋出。<br/>                                                                                                                                                                                                    |
| [**ICrmMonitorClerks**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)<br/>         | 使用這個介面時，可以流覽 [職員集合] 物件，以取得其在取得時的職員集合狀態相關資訊。 這項資訊包括 clerk 的數目、職員使用的 CRM 補償器 ProgID、在 CRM 補償器註冊時所提供的描述、使用 [**ICrmLogControl：： RegisterCompensator) 註冊 (使用：：**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator) 、交易工作單位識別碼和活動識別碼。 個別的 clerk 也可透過「職員實例 CLSID」來唯一識別，它不是以一般方式表示的 COM CLSID，而是唯一的 GUID，可識別此特定的職員存留期。<br/>                                                                                                                                                                                                                                                                                                |
| [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)<br/> | 這個介面可用來查詢交易的目前狀態，以找出此 CRM 員所寫入的記錄檔記錄數目，以及取得實際的記錄檔記錄資料。 記錄檔記錄是從 [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) 介面提供，其格式與最初撰寫的格式不同 (使用 [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)) 。 此外，也可以選擇性地執行 **ICrmMonitorLogRecords** ，以將記錄檔記錄轉換為可查看的格式，以便使用一般監視工具來呈現它們。<br/> 因為 [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)是直接在 crm 人員上執行，所以您可以 [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)的 [**QUERYINTERFACE**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) (也會在 crm 職員) 上執行。 然後，如果需要 ([**ICrmLogControl：： ForceTransactionToAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcetransactiontoabort)) ，就可以用它來直接中止交易。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 補償 Resource Manager 概念](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

