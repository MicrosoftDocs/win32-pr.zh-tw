---
description: COM + CRM 啟動和復原
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: COM + CRM 啟動和復原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a0e631e2e5ecef1621705c9af74aa48898d733b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981128"
---
# <a name="com-crm-startup-and-recovery"></a>COM + CRM 啟動和復原

如果伺服器應用程式已使用 [元件服務] 系統管理工具 (選取 [ **啟用補償資源管理員** ] 核取方塊，則在 com + 應用程式的 [屬性] 頁面的 [ **Advanced** ] 索引標籤上) ，第一次啟動時，它會建立 CRM 記錄檔，供該伺服器應用程式進程中的所有 crm 使用。  (如需設定 CRM 的詳細指示，請參閱設定 [COM + CRM 元件](configuring-com--crm-components.md)。 ) 

針對伺服器應用程式所建立的 CRM 記錄檔名稱是以伺服器應用程式的 GUID)  (為基礎，而且 CRM 記錄檔會放在與 DTC 記錄檔相同的目錄中， (通常是% SystemRoot% \\ winnt \\ system32 \\ DtcLog 目錄) 。 CRM 記錄檔的副檔名為 crmlog。

> [!Note]  
> 基於效能考慮，可能需要變更 CRM 記錄檔的預設位置， (使 DTC 記錄檔位於與 CRM 記錄檔不同的磁片上) 或可能是因為在叢集環境中使用 CRM。 您可以使用 COM + 系統管理 SDK 變更 CRM 記錄檔的位置。 屬性名稱是 CRMLogFile，而且存在於 [**應用程式**](applications.md) 集合物件上。

 

當啟用 CRM 的伺服器應用程式 () 啟動，併發現該伺服器應用程式已經有 CRM 記錄檔，它會在該 CRM 記錄檔上執行復原。 復原 *是完成* 失敗的任何交易的程式，其中牽涉到 crm 基礎結構讀取 crm 記錄檔，以找出任何未完全完成的交易。 如果找到任何，則會聯繫 DTC 以判斷交易結果。 然後，它會建立 CRM 補償器，並視需要將認可或中止通知連同相關聯的記錄檔記錄一起傳遞。

在復原期間，CRM 補償器不會收到準備通知。 CRM 補償器具有旗標，可區別是否在正常作業期間或復原期間呼叫它。

復原通常只會在伺服器應用程式因伺服器應用程式進程損毀或電腦損毀而異常關閉時，才會尋找未完成的交易。 如果允許伺服器應用程式正常關機，因為閒置超時或透過 [元件服務] 系統管理工具手動關機，則記錄檔將會是乾淨的。

開始進行復原的 CRM 伺服器應用程式不會自動啟動。 必須採取一些外部動作，才能啟動需要復原的 CRM 伺服器應用程式。 通常這會在該伺服器應用程式中建立元件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 補償 Resource Manager 概念](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[COM + CRM 操作進程](com--crm-operating-process.md)
</dt> </dl>

 

 



