---
title: IMsTscAxEvents OnRemoteProgramDisplayed 方法
description: 在顯示 RemoteApp 程式時呼叫。
ms.assetid: 24f5ea52-0c13-4024-9448-5c2c1896ca8b
ms.tgt_platform: multiple
keywords:
- OnRemoteProgramDisplayed 方法遠端桌面服務
- OnRemoteProgramDisplayed 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnRemoteProgramDisplayed 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 584e54c487ec24a3c165fdd5eb8e22f243e07f23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686060"
---
# <a name="imstscaxeventsonremoteprogramdisplayed-method"></a>IMsTscAxEvents：： OnRemoteProgramDisplayed 方法

在顯示 RemoteApp 程式時呼叫。

## <a name="syntax"></a>語法


```C++
VOID OnRemoteProgramDisplayed(
  [in] VARIANT_BOOL vbDisplayed,
  [in] ULONG        uDisplayInformation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*vbDisplayed* \[在\]
</dt> <dd>

指出是否要顯示或隱藏 RemoteApp 程式。

</dd> <dt>

*uDisplayInformation* \[在\]
</dt> <dd>

顯示資訊。

<dt>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**鐵路 \_ APPDISPLAY \_ AUTORECONNECT**


</dt> <dd>

自動重新連線正在進行中。

</dd> <dt>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**鐵路 \_ APPDISPLAY \_ DESKTOPHOOKED**


</dt> <dd>

RemoteApp 計數只會進入零。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在事件接收中執行此方法，以接收已顯示 RemoteApp 的通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



 

 





