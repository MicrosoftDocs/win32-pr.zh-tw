---
title: 'SwarmStatus 列舉 (>deliveryoptimization) '
description: 定義傳遞優化用戶端內檔案的狀態。
ms.assetid: D40ABDD3-5573-4A8D-8608-4CB0F396CCAD
keywords:
- SwarmStatus 列舉
topic_type:
- apiref
api_name:
- SwarmStatus
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3622f819679c2fd2b28d66e371a8b88e0a2d2f70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105318"
---
# <a name="swarmstatus-enumeration"></a>SwarmStatus 列舉

定義傳遞優化用戶端內檔案的狀態。

## <a name="syntax"></a>Syntax


```C++
typedef enum _SwarmStatus { 
  SwarmStatus_Downloading  = 0,
  SwarmStatus_Complete     = 1,
  SwarmStatus_Caching      = 2,
  SwarmStatus_Paused       = 3
} SwarmStatus;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="SwarmStatus_Downloading"></span><span id="swarmstatus_downloading"></span><span id="SWARMSTATUS_DOWNLOADING"></span>**SwarmStatus_Downloading**
</dt> <dd>

正在下載檔案。

</dd> <dt>

<span id="SwarmStatus_Complete"></span><span id="swarmstatus_complete"></span><span id="SWARMSTATUS_COMPLETE"></span>**SwarmStatus_Complete**
</dt> <dd>

檔案下載已完成。

</dd> <dt>

<span id="SwarmStatus_Caching"></span><span id="swarmstatus_caching"></span><span id="SWARMSTATUS_CACHING"></span>**SwarmStatus_Caching**
</dt> <dd>

檔案正在進行快取。

</dd> <dt>

<span id="SwarmStatus_Paused"></span><span id="swarmstatus_paused"></span><span id="SWARMSTATUS_PAUSED"></span>**SwarmStatus_Paused**
</dt> <dd>

檔案下載已暫停。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl> |



 

 





