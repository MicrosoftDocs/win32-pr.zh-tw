---
title: 設定 URL 群組
description: 設定 URL 群組
ms.assetid: be222076-51ff-4907-924f-cc7b0d4fe767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407ca18fc5d2797c99e86661bf462eaf0a3fdc5b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109696"
---
# <a name="configuring-the-url-group"></a>設定 URL 群組

URL 群組識別碼會使用 [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) 函式建立，並用於 [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)的呼叫中。 *PPropertyInformation* 參數指向設定之屬性類型的設定結構。 **PropertyInformationLength** 參數會指定設定結構的大小（以位元組為單位）。 例如，在設定 **HttpServerTimeoutsProperty** 時， *pPropertyInformation* 參數必須指向不能小於 [**HTTP \_ TIMEOUT \_ 限制 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) 結構的緩衝區。 URL 群組設定是藉由呼叫 [**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)來查詢。

建立 URL 群組之後，會使用 [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup)將 url 新增至群組。 URL 群組必須與2.0 版要求佇列相關聯，才能接收要求。 為了將 URL 群組與要求佇列產生關聯，應用程式會呼叫 [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) ，並在 *Property* 參數中指定 **HttpServerBindingProperty** 。 如果未設定此屬性，則會將 URL 群組的要求傳遞至要求佇列，而 HTTP 伺服器 API 會產生503回應。 應用程式只能在以低許可權執行時，將先前以服務保留的 Url 新增至 URL 群組。 如需詳細資訊，請參閱 [命名空間保留、註冊和路由](namespace-reservations-registrations-and-routing.md) 主題。

 

 




