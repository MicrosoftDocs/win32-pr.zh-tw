---
description: 說明建立憑證所需的呼叫。
ms.assetid: 74154b3b-75fc-412f-835c-1a6f54e688c6
title: 建立憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f237fd729499aa5153f12f68657e2ce227da7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852683"
---
# <a name="building-a-certificate"></a>建立憑證

建立憑證的呼叫順序如下所示：

1.  [*憑證授權單位*](../secgloss/c-gly.md) 單位 (CA) 透過對 [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) 和 [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) 的呼叫來初始化模組， (會在伺服器初始化) 上進行一次。 CA 會藉由呼叫 [**ICertPolicy2：： initialize**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-initialize) 和 [**ICertExit：： initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize)來初始化原則和結束模組。
2.  中繼會透過 [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) 呼叫 CA， (每個中繼初始化) 都會發生一次。 媒介會藉由呼叫 [**ICertConfig：： GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig)來尋找所需的設定字串。
3.  用戶端會透過每個要求) ，在中繼 (特定的介面中呼叫中繼。 用戶端會將 [*憑證要求*](../secgloss/c-gly.md) 傳送給媒介。 例如，Microsoft Internet Explorer 透過 [憑證註冊控制項](certificate-enrollment-control.md) 將要求傳送至 Microsoft Internet Information Services。
4.  透過 [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) (的中繼至 CA 會在每個要求) 發生一次。 媒介會透過 [**ICertRequest：： Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit)將憑證要求傳送給 CA。 在 Internet Information Services 的案例中，這可以透過使用中的伺服器頁面腳本來完成。
5.  CA 會透過 [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) 介面呼叫原則模組， (會在每個要求) 發生一次。 CA 會呼叫 [**ICertPolicy：： verifyrequest 已**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest)，以通知原則模組要求已到達。 原則模組可以藉由呼叫 [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) 介面的方法，檢查要求並變更憑證。 然後，原則模組可以指出要求是正常的 (如果是，就會在此時建立憑證) 、要求遭到拒絕，或是應該暫停要求。
6.   (選擇性的) 系統管理員透過 [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) 介面呼叫 CA。 如果要求已暫停，系統管理員可以重新提交或拒絕要求，或修改要求屬性和延伸模組。 請注意，如果重新提交要求，原則模組將會有另一個機會處理要求 (，因為呼叫 [**ICertPolicy：： verifyrequest 已**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest)) 。 重新提交或拒絕要求的工作可以透過「憑證授權單位單位」 MMC 嵌入式管理單元，或使用 **ICertAdmin** 的另一個應用程式來執行。
7.  CA 會透過 [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) 介面呼叫 exit 模組。 如果結束模組在呼叫 [**ICertExit：： Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) 時指出 (，請在步驟 1) 有興趣查看所發出的憑證或擱置擱置的要求，CA 將會呼叫 [**ICertExit：： Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify)。
8.  Exit 模組會透過 [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) 介面呼叫 CA。 結束模組可以藉由呼叫 **ICertServerExit** 的方法，檢查要求和新的憑證。

 

 
