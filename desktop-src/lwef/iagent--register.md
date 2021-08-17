---
title: IAgent 註冊
description: IAgent 註冊
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f3400e6f29e62b3d8c194186f52591a0f7bb039a858c3d450e8e8332df4313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962668"
---
# <a name="iagentregister"></a>IAgent：： Register

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

註冊用戶端應用程式的通知接收。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

通知接收介面的 [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) 位址。

</dd> <dt>

<span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*
</dt> <dd>

通知接收識別碼 (用來取消註冊通知接收) 的位址。

</dd> </dl>

您必須註冊通知接收 (也稱為通知接收或事件接收) ，才能從 Microsoft 代理程式伺服器接收事件。

## <a name="see-also"></a>另請參閱

[**IAgent：：取消註冊**](iagent--unregister.md)


 

 




