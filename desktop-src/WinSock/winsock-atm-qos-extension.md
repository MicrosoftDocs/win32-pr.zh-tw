---
description: 本節說明適用于 ATM 的通訊協定特定服務品質 (QOS) 結構，此結構包含在 QOS 結構的 ProviderSpecific 欄位中。
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Winsock ATM QoS 擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422db2df8e4f845086120814f6cf4e6288dcc00c42693eac8da21c466448aaa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612818"
---
# <a name="winsock-atm-qos-extension"></a>Winsock ATM QoS 擴充功能

本節說明適用于 ATM 的通訊協定特定服務品質 ([**qos**](/windows/win32/api/winsock2/ns-winsock2-qos)) 結構，此結構包含在 **QOS** 結構的 [ProviderSpecific](/previous-versions/aa374467(v=vs.80))欄位中。 請注意，Windows 通訊端2用戶端可以選擇性地使用這個 atm 專屬的 **QOS** 結構，而 ATM 服務提供者則需要將泛型 [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec)結構對應到適當的2931資訊元素。 但是，如果同時指定了泛型 **FLOWSPEC** 結構和 atm 專屬的 **qos** 結構，則在有任何衝突時，ATM 特定 **qos** 結構中指定的值應該會優先。 如需 QoS 布建和 **FLOWSPEC** 結構的詳細資訊，請參閱 Windows 通訊端 2 API 規格一節2.7。

適用于 ATM 的通訊協定特定 [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) 結構是 2931 information 元素的串連， (IE) 結構，這些是在下列文字中定義的。 如果應用程式略過採用了3.x 的 IE，服務提供者應該插入合理的預設值，將 [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) 結構中的資訊納入考慮（如果適用）。

重複執行的處理取決於 IE 本身。 如果 IE 重複，且每個 ATM 論壇單向規格都可以重複，則提供者必須正確處理。 在此情況下，清單中的順序會決定喜好設定順序，而較早出現在清單中的專案則更慣用。 如果有重複的 IE，且每個 ATM 論壇單向規格不允許這種情況，則提供者可能會將要求從用戶端失敗 (慣用的選項) 或使用所找到該類型的最後一個 IE。

每個個別的 IE 結構都會以下列方式格式化，並由 **IEType** 欄位識別：

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

**IEType** 欄位的合法值定義為：

``` syntax
typedef enum {
    IE_AALParameters,
    IE_TrafficDescriptor,
    IE_BroadbandBearerCapability,
    IE_BHLI,
    IE_BLLI,
    IE_CalledPartyNumber,
    IE_CalledPartySubaddress,
    IE_CallingPartyNumber,
    IE_CallingPartySubaddress,
    IE_Cause,
    IE_QOSClass,
    IE_TransitNetworkSelection,
} Q2931_IE_TYPE;
```

**Ie** 欄位會由特定的 ie 結構重迭，而 **IELength** 欄位則是 IE 結構的總長度（以位元組為單位），包括 **IEType** 和 **IELength** 欄位。 這些 IE 結構的每個專案的語義和合法值都是依 ATM 的3.x 規格。 SAP \_ 欄位 \_ 不存在可用於特定的 IE 結構（每個 ATM 的3.x 規格）中的選擇性元素。

 

 
