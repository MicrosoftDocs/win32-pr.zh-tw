---
description: 將編碼規則套用至抽象語法所描述的資料結構會提供傳輸語法，以控制在電腦之間傳送資料流程時，如何組織資料流程中的位元組。
ms.assetid: 674e88f9-4b65-4b42-8c44-d24fc03ae2f3
title: DER 傳送語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6757a22743a2c44abb5ef4c46154a08e425e2b1b7045beaacc7fb4f4f206fed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904511"
---
# <a name="der-transfer-syntax"></a>DER 傳送語法

將編碼規則套用至抽象語法所描述的資料結構會提供傳輸語法，以控制在電腦之間傳送資料流程時，如何組織資料流程中的位元組。 可辨別編碼規則使用的傳輸語法一律遵循 *標記、長度、值* 的格式。 格式通常稱為 TLV 三，其中每個欄位 (T、L 或 V) 包含一或多個位元組。

![der 類型、長度和值 (tlv) 三](images/der-tlv-basic.png)

[ *標記* ] 欄位會指定要傳送的資料結構類型，[ *長度* ] 欄位會指定要傳送之內容的位元組數目，而 [ *值* ] 欄位則包含內容。 請注意，如果值欄位包含已建立的資料類型，其 *值* 欄位可以是三個，如下列圖例所示。

![der tlv 三遞迴](images/der-tlv-recursive.png)

請參閱下列主題，以取得有關 TLV 三個元件的詳細資訊。

-   [編碼的標記位元組](about-encoded-tag-bytes.md)
-   [編碼的長度和值位元組](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[結構化類型](about-constructed-types.md)
</dt> <dt>

[可辨別編碼規則](distinguished-encoding-rules.md)
</dt> </dl>

 

 



