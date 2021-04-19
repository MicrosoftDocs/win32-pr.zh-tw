---
description: VDS 會提供物件來執行與服務相關的活動。 本主題說明每個物件。
ms.assetid: ae4d18f2-4d50-480c-bc7a-4eec0334707d
title: Startup 和 Service 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92beb0a4f825f767299a7ced74d43ef2487fa252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997581"
---
# <a name="startup-and-service-objects"></a><span data-ttu-id="2bc86-104">Startup 和 Service 物件</span><span class="sxs-lookup"><span data-stu-id="2bc86-104">Startup and Service Objects</span></span>

<span data-ttu-id="2bc86-105">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="2bc86-105">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="2bc86-106">VDS 會提供物件來執行與服務相關的活動。</span><span class="sxs-lookup"><span data-stu-id="2bc86-106">VDS provides objects for performing service-related activities.</span></span> <span data-ttu-id="2bc86-107">本主題說明每個物件。</span><span class="sxs-lookup"><span data-stu-id="2bc86-107">This topic describes each object.</span></span>

## <a name="service-loader-object"></a><span data-ttu-id="2bc86-108">服務載入器物件</span><span class="sxs-lookup"><span data-stu-id="2bc86-108">Service Loader Object</span></span>

<span data-ttu-id="2bc86-109">服務載入器物件提供應用程式用來載入和初始化 VDS 的方法。</span><span class="sxs-lookup"><span data-stu-id="2bc86-109">The service loader object provides the methods that are used by applications to load and initialize VDS.</span></span> <span data-ttu-id="2bc86-110">若要準備 VDS 以供使用，應用程式必須執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="2bc86-110">To prepare VDS for use, an application must perform the following operations:</span></span>

-   <span data-ttu-id="2bc86-111">建立服務載入器物件的實例，它會傳回 [**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader) 介面。</span><span class="sxs-lookup"><span data-stu-id="2bc86-111">Create an instance of the service loader object, which returns the [**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader) interface.</span></span>
-   <span data-ttu-id="2bc86-112">呼叫 [**IVdsServiceLoader：： LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) 方法以載入服務。</span><span class="sxs-lookup"><span data-stu-id="2bc86-112">Call the [**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) method to load the service.</span></span>

<span data-ttu-id="2bc86-113">如需程式碼範例，請參閱 [載入 VDS](loading-vds.md)。</span><span class="sxs-lookup"><span data-stu-id="2bc86-113">For a code example, see [Loading VDS](loading-vds.md).</span></span>

<span data-ttu-id="2bc86-114">一律允許服務在呼叫服務物件所公開的方法之前，完全初始化。</span><span class="sxs-lookup"><span data-stu-id="2bc86-114">Always allow the service to initialize completely before calling the methods that are exposed by the service object.</span></span> <span data-ttu-id="2bc86-115">您可以使用 [**IVdsService：： IsServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-isserviceready) 方法來判斷載入進程的狀態。</span><span class="sxs-lookup"><span data-stu-id="2bc86-115">Use the [**IVdsService::IsServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-isserviceready) method to determine the status of the load process.</span></span> <span data-ttu-id="2bc86-116">使用 [**IVdsService：： WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) 方法來封鎖對 VDS 物件的呼叫，直到初始化完成為止。</span><span class="sxs-lookup"><span data-stu-id="2bc86-116">Use the [**IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) method to block calls to VDS objects until the initialization completes.</span></span>

<span data-ttu-id="2bc86-117">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="2bc86-117">The following table lists related interfaces, enumerations, and structures.</span></span>

| <span data-ttu-id="2bc86-118">類型</span><span class="sxs-lookup"><span data-stu-id="2bc86-118">Type</span></span>                                              | <span data-ttu-id="2bc86-119">元素</span><span class="sxs-lookup"><span data-stu-id="2bc86-119">Element</span></span>                                         |
|---------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="2bc86-120">一律由這個物件公開的介面</span><span class="sxs-lookup"><span data-stu-id="2bc86-120">Interfaces that are always exposed by this object</span></span> | <span data-ttu-id="2bc86-121">[**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader)。</span><span class="sxs-lookup"><span data-stu-id="2bc86-121">[**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader).</span></span> |
| <span data-ttu-id="2bc86-122">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="2bc86-122">Associated enumerations</span></span>                           | <span data-ttu-id="2bc86-123">無。</span><span class="sxs-lookup"><span data-stu-id="2bc86-123">None.</span></span>                                           |
| <span data-ttu-id="2bc86-124">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="2bc86-124">Associated structures</span></span>                             | <span data-ttu-id="2bc86-125">無。</span><span class="sxs-lookup"><span data-stu-id="2bc86-125">None.</span></span>                                           |



 

## <a name="service-object"></a><span data-ttu-id="2bc86-126">服務物件</span><span class="sxs-lookup"><span data-stu-id="2bc86-126">Service Object</span></span>

<span data-ttu-id="2bc86-127">服務物件是所有 VDS 應用程式核心的多工物件。</span><span class="sxs-lookup"><span data-stu-id="2bc86-127">The service object is a multifunctional object that is central to all VDS applications.</span></span> <span data-ttu-id="2bc86-128">使用這個物件時，呼叫端可以執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="2bc86-128">With this object, a caller can perform the following operations:</span></span>

-   <span data-ttu-id="2bc86-129">判斷服務初始化的狀態。</span><span class="sxs-lookup"><span data-stu-id="2bc86-129">Determine the status of the service initialization.</span></span>
-   <span data-ttu-id="2bc86-130">取得以 VDS 註冊的所有硬體或軟體提供者。</span><span class="sxs-lookup"><span data-stu-id="2bc86-130">Retrieve all hardware or software providers registered with VDS.</span></span>
-   <span data-ttu-id="2bc86-131">報告未配置的磁片。</span><span class="sxs-lookup"><span data-stu-id="2bc86-131">Report on unallocated disks.</span></span>
-   <span data-ttu-id="2bc86-132">傳回與磁片上的磁片區相關聯的檔案系統類型和磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="2bc86-132">Return the file system type and drive letter associated with volumes on a disk.</span></span>
-   <span data-ttu-id="2bc86-133">從登錄中移除未使用的使用者模式路徑和裝載的資料夾，然後重新整理磁片。</span><span class="sxs-lookup"><span data-stu-id="2bc86-133">Remove unused user-mode paths and mounted folders from the registry and refresh disks.</span></span>
-   <span data-ttu-id="2bc86-134">接收 VDS 通知。</span><span class="sxs-lookup"><span data-stu-id="2bc86-134">Receive VDS notifications.</span></span>
-   <span data-ttu-id="2bc86-135">重新開機主機。</span><span class="sxs-lookup"><span data-stu-id="2bc86-135">Reboot the host.</span></span>
-   <span data-ttu-id="2bc86-136">在本機電腦上取出光纖通道 HBA 埠或 iSCSI 啟動器介面卡。</span><span class="sxs-lookup"><span data-stu-id="2bc86-136">Retrieve Fibre Channel HBA ports or iSCSI initiator adapters on the local computer.</span></span>
-   <span data-ttu-id="2bc86-137">安全地準備在本機電腦上公開為磁片的 Lun，以供移除。</span><span class="sxs-lookup"><span data-stu-id="2bc86-137">Safely prepare LUNs exposed as disks on the local computer for removal.</span></span>

<span data-ttu-id="2bc86-138">VDS 通知結構會將物件 Guid 傳遞給已向 VDS 註冊的所有應用程式，以接收通知。</span><span class="sxs-lookup"><span data-stu-id="2bc86-138">VDS notification structures pass object GUIDs to all applications that are registered with VDS to receive notifications.</span></span> <span data-ttu-id="2bc86-139">使用 [**IVdsService：： GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) 方法將物件 GUID 轉換為物件指標。</span><span class="sxs-lookup"><span data-stu-id="2bc86-139">Use the [**IVdsService::GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) method to convert an object GUID to an object pointer.</span></span> <span data-ttu-id="2bc86-140">如需通知模型的完整說明，請參閱 [VDS 通知](vds-notification-model.md)。</span><span class="sxs-lookup"><span data-stu-id="2bc86-140">For a more complete description of the notification model, see [VDS Notifications](vds-notification-model.md).</span></span>

<span data-ttu-id="2bc86-141">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="2bc86-141">The following table lists related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="2bc86-142">類型</span><span class="sxs-lookup"><span data-stu-id="2bc86-142">Type</span></span>                                                                   | <span data-ttu-id="2bc86-143">元素</span><span class="sxs-lookup"><span data-stu-id="2bc86-143">Element</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc86-144">一律由這個物件公開的介面</span><span class="sxs-lookup"><span data-stu-id="2bc86-144">Interfaces that are always exposed by this object</span></span>                      | <span data-ttu-id="2bc86-145">[**IVdsService**](/windows/desktop/api/Vds/nn-vds-ivdsservice)、 [**IVdsServiceHba**](/windows/desktop/api/Vds/nn-vds-ivdsservicehba) \* 、 [**IVdsServiceIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsserviceiscsi) \* 、 [**IVdsServiceUninstallDisk**](/windows/desktop/api/Vds/nn-vds-ivdsserviceuninstalldisk) \* 。</span><span class="sxs-lookup"><span data-stu-id="2bc86-145">[**IVdsService**](/windows/desktop/api/Vds/nn-vds-ivdsservice), [**IVdsServiceHba**](/windows/desktop/api/Vds/nn-vds-ivdsservicehba)\*, [**IVdsServiceIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsserviceiscsi)\*, [**IVdsServiceUninstallDisk**](/windows/desktop/api/Vds/nn-vds-ivdsserviceuninstalldisk)\*.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="2bc86-146">一律會執行但不會對應用程式公開的介面</span><span class="sxs-lookup"><span data-stu-id="2bc86-146">Interfaces that are always implemented but not exposed to applications</span></span> | [<span data-ttu-id="2bc86-147">**IVdsAdmin**</span><span class="sxs-lookup"><span data-stu-id="2bc86-147">**IVdsAdmin**</span></span>](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsadmin)                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="2bc86-148">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="2bc86-148">Associated enumerations</span></span>                                                | <span data-ttu-id="2bc86-149">[**VDS \_查詢 \_ 提供者 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag)標， [**VDS \_ 物件 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_object_type)， [**VDS \_ 服務 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_service_flag)標， [**VDS \_ 磁碟機 \_ 號 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_drive_letter_flag)標， [**VDS \_ 檔 \_ 系統 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_file_system_flag)標， [**VDS \_ 檔 \_ 系統 \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_file_system_prop_flag)的旗標。</span><span class="sxs-lookup"><span data-stu-id="2bc86-149">[**VDS\_QUERY\_PROVIDER\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag), [**VDS\_OBJECT\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_object_type), [**VDS\_SERVICE\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_service_flag), [**VDS\_DRIVE\_LETTER\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_letter_flag), [**VDS\_FILE\_SYSTEM\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_file_system_flag), [**VDS\_FILE\_SYSTEM\_PROP\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_file_system_prop_flag).</span></span>                                                      |
| <span data-ttu-id="2bc86-150">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="2bc86-150">Associated structures</span></span>                                                  | <span data-ttu-id="2bc86-151">[**VDS \_服務 \_**](/windows/desktop/api/Vds/ns-vds-vds_service_prop)類別、 [**VDS \_ 檔 \_ 系統的 \_ 主張**](/windows/desktop/api/Vds/ns-vds-vds_file_system_prop)、 [**VDS \_ 檔 \_ 系統 \_ 類型 \_**](/windows/desktop/api/Vds/ns-vds-vds_file_system_type_prop)、 [**VDS \_ 磁片磁碟機 \_ 信件 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification)、 [**VDS \_ 檔 \_ 系統 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)、 [**VDS \_ 裝入 \_ 點 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification)。</span><span class="sxs-lookup"><span data-stu-id="2bc86-151">[**VDS\_SERVICE\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_service_prop), [**VDS\_FILE\_SYSTEM\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_file_system_prop), [**VDS\_FILE\_SYSTEM\_TYPE\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_file_system_type_prop), [**VDS\_DRIVE\_LETTER\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification), [**VDS\_FILE\_SYSTEM\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification), [**VDS\_MOUNT\_POINT\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification).</span></span> |



 

<span data-ttu-id="2bc86-152">**\* Windows server 2003：** 在 Windows server 2003 R2 之前，不支援這些介面。</span><span class="sxs-lookup"><span data-stu-id="2bc86-152">**\*Windows Server 2003:** These interfaces are not supported until Windows Server 2003 R2.</span></span>

## <a name="initiator-adapter-object"></a><span data-ttu-id="2bc86-153">啟動器介面卡物件</span><span class="sxs-lookup"><span data-stu-id="2bc86-153">Initiator Adapter Object</span></span>

<span data-ttu-id="2bc86-154">啟動器介面卡物件會在 VDS 服務的主機電腦上，為 iSCSI 啟動器介面卡建模。</span><span class="sxs-lookup"><span data-stu-id="2bc86-154">An initiator adapter object models an iSCSI initiator adapter on the host machine of the VDS service.</span></span> <span data-ttu-id="2bc86-155">VDS 服務只能在本機電腦上查看啟動器介面卡。</span><span class="sxs-lookup"><span data-stu-id="2bc86-155">The VDS service can only view initiator adapters on the local machine.</span></span> <span data-ttu-id="2bc86-156">啟動器介面卡物件的角色是用來管理從本機電腦到 iSCSI 目標的登入會話。</span><span class="sxs-lookup"><span data-stu-id="2bc86-156">The role of an initiator adapter object is for managing login sessions from the local computer to iSCSI targets.</span></span>

<span data-ttu-id="2bc86-157">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="2bc86-157">The following table lists related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="2bc86-158">類型</span><span class="sxs-lookup"><span data-stu-id="2bc86-158">Type</span></span>                                              | <span data-ttu-id="2bc86-159">元素</span><span class="sxs-lookup"><span data-stu-id="2bc86-159">Element</span></span>                                                                                                                                                                  |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc86-160">一律由這個物件公開的介面</span><span class="sxs-lookup"><span data-stu-id="2bc86-160">Interfaces that are always exposed by this object</span></span> | <span data-ttu-id="2bc86-161">[**IVdsIscsiInitiatorAdapter**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatoradapter) \* 。</span><span class="sxs-lookup"><span data-stu-id="2bc86-161">[**IVdsIscsiInitiatorAdapter**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatoradapter)\*.</span></span>                                                                                                        |
| <span data-ttu-id="2bc86-162">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="2bc86-162">Associated enumerations</span></span>                           | <span data-ttu-id="2bc86-163">[**VDS \_ISCSI \_ 登入 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_type)。</span><span class="sxs-lookup"><span data-stu-id="2bc86-163">[**VDS\_ISCSI\_LOGIN\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_type).</span></span> <span data-ttu-id="2bc86-164">[**VDS \_ISCSI \_ 登入 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_flag)標， [**VDS \_ ISCSI \_ 驗證 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_auth_type)。</span><span class="sxs-lookup"><span data-stu-id="2bc86-164">[**VDS\_ISCSI\_LOGIN\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_flag), [**VDS\_ISCSI\_AUTH\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_auth_type).</span></span> |
| <span data-ttu-id="2bc86-165">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="2bc86-165">Associated structures</span></span>                             | <span data-ttu-id="2bc86-166">[**VDS \_ISCSI \_ 啟動器 \_ 適配 \_ 卡**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_adapter_prop)。</span><span class="sxs-lookup"><span data-stu-id="2bc86-166">[**VDS\_ISCSI\_INITIATOR\_ADAPTER\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_adapter_prop).</span></span>                                                                                        |



 

<span data-ttu-id="2bc86-167">**\* Windows server 2003：** 在 Windows server 2003 R2 之前，不支援此介面。</span><span class="sxs-lookup"><span data-stu-id="2bc86-167">**\*Windows Server 2003:** This interface is not supported until Windows Server 2003 R2.</span></span>

## <a name="initiator-portal-object"></a><span data-ttu-id="2bc86-168">啟動器入口網站物件</span><span class="sxs-lookup"><span data-stu-id="2bc86-168">Initiator Portal Object</span></span>

<span data-ttu-id="2bc86-169">啟動器入口網站物件會將 iscsi 啟動器上的 iSCSI 啟動器入口網站模型。</span><span class="sxs-lookup"><span data-stu-id="2bc86-169">An initiator portal object models an iSCSI initiator portal on an iSCSI initiator.</span></span> <span data-ttu-id="2bc86-170">啟動器入口網站是一種 IP 位址和埠的組合，主機電腦會透過此通訊埠連接到 iSCSI 子系統上的入口網站。</span><span class="sxs-lookup"><span data-stu-id="2bc86-170">An initiator portal is the combination of an IP address and port through which a host computer connects to a portal on an iSCSI subsystem.</span></span> <span data-ttu-id="2bc86-171">啟動器入口網站物件的角色是作為 MPIO 路徑的其中一個端點，以及設定 IPSEC 安全性設定。</span><span class="sxs-lookup"><span data-stu-id="2bc86-171">The role of an initiator portal object is to serve as one of the endpoints of an MPIO path and to configure IPSEC security settings.</span></span>

<span data-ttu-id="2bc86-172">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="2bc86-172">The following table lists the related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="2bc86-173">類型</span><span class="sxs-lookup"><span data-stu-id="2bc86-173">Type</span></span>                                              | <span data-ttu-id="2bc86-174">元素</span><span class="sxs-lookup"><span data-stu-id="2bc86-174">Element</span></span>                                                                                                                                                                         |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc86-175">一律由這個物件公開的介面</span><span class="sxs-lookup"><span data-stu-id="2bc86-175">Interfaces that are always exposed by this object</span></span> | <span data-ttu-id="2bc86-176">[**IVdsIscsiInitiatorPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatorportal) \* 。</span><span class="sxs-lookup"><span data-stu-id="2bc86-176">[**IVdsIscsiInitiatorPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatorportal)\*.</span></span>                                                                                                                 |
| <span data-ttu-id="2bc86-177">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="2bc86-177">Associated enumerations</span></span>                           | <span data-ttu-id="2bc86-178">[**VDS \_ISCSI \_ IPSEC \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_ipsec_flag)標。</span><span class="sxs-lookup"><span data-stu-id="2bc86-178">[**VDS\_ISCSI\_IPSEC\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_ipsec_flag).</span></span>                                                                                                                        |
| <span data-ttu-id="2bc86-179">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="2bc86-179">Associated structures</span></span>                             | <span data-ttu-id="2bc86-180">[**VDS \_ISCSI \_ 啟動器 \_ 入口網站的 \_ 主張**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_portal_prop)、 [**VDS \_ ISCSI \_ IPSEC \_ 金鑰**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_ipsec_key)、 [**VDS \_ IPADDRESS**](/windows/desktop/api/Vds/ns-vds-vds_ipaddress)。</span><span class="sxs-lookup"><span data-stu-id="2bc86-180">[**VDS\_ISCSI\_INITIATOR\_PORTAL\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_portal_prop), [**VDS\_ISCSI\_IPSEC\_KEY**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_ipsec_key), [**VDS\_IPADDRESS**](/windows/desktop/api/Vds/ns-vds-vds_ipaddress).</span></span> |



 

<span data-ttu-id="2bc86-181">**\* Windows server 2003：** 在 Windows server 2003 R2 之前，不支援此介面。</span><span class="sxs-lookup"><span data-stu-id="2bc86-181">**\*Windows Server 2003:** This interface is not supported until Windows Server 2003 R2.</span></span>

## <a name="hba-port-object"></a><span data-ttu-id="2bc86-182">HBA 埠物件</span><span class="sxs-lookup"><span data-stu-id="2bc86-182">HBA Port Object</span></span>

<span data-ttu-id="2bc86-183">HBA 埠物件會建立光纖通道的主機匯流排介面卡 (HBA) 埠的模型。</span><span class="sxs-lookup"><span data-stu-id="2bc86-183">The HBA port object models a Fibre Channel host bus adapter (HBA) port.</span></span>

<span data-ttu-id="2bc86-184">使用 [**IVdsServiceHba：： QueryHbaPorts**](/windows/desktop/api/Vds/nf-vds-ivdsservicehba-queryhbaports) 方法來判斷本機電腦上的 VDS 已知的 HBA 埠。</span><span class="sxs-lookup"><span data-stu-id="2bc86-184">Use the [**IVdsServiceHba::QueryHbaPorts**](/windows/desktop/api/Vds/nf-vds-ivdsservicehba-queryhbaports) method to determine the HBA ports that are known to VDS on the local computer.</span></span>

<span data-ttu-id="2bc86-185">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="2bc86-185">The following table lists the related interfaces, enumerations, and structures.</span></span>

| <span data-ttu-id="2bc86-186">類型</span><span class="sxs-lookup"><span data-stu-id="2bc86-186">Type</span></span>                                              | <span data-ttu-id="2bc86-187">元素</span><span class="sxs-lookup"><span data-stu-id="2bc86-187">Element</span></span>                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc86-188">一律由這個物件公開的介面</span><span class="sxs-lookup"><span data-stu-id="2bc86-188">Interfaces that are always exposed by this object</span></span> | <span data-ttu-id="2bc86-189">[**IVdsHbaPort**](/windows/desktop/api/Vds/nn-vds-ivdshbaport) \* 。</span><span class="sxs-lookup"><span data-stu-id="2bc86-189">[**IVdsHbaPort**](/windows/desktop/api/Vds/nn-vds-ivdshbaport)\*.</span></span>                                                                                                                            |
| <span data-ttu-id="2bc86-190">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="2bc86-190">Associated enumerations</span></span>                           | <span data-ttu-id="2bc86-191">[**VDS \_HBAPORT \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_type)、 [**VDS \_ HBAPORT \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_status)、 [**VDS \_ HBAPORT \_ SPEED \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_speed_flag)標。</span><span class="sxs-lookup"><span data-stu-id="2bc86-191">[**VDS\_HBAPORT\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_type), [**VDS\_HBAPORT\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_status), [**VDS\_HBAPORT\_SPEED\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_speed_flag).</span></span> |
| <span data-ttu-id="2bc86-192">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="2bc86-192">Associated structures</span></span>                             | <span data-ttu-id="2bc86-193">[**VDS \_HBAPORT 的 \_ 主張**](/windows/desktop/api/Vds/ns-vds-vds_hbaport_prop)。</span><span class="sxs-lookup"><span data-stu-id="2bc86-193">[**VDS\_HBAPORT\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_hbaport_prop).</span></span>                                                                                                                  |



 

<span data-ttu-id="2bc86-194">**\* Windows server 2003：** 在 Windows server 2003 R2 之前，不支援此介面。</span><span class="sxs-lookup"><span data-stu-id="2bc86-194">**\*Windows Server 2003:** This interface is not supported until Windows Server 2003 R2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bc86-195">相關主題</span><span class="sxs-lookup"><span data-stu-id="2bc86-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bc86-196">VDS 物件模型</span><span class="sxs-lookup"><span data-stu-id="2bc86-196">VDS Object Model</span></span>](vds-object-model.md)
</dt> <dt>

[<span data-ttu-id="2bc86-197">**IVdsServiceLoader::LoadService**</span><span class="sxs-lookup"><span data-stu-id="2bc86-197">**IVdsServiceLoader::LoadService**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[<span data-ttu-id="2bc86-198">正在載入 VDS</span><span class="sxs-lookup"><span data-stu-id="2bc86-198">Loading VDS</span></span>](loading-vds.md)
</dt> <dt>

[<span data-ttu-id="2bc86-199">**IVdsService：： GetObject**</span><span class="sxs-lookup"><span data-stu-id="2bc86-199">**IVdsService::GetObject**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject)
</dt> <dt>

[<span data-ttu-id="2bc86-200">VDS 通知</span><span class="sxs-lookup"><span data-stu-id="2bc86-200">VDS Notifications</span></span>](vds-notification-model.md)
</dt> </dl>

 

 
