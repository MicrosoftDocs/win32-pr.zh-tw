---
description: EXPERTSTATUSENUMERATION 列舉包含狀態值。 EXPERTSTATUS 結構的 Status 成員和 ExpertIndicateStatus 中的 Status 參數會使用它。
ms.assetid: 217dce5a-3698-45a9-bb13-8379bcbdd762
title: 'EXPERTSTATUSENUMERATION 列舉 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERT_STATUS_ENUMERATION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ee0729deab566717457f03af27a7e31de8cdf8f1b78f9a5f97b3c3ff406641fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795791"
---
# <a name="expertstatusenumeration-enumeration"></a>EXPERTSTATUSENUMERATION 列舉

**EXPERTSTATUSENUMERATION** 列舉包含狀態值。 [EXPERTSTATUS](expertstatus.md)結構的 **Status** 成員和 [ExpertIndicateStatus](expertindicatestatus.md)中的 *status* 參數會使用它。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  EXPERTSTATUS_INACTIVE  = 0,
  EXPERTSTATUS_STARTING,
  EXPERTSTATUS_RUNNING,
  EXPERTSTATUS_PROBLEM,
  EXPERTSTATUS_ABORTED,
  EXPERTSTATUS_DONE
} EXPERT_STATUS_ENUMERATION;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS \_ 非使用中**
</dt> <dd>

專家從未開始。

</dd> <dt>

<span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**EXPERTSTATUS \_ 開始**
</dt> <dd>

專家即將開始。

</dd> <dt>

<span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS \_ 正在執行**
</dt> <dd>

專家正在正常執行。

</dd> <dt>

<span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**EXPERTSTATUS \_ 問題**
</dt> <dd>

在子 *狀態* 中指定的問題已停止專家。

</dd> <dt>

<span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS 已 \_ 中止**
</dt> <dd>

網路監視器已停止專家。

</dd> <dt>

<span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS \_ 完成**
</dt> <dd>

專家已順利完成。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




