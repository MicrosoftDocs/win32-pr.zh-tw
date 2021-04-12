---
title: 物件模型階層
description: '[SDO] 物件模型中的物件會排列在階層中。 這表示 SDO 中的物件可讓您存取 SDO 中的其他物件。'
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2484b4d7402f8a5b43a590651f36d4d1707bca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375876"
---
# <a name="object-model-hierarchy"></a>物件模型階層

[SDO] 物件模型中的物件會排列在階層中。 這表示 SDO 中的物件可讓您存取 SDO 中的其他物件。

物件可讓您以兩種方式存取其他物件。 其中一個方法是讓物件公開介面，以提供方法來取得其他物件。 這種方法的範例是 Machine 物件。 Machine 物件會公開 [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) 介面。 [**ISdoMachine：： GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo)方法會捕獲服務物件。 [**ISdoMachine：： GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo)方法會捕獲使用者物件。

![公開 isdomachine 介面的電腦物件](images/sdo01.png)

如需詳細資訊，請參閱 [取得服務和使用者 SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos)。

物件提供其他物件之存取權的第二種方式，是將物件集合表示為包含該物件的物件屬性。 若要取出物件集合，請在代表集合之物件的屬性上呼叫 [**ISdo：： GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) 。 例如，若要取出原則集合，請在 NPS 物件所公開的 [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo)介面上呼叫 **ISdo：： GetProperty** 。

> [!Note]  
> 從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。

 

![正在抓取原則集合](images/sdo02.png)

如需抓取原則集合的範例程式碼，請參閱抓取 [集合](/windows/desktop/Nps/sdo-retrieving-a-collection)。

[**NPS 伺服器資料物件**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)具有代表集合的下列屬性：

<dl> <dt>

<span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>核 數 師
</dt> <dd>

審計員集合中唯一的審計員是 [**NT 事件記錄**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties)檔。

</dd> <dt>

<span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>政策
</dt> <dd>

每個 [**原則物件**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) 都有一個代表條件集合的屬性。

</dd> <dt>

<span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>配置 檔
</dt> <dd>

設定檔集合中的每個 [**設定檔物件**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) 都有一個代表屬性集合的屬性。 請參閱 [Sdo 支援的屬性](/windows/desktop/Nps/sdo-sdo-supported-attributes) ，以取得 sdo 所支援的屬性清單。

</dd> <dt>

<span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>協定
</dt> <dd>

通訊協定集合包含 RADIUS 通訊協定物件，其中包含代表 RADIUS 用戶端的用戶端集合。 請參閱 [加入用戶端](/windows/desktop/Nps/sdo-adding-a-client) 以取得範例程式碼，以示範如何取出用戶端集合。

</dd> <dt>

<span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Proxy 原則
</dt> <dd>

此集合包含用於連接要求處理的網路存取原則。

</dd> <dt>

<span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Proxy 設定檔
</dt> <dd>

這個集合包含用於連接要求處理的設定檔。

</dd> <dt>

<span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>RADIUS 伺服器群組
</dt> <dd>

RADIUS 伺服器群組集合中的每個 [**radius 伺服器群組**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) 都有一個屬性，代表該伺服器群組中的伺服器集合。

</dd> <dt>

<span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>要求處理常式
</dt> <dd>

此集合包含「Microsoft 領域評估工具」集合。 您也可以在此集合中取得「Microsoft NT SAM 驗證」和「Microsoft 帳戶處理」設定。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[SDO 物件和屬性](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[SDO 支援的屬性](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 