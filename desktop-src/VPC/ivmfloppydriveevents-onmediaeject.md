---
title: 'IVMFloppyDriveEvents OnMediaEject 方法 (VPCCOMInterfaces .h) '
description: '接收媒體已從磁片磁碟機中取出的通知。 |IVMFloppyDriveEvents OnMediaEject 方法 (VPCCOMInterfaces .h) '
ms.assetid: 3e9c0b5d-8fec-4f34-93d2-c5975403798b
keywords:
- OnMediaEject 方法 Virtual PC
- OnMediaEject 方法 Virtual PC，IVMFloppyDriveEvents 介面
- IVMFloppyDriveEvents 介面 Virtual PC，OnMediaEject 方法
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e624dcbf028caf58a2f50109789e5f89cd34d1d70c4679333b8b742c3b071ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653598"
---
# <a name="ivmfloppydriveeventsonmediaeject-method"></a>IVMFloppyDriveEvents：： OnMediaEject 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

接收媒體已從磁片磁碟機中取出的通知。

## <a name="syntax"></a>語法


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mediaPath* \[在\]
</dt> <dd>

磁片磁碟機的主機磁碟機號或路徑。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

當媒體 (磁片影像或主機磁片磁碟機中的磁片磁碟機) 時，會呼叫這個方法。 用戶端程式必須執行這個介面方法，以接收來自 IVMFloppyDrive 的 vmFloppyDriveEvent \_ OnMediaEject 事件的[](ivmfloppydrive.md)通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents 定義為 a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)
</dt> </dl>

 

