---
title: 存取保留存放區
description: HTTP 伺服器 API 會維護電腦上所有使用者的命名空間保留清單。
ms.assetid: 4b1291fc-cc62-4d4f-9150-18cbb1f6e5c0
keywords:
- 存取保留存放區 HTTP
- 保留存放區 HTTP，存取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a138a0a2385e6338877e5e8623527a64a6eca796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372202"
---
# <a name="accessing-the-reservation-store"></a>存取保留存放區

HTTP 伺服器 API 會維護電腦上所有使用者的命名空間保留清單。 保留專案是由 [UrlPrefix](urlprefix-strings.md) 和對應的 ACL 所組成。 存放區中的每個 UrlPrefix 都有一個 ACL，其中會列出所有允許註冊的使用者，以接收命名空間的要求。 具有委派許可權的使用者可以將其所擁有之命名空間的子樹委派給其他使用者，或使用設定 Api 來刪除現有的保留。

為了將保留新增至持續性保留存放區，應用程式會呼叫 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) 函數，並將設定識別碼參數設定為 **HttpServiceConfigUrlAclInfo** 值。 HTTP 伺服器 API 會先驗證命名空間和使用者識別碼的擁有權，再將保留新增至存放區。

HTTP 伺服器 API 也會提供函數來查詢及刪除 URL 命名空間的服務設定。 呼叫 [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) 函式時，會將設定識別碼參數設定為 **HttpServiceConfigUrlAclInfo** 值查詢，並在 URL 命名空間存放區上刪除 [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) 函數。

 

 




