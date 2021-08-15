---
title: 在電腦物件下發布
description: 一般而言，主機型服務會在主機電腦的電腦物件底下建立 Scp。 以主機為基礎的服務是與單一主機電腦緊密系結的服務。
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aac659ab2bf482ee6d6c57dd1481e487d6e2af95dfd85a092f48f4928499b102
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025356"
---
# <a name="publishing-under-a-computer-object"></a>在電腦物件下發布

一般而言，主機型服務會在主機電腦的電腦物件底下建立 Scp。 以主機為基礎的服務是與單一主機電腦緊密系結的服務。

**若要在電腦物件下建立 Scp**

1.  呼叫 [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) 函式，以取得本機電腦之電腦物件目錄中 (DN) 的分辨名稱。
2.  使用該 DN 系結至電腦物件，並建立 SCP。

如需詳細資訊和程式碼範例，請參閱 [用戶端如何尋找和使用服務連接點](how-clients-find-and-use-a-service-connection-point.md)。

請注意，只有網域成員電腦在目錄中具有有效的電腦物件。

若要取得本機電腦的 DNS 或 NetBIOS 名稱，請呼叫 [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) 函數。

 

 