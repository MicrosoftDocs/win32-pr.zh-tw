---
title: IAgentCharacter GetName
description: IAgentCharacter GetName
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107e6fdb6be3e79dee14177d9f56ee7d258f3455d578641e7d3a3b3cf044c741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962270"
---
# <a name="iagentcharactergetname"></a>IAgentCharacter：： GetName

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

抓取字元的名稱。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*
</dt> <dd>

接收字元名稱值之 BSTR 的位址。

</dd> </dl>

使用 Microsoft 代理程式字元編輯器來編譯時，會定義字元的預設名稱。 字元的名稱可能會根據字元的語言識別項而有所不同。 您可以使用不同的名稱來編譯不同語言的字元。

您也可以使用 **IAgentCharacter： SetName**; 設定字元的名稱。不過，這會變更所有目前字元用戶端的名稱。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： SetName**](iagentcharacter--setname.md)


 

 




