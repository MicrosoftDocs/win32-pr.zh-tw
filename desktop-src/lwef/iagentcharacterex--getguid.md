---
title: IAgentCharacterEx GetGUID
description: IAgentCharacterEx GetGUID
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e43a98617b1e2d25a25167ad5b95462eeb462f40f5a353b5a5ec45ffb3a9cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477966"
---
# <a name="iagentcharacterexgetguid"></a>IAgentCharacterEx：： GetGUID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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

 

 




