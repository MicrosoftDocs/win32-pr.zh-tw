---
title: 'IVMDVDDriveEvents OnMediaInsert 方法 (VPCCOMInterfaces .h) '
description: '接收媒體已插入磁片磁碟機的通知。 |IVMDVDDriveEvents OnMediaInsert 方法 (VPCCOMInterfaces .h) '
ms.assetid: a246e2dd-638e-4d2f-9089-74771cd8bb2b
keywords:
- OnMediaInsert 方法 Virtual PC
- OnMediaInsert 方法 Virtual PC，IVMDVDDriveEvents 介面
- IVMDVDDriveEvents 介面 Virtual PC，OnMediaInsert 方法
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 883f7990de17a9d1dbb21db9651e0f5ad4ec74aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945806"
---
# <a name="ivmdvddriveeventsonmediainsert-method"></a>IVMDVDDriveEvents：： OnMediaInsert 方法

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

ISO 映像的主機磁碟機號或路徑。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

當媒體 (ISO 映像或插入主機磁片磁碟機中的光碟) 時，會呼叫此方法。 用戶端程式必須執行這個介面方法，以接收來自 IVMDVDDrive 的 vmDVDDriveEvent \_ OnInsert 事件的[](ivmdvddrive.md)通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents 定義為 c2a7d8e9-e76c-4eb8-94f7-71a5122d249b<br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMDVDDriveEvents**](ivmdvddriveevents.md)
</dt> </dl>

 

