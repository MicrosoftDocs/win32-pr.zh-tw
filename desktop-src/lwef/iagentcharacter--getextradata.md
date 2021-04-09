---
title: IAgentCharacter GetExtraData
description: IAgentCharacter GetExtraData
ms.assetid: 83f69bae-0ae3-45c5-ba0d-71610993da60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea854479ab85630abc3d110c9c193716ddedd004
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092323"
---
# <a name="iagentcharactergetextradata"></a>IAgentCharacter::GetExtraData

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetExtraData(
   BSTR * pbszExtraData   // address of buffer for additional character data
); 
```

抓取儲存為字元一部分的其他資料。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*
</dt> <dd>

接收字元的其他資料值之 BSTR 的位址。 使用 Microsoft 代理程式字元編輯器來編譯時，會定義字元的其他資料。 字元開發人員可以藉由編輯來提供這個字串。字元的 ACD 檔。 這項設定是選擇性的，可能不會提供給所有字元，也不能在執行時間定義或變更資料。 此外，所提供資料的意義是由字元開發人員定義。

</dd> </dl>

 

 




