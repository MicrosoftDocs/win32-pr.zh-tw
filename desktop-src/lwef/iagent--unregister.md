---
title: IAgent 取消註冊
description: IAgent 取消註冊
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796e033ac823ee7c79fe5312fab2c57dec36e694
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842280"
---
# <a name="iagentunregister"></a>IAgent：：取消註冊

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

從 [**字元**](/windows/desktop/lwef/the-characters-object) 集合中卸載指定字元的字元資料。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*
</dt> <dd>

通知接收識別碼。

</dd> </dl>

當您不再需要 Microsoft 代理程式服務時，例如當您的應用程式關閉時，請使用此方法。

## <a name="see-also"></a>另請參閱

[**IAgent：： Register**](iagent--register.md)


 

 