---
description: 這是連結至具有點陣圖和 BitValue 限定詞之屬性的整數。
ms.assetid: 14c34909-2419-41a1-a1ed-3b647a3c5e75
ms.tgt_platform: multiple
title: 點陣圖和 BitValue 限定詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60dd6b4ad5866ddc79c960316757700bc5fbb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969312"
---
# <a name="bitmap-and-bitvalue-qualifiers"></a>點陣圖和 BitValue 限定詞

點陣圖是連結至具有 **點陣圖** 和 **BitValue** 限定詞之屬性的整數。 屬性值的每個位都會作為 **BitValue** 清單中值陣列的索引。 因為屬性值中的多個位可以同時為 "on"，所以您可以使用單一屬性值來指出多個並行值。

例如，下列 MOF 程式碼範例會建立具有 **點陣圖** 和 **BitValues** 限定詞的 [內容 **類型**] 屬性。 它會進一步建立低序位位 (位0，) 對應至值「唯讀」。 下個位 (位 1) 對應至「隱藏」，依此類推。  (並非所有的位都必須是很重要的。 在這八位系統中，這兩個高序位位（6和7）沒有任何意義。 ) 

``` syntax
[BitMap("0","1","2","3","4","5"),
 BitValues("Read Only",
           "Hidden",
           "System",
           "Volume Label",
           "Subdirectory",
           "Archive")]
byte FileType;
```

如果 [內容 **類型** ] 屬性報告值 7 (bits 0000 0111) ，則檔案為「唯讀」、「系統」和「隱藏」。 如果 [內容 **類型** ] 屬性報告值 18 (0x12，bits 0001 0010) ，它是隱藏的子目錄。

使用 MOF 程式碼有兩種不同類型的點陣圖：

-   以低序位位開頭的連續有效位數 (位 0) 

    您可以定義位值陣列，而不需要明確地指定有效位數（如果有效位數以低序位位開頭 (位) 0），並在不中斷 **BitValue** 陣列中的所有專案的情況下繼續進行。 下列 MOF 程式碼範例會執行與上一個範例相同的功能。

    ``` syntax
    [BitValues("Read Only",
               "Hidden",
               "System",
               "Volume Label",
               "Subdirectory",
               "Archive")]
    byte FileType;
    ```

-   之前有點不重要的位

    如果低序位位沒有意義，或有效位的序列不連續，您必須同時指定 **BitMap** 和 **BitValues** 限定詞。 下列 MOF 程式碼範例會示範低序位位不重要的情況，以及有效位序列中的間隙。

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    在此情況下，設定低序位位 (位 0) 沒有任何意義，而且會被忽略。 但是，設定 bit 1 (0x2) 表示此電子郵件訊息已標示為待處理，設定位 4 (0x8) 指出當電子郵件訊息到達收件者的信箱時，傳送回條應傳送給寄件者，並設定位 5 (0x10) 指定當收件者開啟電子郵件訊息時，應將讀取回條傳送給傳送者。 將這三個有效位數全部設定 (0x1A) 指定電子郵件訊息的三個條件。

## <a name="remarks"></a>備註

在決定是否要使用 **BitMap** / **BitValues** 或 **ValueMap** / **值** 限定詞時，請判斷是否有任何指定的值可能會同時發生。 如果有多個並行值可以存在，您必須使用 **BitMap** / **BitValues**。 如果所有值都是互斥的，您應該使用 **ValueMap** / **值** 限定詞。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ValueMap 和值限定詞](value-map.md)
</dt> </dl>

 

 



