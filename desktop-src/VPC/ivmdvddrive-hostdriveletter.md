---
title: 'IVMDVDDrive HostDriveLetter 屬性 (VPCCOMInterfaces .h) '
description: 為此裝置設定之主機磁片磁碟機的字母。
ms.assetid: e17f707f-e1cf-4302-a69e-caa5829df1af
keywords:
- HostDriveLetter 屬性 Virtual PC
- HostDriveLetter 屬性 Virtual PC，IVMDVDDrive 介面
- IVMDVDDrive 介面 Virtual PC，HostDriveLetter 屬性
topic_type:
- apiref
api_name:
- IVMDVDDrive.HostDriveLetter
- IVMDVDDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60d2599b8fb73e727100111dc37d29a9d13c5d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685806"
---
# <a name="ivmdvddrivehostdriveletter-property"></a>IVMDVDDrive：： HostDriveLetter 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取此裝置的主機磁片磁碟機的字母。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a>屬性值

磁碟機號。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                            | 意義                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                               | 作業成功。<br/>                             |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                 | 參數為 **Null**。<br/>                                |
| <dl> <dt>E \_FAIL</dt> <dt>0x80004005</dt> </dl>                    | 已發生未預期的錯誤。<br/>                         |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>         | 找不到虛擬機器。<br/>                   |
| <dl> <dt>VM \_E \_ 媒體有 \_ 錯誤的 \_ 類型</dt> <dt>0xA00400728</dt> </dl> | 由此 DVD 光碟機所捕捉的媒體不是主機磁片磁碟機。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>         | 已發生未預期的錯誤。<br/>                         |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive 定義為 b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

