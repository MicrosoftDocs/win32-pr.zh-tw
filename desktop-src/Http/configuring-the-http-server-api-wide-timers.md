---
title: 設定 HTTP Server API 寬計時器
description: 設定 HTTP Server API 寬計時器
ms.assetid: 34f80bac-a7c5-4949-9c15-ed63a3582e26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0eb5fc40bedd51884830893673b3bae2341a21110fa2c3b33878dba7a4aef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047348"
---
# <a name="configuring-the-http-server-api-wide-timers"></a>設定 HTTP Server API 寬計時器

HTTP 伺服器 API 範圍的 **HeaderWait** 和 **IdleConnection** 計時器是藉由呼叫1.0 版 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) 函式來設定。 *ConfigId* 參數會設定為 **HttpServiceConfigTimeout** ，而 *pConfigInformation* 參數會指定 [**HTTP 服務設定 \_ \_ \_ TIMEOUT \_ 集**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set)結構，其中包含已設定的計時器和計時器的值。

設定 HTTP 伺服器 API 範圍的超時會需要系統管理許可權，不過查詢它們並不會。 這些設定會針對電腦上的所有應用程式進行設定，並在重新開機 HTTP 服務或重新開機電腦時保存這些設定。 若要查詢現有的 HTTP 伺服器整個 API 的超時，應用程式會呼叫 [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)。

 

 




