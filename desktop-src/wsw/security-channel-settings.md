---
title: 安全性通道設定
description: 安全性通道設定可控制在通道上套用和驗證安全性的方式。
ms.assetid: ad964874-0bc7-4f03-8ceb-33627ff99f08
keywords:
- Windows 的安全性通道設定 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3d6cef77da7a908598e2150ebf09de13a0899a6910a562335c4a5b91d6cf8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927008"
---
# <a name="security-channel-settings"></a>安全性通道設定

安全性通道設定可控制在通道上套用和驗證安全性的方式。 每個安全性通道設定都是以屬性-值組的集合來表示，並以列舉 [**WS \_ 安全性 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)定義屬性索引鍵。 集合中的每個屬性都有合理的預設值。 由於這些預設值的原因，您可以定義和使用安全性描述，而不需要指定任何安全性通道設定。


[安全性](security-binding-settings.md) 系結設定包含屬性值配對的類似集合，其索引鍵是由 [**WS \_ 安全性 \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) 系結屬性結構所定義。 這兩種設定的差異在於安全性通道設定的範圍設定為安全性描述 (也就是說，它們包含全通道的安全性屬性) ，而安全性系結設定的範圍則是其中一個安全性系結，而且可能有許多安全性系結。 因此，例如，包含三個安全性系結的自訂安全性描述將會有一個安全性通道設定包，適用于整個通道和三個安全性系結設定包（每個安全性系結一個）。

下列列舉會搭配安全性通道設定使用：

-   [**WS \_ 保護 \_ 等級**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)
-   [**WS \_ 要求 \_ 安全性 \_ 權杖 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)
-   [**WS \_ 安全性 \_ 演算法 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_id)
-   [**WS \_ 安全性 \_ 演算法 \_ 屬性 \_ 識別碼**](/windows/win32/api/webservices/ne-webservices-ws_move_to)
-   [**WS \_ 安全性 \_ 標頭配置 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_layout)
-   [**WS \_ 安全性 \_ 標頭 \_ 版本**](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_version)
-   [**WS \_ 安全性 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**WS \_ 安全性 \_ 時間戳記 \_ 使用量**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)
-   [**WS \_ XML \_ 安全性 \_ 權杖 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_security_token_property_id)

下列結構會搭配安全性通道設定使用：

-   [**WS \_ 要求 \_ 安全性 \_ 權杖 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property)
-   [**WS \_ 安全性 \_ 演算法 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_property)
-   [**WS \_ 安全性 \_ 演算法 \_ 套件**](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_suite)
-   [**WS \_ 安全性 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)
-   [**WS \_ XML \_ 安全性 \_ 權杖 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_security_token_property)

 

 




