---
description: 您可以防止未經授權的使用者接收他們不應擁有存取權的事件。
ms.assetid: 59788643-f57d-458f-91ab-26552218523b
ms.tgt_platform: multiple
title: 安全地提供事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c92ed1de08dde4891365440f559544a0b26de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194144"
---
# <a name="providing-events-securely"></a>安全地提供事件

您可以防止未經授權的使用者接收他們不應擁有存取權的事件。 您的事件提供者可以提供自己事件類別的實例，就像 [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider) 提供 [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)等類別一樣。 您的事件提供者也可以傳遞內部事件，例如 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)。 如需詳細資訊，請參閱 [撰寫事件提供者](writing-an-event-provider.md)。

事件提供者可以透過下列方式控制事件收件者的存取：

-   藉由執行 [**IWbemEventProviderSecurity：： AccessCheck**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) 來使用存取控制是最有效率的方式。

    此提供者會判斷取用者是否有權接收要求的事件。 如果取用者沒有足夠的許可權可註冊，WMI 會傳回拒絕存取錯誤。 當提供者可以決定誰可以接收事件時，請使用此模式。 例如，提供者可能會提供安全性相關事件，而且可能會要求取用者具有啟用 **SeSecurityPrivilege** 許可權的系統管理員許可權。

-   在用來引發事件的接收器上執行 [**IWbemEventSink：： SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) ，可讓您在所有傳遞的事件的接收上，將安全描述項 (SD) 。

    WMI 會根據 SD 執行存取檢查。 當提供者無法決定誰可以取用其事件時，請使用此模式，但可以決定特定接收的 SD。 例如，如果您的事件提供者藉由呼叫 [**IWbemEventSink：： GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)取得數個接收器，且您想要每個接收的安全描述項，請使用 [**IWbemEventSink：： SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) 。

-   設定事件的 **安全 \_ 描述項** 屬性，可讓您設定每個事件的 SD。

    當傳遞至接收的每個事件都可以有不同的安全描述項時，請使用此方法。 若要使用此方法，請從 [**\_ \_ 事件**](--event.md)或 [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md)衍生提供者所定義的任何外建事件類別，讓您的類別包含 **安全 \_ 描述項** 屬性。 例如，您的事件提供者可能會透過接收來發行安全和一般事件。 在此情況下，請使用系統管理員帳戶安全描述項進行安全事件，並針對可供任何人接收的一般事件使用 **Null** 安全描述項。

## <a name="securing-events-by-decoupled-event-providers"></a>藉由分離事件提供者來保護事件

分離的事件提供者與 nondecoupled 事件提供者在向 WMI 註冊的方式不同。 從低耦合提供者的事件呼叫 [**IWbemEventProviderSecurity：： AccessCheck**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovidersecurity-accesscheck) 絕不會傳播用戶端存取權杖。 WMI 會以與 nondecoupled 事件提供者相同的方式來處理存取控制。 如需有關撰寫低耦合提供者的詳細資訊，請參閱 [將提供者併入應用程式](incorporating-a-provider-in-an-application.md)。

只有在 **主控台** 的 **WMI 控制** 中設定 **完整 \_ 寫入** 許可權的系統管理員，才可以引發命名空間的事件。 如需詳細資訊，請參閱 [使用 WMI 控制項設定命名空間安全性](setting-namespace-security-with-the-wmi-control.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[保護 WMI 事件](securing-wmi-events.md)
</dt> </dl>

 

 
