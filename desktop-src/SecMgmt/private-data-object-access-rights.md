---
description: 列出並說明私用資料物件的存取權限。
ms.assetid: 82be57d0-487c-4eb7-83d5-0dd2d53a452b
title: 私用資料物件存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142aecfe133a9c04237aacf58413e026c4cb3164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468876"
---
# <a name="private-data-object-access-rights"></a>私用資料物件存取權限

此物件類型的存取類型為：



| 存取類型          | Description                                      |
|----------------------|--------------------------------------------------|
| 秘密 \_ 查詢 \_ 值 | 需要此存取類型才能取得秘密。 |
| 密碼 \_ 集 \_ 值   | 需要此存取類型才能修改秘密。   |



 

## <a name="generic-access-masks"></a>一般存取遮罩

此物件類型具有下列一般存取對應：

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    SECRET_QUERY_VALUE

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    SECRET_SET_VALUE

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a>標準存取類型：

此物件不支援 (選擇性) 同步處理標準存取類型。 支援所有必要的存取類型。 此物件類型所有支援之存取類型的遮罩為：

``` syntax
    SECRET_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    SECRET_QUERY_VALUE |
                    SECRET_SET_VALUE
```

 

 



