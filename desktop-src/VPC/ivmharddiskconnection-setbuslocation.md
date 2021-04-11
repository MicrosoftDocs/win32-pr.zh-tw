---
title: 'IVMHardDiskConnection SetBusLocation 方法 (VPCCOMInterfaces .h) '
description: 設定此硬碟所連接的匯流排位置。
ms.assetid: 0aa303ae-d8bf-4d38-94ab-bdbb4e744c7b
keywords:
- SetBusLocation 方法 Virtual PC
- SetBusLocation 方法 Virtual PC，IVMHardDiskConnection 介面
- IVMHardDiskConnection 介面 Virtual PC，SetBusLocation 方法
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61de0f595bc06d497e7f5913da9173ccb3bf1ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317111"
---
# <a name="ivmharddiskconnectionsetbuslocation-method"></a>IVMHardDiskConnection：： SetBusLocation 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

設定此硬碟所連接的匯流排位置。

## <a name="syntax"></a>語法


```C++
HRESULT SetBusLocation(
  [in] long vmBusNumber,
  [in] long vmDeviceNumber
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*vmBusNumber* \[在\]
</dt> <dd>

要使用的匯流排編號。

</dd> <dt>

*vmDeviceNumber* \[在\]
</dt> <dd>

要使用的裝置編號。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                               | Description                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                     | 作業成功。<br/>                                                                    |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                    | 指定的匯流排位置無效。<br/>                                                         |
| <dl> <dt>**VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的**</dt> <dt>0xA004020B</dt> </dl>    | 因為虛擬機器處於執行中或已儲存狀態，所以無法設定匯流排位置。<br/>    |
| <dl> <dt>**VM \_E \_ 磁片 \_ 磁碟機 \_ 匯流排 \_ \_ 使用中的 LOC**</dt> <dt>0xA00400503</dt> </dl> | 無法設定匯流排位置，因為另一個裝置目前已連接到此位置。<br/> |
| <dl> <dt>**VM \_E \_ 磁片磁碟機 \_ 無效**</dt>的 <dt>0xA0040502</dt> </dl>            | 目前的磁片磁碟機無效。<br/>                                                                  |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>               | 目前的虛擬機器無效。<br/>                                                        |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>               | 已發生未預期的錯誤。<br/>                                                                |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection 定義為 aefa36a5-463a-46ae-9e6c-a1fb4e12e671<br/>      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

