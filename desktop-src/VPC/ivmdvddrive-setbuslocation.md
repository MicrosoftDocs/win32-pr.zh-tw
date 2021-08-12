---
title: 'IVMDVDDrive SetBusLocation 方法 (VPCCOMInterfaces .h) '
description: 將 DVD 光碟機連接到虛擬機器中指定的匯流排位置。
ms.assetid: 765274b8-91bc-475a-ac4d-994b2425a421
keywords:
- SetBusLocation 方法 Virtual PC
- SetBusLocation 方法 Virtual PC，IVMDVDDrive 介面
- IVMDVDDrive 介面 Virtual PC，SetBusLocation 方法
topic_type:
- apiref
api_name:
- IVMDVDDrive.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 593a42c21d1ed688185a7fe7123e972998859c010775a2cf4efd5f3bbbbaa98f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595841"
---
# <a name="ivmdvddrivesetbuslocation-method"></a>IVMDVDDrive：： SetBusLocation 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

將 DVD 光碟機連接到虛擬機器中指定的匯流排位置。

## <a name="syntax"></a>語法


```C++
HRESULT SetBusLocation(
  [in] long busNumber,
  [in] long deviceNumber
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*busNumber* \[在\]
</dt> <dd>

要連接此磁片磁碟機的匯流排號碼。 例如，在 IDE 匯流排上，這個數位會表示是否使用主要或次要匯流排號碼。

</dd> <dt>

*deviceNumber* \[在\]
</dt> <dd>

要連接此磁片磁碟機的裝置編號。 例如，在 IDE 匯流排上，這個數位會表示是否要使用主要或次要裝置位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                            | 描述                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                  | 作業成功。<br/>                                                                                                |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                 | 指定的匯流排位置無效。<br/>                                                                                     |
| <dl> <dt>**E \_FAIL**</dt> <dt>0x80004005</dt> </dl>                       | 已發生未預期的錯誤。<br/>                                                                                            |
| <dl> <dt>**VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的**</dt> <dt>0xA004020B</dt> </dl> | 當虛擬機器正在執行或處於儲存狀態時，無法設定匯流排位置。<br/>                                     |
| <dl> <dt>**\_ \_ \_ \_ 使用中的 VM E 匯流排 LOC \_**</dt> </dl>                                                                      | 另一個裝置已附加至指定的匯流排位置。<br/>                                                            |
| <dl> <dt>**VM \_E \_ 磁片磁碟機 \_ 無效**</dt>的 <dt>0xA0040502</dt> </dl>         | 無法初始化目前磁片磁碟機。<br/>                                                                                  |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>            | 因為無法判斷此磁片磁碟機的虛擬機器，所以無法將變更寫入喜好設定檔案。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>            | 已發生未預期的錯誤。<br/>                                                                                            |



 

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

 

