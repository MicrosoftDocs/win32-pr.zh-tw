---
title: 中繼資料匯入
description: WWSAPI 包含的 API 元素可用來處理端點的 WSDL 和原則，其目標為解壓縮可用於與端點通訊的資訊。
ms.assetid: 77738bf1-ef8b-4fd6-a36a-43f1932868dd
keywords:
- 適用于 Windows 的中繼資料匯入 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c36ffdf9bcbf0d63bdef473cc52cd4d545e5a3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103684280"
---
# <a name="metadata-import"></a>中繼資料匯入

WWSAPI 包含的 API 元素可用來處理端點的 WSDL 和原則，其目標為解壓縮可用於與端點通訊的資訊。 當端點所支援的通訊協定尚未已知時，通常會使用這些 Api。


使用下列順序來處理中繼資料：

``` syntax
WsCreateMetadata    // create a metadata object

while there are metadata documents to add
{
    // retrieve the metadata document from it's location
    // (download, read from file, etc)

    // add the document to the metadata object
    WsReadMetadata

    // optionally query the metadata object for any missing documents
    WsGetMissingMetadataDocumentAddress?
}

// get the endpoints from the metadata object
WsGetMetadataEndpoints

for each endpoint
{            
    // examine the endpoint information to see if 
    // the endpoint is relevant for the particular scenario

    if the endpoint is relevant
    {
        // get the policy object from the endpoint

        // get the number of policy alternatives in the policy
        WsGetPolicyAlternativeCount

        for each policy alternative
        {
            // construct a policy constraints structure that specifies
            // what policy is acceptable and what information to extract
            // from the policy

            // see if the policy alternative matches the constraints
            WsMatchPolicyAlternative

            // if there is a match, then use it

            // if there is not a match, then it is also possible to 
            // try with a different constraint structure
        }
    }
}

// If reusing the metadata object for a different set of documents
WsResetMetadata? // reset metadata object, which removes all documents

WsFreeMetadata // free the metadata object
```

如需 WSDL 和 WS-Policy 判斷提示如何對應至 API 的詳細資訊，請參閱 [中繼資料](metadata-mapping.md) 對應主題。

## <a name="security"></a>安全性

下載的中繼資料只會與用來下載的位址一樣好。 應用程式應該確保信任位址。 此外，應用程式應該確保它使用安全性通訊協定來下載不允許篡改中繼資料的元資料檔案。

應用程式應該檢查中繼資料所公開的服務位址。 依預設，執行時間會確保服務的主機名稱符合用來下載中繼資料的原始 URL，但應用程式可能會想要執行額外的檢查。 應用程式可以覆寫 [**WS \_ 中繼資料 \_ 屬性 [ \_ 驗證 \_ 主機 \_ 名**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) ] 屬性，以停用主機名稱驗證。 如果預設已停用的主機名稱檢查已停用，應用程式就必須針對包含服務位址的元資料檔案，保護它本身不信任的不同合作物件。

根據預設，中繼資料執行時間用來還原序列化和處理中繼資料的最大記憶體數量為256k，而且可能加入的檔數目上限為32。 這些預設值可由 [**ws \_ 中繼資料 \_ 屬性 \_ 堆積要求 \_ 的 \_ 大小**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) 和 **ws \_ 中繼資料 \_ 屬性的 \_ 最大 \_ 檔** 屬性覆寫。 這些界限是設計用來限制下載數量，並限制為了累積中繼資料所配置的記憶體數量。 增加這些值可能會導致記憶體使用量過高、CPU 使用量或網路頻寬耗用量。 請注意，由於會以二進位格式擴充字典字串，因此小型訊息可能會導致更大的還原序列化格式，因此依賴小型訊息來限制中繼資料記憶體配置在使用二進位格式時並不夠。

根據預設，原則替代專案的最大數目是32，不過可以透過 [**WS \_ 原則屬性的 \_ \_ 最大 \_ 替代**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) 專案屬性來覆寫。 如果應用程式在尋找相符專案的每個替代專案之間進行迴圈，則可能需要在尋找相符專案之前，先搜尋所有替代專案。 增加最大的替代專案數目可能會導致 CPU 使用率過高。

下列列舉是中繼資料匯入的一部分：

-   [**WS \_ 中繼資料 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id)
-   [**WS \_ 中繼資料 \_ 狀態**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_state)
-   [**WS \_ 原則 \_ 延伸 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_extension_type)
-   [**WS \_ 原則 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id)
-   [**WS \_ 原則 \_ 狀態**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_state)
-   [**WS \_ 安全性系結 \_ \_ 條件約束 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_constraint_type)

下列函數是中繼資料匯入的一部分：

-   [**WsCreateMetadata**](/windows/desktop/api/WebServices/nf-webservices-wscreatemetadata)
-   [**WsFreeMetadata**](/windows/desktop/api/WebServices/nf-webservices-wsfreemetadata)
-   [**WsGetMetadataEndpoints**](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataendpoints)
-   [**WsGetMetadataProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataproperty)
-   [**WsGetMissingMetadataDocumentAddress**](/windows/desktop/api/WebServices/nf-webservices-wsgetmissingmetadatadocumentaddress)
-   [**WsGetPolicyAlternativeCount**](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyalternativecount)
-   [**WsGetPolicyProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyproperty)
-   [**WsMatchPolicyAlternative**](/windows/desktop/api/WebServices/nf-webservices-wsmatchpolicyalternative)
-   [**WsReadMetadata**](/windows/desktop/api/WebServices/nf-webservices-wsreadmetadata)
-   [**WsResetMetadata**](/windows/desktop/api/WebServices/nf-webservices-wsresetmetadata)

下列控制碼是中繼資料匯入的一部分：

-   [WS \_ 中繼資料](ws-metadata.md)
-   [WS \_ 原則](ws-policy.md)

下列結構是中繼資料匯入的一部分：

-   [**WS \_ CERT \_ MESSAGE \_ SECURITY \_ BINDING \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**WS \_ 通道 \_ 屬性 \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property_constraint)
-   [**WS \_ 端點 \_ 原則 \_ 擴充功能**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_policy_extension)
-   [**WS \_ HTTP \_ 標頭 \_ 驗證安全性系結 \_ \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)
-   [**WS \_ 發出的 \_ 權杖 \_ 訊息安全性系結 \_ \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)
-   [**WS \_ KERBEROS \_ APREQ \_ MESSAGE \_ SECURITY \_ BINDING \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**WS \_ 中繼資料 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoint)
-   [**WS \_ 中繼資料 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoints)
-   [**WS \_ 中繼資料 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_property)
-   [**WS \_ 原則 \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_constraints)
-   [**WS \_ 原則 \_ 延伸**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_extension)
-   [**WS \_ 原則 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_properties)
-   [**WS \_ 原則 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_property)
-   [**WS \_ 要求 \_ 安全性 \_ 權杖 \_ 屬性 \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint)
-   [**WS \_ 安全性系結 \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_constraint)
-   [**WS \_ 安全性系結 \_ \_ 屬性 \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property_constraint)
-   [**WS \_ 安全性 \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_security_constraints)
-   [**WS \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性系結 \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)
-   [**WS \_ 安全性 \_ 屬性 \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property_constraint)
-   [**WS \_ SSL \_ 傳輸 \_ 安全性系結 \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)
-   [**WS \_ TCP \_ SSPI \_ 傳輸 \_ 安全性系結 \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)
-   [**WS 使用者 \_ 名稱 \_ 訊息安全性系結 \_ \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)

 

 




