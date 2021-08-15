---
title: ADSI 服務提供者
description: 本主題概述伺服器中所提供的 ADSI 服務提供者。
ms.assetid: 419d7953-a879-4d6c-be74-173d76c3f932
ms.tgt_platform: multiple
keywords:
- ADSI ADSI、服務提供者
- 服務提供者 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66b90aad4e9fa1a6cf6a2229910257f018a411aa7b11b9accca6fcf96dce39b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962196"
---
# <a name="adsi-service-providers"></a>ADSI 服務提供者

ADSI 包含下表列出的服務提供者。



| 服務提供者 | 描述                                                                                | 取得詳細資訊                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| LDAP<br/>  | 與輕量型目錄存取協定相容的命名空間執行。<br/> | [ADSI LDAP 提供者](adsi-ldap-provider.md)<br/>   |
| WinNT<br/> | 命名空間的執行與 Windows 相容。<br/>                               | [ADSI WinNT 提供者](adsi-winnt-provider.md)<br/> |



 

其他服務提供者包含在 ADSI 以外的產品中。 以下是 Microsoft 所實行的 ADSI 服務提供者。



| 服務提供者 | 取得詳細資訊                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| IIS<br/>   | [IIS ADSI 提供者架構](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))<br/> |



 

並非每個服務提供者都支援 ADSI 介面所公開的方法與屬性方法。 由於不同的目錄服務會因儲存的物件和屬性類型而異，因此請使用不同的通訊協定和驗證，ADSI 是設計來與支援的服務提供者順暢地搭配運作。 因此，有一些介面、方法和屬性方法適用于一個服務提供者，例如 LDAP，可能無法在另一個上運作，例如 WinNT。

本節包含提供者特定的資訊，例如 ADsPath 格式、用於該服務提供者的 ADSI 物件清單，以及 ADSI 中所含服務提供者的資料類型和語法資訊。 此外，ADSI 中包含的每個提供者都支援 ADSI 介面的摘要描述。

在 ADSI 中，不同的提供者會與不同的 Dll 相關聯。 LDAP 提供者與 Adsldp.dll、Adsldpc.dll 和 Adsmsext.dll 相關聯。 WinNT 提供者與 Adsnt.dll 相關聯。 路由器提供者與 Activeds.dll 相關聯。

> [!Note]  
> 請勿假設預設的 ADSI 提供者為安全線程。 多執行緒應用程式開發人員應該透過適當的同步處理物件（例如，信號、mutex、重要區段等等）來協調執行緒之間的存取。

 

如需 ADSI 服務提供者的詳細資訊，請參閱 adsi [路由器](adsi-router.md) 和 [Adsi 介面的提供者支援](provider-support-of-adsi-interfaces.md)。

 

