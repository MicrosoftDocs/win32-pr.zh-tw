---
title: 'IVMGuestOS InstallIntegrationComponents 方法 (VPCCOMInterfaces .h) '
description: 找出最新的整合元件，並將其安裝在客體作業系統中。
ms.assetid: 06f302b3-ec2b-471a-8e2e-095ed6ecbd3d
keywords:
- InstallIntegrationComponents 方法 Virtual PC
- InstallIntegrationComponents 方法 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，InstallIntegrationComponents 方法
topic_type:
- apiref
api_name:
- IVMGuestOS.InstallIntegrationComponents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c61ade15736cec16976566f464573b30df7fd918f0f2be84f2f4ebd56e5db514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007188"
---
# <a name="ivmguestosinstallintegrationcomponents-method"></a>IVMGuestOS：： InstallIntegrationComponents 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

找出最新的整合元件，並將其安裝在客體作業系統中。

## <a name="syntax"></a>語法


```C++
HRESULT InstallIntegrationComponents();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                            | 描述                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                  | 作業成功。<br/>                                               |
| <dl> <dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt> </dl>                       | 虛擬機器必須正在執行，才能進行這種操作。<br/>                     |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>                            | 找不到虛擬機器。<br/>                                     |
| <dl> <dt>**VM \_E \_ 磁片磁碟機 \_ 無效**</dt>的 <dt>0xA0040502</dt> </dl>                         | 虛擬機器沒有空的 DVD 光碟機。<br/>                       |
| <dl> <dt>**VM \_E \_ 媒體 \_ 卸載 \_ 失敗**</dt> <dt>0xA0040508</dt> </dl>                   | 嘗試從虛擬機器 DVD 磁片磁碟機卸載媒體失敗。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                            | 已發生未預期的錯誤。<br/>                                           |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案)**</dt> <dt>0x80070002</dt> </dl> | 系統找不到整合元件的 ISO 檔案。<br/>         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

