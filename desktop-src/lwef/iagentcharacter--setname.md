---
title: IAgentCharacter SetName
description: IAgentCharacter SetName
ms.assetid: 4944f910-60e9-446b-82e9-2794f445789a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec058e338adfa8c998bf26a1223ae71f0c7de3d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969074"
---
# <a name="iagentcharactersetname"></a>IAgentCharacter：： SetName

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetName(
   BSTR bszName   // character name
);
```

設定字元的名稱。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

設定字元名稱的 BSTR。 使用 Microsoft 代理程式字元編輯器來編譯時，會定義字元的預設名稱。 您可以使用 **IAgentCharacter：： SetName**; 來變更它。不過，這會變更所有目前字元用戶端的字元名稱。 這個屬性不是持續性 (永久儲存) 。 只要用戶端第一次載入字元，字元的名稱就會還原為預設名稱。

字元的名稱也可能相依于其語言識別項。 您可以使用不同的名稱來編譯不同語言的字元。

伺服器使用 Microsoft 代理程式介面的部分中的字元名稱設定，例如當字元為輸入-使用中時，以及在 Microsoft Agent 工作列快顯功能表中的 [語音命令] 視窗標題。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： GetName**](iagentcharacter--getname.md)


 

 




