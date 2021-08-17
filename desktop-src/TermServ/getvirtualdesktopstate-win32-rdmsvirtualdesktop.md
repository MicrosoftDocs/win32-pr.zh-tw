---
title: Win32_RDMSVirtualDesktop 類別的 GetVirtualDesktopState 方法
description: 捕獲虛擬桌面的狀態。
ms.assetid: 176096ba-2b5f-428c-9216-02e3e97be64e
ms.tgt_platform: multiple
keywords:
- GetVirtualDesktopState 方法遠端桌面服務
- GetVirtualDesktopState 方法遠端桌面服務，Win32_RDMSVirtualDesktop 類別
- Win32_RDMSVirtualDesktop 類別遠端桌面服務，GetVirtualDesktopState 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb59cf90f436d3d44c20daa2a7f8146f688d012310253bafcf0185fe804b89fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059466"
---
# <a name="getvirtualdesktopstate-method-of-the-win32_rdmsvirtualdesktop-class"></a>Win32 RDMSVirtualDesktop 類別的 GetVirtualDesktopState 方法 \_

捕獲虛擬桌面的狀態。

## <a name="syntax"></a>語法


```mof
uint32 GetVirtualDesktopState(
  [out] uint32 VMState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VMState* \[擴展\]
</dt> <dd>

接收值，指出虛擬機器的狀態。

這個參數可以設定為下列其中一個值：

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0 (預設) ) 


</dt> <dd>

無法判斷虛擬機器的狀態。

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) 


</dt> <dd>

虛擬機器未執行。

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) 


</dt> <dd>

虛擬機器已關閉。

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (32768) 


</dt> <dd>

虛擬機器已暫停。

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>已 **暫** 止 (32769) 


</dt> <dd>

虛擬機器處於儲存狀態。

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**啟動** (32770) 


</dt> <dd>

虛擬機器正在啟動。

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**正在儲存** (32773) 


</dt> <dd>

虛擬機器正在儲存其狀態。

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (32774) 


</dt> <dd>

虛擬機器正在關閉。

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**暫停** (32776) 


</dt> <dd>

虛擬機器正在暫停。

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**繼續** (32777) 


</dt> <dd>

虛擬機器正在從暫停狀態繼續。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                              |
| 命名空間<br/>                | 根 \\ CIMv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





