---
title: 安裝程式設定
description: 安裝程式設定需要系統管理員許可權，而且在重新開機時持續存在。
ms.assetid: 96e9c069-829b-4615-b94b-3761bc541440
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43b543bfc81f963341d7b5f690f4b40312ee420
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507045"
---
# <a name="setup-configuration"></a>安裝程式設定

安裝程式設定需要系統管理員許可權，而且在重新開機時持續存在。 一般來說，以系統管理員許可權執行的安裝應用程式會在安裝期間執行這類持續性設定，讓應用程式可以在較低的許可權執行，不過持續設定可能會在任何時間執行。 安裝程式設定可以包含下列四個活動中的任何一項：

-   建立 URL 保留專案。 HTTP API 可讓安裝應用程式保留與特定應用程式相關聯之要求佇列的 URL 首碼。 為了保留 URL，安裝應用程式會呼叫 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) 函式，並將 *ConfigId* 參數設定為 **HttpServiceConfigUrlAclInfo** ，並將 *pConfigInformation* 參數中的指標傳遞至包含註冊資訊的 [**HTTP \_ 服務 \_ \_ \_ 設定 URLACL 集**](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_set) 結構。 如需詳細資訊，請參閱 [命名空間保留、註冊和路由](namespace-reservations-registrations-and-routing.md)。
-   正在設定 SSL。 若要設定 SSL，系統管理員會呼叫 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) 函式，並將 *ConfigId* 參數設定為 **HttpServiceConfigSSLCertInfo** ，並將 *pConfigInformation* 參數中的指標傳遞至包含 ssl 憑證資訊的 [**HTTP \_ 服務 \_ \_ \_ 設定 ssl 集**](/windows/desktop/api/Http/ns-http-http_service_config_ssl_set) 結構。
-   設定其他 HTTP 伺服器範圍的持續性設定，例如 HTTP 伺服器將接聽的 IP 位址，以及整個伺服器的超時值。 請參閱 [IP 接聽清單](ip-listen-list.md) 和 [**HTTP \_ 服務 \_ \_ \_ 設定超時設定**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set)。

 

 




