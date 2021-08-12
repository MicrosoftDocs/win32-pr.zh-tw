---
description: 提供在路徑中使用64位值的限制。
ms.assetid: 63f4f6c5-7803-425d-912f-bb1dd716e617
ms.tgt_platform: multiple
title: 64位值的類別實例支援
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae778bcaad724d727bbda6d6a421ae19c562acdd50c33aa7764bea3b1861273e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556825"
---
# <a name="class-instance-support-for-64-bit-values"></a>64位值的類別實例支援

您可以使用64位的索引鍵值作為路徑的一部分，但有下列限制：

-   只要您未超過32位範圍，就可以從索引鍵指派和取出值，就像是32位屬性一樣。
-   當您超過已簽署類型的 0x7FFFFFFF (的整數值時) 、 (不帶正負號類型的 0x80000000) 或32位，您必須使用引號。
-   64位值的唯一有效路徑位於實例的 **\_ \_ RELPATH** 或 **\_ \_ path** 屬性中。 因此，WMI 不支援對等值的十六進位標記法。
-   如果 WMI 將實例索引鍵記錄為負數，則您必須使用原始數位來取得實例。

查詢的語法不會受到影響，且行為會如預期般運作。 這個行為只會影響物件路徑、 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)和 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 作業。

下列範例顯示類別實例可以有64位的索引鍵值。

``` syntax
class MyBig
{
  [key] sint64 k;
  sint64 p;
};

instance of MyBig
{
  k = 2;
  p = 3;
};
```

 

 



