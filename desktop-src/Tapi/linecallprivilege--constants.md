---
description: LINECALLPRIVILEGE \_ 位旗標常數描述具有呼叫控制碼的應用程式可能需要對應的呼叫之存取權限或許可權的種類。
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: 'LINECALLPRIVILEGE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c00dd43442345c545bb5e0b1718131b6815fd236f9c7d770c0f3b47b10b47a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660048"
---
# <a name="linecallprivilege_-constants"></a>LINECALLPRIVILEGE \_ 常數

**LINECALLPRIVILEGE \_** 位旗標常數描述具有呼叫控制碼的應用程式可能需要對應的呼叫之存取權限或許可權的種類。

<dl> <dt>

<span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**LINECALLPRIVILEGE \_ 監視**
</dt> <dd> <dl> <dt>



應用程式具有呼叫的監視器許可權。 這些許可權可讓應用程式監視狀態變更，以及查詢有關呼叫的資訊和狀態。


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE \_ 無**
</dt> <dd> <dl> <dt>



應用程式沒有呼叫的許可權。 應用程式的控制碼是 void，不應該使用。


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**LINECALLPRIVILEGE \_ 擁有者**
</dt> <dd> <dl> <dt>



應用程式具有呼叫的擁有者許可權。 這些許可權可讓應用程式以影響撥號狀態的方式來操作呼叫。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

第一次提供呼叫控制碼給應用程式，或每當該應用程式的呼叫許可權遭到修改時，就會將 [**行 \_ CALLSTATE**](line-callstate.md) 訊息傳送至應用程式。 當應用程式進行呼叫時，如果接收應用程式還沒有具有擁有者許可權的控制碼，則此訊息會通知應用程式其對呼叫的新許可權。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




