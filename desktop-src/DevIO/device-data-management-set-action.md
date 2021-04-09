---
description: 定義 IOCTL \_ 儲存區 \_ 管理 \_ 資料 \_ 集 \_ 屬性控制項程式碼的一組動作。
ms.assetid: ff688c9a-8669-4699-aab9-1e2e3a5c7fca
title: 'DEVICE_DATA_MANAGEMENT_SET_ACTION (WinIoCtl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524d1dbd2ecf09dbcfa66fa766089dde7cf04a0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847284"
---
# <a name="device_data_management_set_action"></a>裝置 \_ 資料 \_ 管理 \_ 設定 \_ 動作

下列常數值是 **裝置 \_ 資料 \_ 管理 \_ 集合 \_ 動作** 類型的可能值集合，其定義為 **DWORD** 類型。

<dl> <dt>

<span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction \_ 無**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



未執行任何動作。


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction \_ Trim**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



執行 trim 動作。


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**DeviceDsmAction \_ 通知**
</dt> <dd> <dl> <dt>

2 \| **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000002) 
</dt> <dt>



會執行通知動作。 這些參數是在 [**裝置 \_ DSM \_ 通知 \_ 參數**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) 結構中。 **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000000) 是一個位旗標，用來向驅動程式堆疊指出這項作業是不具破壞性的。


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction \_ OffloadRead**
</dt> <dd> <dl> <dt>

3 \| **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000003) 
</dt> <dt>



執行卸載讀取動作。 參數位於 [**裝置 \_ DSM 卸載 \_ \_ 讀取 \_ 參數**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) 結構中。 輸出位於 [**儲存體卸載 \_ \_ 讀取 \_ 輸出**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) 結構中。 **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000000) 是一個位旗標，用來向驅動程式堆疊指出這項作業是不具破壞性的。

**Windows 7 和 Windows Server 2008 R2：** 在 Windows 8 和 Windows Server 2012 之前，不支援這個值。


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction \_ OffloadWrite**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



執行卸載寫入動作。 參數位於 [**裝置 \_ DSM 卸載 \_ \_ 寫入 \_ 參數**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) 結構中。 輸出位於 [**儲存體卸載 \_ \_ 寫入 \_ 輸出**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) 結構中。

**Windows 7 和 Windows Server 2008 R2：** 在 Windows 8 和 Windows Server 2012 之前，不支援這個值。


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**DeviceDsmAction \_ 配置**
</dt> <dd> <dl> <dt>

5 \| **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000005) 
</dt> <dt>



傳入的第一個資料集範圍會傳回配置點陣圖。 輸出為 [**裝置 \_ 資料 \_ 集 LB 布建 \_ \_ \_ 狀態**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) 結構。 **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000000) 是一個位旗標，用來向驅動程式堆疊指出這項作業是不具破壞性的。

**Windows 7 和 Windows Server 2008 R2：** 在 Windows 8 和 Windows Server 2012 之前，不支援這個值。


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**DeviceDsmAction \_ 修復**
</dt> <dd> <dl> <dt>

6 \| **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000006) 
</dt> <dt>



執行修復動作。 **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000000) 是一個位旗標，用來向驅動程式堆疊指出這項作業是不具破壞性的。

**Windows 7 和 Windows Server 2008 R2：** 在 Windows 8 和 Windows Server 2012 之前，不支援這個值。


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**DeviceDsmAction \_ 清除**
</dt> <dd> <dl> <dt>

7 \| **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000007) 
</dt> <dt>



執行清除動作。 **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000000) 是一個位旗標，用來向驅動程式堆疊指出這項作業是不具破壞性的。

**Windows 7 和 Windows Server 2008 R2：** 在 Windows 8 和 Windows Server 2012 之前，不支援這個值。


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**DeviceDsmAction \_ 復原**
</dt> <dd> <dl> <dt>

8 \| **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000008) 
</dt> <dt>



執行復原動作。 **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000000) 是一個位旗標，用來向驅動程式堆疊指出這項作業是不具破壞性的。

**Windows 7 和 Windows Server 2008 R2：** 在 Windows 8 和 Windows Server 2012 之前，不支援這個值。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                                         |
| 標頭<br/>                   | <dl> <dt>WinIoCtl (包含) 的 Windows。h </dt> </dl> |



 

 




