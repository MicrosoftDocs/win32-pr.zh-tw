---
title: HTTP 伺服器 API 版本2.0 函式
description: HTTP 伺服器 API 2.0 版提供下列功能。
ms.assetid: 12daffca-b403-4f06-8037-206f90e33252
keywords:
- HTTP 伺服器 API 版本2.0 函式
- 函數 HTTP，HTTP 伺服器 API 版本2。0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e4d5c09c001caa58d43c1e61d800f66b39706b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549073"
---
# <a name="http-server-api-version-20-functions"></a>HTTP 伺服器 API 版本2.0 函式

HTTP 伺服器 API 2.0 版提供下列功能。

| 函式 | 描述 |
|-|-|
| [**HttpDelegateRequestEx**](/windows/win32/api/http/nf-http-httpdelegaterequestex) | 將要求從來源要求佇列委派至目標要求佇列。 |
| [**HttpFindUrlGroupId**](/windows/win32/api/http/nf-http-httpfindurlgroupid) | 抓取 URL 的 URL 群組識別碼和要求佇列。 |
| [**HttpIsFeatureSupported**](/windows/win32/api/http/nf-http-httpisfeaturesupported) | 檢查是否支援特定功能。 |

## <a name="server-session"></a>伺服器會話

| 函式 | 描述 |
|-|-|
| [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession) | |
| [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) | |
| [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty) | |
| [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) | |

## <a name="url-groups"></a>URL 群組

| 函式 | 描述 |
|-|-|
| [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) | |
| [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) | |
| [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) | |
| [**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty) | |
| [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) | |
| [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) | |

## <a name="request-queue"></a>要求佇列

| 函式 | 描述 |
|-|-|
| [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue) | |
| [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) | |
| [**HttpQueryRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) | |
| [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) | |
| [**HttpShutdownRequestQueue**](/windows/desktop/api/Http/nf-http-httpshutdownrequestqueue) | |
| [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) | |

## <a name="related-topics"></a>相關主題

[HTTP 伺服器 API 版本2.0 結構](http-server-api-version-2-0-structures.md)
