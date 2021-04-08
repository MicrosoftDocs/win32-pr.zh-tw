---
description: 需要 CRM 介面，才能為使用 Visual Basic 和 Visual C++ 開發的 CRM 工作者和 CRM Compensators 提供支援。
ms.assetid: 68a75da7-1f35-41a4-8872-e3f4ad1fc30d
title: COM + CRM 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ba3235b1cd2a82fc913dd676bbb78324f340cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689180"
---
# <a name="com-crm-interfaces"></a>COM + CRM 介面

需要 CRM 介面，才能為使用 Visual Basic 和 Visual C++ 開發的 CRM 工作者和 CRM Compensators 提供支援。

您可以使用 COM + 補償 Resource Manager (CRM) 快速輕鬆地整合應用程式資源與 Microsoft Distributed Transaction Coordinator (DTC) 交易。

使用 Visual Basic 撰寫的元件更容易將記錄檔記錄建立為變數集合。 此外，Visual Basic 元件是以執行緒為單位，這表示必須能夠將多執行緒單元的介面封送處理至單一執行緒的單元。 使用 Visual C++ 開發的 CRM 元件也可以使用單元執行緒模型，不過建議您改為使用這兩個執行緒模型。

下表所述的介面提供 COM + Crm 開發人員的詳細參考資訊。



| CRM 介面                                             | Description                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator)                 | 此介面會在 Visual C++ 中傳遞非結構化記錄。                                                           |
| [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) | 使用 Visual Basic 時，這個介面會將結構化記錄檔記錄傳遞給 CRM 補償器。                            |
| [**ICrmFormatLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmformatlogrecords)       | 這個介面會將記錄檔記錄轉換成可看見的格式，讓它們可以使用一般監視工具來呈現。 |
| [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)                   | CRM 工作者和 CRM 補償器會使用這個介面將記錄寫入記錄檔，並使其成為持久的。           |
| [**ICrmMonitor**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)                         | 此介面會捕獲 CRM 目前狀態的快照集，並保留特定的 CRM 職員。                          |
| [**ICrmMonitorClerks**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)             | 此介面會取得 clerk 狀態的相關資訊。                                                             |
| [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)     | 此介面會監視特定 CRM 職員針對指定交易所維護的個別記錄檔記錄。            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 補償 Resource Manager 概念](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



