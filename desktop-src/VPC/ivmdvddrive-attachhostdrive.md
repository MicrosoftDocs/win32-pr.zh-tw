---
title: 'IVMDVDDrive AttachHostDrive 方法 (VPCCOMInterfaces .h) '
description: 將主機磁片磁碟機連接到虛擬機器中的 DVD 光碟機。
ms.assetid: 68e658ba-470c-452c-8124-5bb2ec81911b
keywords:
- AttachHostDrive 方法 Virtual PC
- AttachHostDrive 方法 Virtual PC，IVMDVDDrive 介面
- IVMDVDDrive 介面 Virtual PC，AttachHostDrive 方法
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c82229488ebb705cab1a684a207f973356d2d43177c4123ae4f456b55fbe6840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136851"
---
# <a name="ivmdvddriveattachhostdrive-method"></a>IVMDVDDrive：： AttachHostDrive 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

將主機磁片磁碟機連接到虛擬機器中的 DVD 光碟機。

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

要附加之主機磁片磁碟機的字母。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                    | 描述                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                          | 作業成功。<br/>                                                                                                                                             |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>         | 未指定任何磁碟機號，或指定的磁碟機號無效。<br/>                                                                                                  |
| <dl> <dt>**E \_FAIL**</dt> <dt>0x80004005</dt> </dl>               | 已發生未預期的錯誤。<br/>                                                                                                                                         |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>    | 找不到虛擬機器。<br/>                                                                                                                                   |
| <dl> <dt>**VM \_\_ \_ \_ 使用中的 E 磁片磁碟機**</dt> <dt>0xA0040727</dt> </dl> | 主機 DVD 光碟機或 ISO 映像已連結到虛擬機器中的這個磁片磁碟機，或指定的主機磁片磁碟機已在另一部虛擬機器中使用。<br/> |
| <dl> <dt>**VM \_E \_ 磁片磁碟機 \_ 無效**</dt>的 <dt>0xA0040502</dt> </dl> | 此磁片磁碟機的匯流排位置無效，或磁片磁碟機似乎不是有效的 DVD 光碟機。<br/>                                                                         |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>    | 已發生未預期的錯誤。<br/>                                                                                                                                         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive 定義為 b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

