---
title: IAgentNotifySinkEx DefaultCharacterChange
description: IAgentNotifySinkEx DefaultCharacterChange
ms.assetid: 13acb502-e247-433f-abf3-2d78a2d6a4a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ec212887d17d1aa59d942ece79b3e6928900ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966808"
---
# <a name="iagentnotifysinkexdefaultcharacterchange"></a>IAgentNotifySinkEx：:D efaultCharacterChange

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT DefaultCharacterChange(
   BSTR bszGUID  // character identifier
);
```

在預設字元變更時通知用戶端應用程式。

-   沒有傳回值。

<dl> <dt>

<span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*
</dt> <dd>

字元的唯一識別碼。

</dd> </dl>

當使用者變更指派為使用者預設字元的字元時，伺服器會將此事件傳送給已載入預設字元的用戶端。 此事件會傳回字元的唯一識別碼 (GUID) 以大括弧和連字號格式格式化，這是在使用 Microsoft Agent 字元編輯器建立字元時所定義。

出現新的字元時，它會假設與任何已載入的字元實例或先前的預設字元相同的大小，) 的順序 (。

## <a name="see-also"></a>另請參閱

[**IAgent：： Load**](iagent--load.md)


 

 




