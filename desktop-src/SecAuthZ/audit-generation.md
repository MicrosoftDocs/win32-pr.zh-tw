---
description: C2 層級安全性需求指定系統管理員必須能夠審核安全性相關事件，而且此審核資料的存取權必須限制為授權的系統管理員。
ms.assetid: 411001b1-94cd-465f-8558-c8aa119e4303
title: 稽核產生
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d00be8b6d94b29a42436fdabc63be8d2c05789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990447"
---
# <a name="audit-generation"></a>稽核產生

C2 層級安全性需求指定系統管理員必須能夠審核安全性相關事件，而且此審核資料的存取權必須限制為授權的系統管理員。 Windows API 提供的功能可讓系統管理員監視安全性相關事件。

安全物件的安全描述項可以有 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) 。 SACL 包含 (Ace) 的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) ，可指定產生審核報告的存取嘗試類型。 每個 ACE 都會識別信任者、一組存取權限，以及一組旗標，指出系統是否針對失敗的存取嘗試、成功的存取嘗試，或兩者都產生審核訊息。

系統會將 audit 訊息寫入安全性事件記錄檔。 如需存取安全性事件記錄檔中記錄的詳細資訊，請參閱 [事件記錄](/windows/desktop/EventLog/event-logging)。

若要讀取或寫入物件的 SACL，執行緒必須先啟用「SE \_ 安全性 \_ 名稱」許可權。 如需詳細資訊，請參閱 [SACL 訪問](sacl-access-right.md)許可權。

當用戶端嘗試存取私用物件時，Windows API 也會提供伺服器應用程式的支援，以產生審核訊息。 如需詳細資訊，請參閱 [審核私用物件的存取權](auditing-access-to-private-objects.md)。

 

 
