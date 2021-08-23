---
description: NLA 用戶端可以用整個系統來記錄網路設定資訊，讓未來的查詢傳回指定的設定資訊，而不論網路是否為作用中。
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: 使用 NLA 註冊服務實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a623f28d30d02cd3a1266e173dbe28270f377a55c3f59f8ff095cf3d023a80eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641678"
---
# <a name="registering-a-service-instance-with-nla"></a>使用 NLA 註冊服務實例

NLA 用戶端可以用整個系統來記錄網路設定資訊，讓未來的查詢傳回指定的設定資訊，而不論網路是否為作用中。 這項功能可讓 NLA 用戶端影響跨多個應用程式的一致網路資訊使用者體驗。

## <a name="parameters"></a>參數

若要向網路定位知悉服務供應商註冊服務實例，請使用 [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) 函數。 為了適當地註冊服務實例，必須使用適當的資訊來設定 **WSASetService** 函式的某些參數，如本節所述。 如需快速參考， **WSASetService** 函式具有下列語法：

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

針對 *lpqsRegInfo* 參數，請提供來自 nla sp 查詢結果的 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 結構，或依照在 [查詢 NLA](querying-nla-2.md)中所指定的 nla sp 查詢需求來遵循。

*EssOperation* 參數支援的作業如下：

<dl> <dt>

<span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>RNRSERVICE \_ 註冊
</dt> <dd>

在 *lpqsRegInfo* 中提供的 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構中所定義的網路，會藉由將網路實例儲存在目前使用者的登錄區中（允許模擬），為使用中的使用者提供持續性。

</dd> <dt>

<span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE \_ 刪除
</dt> <dd>

如果 *lpqsRegInfo* 中提供的 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構中所定義的網路是永久性的，則會將它移除。

</dd> </dl>

您可以使用下列選項來修改 *essOperation* 參數中指定的作業，這些選項可以使用二進位或邏輯來指定：

<dl> <dt>

<span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>NLA \_ 易記 \_ 名稱
</dt> <dd>

搭配 RNRSERVICE REGISTER 使用時 \_ ，會檢查 *lpqsRegInfo* 中定義之網路的 *lpszComment* 欄位是否有效，並持續儲存。 搭配 RNRSERVICE DELETE 使用 \_ 和定義的網路具有易記名稱時，會移除易記名稱，但不會保留網路專案的完整名稱。

</dd> <dt>

<span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>NLA \_ ALLUSERS \_ NETWORK
</dt> <dd>

與 RNRSERVICE REGISTER 搭配使用時 \_ ，專案會持續儲存在 HKEY \_ 本機電腦下 \_ ，讓它可在本機電腦上的所有使用者進行查詢時使用。 與 RNRSERVICE DELETE 一起使用時 \_ ，會從 HKEY 本機電腦中移除指定的網路 \_ \_ 。 如果指定的網路不存在，就會傳回錯誤。 若要從目前使用者的登錄 hive 刪除網路，則不得指定此旗標。 此旗標只在本機系統管理員的安全性內容中有效。

</dd> </dl>

NLA 支援下列 [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) 函式呼叫的錯誤碼：

| 錯誤             | 意義                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED | 未執行成功呼叫 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 函式來初始化 NLA。                                                                  |
| WSAEACCESS        | NLA \_ ALLUSERS \_ NETWORK 是在 *dwControlFlags* 中指定，而不是在本機系統管理員的安全性內容中。                                                |
| WSAEALREADY       | 已依要求的方式持續儲存指定的網路，且 *dwControlFlags* 中未指定任何旗標來表示現有專案的更新。 |
| WSAEAFNOSUPPORT   | 指定的通訊協定系列不支援。 NLA 只支援 IP 通訊協定系列。                                                             |
| WSAEPFNOSUPPORT   | 指定了不支援的通訊協定。 NLA 只支援 IP 通訊協定。                                                                              |



 

 

 



