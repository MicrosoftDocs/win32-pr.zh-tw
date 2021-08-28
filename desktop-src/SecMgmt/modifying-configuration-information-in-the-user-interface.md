---
description: 附件嵌入式管理單元延伸模組必須允許使用者修改服務的設定資訊。
ms.assetid: fb36fcce-5a69-49cd-8cd3-b0b048f2f566
title: 修改消費者介面中的設定資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 414e2ab1475ec1c3241d60b96d182a522c299a9f5cf6134f50339c2088c99d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005116"
---
# <a name="modifying-configuration-information-in-the-user-interface"></a>修改消費者介面中的設定資訊

附件嵌入式管理單元延伸模組必須允許使用者修改服務的設定資訊。 修改過的資訊應該由附件嵌入式管理單元延伸模組儲存，直到 [安全性設定] 嵌入式管理單元呼叫 [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) 介面的方法來取得資訊為止。

若要避免記憶體流失，請呼叫 [**ISceSvcAttachmentPersistInfo：： FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer)，以釋放嵌入式管理單元擴充功能所配置的記憶體。

 

 



