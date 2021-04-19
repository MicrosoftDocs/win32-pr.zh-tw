---
title: 'IVMFloppyDriveEvents OnMediaInsert 方法 (VPCCOMInterfaces .h) '
description: '接收媒體已插入磁片磁碟機的通知。 |IVMFloppyDriveEvents OnMediaInsert 方法 (VPCCOMInterfaces .h) '
ms.assetid: 922fca14-8ef6-4d3d-b1b6-72d2ea83e8ef
keywords:
- OnMediaInsert 方法 Virtual PC
- OnMediaInsert 方法 Virtual PC，IVMFloppyDriveEvents 介面
- IVMFloppyDriveEvents 介面 Virtual PC，OnMediaInsert 方法
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d607a2f63836ca1cb151e602b2d3b2021f4e3913
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106997235"
---
# <a name="ivmfloppydriveeventsonmediainsert-method"></a>IVMFloppyDriveEvents：： OnMediaInsert 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

接收媒體已插入磁片磁碟機的通知。

## <a name="syntax"></a>語法


```C++
HRESULT OnMediaInsert(
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

當媒體 (磁片影像，或插入主機磁片磁碟機) 中的磁片時，會呼叫此方法。 用戶端程式必須執行這個介面方法，以接收來自 IVMFloppyDrive 的 vmFloppyDriveEvent \_ OnMediaInsert 事件的[](ivmfloppydrive.md)通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents 定義為 a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)
</dt> </dl>

 

