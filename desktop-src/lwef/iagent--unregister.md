---
title: IAgent 取消註冊
description: IAgent 取消註冊
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101d0473e8563e8b0899e2f5d0bd2a440c31d17b4a0c142b43f47855ddf166b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976478"
---
# <a name="iagentunregister"></a>IAgent：：取消註冊

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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


 

 