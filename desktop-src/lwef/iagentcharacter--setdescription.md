---
title: IAgentCharacter SetDescription
description: IAgentCharacter SetDescription
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d96765d3faddafef00a28826ec5a9fdd92acb6884ac3aa659ad88ba2c091a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609818"
---
# <a name="iagentcharactersetdescription"></a>IAgentCharacter：： SetDescription

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

設定字元的描述。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*
</dt> <dd>

設定字元描述的 BSTR。 使用 Microsoft 代理程式字元編輯器來編譯時，會定義字元的預設描述。 描述設定是選擇性的，可能不會提供所有字元。 您可以使用 **IAgentCharacter：： setDescription**; 來變更字元的描述。不過，這個值不是持續性 (永久儲存) 。 當用戶端第一次載入字元時，字元的描述會還原為其預設設定。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： GetDescription**](iagentcharacter--getdescription.md)


 

 




