---
title: 'IVMDVDDrive ReleaseHostDrive 方法 (VPCCOMInterfaces .h) '
description: 從 DVD 光碟機釋放已捕捉的主機磁片磁碟機。
ms.assetid: 88bbe364-0c39-40c2-89e7-22ffd66259a2
keywords:
- ReleaseHostDrive 方法 Virtual PC
- ReleaseHostDrive 方法 Virtual PC，IVMDVDDrive 介面
- IVMDVDDrive 介面 Virtual PC，ReleaseHostDrive 方法
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ed2c551ba619855743266b9b506a0c579f92a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384438"
---
# <a name="ivmdvddrivereleasehostdrive-method"></a>IVMDVDDrive：： ReleaseHostDrive 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

從 DVD 光碟機釋放已捕捉的主機磁片磁碟機。

## <a name="syntax"></a>語法


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                         | Description                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                               | 作業成功。<br/>                                      |
| <dl> <dt>**E \_FAIL**</dt> <dt>0x80004005</dt> </dl>                    | 已發生未預期的錯誤。<br/>                                  |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>         | 找不到虛擬機器。<br/>                            |
| <dl> <dt>**VM \_E \_ 媒體有 \_ 錯誤的 \_ 類型**</dt> <dt>0xA00400728</dt> </dl> | 目前所捕獲的媒體不是主機磁片磁碟機。<br/>             |
| <dl> <dt>**VM \_E \_ 磁片磁碟機 \_ 無效**</dt>的 <dt>0xA0040502</dt> </dl>      | 因為匯流排位置無效，所以無法初始化磁片磁碟機。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>         | 已發生未預期的錯誤。<br/>                                  |



 

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

 

