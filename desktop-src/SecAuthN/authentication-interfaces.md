---
description: 列出驗證 Api 中的介面。
ms.assetid: bde3bcae-2152-4589-92a0-b44d98f233ef
title: 驗證介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b101fd4fdd3c518d24b5b6f798fcaa4e0327dd22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193288"
---
# <a name="authentication-interfaces"></a>驗證介面

驗證介面會根據使用方式進行分類，如下所示：

-   [智慧卡介面](#smart-card-interfaces)
-   [身分識別共用介面](#identity-sharing-interfaces)

## <a name="smart-card-interfaces"></a>智慧卡介面

智慧卡 SDK 提供下列 COM 介面。 特定介面的方法會列在 [目錄] 和該介面的 [參考] 頁面上。



| 介面                                    | 描述                                                                                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IByteBuffer**](ibytebuffer.md)           | 管理資料流程物件。                                                                                                                                                                 |
| [**ISCard**](iscard.md)                     | 開啟並管理與 [*智慧卡*](/windows/desktop/SecGloss/s-gly)的連接。                                                                    |
| [**ISCardAuth**](iscardauth.md)             | 驗證應用程式、智慧卡或使用者。                                                                                                                                       |
| [**ISCardCmd**](iscardcmd.md)               |  (APDU) 來建立和管理智慧卡 [*應用程式協定資料單位*](/windows/desktop/SecGloss/a-gly) 。 |
| [**ISCardDatabase**](iscarddatabase.md)     | 執行智慧卡 [*資源管理員*](/windows/desktop/SecGloss/r-gly) 資料庫作業。                                              |
| [**ISCardFileAccess**](iscardfileaccess.md) | 執行常見的檔案服務，例如尋找、選取、讀取、寫入、建立和刪除檔案。                                                                               |
| [**ISCardISO7816**](iscardiso7816.md)       | 構造 APDU 命令。                                                                                                                                                              |
| [**ISCardLocate**](iscardlocate.md)         | 尋找智慧卡。                                                                                                                                                                    |
| [**ISCardManage**](iscardmanage.md)         | 管理智慧卡系統。                                                                                                                                                           |
| [**ISCardTypeConv**](iscardtypeconv.md)     | 提供用來支援其他智慧卡 COM 介面的方法。 這個介面僅提供回溯相容性，不應再使用。                               |
| [**ISCardVerify**](iscardverify.md)         | 驗證或變更信用卡持有者驗證 (CHV) 原則。                                                                                                                               |



 

## <a name="identity-sharing-interfaces"></a>身分識別共用介面

身分識別共用 SDK 提供下列 COM 介面。 特定介面的方法會列在 [目錄] 和該介面的 [參考] 頁面上。



| 介面                                                          | 描述                                                                              |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**IAssociatedIdentityProvider**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iassociatedidentityprovider) | 允許身分識別提供者將身分識別與本機使用者帳戶建立關聯。            |
| [**IIdentityAdvise**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iidentityadvise)                         | 允許身分識別提供者在更新身分識別時通知呼叫的應用程式。 |
| [**IIdentityProvider**](/windows/desktop/api/Identityprovider/nn-identityprovider-iidentityprovider)                     | 代表身分識別提供者。                                                         |
| [**IIdentityStore**](/windows/desktop/api/Identitystore/nn-identitystore-iidentitystore)                           | 提供列舉和管理身分識別和身分識別提供者的方法。              |



 

 

 
