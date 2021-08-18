---
description: 帳戶物件存取權限類型具有下列存取類型。
ms.assetid: 42fb22bb-8135-4a8f-bce6-e767d6c5aaea
title: 帳戶物件存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb1251eecfd32bc574307cbc4f0f1327e4f96eb7fa7051d1dd638beb59e7ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895105"
---
# <a name="account-object-access-rights"></a>帳戶物件存取權限

帳戶物件存取權限類型具有下列存取類型。



| 存取類型                     | Description                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 帳戶 \_ 視圖                   | 需要此存取類型才能讀取帳戶資訊。 這包括指派給帳戶的 [*許可權*](/windows/desktop/SecGloss/p-gly) 、指派的記憶體配額，以及授與的任何特殊存取類型。 |
| 帳戶 \_ 調整 \_ 許可權     | 需要有此存取類型，才能將許可權指派給帳戶或從中移除許可權。                                                                                                                                                            |
| 帳戶 \_ 調整 \_ 配額         | 變更指派給帳戶的系統配額需要此存取類型。                                                                                                                                                                      |
| 帳戶 \_ 調整 \_ 系統 \_ 存取 | 需要此存取類型才能更新帳戶的系統存取旗標。                                                                                                                                                                       |



 

## <a name="generic-access-masks"></a>一般存取遮罩

[**Account**](account-object.md)物件會將下列從一般存取類型的對應發行至特定的存取類型。

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                        ACCOUNT_VIEW 
            
    GENERIC_WRITE       STANDARD_RIGHTS_WRITE |
                        ACCOUNT_ADJUST_PRIVILEGES |
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS

    GENERIC_EXECUTE        STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a>標準存取類型

此物件不支援 (選擇性) 同步處理標準存取類型。 支援所有必要的存取類型。 此物件類型所有支援之存取類型的遮罩如下所示。

``` syntax
    ACCOUNT_ALL_ACCESS  STANDARD_RIGHTS_REQUIRED |
                        ACCOUNT_VIEW |
                        ACCOUNT_ADJUST_PRIVILEGES |    
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS
```

 

 
