---
title: 'IVMFloppyDrive AttachHostDrive 方法 (VPCCOMInterfaces .h) '
description: 將主機上的實體磁片磁碟機附加至虛擬機器中的磁片磁碟機。
ms.assetid: 9be84e06-e38a-419a-be50-dddd0cc6d2dd
keywords:
- AttachHostDrive 方法 Virtual PC
- AttachHostDrive 方法 Virtual PC，IVMFloppyDrive 介面
- IVMFloppyDrive 介面 Virtual PC，AttachHostDrive 方法
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a21785e3e1e4ec77146f048ab4cce018de9d8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025231"
---
# <a name="ivmfloppydriveattachhostdrive-method"></a>IVMFloppyDrive：： AttachHostDrive 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

將主機上的實體磁片磁碟機附加至虛擬機器中的磁片磁碟機。

## <a name="syntax"></a>語法


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*r* \[在\]
</dt> <dd>

要連接之主機電腦上的實體磁片磁碟機磁碟機號。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                 | Description                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>                                                                     |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | *R* 參數為 **Null**、不是有效的磁片磁碟機，或指定的路徑是空的。<br/> |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl> | 此虛擬機器的設定無效或找不到。<br/>                       |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/>                                                                 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive 定義為661abee6-112a-4ed9-babf-3c874969f10e<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

