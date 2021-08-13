---
title: 'IVMFloppyDrive ReleaseHostDrive 方法 (VPCCOMInterfaces .h) '
description: 從軟碟磁碟機釋放主機上的實體磁片磁碟機。
ms.assetid: 6d5a8e7c-684c-42bc-84e5-76d3e761b7f0
keywords:
- ReleaseHostDrive 方法 Virtual PC
- ReleaseHostDrive 方法 Virtual PC，IVMFloppyDrive 介面
- IVMFloppyDrive 介面 Virtual PC，ReleaseHostDrive 方法
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44202754528483f88ab045b848e83a6a41a318b1e1ffed6122c2a2ac971237c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594844"
---
# <a name="ivmfloppydrivereleasehostdrive-method"></a>IVMFloppyDrive：： ReleaseHostDrive 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

從軟碟磁碟機釋放主機上的實體磁片磁碟機。

## <a name="syntax"></a>語法


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                          | 描述                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                | 作業成功。<br/>                                               |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>          | 此虛擬機器的設定無效或找不到。<br/> |
| <dl> <dt>**VM \_E \_ 媒體有 \_ 錯誤的 \_ 類型**</dt> <dt>0xA00400728</dt> </dl>  | 連接到這個磁片磁碟機的媒體不是實體磁片磁碟機。<br/>     |
| <dl> <dt>**VM \_E \_ 未 \_ \_ 捕獲媒體**</dt> <dt>0xA00400652</dt> </dl> | 沒有媒體連接到這個磁片磁碟機。<br/>                            |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>          | 已發生未預期的錯誤。<br/>                                           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive 定義為661abee6-112a-4ed9-babf-3c874969f10e<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

