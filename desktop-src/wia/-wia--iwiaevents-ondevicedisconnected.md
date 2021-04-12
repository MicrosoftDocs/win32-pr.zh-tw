---
description: 當新的 Windows 映像取得 (WIA) 硬體裝置中斷連線時所發生的事件。
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: Wia. OnDeviceDisconnected 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceDisconnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 45652f3c447c1dd0f59b0470823782c6ba635cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192804"
---
# <a name="wiaondevicedisconnected-event"></a>Wia. OnDeviceDisconnected 事件

當新的 Windows 映像取得 (WIA) 硬體裝置中斷連線時所發生的事件。

## <a name="syntax"></a>語法


```JScript
Wia.OnDeviceDisconnected(
  Id
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*識別碼* 
</dt> <dd>

字串，其中包含已連線裝置的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

當硬體裝置與電腦中斷連線時，WIA 會通知腳本或應用程式。 執行 **objWia** \_ **OnDeviceDisconnected ()** 副程式，以允許腳本或應用程式回應裝置中斷連接。

例如，您可能想要在從電腦移除裝置時，重新整理 [**裝置**](-wia-iwia-devices.md) 集合的腳本。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




