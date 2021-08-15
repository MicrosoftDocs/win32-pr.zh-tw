---
title: 安全性處理結果
description: 在安全通道上，只有成功通過安全性檢查的訊息會傳遞至應用程式。
ms.assetid: 891e1f91-406e-4997-9da6-59b5fe578d0d
keywords:
- Windows 的安全性處理結果 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53009729b3d7f1c8ff6b9e38a054d8dbadf202b7a0caa4a92c7861232c8390a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962927"
---
# <a name="security-processing-results"></a>安全性處理結果

在安全通道上，只有成功通過安全性檢查的訊息會傳遞至應用程式。 針對這些訊息，安全性驗證的一些結果會以訊息屬性的形式附加，而應用程式可能會解壓縮並檢查這些屬性，以執行其他步驟，例如授權檢查。


函數 [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) 可用來取出 [**WS \_ MESSAGE \_ PROPERTY \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)中定義的任何安全性相關屬性。 如果查詢要求的安全性屬性不適用於通道上使用的安全性類型， **WsGetMessageProperty** 會傳回錯誤。 訊息會繼續擁有查詢函數所傳回的屬性。

下列 API 元素用於安全性處理結果。

| 列舉型別                                                                | 描述                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**WS \_ 安全性 \_ 權杖 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_property_id) | 定義可以從安全性權杖解壓縮之欄位和屬性的索引鍵。 |



 



| 函式                                                         | 描述                                           |
|------------------------------------------------------------------|-------------------------------------------------------|
| [**WsGetSecurityTokenProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritytokenproperty) | 從安全性權杖中解壓縮欄位或屬性。 |



 



| Handle                                       | Description                                     |
|----------------------------------------------|-------------------------------------------------|
| [WS \_ 安全性 \_ 權杖](ws-security-token.md) | 代表安全性權杖的不透明控制碼。 |



 

 

 




