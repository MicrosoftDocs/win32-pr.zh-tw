---
title: IAgentCharacterEx GetGUID
description: IAgentCharacterEx GetGUID
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e0e14d0931774bf6ab5e1c8599bbebaadd0ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932417"
---
# <a name="iagentcharacterexgetguid"></a>IAgentCharacterEx：： GetGUID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetGUID(
   BSTR * pbszGUID  // address of character's ID
);
```

捕獲字元的唯一識別碼。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*
</dt> <dd>

接收字元識別碼之 BSTR 的位址。

</dd> </dl>

屬性會傳回 GUID 的字串表示， (以大括弧和連字號) 格式化，以供伺服器用來唯一識別該字元。 使用 Microsoft 代理程式字元編輯器來編譯時，會設定字元識別碼。 此為唯讀屬性。

 

 




