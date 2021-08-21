---
title: Active Directory 網域服務
description: microsoft Active Directory Domain Services 是建置於 Windows 2000 Server、Windows Server 2003 和 microsoft Windows Server 2008 使用網域控制站之作業系統的分散式網路基礎。
ms.assetid: 9fc78c72-c59c-4c4d-ace5-00a431645c4b
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory
- Active Directory Active Directory、起始頁
- Active Directory Domain Services Active Directory、起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54fd3814767d47124cec8c824c5de948061cc744d4105a598de98f78f970003e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118025245"
---
# <a name="active-directory-domain-services"></a>Active Directory Domain Services

## <a name="purpose"></a>目的

microsoft Active Directory Domain Services 是建置於 Windows 2000 Server、Windows Server 2003 和 microsoft Windows Server 2008 使用網域控制站之作業系統的分散式網路基礎。 Active Directory Domain Services 針對網路中的物件（例如使用者、電腦、印表機和服務），提供安全、結構化、階層式的資料存放區。 Active Directory Domain Services 提供尋找和使用這些物件的支援。

本指南概述基本工作的 Active Directory Domain Services 和範例程式碼，例如搜尋物件和讀取屬性，到更先進的工作，例如服務發行。

Windows 2000 伺服器和更新版本的作業系統提供使用者介面，讓使用者和系統管理員可以使用 Active Directory Domain Services 中的物件和資料。 本指南說明如何擴充和自訂該使用者介面。 它也會描述如何藉由定義新的物件類別和屬性來擴充 Active Directory Domain Services。

> [!Note]  
> 下列檔適用于電腦程式設計人員。 如果您是嘗試偵測列印錯誤或家用網路問題的使用者，請參閱 [Microsoft 社區論壇](https://answers.microsoft.com)。

 

## <a name="where-applicable"></a>適用時

網路系統管理員撰寫可存取 Active Directory Domain Services 的腳本和應用程式，以自動化一般管理工作，例如新增使用者和群組、管理印表機，以及設定網路資源的許可權。

獨立軟體廠商和使用者開發人員可以使用 Active Directory Domain Services 程式設計，以目錄啟用其產品和應用程式。 服務可以在 Active Directory Domain Services 中自行發佈;用戶端可以使用 Active Directory Domain Services 來尋找服務，而且兩者都可以使用 Active Directory Domain Services 來找出並使用網路上的其他物件。

## <a name="developer-audience"></a>開發人員對象

存取 Active Directory Domain Services 中資料的應用程式可以使用 [Active Directory 服務介面](../adsi/active-directory-service-interfaces-adsi.md) Api、 [輕量型目錄存取協定](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) api 或 [DirectoryServices](/dotnet/api/system.directoryservices) 命名空間來撰寫。

## <a name="run-time-requirements"></a>執行階段需求求

Active Directory Domain Services 在 Windows 2000 和更新版本的網域控制站上執行。 不過，您可以撰寫用戶端應用程式，並在 Windows Vista、Windows Server 2003、Windows XP、Windows 2000、Windows NT 4.0、Windows 98 和 Windows 95 上執行。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[關於 Active Directory Domain Services](about-active-directory-domain-services.md)
</dt> <dd>

Active Directory Domain Services 的一般資訊。

</dd> <dt>

[使用 Active Directory 網域服務](using-active-directory-domain-services.md)
</dt> <dd>

Active Directory Domain Services 程式設計指南。

</dd> <dt>

[Active Directory Domain Services 參考](active-directory-domain-services-reference.md)
</dt> <dd>

Active Directory Domain Services 程式設計參考。

</dd> </dl>

 

 