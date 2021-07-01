---
title: IAgentCharacter StopAll
description: IAgentCharacter StopAll
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558ca23b500ee2146470c8d595b2a5a64febf59a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120911"
---
# <a name="iagentcharacterstopall"></a>IAgentCharacter::StopAll

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

停止 (要求) 的所有動畫，並將其從字元的動畫佇列中移除。

<dl> <dt>

<span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*
</dt> <dd>

代表要停止 (的要求類型，並從字元的佇列) 移除的位位，由下列所組成：



| 值                                                                                  |  描述                                                                                                        |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **const 不帶正負號的 long** **STOP \_ TYPE \_ ALL = 0xffffffff;**<br/>              | 停止所有的動畫要求，包括未排入佇列的 [**準備**](iagentcharacter--prepare.md) 要求。 |
| **const 不帶正負號的 long** **STOP \_ 類型 \_ PLAY = 0x00000001;**<br/>             | 停止所有播放要求。                                                                                 |
| **const 不帶正負號的 long** **STOP \_ 類型 \_ MOVE = 0x00000002;**<br/>             | 停止所有 [**移動**](https://www.bing.com/search?q=**Move**) 要求。                                               |
| **const 不帶正負號的 long** **STOP \_ 類型 \_ 話 = 0x00000004;**<br/>            | 停止所有 [**朗讀**](iagentcharacter--speak.md) 的要求。                                              |
| **const 不帶正負號的 long** **STOP \_ TYPE \_ PREPARE = 0x00000008;**<br/>          | 停止所有已排入佇列的 [**準備**](iagentcharacter--prepare.md) 要求。                                   |
| **const 不帶正負號的 long** **STOP \_ 類型 \_ NONQUEUEDPREPARE = 0x00000010;**<br/> | 停止所有未排入佇列的 [**準備**](iagentcharacter--prepare.md) 要求。                               |
| **const 不帶正負號的 long** **STOP \_ 類型 \_ VISIBLE = 0x00000020;**<br/>          | 停止所有 [**隱藏**](iagentcharacter--hide.md) 或 [**顯示**](iagentcharacter--show.md) 要求。       |



 

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： Stop**](iagentcharacter--stop.md)


 

 





