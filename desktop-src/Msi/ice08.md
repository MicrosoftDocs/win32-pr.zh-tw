---
description: ICE08 會驗證元件資料表不包含重複的 Guid。 每個元件都必須有唯一的 GUID。 如果元件資料表不存在，則不會進行驗證。
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6075b7c895242fe5cfa7608a414643a9e3491787fc59037f8761fa66b18354
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745318"
---
# <a name="ice08"></a>ICE08

ICE08 會驗證 [元件資料表](component-table.md) 不包含重複的 [guid](guid.md)。 每個元件都必須有唯一的 GUID。 如果元件資料表不存在，則不會進行驗證。

## <a name="result"></a>結果

如果元件資料表的 [元件] 資料行中有兩個或多個專案包含相同的 GUID，ICE08 會張貼錯誤訊息。

## <a name="example"></a>範例

在下列範例中，ICE08 會張貼訊息，指出紅色和綠色元件有重複的 Guid。

[元件資料表](component-table.md) (部分) 



| 元件 | ComponentId                            |
|-----------|----------------------------------------|
| 紅色       | {0000000A-0003-0000-0000-624474736554} |
| 藍色      | {0000000A-0003-0000-0000-624474736354} |
| 綠色     | {0000000A-0003-0000-0000-624474736554} |



 

若要修正這個錯誤，請變更其中一個重複的 Guid。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



