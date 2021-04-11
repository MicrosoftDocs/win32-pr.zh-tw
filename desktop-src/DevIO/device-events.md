---
description: 應用程式（包括服務）可以註冊以接收裝置事件的通知。
ms.assetid: c89da4ac-57dd-4d95-ac86-3eb137dee0bc
title: '裝置事件 (IoEvent .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce58ba5dd21cdd505e945687603ddb54e77b2440
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187588"
---
# <a name="device-events-ioeventh"></a>裝置事件 (IoEvent .h) 

應用程式（包括服務）可以註冊以接收裝置事件的通知。 例如，目錄服務可以接收正在掛接或卸載的磁片區通知，讓它可以調整磁片區上檔案的路徑。 系統會將應用程式傳送至 [**WM \_ DEVICECHANGE**](wm-devicechange.md) 訊息，以通知應用程式裝置事件已發生。 系統會透過叫用服務的事件處理常式函式 [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)，通知服務裝置事件已發生。

若要接收裝置事件通知，請使用 [**開發 \_ 廣播 \_ 控制碼**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle)結構來呼叫 [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)函式。 務必將 **dbch \_ 控制碼** 成員設定為從 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函數取得的裝置控制碼。 此外，請將 **dbch \_ devicetype** 成員設定為 **DBT \_ DEVTYP \_ 控制碼**。 函數會傳回裝置通知控制碼。 請注意，這與磁片區控制碼不同。

當您的應用程式收到通知時，如果事件種類是 [DBT \_ CUSTOMEVENT](dbt-customevent.md)，您可能會收到 IoEvent 中定義的其中一個裝置事件。 若要判斷是否發生上述其中一個事件，請使用下列步驟。

1.  將事件資料視為 [**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) 結構。 確認 **dbch \_ devicetype** 成員已設定為 **DBT \_ DEVTYP \_ 控制碼**。
2.  如果 **dbch \_ Devicetype** 是 **DBT \_ DEVTYP \_ 控制碼**，則事件資料實際上是 [**開發 \_ 廣播 \_ 控制碼**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) 結構的指標。
3.  使用 [**IsEqualGUID**](/windows/win32/api/guiddef/nf-guiddef-isequalguid)函數，比較 **dbch \_ eventguid** 成員與下表所列的 **GUID**。

<dl> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**GUID \_ IO \_ CDROM \_ 獨佔 \_ 鎖定**
</dt> <dd> <dl> <dt>

bc56c139-7a10-47ee-a294-4c6a38f0149a
</dt> <dt>



已鎖定 CD-ROM 裝置以進行獨佔存取。

**Windows Server 2003 和 WINDOWS XP：** 此值的支援需要 IMAPI.EXE 2.0。 如需詳細資訊，請參閱 [影像主控 API](/windows/desktop/imapi/portal)。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID \_ IO \_ CDROM \_ 獨佔 \_ 解除鎖定**
</dt> <dd> <dl> <dt>

a3b6d27d-5e35-4885-81e5-ee18c00ed779
</dt> <dt>



已鎖定為獨佔存取的 CD-ROM 裝置已解除鎖定。

**Windows Server 2003 和 WINDOWS XP：** 此值的支援需要 IMAPI.EXE 2.0。 如需詳細資訊，請參閱 [影像主控 API](/windows/desktop/imapi/portal)。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**GUID \_ IO \_ 裝置 \_ 即將 \_ 就緒**
</dt> <dd> <dl> <dt>

d07433f0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



正在啟動媒體功能。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**GUID \_ IO \_ 裝置 \_ 外部 \_ 要求**
</dt> <dd> <dl> <dt>

d07433d0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



此事件有幾個可能的原因：如需詳細資訊，請參閱取得事件狀態通知命令的 T10 MMC 規格，網址為 [https://www.t10.org/](https://www.t10.org/) 。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**GUID \_ IO \_ 媒體 \_ 抵達**
</dt> <dd> <dl> <dt>

d07433c0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



卸除式媒體已新增至裝置。 **Dbch \_ 資料** 成員是 [**類別 \_ 媒體 \_ 變更 \_ 內容**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context)結構的指標。 **NewState** 成員提供狀態資訊。 例如， **MediaUnavailable** 的值表示媒體無法使用 (例如，因為使用中的錄製會話) 。

**WINDOWS XP：****Dbch \_ 資料** 成員是 **ULONG** 值，代表從系統啟動之後變更媒體的次數。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**GUID \_ IO \_ 媒體 \_ 退出 \_ 要求**
</dt> <dd> <dl> <dt>

d07433d1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



卸載式媒體的磁片磁碟機已收到來自使用者的要求，以將指定的位置或媒體退出。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**\_移除 GUID IO \_ 媒體 \_**
</dt> <dd> <dl> <dt>

d07433c1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



卸載式媒體已從裝置移除或無法使用。 **Dbch \_ 資料** 成員是 [**類別 \_ 媒體 \_ 變更 \_ 內容**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context)結構的指標。 **NewState** 成員提供狀態資訊。 例如， **MediaUnavailable** 的值表示媒體無法使用 (例如，因為使用中的錄製會話) 。

**WINDOWS XP：****Dbch \_ 資料** 成員是 **ULONG** 值，代表從系統啟動之後變更媒體的次數。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**GUID \_ IO \_ 磁片區 \_ 變更**
</dt> <dd> <dl> <dt>

7373654a-812a-11d0-bec7-08002be2092f
</dt> <dt>



磁片區標籤已變更。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**GUID \_ IO \_ 磁片區 \_ 變更 \_ 大小**
</dt> <dd> <dl> <dt>

3a1625be-ad03-49f1-8ef8-6bbac182d1fd
</dt> <dt>



磁片區上的檔案系統大小已變更。

**Windows Server 2003 和 WINDOWS XP：** 不支援這個值。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**GUID \_ IO \_ 磁片區 \_ 卸載**
</dt> <dd> <dl> <dt>

d16a55e8-1059-11d2-8ffd-00a0c9a06d32
</dt> <dt>



嘗試卸載磁片區正在進行中。 您應該關閉磁片區上的所有檔案和目錄控制碼。 此事件之前不一定會有 **GUID \_ IO 磁片區 \_ \_ 鎖定** 事件。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**GUID \_ IO \_ 磁片區 \_ 卸載 \_ 失敗**
</dt> <dd> <dl> <dt>

e3c5b178-105d-11d2-8ffd-00a0c9a06d32
</dt> <dt>



嘗試卸載磁片區失敗。 發生這種情況的原因通常是因為另一個進程關閉未完成的控制碼，而無法回應 **GUID \_ IO \_ 磁片區 \_ 卸載** 通知。 因為卸載失敗，所以您可以重新開啟受影響磁片區的任何控制碼。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**GUID \_ IO \_ 磁片區 \_ FVE \_ 狀態 \_ 變更**
</dt> <dd> <dl> <dt>

062998b2-ee1f-4b6a-b857-e76cbbe9a6da
</dt> <dt>



磁片區的 BitLocker 磁碟機加密狀態已變更。 當 BitLocker 啟用或停用，或加密開始、結束、暫停或繼續時，就會發出此事件的信號。

**Windows Server 2003 和 WINDOWS XP：** 不支援這個值。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**GUID \_ IO \_ 磁片區 \_ 鎖定**
</dt> <dd> <dl> <dt>

50708874-c9af-11d1-8fef-00a0c9a06d32
</dt> <dt>



另一個進程正在嘗試鎖定磁片區。 您應該關閉磁片區上的所有檔案和目錄控制碼。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**GUID \_ IO \_ 磁片區 \_ 鎖定 \_ 失敗**
</dt> <dd> <dl> <dt>

ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32
</dt> <dt>



嘗試鎖定磁片區失敗。 發生這種情況的原因通常是因為另一個進程關閉未處理的控制碼，而無法回應 **GUID \_ IO \_ 磁片區 \_ 鎖定** 事件。 因為鎖定失敗，所以您可以重新開啟受影響磁片區的任何控制碼。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**GUID \_ IO \_ 磁片區 \_ 掛接**
</dt> <dd> <dl> <dt>

b5804878-1a96-11d2-8ffd-00a0c9a06d32
</dt> <dt>



磁片區已由另一個進程裝載。 您可以開啟一個或多個控制碼。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**GUID \_ IO \_ 磁片區 \_ 名稱 \_ 變更**
</dt> <dd> <dl> <dt>

2de97f83-4c06-11d2-a532-00609713055a
</dt> <dt>



磁片區名稱已變更。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**GUID \_ IO \_ 磁片區 \_ 需要 \_ CHKDSK**
</dt> <dd> <dl> <dt>

799a0960-0a0b-4e03-ad88-2fa7c6ce748a
</dt> <dt>



檔案系統在磁片區上偵測到損毀。 應用程式應該會在磁片區上執行 CHKDSK，或通知使用者這麼做。

**Windows Server 2003 和 WINDOWS XP：** 不支援這個值。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**GUID \_ IO \_ 磁片區 \_ 實體設定 \_ \_ 變更**
</dt> <dd> <dl> <dt>

2de97f84-4c06-11d2-a532-00609713055a
</dt> <dt>



磁片區的實體構成或目前實體狀態已變更。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**GUID \_ IO \_ 磁片區 \_ 準備 \_ 退出**
</dt> <dd> <dl> <dt>

c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6
</dt> <dt>



檔案系統正在準備要取出的光碟。 例如，檔案系統正在停止背景格式化作業，或在一次性寫入媒體上關閉會話。

**Windows Server 2003 和 WINDOWS XP：** 不支援這個值。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**GUID \_ IO \_ 磁片區 \_ 唯一 \_ 識別碼 \_ 變更**
</dt> <dd> <dl> <dt>

af39da42-6622-41f5-970b-139d092fa3d9
</dt> <dt>



磁片區的唯一識別碼已變更。 如需有關唯一識別碼的詳細資訊，請參閱 [**IOCTL \_ MOUNTDEV \_ QUERY \_ unique \_ ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id)。

**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 在 Windows Server 2008 R2 和 Windows 7 之前，不支援這個值。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**GUID \_ IO \_ 磁片區 \_ 解除鎖定**
</dt> <dd> <dl> <dt>

9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32
</dt> <dt>



另一個進程已解除鎖定磁片區。 您可以開啟一個或多個控制碼。


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**GUID \_ IO \_ 磁片區 \_ 磨損 \_**
</dt> <dd> <dl> <dt>

873113ca-1486-4508-82ac-c3b2e5297aaa
</dt> <dt>



媒體正在磨損。當檔案系統判斷磁片區的錯誤率太高，或其瑕疵更換空間即將耗盡時，就會傳送此事件。

**Windows Server 2003 和 WINDOWS XP：** 不支援這個值。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

**Guid io \_ 磁片 \_ 區 \_ 卸載** 和 **guid \_ io \_ 磁片區 \_ 卸載 \_ 失敗** 的事件是相關的，因為 **guid \_ io 磁片區 \_ \_ 鎖定** 和 **guid \_ io 磁片區 \_ \_ 鎖定 \_ 失敗** 事件。 **Guid \_ io 磁片 \_ 區 \_ 卸載** 和 **guid \_ io \_ 磁片區 \_ 鎖定** 事件指出正在嘗試操作。 您應該對事件通知採取動作，並記錄所採取的動作。 **Guid \_ io 磁片 \_ 區 \_ 卸載 \_ 失敗**， **guid \_ io \_ 磁片區 \_ 鎖定 \_ 失敗** 事件表示嘗試的作業失敗。 然後，您可以使用記錄來復原您針對操作所做的動作。

[**開發 \_ 廣播 \_ 控點**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle)結構的 **dbch \_ hdevnotify** 成員指出受影響的裝置。 請注意，這是 [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)所傳回的裝置通知控制碼，而不是磁片區控制碼。 若要在磁片區上執行作業，請將這個控制碼對應到相對應的磁片區控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2003<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>IoEvent。h</dt> </dl> |



 

