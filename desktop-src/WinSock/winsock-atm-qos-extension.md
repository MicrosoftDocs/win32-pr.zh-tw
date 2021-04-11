---
description: 本節說明適用于 ATM 的通訊協定特定服務品質 (QOS) 結構，此結構包含在 QOS 結構的 ProviderSpecific 欄位中。
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Winsock ATM QoS 擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075c9dcbd8b9148f41d39c99e2118ed638a577ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112989"
---
# <a name="winsock-atm-qos-extension"></a><span data-ttu-id="1009f-103">Winsock ATM QoS 擴充功能</span><span class="sxs-lookup"><span data-stu-id="1009f-103">Winsock ATM QoS Extension</span></span>

<span data-ttu-id="1009f-104">本節說明適用于 ATM 的通訊協定特定服務品質 ([**qos**](/windows/win32/api/winsock2/ns-winsock2-qos)) 結構，此結構包含在 **QOS** 結構的 [ProviderSpecific](/previous-versions/aa374467(v=vs.80))欄位中。</span><span class="sxs-lookup"><span data-stu-id="1009f-104">This section describes the protocol-specific Quality of Service ([**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)) structure for ATM, which is contained in the [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) field of the **QOS** structure.</span></span> <span data-ttu-id="1009f-105">請注意，使用此 ATM 專屬的 **QOS** 結構是 Windows 通訊端2用戶端的選用專案，而且必須要有 atm 服務提供者，才能將泛型 [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) 結構對應到適當的 Q. 2931 資訊元素。</span><span class="sxs-lookup"><span data-stu-id="1009f-105">Note that the use of this ATM-specific **QOS** structure is optional by Windows Sockets 2 clients, and the ATM service provider is required to map the generic [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) structure to appropriate Q.2931 information elements.</span></span> <span data-ttu-id="1009f-106">但是，如果同時指定了泛型 **FLOWSPEC** 結構和 atm 專屬的 **qos** 結構，則在有任何衝突時，ATM 特定 **qos** 結構中指定的值應該會優先。</span><span class="sxs-lookup"><span data-stu-id="1009f-106">However, if both the generic **FLOWSPEC** structure and ATM-specific **QOS** structure are specified, the value specified in the ATM-specific **QOS** structure should take precedence should there be any conflicts.</span></span> <span data-ttu-id="1009f-107">如需 QoS 布建和 **FLOWSPEC** 結構的詳細資訊，請參閱 Windows 通訊端 2 API 規格一節2.7。</span><span class="sxs-lookup"><span data-stu-id="1009f-107">See Windows Sockets 2 API Specification Section 2.7 for more information about QoS provisions and **FLOWSPEC** structure.</span></span>

<span data-ttu-id="1009f-108">適用于 ATM 的通訊協定特定 [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) 結構是 2931 information 元素的串連， (IE) 結構，這些是在下列文字中定義的。</span><span class="sxs-lookup"><span data-stu-id="1009f-108">The protocol-specific [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) structure for ATM is a concatenation of Q.2931 information element (IE) structures, which are defined in the following text.</span></span> <span data-ttu-id="1009f-109">如果應用程式略過採用了3.x 的 IE，服務提供者應該插入合理的預設值，將 [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) 結構中的資訊納入考慮（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="1009f-109">If an application omits an IE that UNI 3.x mandates, the service provider should insert a reasonable default value, taking the information in the [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) structure into account if applicable.</span></span>

<span data-ttu-id="1009f-110">重複執行的處理取決於 IE 本身。</span><span class="sxs-lookup"><span data-stu-id="1009f-110">The handling of repeated IEs is dependent on the IE itself.</span></span> <span data-ttu-id="1009f-111">如果 IE 重複，且每個 ATM 論壇單向規格都可以重複，則提供者必須正確處理。</span><span class="sxs-lookup"><span data-stu-id="1009f-111">If an IE is repeated and it is one that is allowed to be repeated per the ATM Forum UNI specification then the provider must handle it properly.</span></span> <span data-ttu-id="1009f-112">在此情況下，清單中的順序會決定喜好設定順序，而較早出現在清單中的專案則更慣用。</span><span class="sxs-lookup"><span data-stu-id="1009f-112">In this case, order in the list determines preference order, with elements appearing earlier in the list being more preferred.</span></span> <span data-ttu-id="1009f-113">如果有重複的 IE，且每個 ATM 論壇單向規格不允許這種情況，則提供者可能會將要求從用戶端失敗 (慣用的選項) 或使用所找到該類型的最後一個 IE。</span><span class="sxs-lookup"><span data-stu-id="1009f-113">If an IE is repeated and this is not allowed per ATM Forum UNI specification, the provider may either fail the request from the client (the preferred option) or use the last IE of that type found.</span></span>

<span data-ttu-id="1009f-114">每個個別的 IE 結構都會以下列方式格式化，並由 **IEType** 欄位識別：</span><span class="sxs-lookup"><span data-stu-id="1009f-114">Each individual IE structure is formatted in the following manner and identified by the **IEType** field:</span></span>

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

<span data-ttu-id="1009f-115">**IEType** 欄位的合法值定義為：</span><span class="sxs-lookup"><span data-stu-id="1009f-115">Legal values for the **IEType** field are defined as:</span></span>

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

<span data-ttu-id="1009f-116">**Ie** 欄位會由特定的 ie 結構重迭，而 **IELength** 欄位則是 IE 結構的總長度（以位元組為單位），包括 **IEType** 和 **IELength** 欄位。</span><span class="sxs-lookup"><span data-stu-id="1009f-116">The **IE** field is overlaid by a specific IE structure and the **IELength** field is the total length in bytes of the IE structure including the **IEType** and **IELength** fields.</span></span> <span data-ttu-id="1009f-117">這些 IE 結構的每個專案的語義和合法值都是依 ATM 的3.x 規格。</span><span class="sxs-lookup"><span data-stu-id="1009f-117">The semantics and legal values for each element of these IE structures are per ATM UNI 3.x specification.</span></span> <span data-ttu-id="1009f-118">SAP \_ 欄位 \_ 不存在可用於特定的 IE 結構（每個 ATM 的3.x 規格）中的選擇性元素。</span><span class="sxs-lookup"><span data-stu-id="1009f-118">SAP\_FIELD\_ABSENT can be used for those elements that are optional for a given IE structure, per ATM UNI 3.x specification.</span></span>

 

 
