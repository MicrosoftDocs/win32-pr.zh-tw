---
description: TLV 內建的長度欄位會識別值欄位中編碼的位元組數目。
ms.assetid: d72371f9-fe55-468d-b15b-0f8948674619
title: 編碼的長度和值位元組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45eaec36875446d7493f37fc150f7b5f9d1a59c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001361"
---
# <a name="encoded-length-and-value-bytes"></a>編碼的長度和值位元組

TLV 內建的 *長度* 欄位會識別 *值* 欄位中編碼的位元組數目。 *值* 欄位包含在電腦之間傳送的內容。 如果 [ *值* ] 欄位包含少於128個位元組，則 [ *長度* ] 欄位只需要一個位元組。 *長度* 欄位的位7是零 (0) 而其餘的位會識別要傳送之內容的位元組數目。 如果 [ *值* ] 欄位包含超過127個位元組，則 [ *長度* ] 欄位中的位7是一個 (1) 而其餘的位會識別包含長度所需的位元組數目。 下圖顯示範例。

![der tlv 長度位元組](images/der-tlv-lengthbyte.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DER 傳送語法](about-der-transfer-syntax.md)
</dt> <dt>

[編碼的標記位元組](about-encoded-tag-bytes.md)
</dt> </dl>

 

 



