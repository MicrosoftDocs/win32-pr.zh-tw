---
description: 設定程式庫應用程式
ms.assetid: db375e0f-74ca-44df-918a-b0e48742a594
title: 設定程式庫應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8ea0018d74070828384db25d76c73e7b5b3dba8a7dfc7d091c94e38aa0c3bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047496"
---
# <a name="configuring-library-applications"></a>設定程式庫應用程式

由於 COM + 程式庫應用程式是在用戶端的進程中執行，因此程式庫應用程式的可設定元素與伺服器應用程式的設定元素截然不同。 您無法設定裝載進程所決定的應用程式任何方面。

在應用層級中，程式庫應用程式可能會有數個設定受限或無法使用。 下表說明這些條件約束：



| 屬性                                       | 描述                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 安全性層級<br/>                       | 您必須選擇元件層級的存取檢查。 程式庫應用程式無法影響進程層級的存取檢查。 請參閱 [設定存取檢查的安全性層級](setting-a-security-level-for-access-checks.md)。<br/>             |
| 啟用或停用驗證<br/> | 您可以指定程式庫應用程式是否將參與主機進程所執行的驗證。 請參閱 [啟用程式庫應用程式的驗證](enabling-authentication-for-a-library-application.md)。<br/> |
| 模擬等級<br/>                  | 無法。 使用主機進程的設定。 <br/>                                                                                                                                                                             |
| 安全性身分識別<br/>                    | 無法。 應用程式會在主機進程的身分識別下執行。<br/>                                                                                                                                                          |
| 伺服器進程關機<br/>              | 無法。<br/>                                                                                                                                                                                                                       |
| 啟用 3 GB 支援<br/>                  | 無法。<br/>                                                                                                                                                                                                                       |
| 在偵錯工具中啟動<br/>                   | 無法。<br/>                                                                                                                                                                                                                       |
| 啟用 CRM<br/>                           | 無法。<br/>                                                                                                                                                                                                                       |
| 排隊<br/>                              | 無法。<br/>                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 應用程式總覽](com--application-overview.md)
</dt> </dl>

 

 




