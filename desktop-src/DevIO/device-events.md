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
# <a name="device-events-ioeventh"></a><span data-ttu-id="1c561-103">裝置事件 (IoEvent .h) </span><span class="sxs-lookup"><span data-stu-id="1c561-103">Device Events (IoEvent.h)</span></span>

<span data-ttu-id="1c561-104">應用程式（包括服務）可以註冊以接收裝置事件的通知。</span><span class="sxs-lookup"><span data-stu-id="1c561-104">Applications, including services, can register to receive notification of device events.</span></span> <span data-ttu-id="1c561-105">例如，目錄服務可以接收正在掛接或卸載的磁片區通知，讓它可以調整磁片區上檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="1c561-105">For example, a catalog service can receive notice of volumes being mounted or dismounted so it can adjust the paths to files on the volume.</span></span> <span data-ttu-id="1c561-106">系統會將應用程式傳送至 [**WM \_ DEVICECHANGE**](wm-devicechange.md) 訊息，以通知應用程式裝置事件已發生。</span><span class="sxs-lookup"><span data-stu-id="1c561-106">The system notifies an application that a device event has occurred by sending the application a [**WM\_DEVICECHANGE**](wm-devicechange.md) message.</span></span> <span data-ttu-id="1c561-107">系統會透過叫用服務的事件處理常式函式 [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)，通知服務裝置事件已發生。</span><span class="sxs-lookup"><span data-stu-id="1c561-107">The system notifies a service that a device event has occurred by invoking the service's event handler function, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span></span>

<span data-ttu-id="1c561-108">若要接收裝置事件通知，請使用 [**開發 \_ 廣播 \_ 控制碼**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle)結構來呼叫 [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)函式。</span><span class="sxs-lookup"><span data-stu-id="1c561-108">To receive device event notices, call the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function with a [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure.</span></span> <span data-ttu-id="1c561-109">務必將 **dbch \_ 控制碼** 成員設定為從 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函數取得的裝置控制碼。</span><span class="sxs-lookup"><span data-stu-id="1c561-109">Be sure to set the **dbch\_handle** member to the device handle obtained from the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="1c561-110">此外，請將 **dbch \_ devicetype** 成員設定為 **DBT \_ DEVTYP \_ 控制碼**。</span><span class="sxs-lookup"><span data-stu-id="1c561-110">Also, set the **dbch\_devicetype** member to **DBT\_DEVTYP\_HANDLE**.</span></span> <span data-ttu-id="1c561-111">函數會傳回裝置通知控制碼。</span><span class="sxs-lookup"><span data-stu-id="1c561-111">The function returns a device notification handle.</span></span> <span data-ttu-id="1c561-112">請注意，這與磁片區控制碼不同。</span><span class="sxs-lookup"><span data-stu-id="1c561-112">Note that this is not the same as the volume handle.</span></span>

<span data-ttu-id="1c561-113">當您的應用程式收到通知時，如果事件種類是 [DBT \_ CUSTOMEVENT](dbt-customevent.md)，您可能會收到 IoEvent 中定義的其中一個裝置事件。</span><span class="sxs-lookup"><span data-stu-id="1c561-113">When your application receives notification, if the event type is [DBT\_CUSTOMEVENT](dbt-customevent.md), you may have received one of the device events defined in IoEvent.h.</span></span> <span data-ttu-id="1c561-114">若要判斷是否發生上述其中一個事件，請使用下列步驟。</span><span class="sxs-lookup"><span data-stu-id="1c561-114">To determine if one of these events has occurred, use the following steps.</span></span>

1.  <span data-ttu-id="1c561-115">將事件資料視為 [**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) 結構。</span><span class="sxs-lookup"><span data-stu-id="1c561-115">Treat the event data as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span> <span data-ttu-id="1c561-116">確認 **dbch \_ devicetype** 成員已設定為 **DBT \_ DEVTYP \_ 控制碼**。</span><span class="sxs-lookup"><span data-stu-id="1c561-116">Verify that the **dbch\_devicetype** member is set to **DBT\_DEVTYP\_HANDLE**.</span></span>
2.  <span data-ttu-id="1c561-117">如果 **dbch \_ Devicetype** 是 **DBT \_ DEVTYP \_ 控制碼**，則事件資料實際上是 [**開發 \_ 廣播 \_ 控制碼**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1c561-117">If **dbch\_devicetype** is **DBT\_DEVTYP\_HANDLE**, the event data is really a pointer to a [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure.</span></span>
3.  <span data-ttu-id="1c561-118">使用 [**IsEqualGUID**](/windows/win32/api/guiddef/nf-guiddef-isequalguid)函數，比較 **dbch \_ eventguid** 成員與下表所列的 **GUID**。</span><span class="sxs-lookup"><span data-stu-id="1c561-118">Compare the **dbch\_eventguid** member to the **GUID** s listed in the following table using the [**IsEqualGUID**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) function.</span></span>

<dl> <dt>

<span data-ttu-id="1c561-119"><span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**GUID \_ IO \_ CDROM \_ 獨佔 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="1c561-119"><span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**GUID\_IO\_CDROM\_EXCLUSIVE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-120">bc56c139-7a10-47ee-a294-4c6a38f0149a</span><span class="sxs-lookup"><span data-stu-id="1c561-120">bc56c139-7a10-47ee-a294-4c6a38f0149a</span></span>
</dt> <dt>



<span data-ttu-id="1c561-121">已鎖定 CD-ROM 裝置以進行獨佔存取。</span><span class="sxs-lookup"><span data-stu-id="1c561-121">The CD-ROM device has been locked for exclusive access.</span></span>

<span data-ttu-id="1c561-122">**Windows Server 2003 和 WINDOWS XP：** 此值的支援需要 IMAPI.EXE 2.0。</span><span class="sxs-lookup"><span data-stu-id="1c561-122">**Windows Server 2003 and Windows XP:** Support for this value requires IMAPI 2.0.</span></span> <span data-ttu-id="1c561-123">如需詳細資訊，請參閱 [影像主控 API](/windows/desktop/imapi/portal)。</span><span class="sxs-lookup"><span data-stu-id="1c561-123">For more information, see [Image Mastering API](/windows/desktop/imapi/portal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-124"><span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID \_ IO \_ CDROM \_ 獨佔 \_ 解除鎖定**</span><span class="sxs-lookup"><span data-stu-id="1c561-124"><span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID\_IO\_CDROM\_EXCLUSIVE\_UNLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-125">a3b6d27d-5e35-4885-81e5-ee18c00ed779</span><span class="sxs-lookup"><span data-stu-id="1c561-125">a3b6d27d-5e35-4885-81e5-ee18c00ed779</span></span>
</dt> <dt>



<span data-ttu-id="1c561-126">已鎖定為獨佔存取的 CD-ROM 裝置已解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="1c561-126">A CD-ROM device that was locked for exclusive access has been unlocked.</span></span>

<span data-ttu-id="1c561-127">**Windows Server 2003 和 WINDOWS XP：** 此值的支援需要 IMAPI.EXE 2.0。</span><span class="sxs-lookup"><span data-stu-id="1c561-127">**Windows Server 2003 and Windows XP:** Support for this value requires IMAPI 2.0.</span></span> <span data-ttu-id="1c561-128">如需詳細資訊，請參閱 [影像主控 API](/windows/desktop/imapi/portal)。</span><span class="sxs-lookup"><span data-stu-id="1c561-128">For more information, see [Image Mastering API](/windows/desktop/imapi/portal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-129"><span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**GUID \_ IO \_ 裝置 \_ 即將 \_ 就緒**</span><span class="sxs-lookup"><span data-stu-id="1c561-129"><span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**GUID\_IO\_DEVICE\_BECOMING\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-130">d07433f0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="1c561-130">d07433f0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="1c561-131">正在啟動媒體功能。</span><span class="sxs-lookup"><span data-stu-id="1c561-131">Media spin-up is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-132"><span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**GUID \_ IO \_ 裝置 \_ 外部 \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="1c561-132"><span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**GUID\_IO\_DEVICE\_EXTERNAL\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-133">d07433d0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="1c561-133">d07433d0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="1c561-134">此事件有幾個可能的原因：如需詳細資訊，請參閱取得事件狀態通知命令的 T10 MMC 規格，網址為 [https://www.t10.org/](https://www.t10.org/) 。</span><span class="sxs-lookup"><span data-stu-id="1c561-134">There are several possible causes for this event; for more information, refer to T10 MMC specification of the GET EVENT STATUS NOTIFICATION Command, at [https://www.t10.org/](https://www.t10.org/).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-135"><span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**GUID \_ IO \_ 媒體 \_ 抵達**</span><span class="sxs-lookup"><span data-stu-id="1c561-135"><span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**GUID\_IO\_MEDIA\_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-136">d07433c0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="1c561-136">d07433c0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="1c561-137">卸除式媒體已新增至裝置。</span><span class="sxs-lookup"><span data-stu-id="1c561-137">Removable media has been added to the device.</span></span> <span data-ttu-id="1c561-138">**Dbch \_ 資料** 成員是 [**類別 \_ 媒體 \_ 變更 \_ 內容**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1c561-138">The **dbch\_data** member is a pointer to a [**CLASS\_MEDIA\_CHANGE\_CONTEXT**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) structure.</span></span> <span data-ttu-id="1c561-139">**NewState** 成員提供狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="1c561-139">The **NewState** member provides status information.</span></span> <span data-ttu-id="1c561-140">例如， **MediaUnavailable** 的值表示媒體無法使用 (例如，因為使用中的錄製會話) 。</span><span class="sxs-lookup"><span data-stu-id="1c561-140">For example, a value of **MediaUnavailable** indicates that the media is not available (for example, due to an active recording session).</span></span>

<span data-ttu-id="1c561-141">**WINDOWS XP：\*\*\*\*Dbch \_ 資料** 成員是 **ULONG** 值，代表從系統啟動之後變更媒體的次數。</span><span class="sxs-lookup"><span data-stu-id="1c561-141">**Windows XP:** The **dbch\_data** member is a **ULONG** value that represents the number of times that media has been changed since system startup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-142"><span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**GUID \_ IO \_ 媒體 \_ 退出 \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="1c561-142"><span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**GUID\_IO\_MEDIA\_EJECT\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-143">d07433d1-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="1c561-143">d07433d1-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="1c561-144">卸載式媒體的磁片磁碟機已收到來自使用者的要求，以將指定的位置或媒體退出。</span><span class="sxs-lookup"><span data-stu-id="1c561-144">The removable media's drive has received a request from the user to eject the specified slot or media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-145"><span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**\_移除 GUID IO \_ 媒體 \_**</span><span class="sxs-lookup"><span data-stu-id="1c561-145"><span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**GUID\_IO\_MEDIA\_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-146">d07433c1-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="1c561-146">d07433c1-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="1c561-147">卸載式媒體已從裝置移除或無法使用。</span><span class="sxs-lookup"><span data-stu-id="1c561-147">Removable media has been removed from the device or is unavailable.</span></span> <span data-ttu-id="1c561-148">**Dbch \_ 資料** 成員是 [**類別 \_ 媒體 \_ 變更 \_ 內容**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1c561-148">The **dbch\_data** member is a pointer to a [**CLASS\_MEDIA\_CHANGE\_CONTEXT**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) structure.</span></span> <span data-ttu-id="1c561-149">**NewState** 成員提供狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="1c561-149">The **NewState** member provides status information.</span></span> <span data-ttu-id="1c561-150">例如， **MediaUnavailable** 的值表示媒體無法使用 (例如，因為使用中的錄製會話) 。</span><span class="sxs-lookup"><span data-stu-id="1c561-150">For example, a value of **MediaUnavailable** indicates that the media is not available (for example, due to an active recording session).</span></span>

<span data-ttu-id="1c561-151">**WINDOWS XP：\*\*\*\*Dbch \_ 資料** 成員是 **ULONG** 值，代表從系統啟動之後變更媒體的次數。</span><span class="sxs-lookup"><span data-stu-id="1c561-151">**Windows XP:** The **dbch\_data** member is a **ULONG** value that represents the number of times that media has been changed since system startup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-152"><span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**GUID \_ IO \_ 磁片區 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="1c561-152"><span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**GUID\_IO\_VOLUME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-153">7373654a-812a-11d0-bec7-08002be2092f</span><span class="sxs-lookup"><span data-stu-id="1c561-153">7373654a-812a-11d0-bec7-08002be2092f</span></span>
</dt> <dt>



<span data-ttu-id="1c561-154">磁片區標籤已變更。</span><span class="sxs-lookup"><span data-stu-id="1c561-154">The volume label has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-155"><span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**GUID \_ IO \_ 磁片區 \_ 變更 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="1c561-155"><span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**GUID\_IO\_VOLUME\_CHANGE\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-156">3a1625be-ad03-49f1-8ef8-6bbac182d1fd</span><span class="sxs-lookup"><span data-stu-id="1c561-156">3a1625be-ad03-49f1-8ef8-6bbac182d1fd</span></span>
</dt> <dt>



<span data-ttu-id="1c561-157">磁片區上的檔案系統大小已變更。</span><span class="sxs-lookup"><span data-stu-id="1c561-157">The size of the file system on the volume has changed.</span></span>

<span data-ttu-id="1c561-158">**Windows Server 2003 和 WINDOWS XP：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="1c561-158">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-159"><span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**GUID \_ IO \_ 磁片區 \_ 卸載**</span><span class="sxs-lookup"><span data-stu-id="1c561-159"><span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**GUID\_IO\_VOLUME\_DISMOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-160">d16a55e8-1059-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="1c561-160">d16a55e8-1059-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="1c561-161">嘗試卸載磁片區正在進行中。</span><span class="sxs-lookup"><span data-stu-id="1c561-161">An attempt to dismount the volume is in progress.</span></span> <span data-ttu-id="1c561-162">您應該關閉磁片區上的所有檔案和目錄控制碼。</span><span class="sxs-lookup"><span data-stu-id="1c561-162">You should close all handles to files and directories on the volume.</span></span> <span data-ttu-id="1c561-163">此事件之前不一定會有 **GUID \_ IO 磁片區 \_ \_ 鎖定** 事件。</span><span class="sxs-lookup"><span data-stu-id="1c561-163">This event will not necessarily be preceded by a **GUID\_IO\_VOLUME\_LOCK** event.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-164"><span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**GUID \_ IO \_ 磁片區 \_ 卸載 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="1c561-164"><span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**GUID\_IO\_VOLUME\_DISMOUNT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-165">e3c5b178-105d-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="1c561-165">e3c5b178-105d-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="1c561-166">嘗試卸載磁片區失敗。</span><span class="sxs-lookup"><span data-stu-id="1c561-166">An attempt to dismount a volume failed.</span></span> <span data-ttu-id="1c561-167">發生這種情況的原因通常是因為另一個進程關閉未完成的控制碼，而無法回應 **GUID \_ IO \_ 磁片區 \_ 卸載** 通知。</span><span class="sxs-lookup"><span data-stu-id="1c561-167">This often happens because another process failed to respond to a **GUID\_IO\_VOLUME\_DISMOUNT** notice by closing its outstanding handles.</span></span> <span data-ttu-id="1c561-168">因為卸載失敗，所以您可以重新開啟受影響磁片區的任何控制碼。</span><span class="sxs-lookup"><span data-stu-id="1c561-168">Because the dismount failed, you may reopen any handles to the affected volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-169"><span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**GUID \_ IO \_ 磁片區 \_ FVE \_ 狀態 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="1c561-169"><span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**GUID\_IO\_VOLUME\_FVE\_STATUS\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-170">062998b2-ee1f-4b6a-b857-e76cbbe9a6da</span><span class="sxs-lookup"><span data-stu-id="1c561-170">062998b2-ee1f-4b6a-b857-e76cbbe9a6da</span></span>
</dt> <dt>



<span data-ttu-id="1c561-171">磁片區的 BitLocker 磁碟機加密狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="1c561-171">The volume's BitLocker Drive Encryption status has changed.</span></span> <span data-ttu-id="1c561-172">當 BitLocker 啟用或停用，或加密開始、結束、暫停或繼續時，就會發出此事件的信號。</span><span class="sxs-lookup"><span data-stu-id="1c561-172">This event is signaled when BitLocker is enabled or disabled, or when encryption begins, ends, pauses, or resumes.</span></span>

<span data-ttu-id="1c561-173">**Windows Server 2003 和 WINDOWS XP：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="1c561-173">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-174"><span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**GUID \_ IO \_ 磁片區 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="1c561-174"><span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**GUID\_IO\_VOLUME\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-175">50708874-c9af-11d1-8fef-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="1c561-175">50708874-c9af-11d1-8fef-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="1c561-176">另一個進程正在嘗試鎖定磁片區。</span><span class="sxs-lookup"><span data-stu-id="1c561-176">Another process is attempting to lock the volume.</span></span> <span data-ttu-id="1c561-177">您應該關閉磁片區上的所有檔案和目錄控制碼。</span><span class="sxs-lookup"><span data-stu-id="1c561-177">You should close all handles to files and directories on the volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-178"><span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**GUID \_ IO \_ 磁片區 \_ 鎖定 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="1c561-178"><span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**GUID\_IO\_VOLUME\_LOCK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-179">ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="1c561-179">ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="1c561-180">嘗試鎖定磁片區失敗。</span><span class="sxs-lookup"><span data-stu-id="1c561-180">An attempt to lock a volume failed.</span></span> <span data-ttu-id="1c561-181">發生這種情況的原因通常是因為另一個進程關閉未處理的控制碼，而無法回應 **GUID \_ IO \_ 磁片區 \_ 鎖定** 事件。</span><span class="sxs-lookup"><span data-stu-id="1c561-181">This often happens because another process failed to respond to a **GUID\_IO\_VOLUME\_LOCK** event by closing its outstanding handles.</span></span> <span data-ttu-id="1c561-182">因為鎖定失敗，所以您可以重新開啟受影響磁片區的任何控制碼。</span><span class="sxs-lookup"><span data-stu-id="1c561-182">Because the lock failed, you may reopen any handles to the affected volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-183"><span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**GUID \_ IO \_ 磁片區 \_ 掛接**</span><span class="sxs-lookup"><span data-stu-id="1c561-183"><span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**GUID\_IO\_VOLUME\_MOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-184">b5804878-1a96-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="1c561-184">b5804878-1a96-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="1c561-185">磁片區已由另一個進程裝載。</span><span class="sxs-lookup"><span data-stu-id="1c561-185">The volume has been mounted by another process.</span></span> <span data-ttu-id="1c561-186">您可以開啟一個或多個控制碼。</span><span class="sxs-lookup"><span data-stu-id="1c561-186">You may open one or more handles to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-187"><span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**GUID \_ IO \_ 磁片區 \_ 名稱 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="1c561-187"><span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**GUID\_IO\_VOLUME\_NAME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-188">2de97f83-4c06-11d2-a532-00609713055a</span><span class="sxs-lookup"><span data-stu-id="1c561-188">2de97f83-4c06-11d2-a532-00609713055a</span></span>
</dt> <dt>



<span data-ttu-id="1c561-189">磁片區名稱已變更。</span><span class="sxs-lookup"><span data-stu-id="1c561-189">The volume name has been changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-190"><span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**GUID \_ IO \_ 磁片區 \_ 需要 \_ CHKDSK**</span><span class="sxs-lookup"><span data-stu-id="1c561-190"><span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**GUID\_IO\_VOLUME\_NEED\_CHKDSK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-191">799a0960-0a0b-4e03-ad88-2fa7c6ce748a</span><span class="sxs-lookup"><span data-stu-id="1c561-191">799a0960-0a0b-4e03-ad88-2fa7c6ce748a</span></span>
</dt> <dt>



<span data-ttu-id="1c561-192">檔案系統在磁片區上偵測到損毀。</span><span class="sxs-lookup"><span data-stu-id="1c561-192">A file system has detected corruption on the volume.</span></span> <span data-ttu-id="1c561-193">應用程式應該會在磁片區上執行 CHKDSK，或通知使用者這麼做。</span><span class="sxs-lookup"><span data-stu-id="1c561-193">The application should run CHKDSK on the volume or notify the user to do so.</span></span>

<span data-ttu-id="1c561-194">**Windows Server 2003 和 WINDOWS XP：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="1c561-194">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-195"><span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**GUID \_ IO \_ 磁片區 \_ 實體設定 \_ \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="1c561-195"><span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**GUID\_IO\_VOLUME\_PHYSICAL\_CONFIGURATION\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-196">2de97f84-4c06-11d2-a532-00609713055a</span><span class="sxs-lookup"><span data-stu-id="1c561-196">2de97f84-4c06-11d2-a532-00609713055a</span></span>
</dt> <dt>



<span data-ttu-id="1c561-197">磁片區的實體構成或目前實體狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="1c561-197">The physical makeup or current physical state of the volume has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-198"><span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**GUID \_ IO \_ 磁片區 \_ 準備 \_ 退出**</span><span class="sxs-lookup"><span data-stu-id="1c561-198"><span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**GUID\_IO\_VOLUME\_PREPARING\_EJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-199">c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6</span><span class="sxs-lookup"><span data-stu-id="1c561-199">c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6</span></span>
</dt> <dt>



<span data-ttu-id="1c561-200">檔案系統正在準備要取出的光碟。</span><span class="sxs-lookup"><span data-stu-id="1c561-200">The file system is preparing the disc to be ejected.</span></span> <span data-ttu-id="1c561-201">例如，檔案系統正在停止背景格式化作業，或在一次性寫入媒體上關閉會話。</span><span class="sxs-lookup"><span data-stu-id="1c561-201">For example, the file system is stopping a background formatting operation or closing the session on write-once media.</span></span>

<span data-ttu-id="1c561-202">**Windows Server 2003 和 WINDOWS XP：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="1c561-202">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-203"><span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**GUID \_ IO \_ 磁片區 \_ 唯一 \_ 識別碼 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="1c561-203"><span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**GUID\_IO\_VOLUME\_UNIQUE\_ID\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-204">af39da42-6622-41f5-970b-139d092fa3d9</span><span class="sxs-lookup"><span data-stu-id="1c561-204">af39da42-6622-41f5-970b-139d092fa3d9</span></span>
</dt> <dt>



<span data-ttu-id="1c561-205">磁片區的唯一識別碼已變更。</span><span class="sxs-lookup"><span data-stu-id="1c561-205">The volume's unique identifier has been changed.</span></span> <span data-ttu-id="1c561-206">如需有關唯一識別碼的詳細資訊，請參閱 [**IOCTL \_ MOUNTDEV \_ QUERY \_ unique \_ ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id)。</span><span class="sxs-lookup"><span data-stu-id="1c561-206">For more information about the unique identifier, see [**IOCTL\_MOUNTDEV\_QUERY\_UNIQUE\_ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).</span></span>

<span data-ttu-id="1c561-207">**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 在 Windows Server 2008 R2 和 Windows 7 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="1c561-207">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported until Windows Server 2008 R2 and Windows 7.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-208"><span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**GUID \_ IO \_ 磁片區 \_ 解除鎖定**</span><span class="sxs-lookup"><span data-stu-id="1c561-208"><span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**GUID\_IO\_VOLUME\_UNLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-209">9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="1c561-209">9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="1c561-210">另一個進程已解除鎖定磁片區。</span><span class="sxs-lookup"><span data-stu-id="1c561-210">The volume has been unlocked by another process.</span></span> <span data-ttu-id="1c561-211">您可以開啟一個或多個控制碼。</span><span class="sxs-lookup"><span data-stu-id="1c561-211">You may open one or more handles to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c561-212"><span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**GUID \_ IO \_ 磁片區 \_ 磨損 \_**</span><span class="sxs-lookup"><span data-stu-id="1c561-212"><span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**GUID\_IO\_VOLUME\_WEARING\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c561-213">873113ca-1486-4508-82ac-c3b2e5297aaa</span><span class="sxs-lookup"><span data-stu-id="1c561-213">873113ca-1486-4508-82ac-c3b2e5297aaa</span></span>
</dt> <dt>



<span data-ttu-id="1c561-214">媒體正在磨損。當檔案系統判斷磁片區的錯誤率太高，或其瑕疵更換空間即將耗盡時，就會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="1c561-214">The media is wearing out. This event is sent when a file system determines that the error rate on a volume is too high, or its defect replacement space is almost exhausted.</span></span>

<span data-ttu-id="1c561-215">**Windows Server 2003 和 WINDOWS XP：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="1c561-215">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c561-216">備註</span><span class="sxs-lookup"><span data-stu-id="1c561-216">Remarks</span></span>

<span data-ttu-id="1c561-217">**Guid io \_ 磁片 \_ 區 \_ 卸載** 和 **guid \_ io \_ 磁片區 \_ 卸載 \_ 失敗** 的事件是相關的，因為 **guid \_ io 磁片區 \_ \_ 鎖定** 和 **guid \_ io 磁片區 \_ \_ 鎖定 \_ 失敗** 事件。</span><span class="sxs-lookup"><span data-stu-id="1c561-217">The **GUID\_IO\_VOLUME\_DISMOUNT** and **GUID\_IO\_VOLUME\_DISMOUNT\_FAILED** events are related, as are the **GUID\_IO\_VOLUME\_LOCK** and **GUID\_IO\_VOLUME\_LOCK\_FAILED** event.</span></span> <span data-ttu-id="1c561-218">**Guid \_ io 磁片 \_ 區 \_ 卸載** 和 **guid \_ io \_ 磁片區 \_ 鎖定** 事件指出正在嘗試操作。</span><span class="sxs-lookup"><span data-stu-id="1c561-218">The **GUID\_IO\_VOLUME\_DISMOUNT** and **GUID\_IO\_VOLUME\_LOCK** events indicate that an operation is being attempted.</span></span> <span data-ttu-id="1c561-219">您應該對事件通知採取動作，並記錄所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="1c561-219">You should act on the event notification, and record the action taken.</span></span> <span data-ttu-id="1c561-220">**Guid \_ io 磁片 \_ 區 \_ 卸載 \_ 失敗**， **guid \_ io \_ 磁片區 \_ 鎖定 \_ 失敗** 事件表示嘗試的作業失敗。</span><span class="sxs-lookup"><span data-stu-id="1c561-220">The **GUID\_IO\_VOLUME\_DISMOUNT\_FAILED** and **GUID\_IO\_VOLUME\_LOCK\_FAILED** events indicate that the attempted operation failed.</span></span> <span data-ttu-id="1c561-221">然後，您可以使用記錄來復原您針對操作所做的動作。</span><span class="sxs-lookup"><span data-stu-id="1c561-221">You may then use your record to undo the actions you made in response to the operation.</span></span>

<span data-ttu-id="1c561-222">[**開發 \_ 廣播 \_ 控點**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle)結構的 **dbch \_ hdevnotify** 成員指出受影響的裝置。</span><span class="sxs-lookup"><span data-stu-id="1c561-222">The **dbch\_hdevnotify** member of the [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure indicates the affected device.</span></span> <span data-ttu-id="1c561-223">請注意，這是 [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)所傳回的裝置通知控制碼，而不是磁片區控制碼。</span><span class="sxs-lookup"><span data-stu-id="1c561-223">Note that this is the device notification handle returned by [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), not a volume handle.</span></span> <span data-ttu-id="1c561-224">若要在磁片區上執行作業，請將這個控制碼對應到相對應的磁片區控制碼。</span><span class="sxs-lookup"><span data-stu-id="1c561-224">To perform operations on the volume, map this handle to the corresponding volume handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c561-225">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c561-225">Requirements</span></span>



| <span data-ttu-id="1c561-226">需求</span><span class="sxs-lookup"><span data-stu-id="1c561-226">Requirement</span></span> | <span data-ttu-id="1c561-227">值</span><span class="sxs-lookup"><span data-stu-id="1c561-227">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1c561-228">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c561-228">Minimum supported client</span></span><br/> | <span data-ttu-id="1c561-229">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c561-229">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="1c561-230">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c561-230">Minimum supported server</span></span><br/> | <span data-ttu-id="1c561-231">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1c561-231">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="1c561-232">標頭</span><span class="sxs-lookup"><span data-stu-id="1c561-232">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c561-233"><dt>IoEvent。h</dt></span><span class="sxs-lookup"><span data-stu-id="1c561-233"><dt>IoEvent.h</dt></span></span> </dl> |



 

