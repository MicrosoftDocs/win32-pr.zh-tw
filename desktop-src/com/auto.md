---
title: 自動
description: 判斷在傳送 COM RPC 通知時是否自動啟動偵錯工具。
ms.assetid: e05ae7cb-79d1-4543-aef3-9397548c2030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c7730c3c6e0fe9dc01b43a7c4f9621897f9f16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966217"
---
# <a name="auto"></a>自動

判斷在傳送 COM RPC 通知時是否自動啟動偵錯工具。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\DebugObjectRPCEnabled\AeDebug
   Auto = value
```

## <a name="remarks"></a>備註

這是 **REG \_ 單字** 值。



| 值 | 描述                    |
|-------|--------------------------------|
| 1     | 自動啟動偵錯工具。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> </dl>

 

 




