---
description: 連接新的 Windows 映像取得 (WIA) 硬體裝置時所發生的事件。
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: Wia. OnDeviceConnected 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceConnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 952b738e8afa0850bd67bab1206382e96419513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192805"
---
# <a name="wiaondeviceconnected-event"></a>Wia. OnDeviceConnected 事件

連接新的 Windows 映像取得 (WIA) 硬體裝置時所發生的事件。

## <a name="syntax"></a>語法


```JScript
Wia.OnDeviceConnected(
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

每當有新的硬體裝置連接到電腦時，WIA 都會通知腳本或應用程式。 執行 **objWia** \_ **OnDeviceConnected ()** 副程式，以允許腳本或應用程式回應裝置連線。

例如，您可能想要在安裝新裝置時，重新整理 [**裝置**](-wia-iwia-devices.md) 集合的腳本。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




