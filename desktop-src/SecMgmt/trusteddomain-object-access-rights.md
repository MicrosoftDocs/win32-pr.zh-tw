---
description: 列出並說明 TrustedDomain 物件的存取權限。
ms.assetid: eb82864c-7e69-4ed5-a55d-d6792670bcd1
title: TrustedDomain 物件存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efeaf621cc3727cb936e69806bbcf89dabe5d41eb39b38dce3f9f23a0200dcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118893006"
---
# <a name="trusteddomain-object-access-rights"></a>TrustedDomain 物件存取權限

[**TrustedDomain**](trusteddomain-object.md)物件類型具有下列存取類型：



| 存取類型                  | 描述                                                                      |
|------------------------------|----------------------------------------------------------------------------------|
| 受信任的 \_ 查詢 \_ 功能變數名稱 \_ | 需要此存取類型才能查詢受信任網域的名稱。              |
| 信任的 \_ 設定 \_ 控制器    | 需要此存取類型才能設定受信任網域的控制器清單。 |
| 信任的 \_ 查詢 \_ POSIX        | 需要此存取類型才能取得受信任網域的 Posix 識別碼位移。  |
| 信任的 \_ 組 \_ POSIX          | 需要此存取類型才能設定受信任網域的 Posix 識別碼位移。       |



 

## <a name="generic-access-masks"></a>一般存取遮罩

此物件類型具有下列一般存取對應：

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                    TRUSTED_QUERY_DOMAIN_NAME

    GENERIC_WRITE        STANDARD_RIGHTS_WRITE |
                    TRUSTED_SET_POSIX

    GENERIC_EXECUTE    STANDARD_RIGHTS_EXECUTE |
                    TRUSTED_QUERY_POSIX
```

## <a name="standard-access-types"></a>標準存取類型

此物件不支援 (選擇性) 同步處理標準存取類型。 支援所有必要的存取類型。 此物件類型所有支援之存取類型的遮罩為：

``` syntax
    TRUSTED_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    TRUSTED_QUERY_DOMAIN_NAME |
                    TRUSTED_QUERY_CONTROLLERS |
                    TRUSTED_SET_CONTROLLERS
```

 

 



