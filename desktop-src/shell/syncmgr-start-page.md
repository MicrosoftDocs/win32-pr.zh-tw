---
description: 同步處理管理員提供集中式的標準技術，可在行動電腦或連接到區域網路的電腦上同步處理檔案，以供離線使用。
title: 同步處理管理員
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6cdac7e5-8985-407a-98bb-936bb20ed069
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbOrient
ms.openlocfilehash: 2fc56b2afec4fdedf98fe213437a27f2592ce72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991615"
---
# <a name="synchronization-manager"></a>同步處理管理員

## <a name="purpose"></a>目的

同步處理管理員提供集中式的標準技術，可在行動電腦或連接到區域網路的電腦上同步處理檔案，以供離線使用。 與連線功能、通知 (系統事件通知服務) 和用戶端快取，同步處理管理員會提供基礎結構來支援行動計算。 作業系統會提供所有應用程式可使用的整合式模型，而不是每個應用程式執行自己的技術來快取和同步處理網路資源以供本機使用。 與通訊協定無關的檔案會進行同步處理。 例如，電子郵件程式可以使用 SMTP、NMTP 或 POP3 傳送訊息，而瀏覽器可以使用 HTTP，而資料庫可以使用遠端程序呼叫， (RPC)  (RPC) 。 開發人員可以在其應用程式中使用同步處理管理員的通用介面，在使用者的本機電腦和網路存放裝置之間同步處理檔案。

## <a name="where-applicable"></a>適用時

同步處理管理員適用于主要在行動電腦上執行的應用程式。 在連接到高延遲區域網路的電腦上執行的應用程式，也可能會因為使用同步處理管理員而受益。

## <a name="developer-audience"></a>開發人員對象

本檔適用于開發行動電腦運算和高延遲區域網路應用程式的軟體發展人員。 本檔提供同步處理管理員所有部分的完整參考，包括同步處理管理員的方法和介面。

## <a name="run-time-requirements"></a>執行階段需求求

需要 Windows Server 2003、Windows XP、Windows 2000 或 Windows Millennium Edition (Windows Me) 。 也可用於 Microsoft Windows NT 4.0、Windows 98 和 Windows 95 的可轉散發套件。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                       | 描述                                                                                                                                         |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於同步處理管理員](syncmgr-about.md)<br/>                               | 同步處理管理員提供集中式的標準技術，可同步處理檔案以在本機電腦上離線使用。<br/>     |
| [行動計算設定](syncmgr-mobile-computing-configs.md)<br/>          | 應用程式可以使用同步處理管理員，讓檔案和資源在本機快取，並在行動和桌上型電腦上同步處理。<br/> |
| [應用程式案例](syncmgr-app-scenarios.md)<br/>                               | 可以使用同步處理管理員的應用程式和服務。<br/>                                                                          |
| [同步處理管理員架構](syncmgr-architecture.md)<br/>                 |                                                                                                                                                     |
| [從程式使用同步處理管理員](syncmgr-using-from-a-program.md)<br/> |                                                                                                                                                     |
| [同步處理管理員參考](syncmgr-reference.md)<br/>                       | 下列程式設計項目組成同步處理管理員的 API。<br/>                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於系統事件通知服務](../sens/about-system-event-notification-service.md)
</dt> </dl>

 

 
