---
description: 瞭解如何從您的 Windows 應用程式使用高速 NVMe 裝置。
ms.assetid: 037AF841-C2C9-4551-9CCB-F2A2F199083A
title: 使用 NVMe 磁片磁碟機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be94adf8355940bd93de137d122d91e468c2173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001355"
---
# <a name="working-with-nvme-drives"></a><span data-ttu-id="bf6f9-103">使用 NVMe 磁片磁碟機</span><span class="sxs-lookup"><span data-stu-id="bf6f9-103">Working with NVMe drives</span></span>

<span data-ttu-id="bf6f9-104">**適用範圍：**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-104">**Applies to:**</span></span>

-   <span data-ttu-id="bf6f9-105">Windows 10</span><span class="sxs-lookup"><span data-stu-id="bf6f9-105">Windows 10</span></span>
-   <span data-ttu-id="bf6f9-106">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bf6f9-106">Windows Server 2016</span></span>

<span data-ttu-id="bf6f9-107">瞭解如何從您的 Windows 應用程式使用高速 NVMe 裝置。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-107">Learn how to work with high-speed NVMe devices from your Windows application.</span></span> <span data-ttu-id="bf6f9-108">您可以透過 **StorNVMe.sys** 啟用裝置存取，並在 Windows Server 2012 R2 和 Windows 8.1 中首次引進驅動程式驅動程式。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-108">Device access is enabled via **StorNVMe.sys**, the in-box driver first introduced in Windows Server 2012 R2 and Windows 8.1.</span></span> <span data-ttu-id="bf6f9-109">Windows 7 裝置也可以透過 KB 熱修正來取得此功能。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-109">It's also available to Windows 7 devices through a KB hot fix.</span></span> <span data-ttu-id="bf6f9-110">在 Windows 10 中引進了幾項新功能，包括廠商專屬 NVMe 命令的傳遞機制，以及現有 IOCTLs 的更新。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-110">In Windows 10, several new features were introduced, including a pass-through mechanism for vendor-specific NVMe commands and updates to existing IOCTLs.</span></span>

<span data-ttu-id="bf6f9-111">本主題概要說明您可以用來存取 Windows 10 中 NVMe 磁片磁碟機的一般使用 Api。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-111">This topic provides an overview of general-use APIs that you can use to access NVMe drives in Windows 10.</span></span> <span data-ttu-id="bf6f9-112">它也會說明：</span><span class="sxs-lookup"><span data-stu-id="bf6f9-112">It also describes:</span></span>

-   <span data-ttu-id="bf6f9-113">如何使用[傳遞](#pass-through-mechanism)來傳送廠商專屬 NVMe 命令</span><span class="sxs-lookup"><span data-stu-id="bf6f9-113">How to send a vendor-specific NVMe command with [pass-through](#pass-through-mechanism)</span></span>
-   <span data-ttu-id="bf6f9-114">如何 [傳送識別、取得功能或取得記錄頁面命令](#protocol-specific-queries) 至 NVMe 磁片磁碟機</span><span class="sxs-lookup"><span data-stu-id="bf6f9-114">How to [send an Identify, Get Features, or Get Log Pages command](#protocol-specific-queries) to the NVMe drive</span></span>
-   <span data-ttu-id="bf6f9-115">如何從 NVMe 磁片磁碟機[取得溫度資訊](#temperature-queries)</span><span class="sxs-lookup"><span data-stu-id="bf6f9-115">How to [obtain temperature information](#temperature-queries) from an NVMe drive</span></span>
-   <span data-ttu-id="bf6f9-116">如何執行行為變更命令，例如 [設定溫度閾值](#behavior-changing-commands)</span><span class="sxs-lookup"><span data-stu-id="bf6f9-116">How to perform behavior changing commands, such as [setting temperature thresholds](#behavior-changing-commands)</span></span>

## <a name="apis-for-working-with-nvme-drives"></a><span data-ttu-id="bf6f9-117">使用 NVMe 磁片磁碟機的 Api</span><span class="sxs-lookup"><span data-stu-id="bf6f9-117">APIs for working with NVMe drives</span></span>

<span data-ttu-id="bf6f9-118">您可以使用下列一般用途的 Api，在 Windows 10 中存取 NVMe 磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-118">You can use the following general-use APIs to access NVMe drives in Windows 10.</span></span> <span data-ttu-id="bf6f9-119">您可以在使用者模式應用程式的 **winioctl** 中找到這些 api，並針對核心模式驅動程式使用 **ntddstor。**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-119">These APIs can be found in **winioctl.h** for user mode applications, and **ntddstor.h** for kernel mode drivers.</span></span> <span data-ttu-id="bf6f9-120">如需標頭檔的詳細資訊，請參閱 [標頭檔](#header-files)。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-120">For more information about header files, see [Header files](#header-files).</span></span>

-   <span data-ttu-id="bf6f9-121">[**IOCTL \_儲存體 \_ 通訊協定 \_ 命令**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) ：使用此 IOCTL 搭配 **儲存體 \_ 通訊協定 \_ 命令** 結構來發出 NVMe 命令。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-121">[**IOCTL\_STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : Use this IOCTL with the **STORAGE\_PROTOCOL\_COMMAND** structure to issue NVMe commands.</span></span> <span data-ttu-id="bf6f9-122">這個 IOCTL 可啟用 NVMe 傳遞，並支援在 NVMe 中使用命令效果記錄檔。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-122">This IOCTL enables NVMe pass-through and supports the Command Effects log in NVMe.</span></span> <span data-ttu-id="bf6f9-123">您可以將它與廠商特定的命令搭配使用。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-123">You can use it with vendor-specific commands.</span></span> <span data-ttu-id="bf6f9-124">如需詳細資訊，請參閱 [傳遞機制](#pass-through-mechanism)。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-124">For more info, see [Pass-through mechanism](#pass-through-mechanism).</span></span>

-   <span data-ttu-id="bf6f9-125">[**儲存體 \_通訊協定 \_ 命令**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) ：此輸入緩衝區結構包含 **ReturnStatus** 欄位，可用來報告下列狀態值。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-125">[**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : This input-buffer structure includes a **ReturnStatus** field that can be used report the following status values.</span></span>
    -   <span data-ttu-id="bf6f9-126">**儲存體 \_ 通訊協定 \_ 狀態 \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-126">**STORAGE\_PROTOCOL\_STATUS\_PENDING**</span></span>
    -   <span data-ttu-id="bf6f9-127">**儲存體 \_ 通訊協定 \_ 狀態 \_ 成功**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-127">**STORAGE\_PROTOCOL\_STATUS\_SUCCESS**</span></span>
    -   <span data-ttu-id="bf6f9-128">**儲存體 \_ 通訊協定 \_ 狀態 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-128">**STORAGE\_PROTOCOL\_STATUS\_ERROR**</span></span>
    -   <span data-ttu-id="bf6f9-129">**儲存體 \_ 通訊協定 \_ 狀態 \_ 不正確 \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-129">**STORAGE\_PROTOCOL\_STATUS\_INVALID\_REQUEST**</span></span>
    -   <span data-ttu-id="bf6f9-130">**儲存體 \_ 通訊協定 \_ 狀態 \_ 無 \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-130">**STORAGE\_PROTOCOL\_STATUS\_NO\_DEVICE**</span></span>
    -   <span data-ttu-id="bf6f9-131">**儲存體 \_ 通訊協定 \_ 狀態 \_ 忙碌中**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-131">**STORAGE\_PROTOCOL\_STATUS\_BUSY**</span></span>
    -   <span data-ttu-id="bf6f9-132">**儲存體 \_ 通訊協定 \_ 狀態 \_ 資料 \_ 溢出**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-132">**STORAGE\_PROTOCOL\_STATUS\_DATA\_OVERRUN**</span></span>
    -   <span data-ttu-id="bf6f9-133">**儲存體 \_ 通訊 \_ 協定 \_ 狀態 \_ 資源不足**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-133">**STORAGE\_PROTOCOL\_STATUS\_INSUFFICIENT\_RESOURCES**</span></span>
    -   <span data-ttu-id="bf6f9-134">**\_ \_ \_ 不支援儲存體通訊協定狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-134">**STORAGE\_PROTOCOL\_STATUS\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="bf6f9-135">[**IOCTL \_儲存體 \_ 查詢 \_ 屬性**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) ：使用此 IOCTL 搭配 **儲存體 \_ 屬性 \_ 查詢** 結構來取得裝置資訊。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-135">[**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : Use this IOCTL with the **STORAGE\_PROPERTY\_QUERY** structure to retrieve device information.</span></span> <span data-ttu-id="bf6f9-136">如需詳細資訊，請參閱 [通訊協定特定的查詢](#protocol-specific-queries) 和 [溫度查詢](#temperature-queries)。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-136">For more info, see [Protocol-specific queries](#protocol-specific-queries) and [Temperature queries](#temperature-queries).</span></span>

-   <span data-ttu-id="bf6f9-137">[**儲存體 \_屬性 \_ 查詢**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) ：此結構包含 **PropertyId** 和 **AdditionalParameters** 欄位，以指定要查詢的資料。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-137">[**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : This structure includes the **PropertyId** and **AdditionalParameters** fields to specify the data to be queried.</span></span> <span data-ttu-id="bf6f9-138">在 [ **PropertyId** ] 欄位中，使用 [ **儲存體 \_ 屬性 \_ 識別碼** ] 列舉來指定資料類型。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-138">In the **PropertyId** filed, use the **STORAGE\_PROPERTY\_ID** enumeration to specify the type of data.</span></span> <span data-ttu-id="bf6f9-139">您可以使用 [ **AdditionalParameters** ] 欄位來指定更多詳細資料，視資料類型而定。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-139">Use the **AdditionalParameters** field to specify more details, depending on the type of data.</span></span> <span data-ttu-id="bf6f9-140">針對通訊協定特定的資料，請使用 **AdditionalParameters** 欄位中的 **儲存體 \_ 通訊協定 \_ 特定 \_ 資料** 結構。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-140">For protocol-specific data, use the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** structure in the **AdditionalParameters** field.</span></span> <span data-ttu-id="bf6f9-141">針對溫度資料，請使用 **AdditionalParameters** 欄位中的 **儲存體 \_ 溫度 \_ 資訊** 結構。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-141">For temperature data, use the **STORAGE\_TEMPERATURE\_INFO** structure in the **AdditionalParameters** field.</span></span>
-   <span data-ttu-id="bf6f9-142">[**儲存體 \_屬性 \_ 識別碼**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) ：此列舉包含新的值，可讓 **IOCTL \_ 儲存體 \_ 查詢 \_ 屬性** 取得特定通訊協定和溫度資訊。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-142">[**STORAGE\_PROPERTY\_ID**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : This enumeration includes new values that allow **IOCTL\_STORAGE\_QUERY\_PROPERTY** to retrieve protocol-specific and temperature information.</span></span>

    -   <span data-ttu-id="bf6f9-143">**StorageAdapterProtocolSpecificProperty**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-143">**StorageAdapterProtocolSpecificProperty**</span></span>
    -   <span data-ttu-id="bf6f9-144">**StorageDeviceProtocolSpecificProperty**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-144">**StorageDeviceProtocolSpecificProperty**</span></span>

    <span data-ttu-id="bf6f9-145">使用這些通訊協定特定的其中一個屬性識別碼搭配 **儲存體 \_ 通訊協定 \_ 特定 \_ 資料** ，以取得 [**儲存體 \_ 通訊協定 \_ 資料 \_ 描述**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) 元結構中的通訊協定特定資料。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-145">Use one of these protocol-specific property IDs in combination with **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** to retrieve protocol-specific data in the [**STORAGE\_PROTOCOL\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) structure.</span></span>

    -   <span data-ttu-id="bf6f9-146">**StorageAdapterTemperatureProperty**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-146">**StorageAdapterTemperatureProperty**</span></span>
    -   <span data-ttu-id="bf6f9-147">**StorageDeviceTemperatureProperty**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-147">**StorageDeviceTemperatureProperty**</span></span>

    <span data-ttu-id="bf6f9-148">使用其中一個溫度屬性識別碼，以取得 [**儲存體 \_ 溫度 \_ 資料 \_ 描述**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) 元結構中的溫度資料。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-148">Use one of these temperature property IDs to retrieve temperature data in the [**STORAGE\_TEMPERATURE\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) structure.</span></span>

-   <span data-ttu-id="bf6f9-149">[**儲存體 \_通訊協定 \_ 特定 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data)：當此結構用於 **儲存體 \_ 屬性 \_ 查詢** 的 **AdditionalParameters** 欄位，以及指定 [**儲存體 \_ 通訊協定 \_ NVMe \_ 資料 \_ 類型**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type)列舉值時，抓取 NVMe 特定的資料。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-149">[**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : Retrieve NVMe-specific data when this structure is used for the **AdditionalParameters** field of **STORAGE\_PROPERTY\_QUERY** and a [**STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) enum value is specified.</span></span> <span data-ttu-id="bf6f9-150">在 **儲存體 \_ 通訊協定 \_ 特定 \_ 資料** 結構的 **DataType** 欄位中，使用下列其中一個 **儲存體 \_ 通訊協定 \_ NVME \_ 資料 \_ 類型** 值：</span><span class="sxs-lookup"><span data-stu-id="bf6f9-150">Use one of the following **STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE** values in the **DataType** field of the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** structure:</span></span>

    -   <span data-ttu-id="bf6f9-151">使用 **NVMeDataTypeIdentify** 來取得識別控制器資料或識別命名空間資料。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-151">Use **NVMeDataTypeIdentify** to get Identify Controller data or Identify Namespace data.</span></span>
    -   <span data-ttu-id="bf6f9-152">使用 **NVMeDataTypeLogPage** 取得記錄頁面 (包括智慧型/健康情況資料) 。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-152">Use **NVMeDataTypeLogPage** to get log pages (including SMART/health data).</span></span>
    -   <span data-ttu-id="bf6f9-153">使用 **NVMeDataTypeFeature** 取得 NVMe 磁片磁碟機的功能。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-153">Use **NVMeDataTypeFeature** to get features of the NVMe drive.</span></span>

-   <span data-ttu-id="bf6f9-154">[**儲存體 \_溫度 \_ 資訊**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) ：此結構是用來保存特定溫度資料。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-154">[**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : This structure is used to hold specific temperature data.</span></span> <span data-ttu-id="bf6f9-155">它會在 **儲存體 \_ TEMERATURE \_ 資料 \_ 描述** 元中用來傳回溫度查詢的結果。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-155">It's used in the **STORAGE\_TEMERATURE\_DATA\_DESCRIPTOR** to return the results of a temperature query.</span></span>

-   <span data-ttu-id="bf6f9-156">[**IOCTL \_儲存體 \_ 設定 \_ 溫度 \_ 閾值**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) ：使用此 IOCTL 搭配 **儲存 \_ 溫度 \_ 閾值** 結構來設定溫度閾值。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-156">[**IOCTL\_STORAGE\_SET\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : Use this IOCTL with the **STORAGE\_TEMPERATURE\_THRESHOLD** structure to set temperature thresholds.</span></span> <span data-ttu-id="bf6f9-157">如需詳細資訊，請參閱 [行為變更命令](#behavior-changing-commands)。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-157">For more info, see [Behavior changing commands](#behavior-changing-commands).</span></span>

-   <span data-ttu-id="bf6f9-158">[**儲存體 \_溫度 \_ 閾值**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) ：此結構會用來做為輸入緩衝區，以指定溫度閾值。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-158">[**STORAGE\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : This structure is used as an input buffer to specify the temperature threshold.</span></span> <span data-ttu-id="bf6f9-159">**OverThreshold** 欄位 (布林值) 指定 **臨界** 值欄位是否為超過臨界值，否則為不 (; 否則為臨界值) 。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-159">The **OverThreshold** field (boolean) specifies if the **Threshold** field is the over threshold value or not (otherwise, it's the under threshold value).</span></span>

## <a name="pass-through-mechanism"></a><span data-ttu-id="bf6f9-160">傳遞機制</span><span class="sxs-lookup"><span data-stu-id="bf6f9-160">Pass-through mechanism</span></span>

<span data-ttu-id="bf6f9-161">NVMe 規格中未定義的命令是主機 OS 處理最困難的方式–主機無法深入瞭解命令可能對目標裝置造成的影響、公開的基礎結構 (命名空間/區塊大小) ，以及其行為。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-161">Commands which are not defined in the NVMe specification are the most difficult for the host OS to handle – the host has no insight into the effects that the commands may have on the target device, the exposed infrastructure (namespaces/block sizes), and its behavior.</span></span>

<span data-ttu-id="bf6f9-162">為了透過 Windows 儲存體堆疊更妥善地攜帶這類裝置特定命令，新的傳遞機制可讓廠商特定的命令通過管道。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-162">To better carry such device specific commands through the Windows storage stack, a new pass-through mechanism allows vendor-specific commands to be piped through.</span></span> <span data-ttu-id="bf6f9-163">此傳遞管道也有助於開發管理和測試控管。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-163">This pass-through pipe will also aid in development of management and testing tools.</span></span> <span data-ttu-id="bf6f9-164">不過，此傳遞機制需要使用命令效果記錄檔。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-164">However, this pass-through mechanism requires use of the Command Effects Log.</span></span> <span data-ttu-id="bf6f9-165">此外，StoreNVMe.sys 需要在命令效果記錄檔中描述所有命令，而不只是傳遞命令。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-165">Moreover, StoreNVMe.sys requires all commands, not just pass-through commands, to be described in the Command Effects Log.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf6f9-166">如果命令效果記錄中未描述任何命令，StorNVMe.sys 和 Storport.sys 會封鎖該裝置的任何命令。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-166">StorNVMe.sys and Storport.sys will block any command to a device if it is not described in the Command Effects Log.</span></span>

 

### <a name="supporting-the-command-effects-log"></a><span data-ttu-id="bf6f9-167">支援命令效果記錄檔</span><span class="sxs-lookup"><span data-stu-id="bf6f9-167">Supporting the Command Effects Log</span></span>

<span data-ttu-id="bf6f9-168">命令效果記錄 (如支援和效果的命令中所述，在 [NVMe 規格 1.2](https://nvmexpress.org/specifications) 的5.10.1.5 一節中，) 可讓廠商專屬命令的效果與規格定義的命令進行描述。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-168">The Command Effects Log (as described in Commands Supported and Effects, section 5.10.1.5 of [NVMe Specification 1.2](https://nvmexpress.org/specifications)) allows the description of the effects of vendor-specific commands together with specification-defined commands.</span></span> <span data-ttu-id="bf6f9-169">這可促進命令支援驗證以及命令列為優化，因此應該針對裝置支援的整組命令來執行。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-169">This facilitates both command support validation as well as command behavior optimization, and therefore should be implemented for the entire set of commands that the device supports.</span></span> <span data-ttu-id="bf6f9-170">下列條件描述如何根據命令的命令效果記錄專案傳送命令的結果。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-170">The following conditions describe the result on how the command is sent based on its Command Effects Log entry.</span></span>

<span data-ttu-id="bf6f9-171">針對命令效果記錄檔中所述的任何特定命令 .。。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-171">For any specific command described in the Command Effects Log...</span></span>

<span data-ttu-id="bf6f9-172">**While**：</span><span class="sxs-lookup"><span data-stu-id="bf6f9-172">**While**:</span></span>

-   <span data-ttu-id="bf6f9-173">支援的命令 (CSUPP) 設定為 ' 1 '，表示控制器 (位01所支援的命令) </span><span class="sxs-lookup"><span data-stu-id="bf6f9-173">Command Supported (CSUPP) is set to ‘1’ signifying that the command is supported by the controller (Bit 01)</span></span>

    > [!Note]  
    > <span data-ttu-id="bf6f9-174">當 CSUPP 設定為 ' 0 ' 時 (表示不支援命令) 將會封鎖命令</span><span class="sxs-lookup"><span data-stu-id="bf6f9-174">When CSUPP is set to ‘0’ (signifying that the command is not supported) the command will be blocked</span></span>

     

<span data-ttu-id="bf6f9-175">**如果** 有下列任何一項設定，則為：</span><span class="sxs-lookup"><span data-stu-id="bf6f9-175">**And if** any of the following is set:</span></span>

-   <span data-ttu-id="bf6f9-176">控制器功能變更 (CCC) 設定為 ' 1 '，表示命令可能會變更控制器功能 (Bit 04) </span><span class="sxs-lookup"><span data-stu-id="bf6f9-176">Controller Capability Change (CCC) is set to ‘1’ signifying that the command may change controller capabilities (Bit 04)</span></span>

-   <span data-ttu-id="bf6f9-177">命名空間清查變更 (NIC) 設定為 ' 1 '，表示命令可能會變更多個命名空間的數目或功能 (位 03) </span><span class="sxs-lookup"><span data-stu-id="bf6f9-177">Namespace Inventory Change (NIC) is set to ‘1’ signifying that the command may change the number, or capabilities for multiple namespaces (Bit 03)</span></span>

-   <span data-ttu-id="bf6f9-178">命名空間功能變更 (NCC) 設定為 ' 1 '，表示命令可能會變更單一命名空間 (位02的功能) </span><span class="sxs-lookup"><span data-stu-id="bf6f9-178">Namespace Capability Change (NCC) is set to ‘1’ signifying that the command may change the capabilities of a single namespace (Bit 02)</span></span>

-   <span data-ttu-id="bf6f9-179">命令提交和執行 (CSE) 設定為001b 或010b，表示當相同或任何命名空間沒有其他未完成的命令時，可能會提交命令，而且在這個命令完成 (位18:16 之前，不應將另一個命令提交至相同或任何命名空間) </span><span class="sxs-lookup"><span data-stu-id="bf6f9-179">Command Submission and Execution (CSE) is set to 001b or 010b, signifying that the command may be submitted when there is no other outstanding command to the same or any namespace, and that another command should not be submitted to the same or any namespace until this command is complete (Bits 18:16)</span></span>

<span data-ttu-id="bf6f9-180">**然後** ，命令會傳送為介面卡未完成的唯一命令。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-180">**Then** the command will be sent as the only command outstanding to the adapter.</span></span>

<span data-ttu-id="bf6f9-181">**否則** 為：</span><span class="sxs-lookup"><span data-stu-id="bf6f9-181">**Else if**:</span></span>

-   <span data-ttu-id="bf6f9-182">命令提交和執行 (CSE) 設定為001b，表示在相同的命名空間沒有其他未處理的命令時可能會提交命令，而且在此命令 18:16 (完成之前，不應將另一個命令提交至相同的命名空間) </span><span class="sxs-lookup"><span data-stu-id="bf6f9-182">Command Submission and Execution (CSE) is set to 001b, signifying that the command may be submitted when there is no other outstanding command to the same namespace, and that another command should not be submitted to the same namespace until this command is complete (Bits 18:16)</span></span>

<span data-ttu-id="bf6f9-183">**然後** 命令會以唯一未完成的命令傳送給邏輯單元編號物件 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-183">**Then** the command will be sent as the only command outstanding to the Logical Unit Number object (LUN).</span></span>

<span data-ttu-id="bf6f9-184">**否則**，此命令會與未抑制的其他命令一起傳送。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-184">**Otherwise**, the command is sent with other commands outstanding without inhibition.</span></span> <span data-ttu-id="bf6f9-185">例如，如果將廠商專屬的命令傳送至裝置，以抓取未定義規格的統計資訊，則變更裝置的行為或功能以執行 i/o 命令應該不會有任何風險。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-185">For example, if a vendor-specific command is sent to the device to retrieve statistical information that is not spec-defined, there should be no risk to changing the device’s behavior or capability to execute I/O commands.</span></span> <span data-ttu-id="bf6f9-186">這類要求可能會以平行方式提供給 i/o，而且不需要暫停-繼續。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-186">Such requests could be serviced in parallel to I/O and no pause-resume would be necessary.</span></span>

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a><span data-ttu-id="bf6f9-187">使用 IOCTL \_ 儲存體 \_ 通訊協定 \_ 命令傳送命令</span><span class="sxs-lookup"><span data-stu-id="bf6f9-187">Using IOCTL\_STORAGE\_PROTOCOL\_COMMAND to send commands</span></span>

<span data-ttu-id="bf6f9-188">您可以使用 Windows 10 中引進的 [**IOCTL \_ 儲存 \_ 通訊協定 \_ 命令**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command)來進行傳遞。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-188">Pass-through can be conducted using the [**IOCTL\_STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), introduced in Windows 10.</span></span> <span data-ttu-id="bf6f9-189">這個 IOCTL 的設計與現有的 SCSI 和 ATA 傳遞 IOCTLs 具有類似的行為，以將內嵌的命令傳送至目標裝置。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-189">This IOCTL was designed to have a similar behavior as the existing SCSI and ATA pass-through IOCTLs, to send an embedded command to the target device.</span></span> <span data-ttu-id="bf6f9-190">透過這個 IOCTL，傳遞可以傳送至存放裝置（包括 NVMe 磁片磁碟機）。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-190">Via this IOCTL, pass-through can be sent to a storage device, including an NVMe drive.</span></span>

<span data-ttu-id="bf6f9-191">例如，在 NVMe 中，IOCTL 將允許傳送下列命令程式碼。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-191">For example, in NVMe, the IOCTL will allow the sending down of the following command codes.</span></span>

-   <span data-ttu-id="bf6f9-192">廠商特定的系統管理命令 (C0h – FFh) </span><span class="sxs-lookup"><span data-stu-id="bf6f9-192">Vendor Specific Admin Commands (C0h – FFh)</span></span>
-   <span data-ttu-id="bf6f9-193">廠商特定 NVMe 命令 (80h – FFh) </span><span class="sxs-lookup"><span data-stu-id="bf6f9-193">Vendor Specific NVMe Commands (80h – FFh)</span></span>

<span data-ttu-id="bf6f9-194">如同所有其他 IOCTLs，請使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 來傳送傳遞的 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-194">As with all other IOCTLs, Use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) to send the pass-through IOCTL down.</span></span> <span data-ttu-id="bf6f9-195">您可以使用在 **ntddstor** 中找到的 [**儲存體 \_ 通訊協定 \_ 命令**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command)輸入緩衝區結構來填入 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-195">The IOCTL is populated using the [**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) input-buffer structure found in **ntddstor.h**.</span></span> <span data-ttu-id="bf6f9-196">使用廠商特定的命令填入 **命令** 欄位。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-196">Populate the **Command** field with the vendor-specific command.</span></span>


```C++
typedef struct _STORAGE_PROTOCOL_COMMAND {

    ULONG   Version;                        // STORAGE_PROTOCOL_STRUCTURE_VERSION
    ULONG   Length;                         // sizeof(STORAGE_PROTOCOL_COMMAND)

    STORAGE_PROTOCOL_TYPE  ProtocolType;
    ULONG   Flags;                          // Flags for the request

    ULONG   ReturnStatus;                   // return value
    ULONG   ErrorCode;                      // return value, optional

    ULONG   CommandLength;                  // non-zero value should be set by caller
    ULONG   ErrorInfoLength;                // optional, can be zero
    ULONG   DataToDeviceTransferLength;     // optional, can be zero. Used by WRITE type of request.
    ULONG   DataFromDeviceTransferLength;   // optional, can be zero. Used by READ type of request.

    ULONG   TimeOutValue;                   // in unit of seconds

    ULONG   ErrorInfoOffset;                // offsets need to be pointer aligned
    ULONG   DataToDeviceBufferOffset;       // offsets need to be pointer aligned
    ULONG   DataFromDeviceBufferOffset;     // offsets need to be pointer aligned

    ULONG   CommandSpecific;                // optional information passed along with Command.
    ULONG   Reserved0;

    ULONG   FixedProtocolReturnData;        // return data, optional. Some protocol, such as NVMe, may return a small amount data (DWORD0 from completion queue entry) without the need of separate device data transfer.
    ULONG   Reserved1[3];

    _Field_size_bytes_full_(CommandLength) UCHAR Command[ANYSIZE_ARRAY];

} STORAGE_PROTOCOL_COMMAND, *PSTORAGE_PROTOCOL_COMMAND;
```



<span data-ttu-id="bf6f9-197">要傳送的廠商特定命令應該填入上面的反白顯示欄位中。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-197">The vendor specific command desired to be sent should be populated in the highlighted field above.</span></span> <span data-ttu-id="bf6f9-198">請再次注意，命令效果記錄檔必須針對傳遞命令來執行。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-198">Note again that the Command Effects Log must be implemented for pass-through commands.</span></span> <span data-ttu-id="bf6f9-199">尤其是，這些命令必須在命令效果記錄檔中報告為支援 (如需詳細資訊) ，請參閱上一節。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-199">In particular, these commands need to be reported as supported in the Command Effects Log (see previous section for more information).</span></span> <span data-ttu-id="bf6f9-200">另請注意，PRP 欄位是驅動程式特定的，因此傳送命令的應用程式可以將其保留為0。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-200">Also note that PRP fields are driver specific thus applications sending commands can leave them as 0.</span></span>

<span data-ttu-id="bf6f9-201">最後，此傳遞 IOCTL 是為了傳送廠商特定的命令。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-201">Finally, this pass-through IOCTL is intended for sending vendor-specific commands.</span></span> <span data-ttu-id="bf6f9-202">若要傳送其他系統管理員或非廠商特定 NVMe 命令（例如識別），則不應使用此傳遞 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-202">To send other admin or non-vendor specific NVMe commands such as Identify, this pass-through IOCTL should not be used.</span></span> <span data-ttu-id="bf6f9-203">例如，您應該使用 [ **IOCTL \_ 儲存體 \_ 查詢] \_ 屬性** 來識別或取得記錄頁面。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-203">For example, **IOCTL\_STORAGE\_QUERY\_PROPERTY** should be used for Identify or Get Log Pages.</span></span> <span data-ttu-id="bf6f9-204">如需詳細資訊，請參閱下一節的 [通訊協定特定查詢](/windows)。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-204">For more info, see the next section, [Protocol-specific queries](/windows).</span></span>

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a><span data-ttu-id="bf6f9-205">不要透過傳遞機制更新固件</span><span class="sxs-lookup"><span data-stu-id="bf6f9-205">Don't update firmware through the pass-through mechanism</span></span>

<span data-ttu-id="bf6f9-206">不應使用傳遞來傳送固件下載和啟用命令。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-206">Firmware download and activation commands should not be sent using pass-through.</span></span> <span data-ttu-id="bf6f9-207">**IOCTL \_儲存體 \_ 通訊協定 \_ 命令** 只能用於廠商特定的命令。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-207">**IOCTL\_STORAGE\_PROTOCOL\_COMMAND** should only be used for vendor-specific commands.</span></span>

<span data-ttu-id="bf6f9-208">相反地，請使用 Windows 10) 引進的下列一般儲存體 IOCTLs (，以避免使用 SCSI \_ 微型埠版本的固件 IOCTL 直接使用應用程式。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-208">Instead, use the following general storage IOCTLs (introduced in Windows 10) to avoid applications directly using the SCSI\_miniport version of the Firmware IOCTL.</span></span> <span data-ttu-id="bf6f9-209">儲存體驅動程式會將 IOCTL 轉譯成 SCSI 命令，或將 IOCTL 的 SCSI \_ 微型埠版本轉譯為微型埠。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-209">Storage drivers will translate the IOCTL to either a SCSI command or the SCSI\_miniport version of the IOCTL to the miniport.</span></span>

<span data-ttu-id="bf6f9-210">建議您在 Windows 10 和 Windows Server 2016 中開發固件升級工具，以進行這些 IOCTLs：</span><span class="sxs-lookup"><span data-stu-id="bf6f9-210">These IOCTLs are recommended for developing firmware upgrade tools in Windows 10 and Windows Server 2016:</span></span>

-   [<span data-ttu-id="bf6f9-211">**IOCTL \_ 儲存體 \_ 固件 \_ 取得 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-211">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [<span data-ttu-id="bf6f9-212">**IOCTL \_ 儲存體 \_ 固件 \_ 下載**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-212">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [<span data-ttu-id="bf6f9-213">**\_啟用 IOCTL 儲存體 \_ 固件 \_**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-213">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

<span data-ttu-id="bf6f9-214">為了取得儲存體資訊和更新固件，Windows 也支援 PowerShell Cmdlet 來快速進行：</span><span class="sxs-lookup"><span data-stu-id="bf6f9-214">For getting storage information and updating firmware, Windows also supports PowerShell cmdlets for doing this quickly:</span></span>

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> <span data-ttu-id="bf6f9-215">若要更新 Windows 8.1 中 NVMe 的固件，請使用 IOCTL \_ SCSI \_ 微型埠 \_ 固件。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-215">To update firmware on NVMe in Windows 8.1, use IOCTL\_SCSI\_MINIPORT\_FIRMWARE.</span></span> <span data-ttu-id="bf6f9-216">這個 IOCTL 未 backport 至 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-216">This IOCTL was not backported to Windows 7.</span></span> <span data-ttu-id="bf6f9-217">如需詳細資訊，請參閱 [Windows 8.1 中的升級 NVMe 裝置的固件](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device)。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-217">For more information, see [Upgrading Firmware for an NVMe Device in Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).</span></span>

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a><span data-ttu-id="bf6f9-218">透過傳遞機制傳回錯誤</span><span class="sxs-lookup"><span data-stu-id="bf6f9-218">Returning errors through the pass-through mechanism</span></span>

<span data-ttu-id="bf6f9-219">類似于 SCSI 和 ATA 傳遞 IOCTLs，當命令/要求傳送至微型埠或裝置時，如果成功，則會傳回 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-219">Similar to SCSI and ATA pass-through IOCTLs, when a command/request is sent to the miniport or device, the IOCTL returns if it was successful or not.</span></span> <span data-ttu-id="bf6f9-220">在 [**儲存體 \_ 通訊協定 \_ 命令**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) 結構中，IOCTL 會透過 **ReturnStatus** 欄位傳回狀態。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-220">In the [**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) structure, the IOCTL returns the status through the **ReturnStatus** field.</span></span>

### <a name="example-sending-a-vendor-specific-command"></a><span data-ttu-id="bf6f9-221">範例：傳送廠商特定的命令</span><span class="sxs-lookup"><span data-stu-id="bf6f9-221">Example: sending a vendor-specific command</span></span>

<span data-ttu-id="bf6f9-222">在此範例中，會透過傳遞到 NVMe 磁片磁碟機，將任意的廠商專屬命令 (0xFF) 傳送到 NVMe 磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-222">In this example, an arbitrary vendor-specific command (0xFF) is sent via pass-through to an NVMe drive.</span></span> <span data-ttu-id="bf6f9-223">下列程式碼會配置緩衝區、初始化查詢，然後透過 DeviceIoControl 將命令向下傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-223">The following code allocates a buffer, initializes a query, and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    ZeroMemory(buffer, bufferLength);  
    protocolCommand = (PSTORAGE_PROTOCOL_COMMAND)buffer;  

    protocolCommand->Version = STORAGE_PROTOCOL_STRUCTURE_VERSION;  
    protocolCommand->Length = sizeof(STORAGE_PROTOCOL_COMMAND);  
    protocolCommand->ProtocolType = ProtocolTypeNvme;  
    protocolCommand->Flags = STORAGE_PROTOCOL_COMMAND_FLAG_ADAPTER_REQUEST;  
    protocolCommand->CommandLength = STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->ErrorInfoLength = sizeof(NVME_ERROR_INFO_LOG);  
    protocolCommand->DataFromDeviceTransferLength = 4096;  
    protocolCommand->TimeOutValue = 10;  
    protocolCommand->ErrorInfoOffset = FIELD_OFFSET(STORAGE_PROTOCOL_COMMAND, Command) + STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->DataFromDeviceBufferOffset = protocolCommand->ErrorInfoOffset + protocolCommand->ErrorInfoLength;  
    protocolCommand->CommandSpecific = STORAGE_PROTOCOL_SPECIFIC_NVME_ADMIN_COMMAND;  

    command = (PNVME_COMMAND)protocolCommand->Command;  

    command->CDW0.OPC = 0xFF;  
    command->u.GENERAL.CDW10 = 0xto_fill_in;  
    command->u.GENERAL.CDW12 = 0xto_fill_in;  
    command->u.GENERAL.CDW13 = 0xto_fill_in;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_PROTOCOL_COMMAND,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL 
                             );  
```



<span data-ttu-id="bf6f9-224">在此範例中，我們會預期 `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` 命令是否成功至裝置。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-224">In this example, we expect `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` if the command succeeded to the device.</span></span>

## <a name="protocol-specific-queries"></a><span data-ttu-id="bf6f9-225">特定通訊協定的查詢</span><span class="sxs-lookup"><span data-stu-id="bf6f9-225">Protocol-specific queries</span></span>

<span data-ttu-id="bf6f9-226">Windows 8.1 引進了資料抓取的 [**IOCTL \_ 儲存體 \_ 查詢 \_ 屬性**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) 。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-226">Windows 8.1 introduced [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) for data retrieval.</span></span> <span data-ttu-id="bf6f9-227">在 Windows 10 中，已增強 IOCTL 以支援一般要求的 NVMe 功能，例如 **取得記錄頁面**、 **取得功能** 和 **識別**。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-227">In Windows 10, the IOCTL was enhanced to support commonly requested NVMe features such as **Get Log Pages**, **Get Features**, and **Identify**.</span></span> <span data-ttu-id="bf6f9-228">這可讓您抓取 NVMe 特定資訊，以供監視和清查之用。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-228">This allows for the retrieval of NVMe specific information for monitoring and inventory purposes.</span></span>

<span data-ttu-id="bf6f9-229">以下顯示 IOCTL 的輸入緩衝區、Windows 10)  ([**儲存體 \_ 屬性 \_ 查詢**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) 。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-229">The input buffer for the IOCTL, [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



<span data-ttu-id="bf6f9-230">使用 [**IOCTL \_ 儲存體 \_ 查詢 \_ 屬性**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) 來取出 [**儲存體 \_ 通訊協定 \_ 資料 \_ 描述**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor)項中 NVMe 的通訊協定特定資訊時，請設定 [**存放裝置 \_ 屬性 \_ 查詢**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) 結構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bf6f9-230">When using [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) to retrieve NVMe protocol-specific information in the [**STORAGE\_PROTOCOL\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor), configure the [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure as follows:</span></span>

-   <span data-ttu-id="bf6f9-231">配置可同時包含 [**儲存體 \_ 屬性 \_ 查詢**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) 和 [**儲存體 \_ 通訊協定 \_ 特定 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) 結構的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-231">Allocate a buffer that can contains both a [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) and a [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure.</span></span>

-   <span data-ttu-id="bf6f9-232">分別將控制器或裝置/命名空間要求的 **PropertyID** 欄位設定為 **StorageAdapterProtocolSpecificProperty** 或 **StorageDeviceProtocolSpecificProperty** 。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-232">Set the **PropertyID** field to **StorageAdapterProtocolSpecificProperty** or **StorageDeviceProtocolSpecificProperty** for a controller or device/namespace request, respectively.</span></span>

-   <span data-ttu-id="bf6f9-233">將 **QueryType** 欄位設定為 **PropertyStandardQuery**。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-233">Set the **QueryType** field to **PropertyStandardQuery**.</span></span>

-   <span data-ttu-id="bf6f9-234">以所需的值填入 [**儲存體 \_ 通訊協定 \_ 特定的 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) 結構。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-234">Fill the [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure with the desired values.</span></span> <span data-ttu-id="bf6f9-235">**儲存體 \_ 通訊協定 \_ 特定 \_ 資料** 的開始是 [**儲存體 \_ 屬性 \_ 查詢**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query)的 **AdditionalParameters** 欄位。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-235">The start of the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** is the **AdditionalParameters** field of [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).</span></span>

<span data-ttu-id="bf6f9-236">從 Windows 10)  ([**儲存體 \_ 通訊協定 \_ 特定的 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) 結構，如下所示。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-236">The [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                 

    ULONG   ProtocolDataRequestValue;
    ULONG   ProtocolDataRequestSubValue;

    ULONG   ProtocolDataOffset;         
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;   
    ULONG   Reserved[3];

} STORAGE_PROTOCOL_SPECIFIC_DATA, *PSTORAGE_PROTOCOL_SPECIFIC_DATA;
```



<span data-ttu-id="bf6f9-237">若要指定 NVMe 通訊協定特定資訊的類型，請設定 [**儲存體 \_ 通訊協定 \_ 特定的 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) 結構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bf6f9-237">To specify a type of NVMe protocol-specific information, configure the [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure as follows:</span></span>

-   <span data-ttu-id="bf6f9-238">將 **ProtocolType** 欄位設定為 **ProtocolTypeNVMe**。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-238">Set the **ProtocolType** field to **ProtocolTypeNVMe**.</span></span>

-   <span data-ttu-id="bf6f9-239">將 **DataType** 欄位設定為 [**儲存體 \_ 通訊協定 \_ NVME \_ 資料 \_ 類型**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type)所定義的列舉值：</span><span class="sxs-lookup"><span data-stu-id="bf6f9-239">Set the **DataType** field to an enumeration value defined by [**STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):</span></span>

    -   <span data-ttu-id="bf6f9-240">使用 **NVMeDataTypeIdentify** 來取得識別控制器資料或識別命名空間資料。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-240">Use **NVMeDataTypeIdentify** to get Identify Controller data or Identify Namespace data.</span></span>
    -   <span data-ttu-id="bf6f9-241">使用 **NVMeDataTypeLogPage** 取得記錄頁面 (包括智慧型/健康情況資料) 。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-241">Use **NVMeDataTypeLogPage** to get log pages (including SMART/health data).</span></span>
    -   <span data-ttu-id="bf6f9-242">使用 **NVMeDataTypeFeature** 取得 NVMe 磁片磁碟機的功能。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-242">Use **NVMeDataTypeFeature** to get features of the NVMe drive.</span></span>

<span data-ttu-id="bf6f9-243">使用 **ProtocolTypeNVMe** 做為 **ProtocolType** 時，可以使用 NVMe 磁片磁碟機上的其他 i/o 來平行抓取通訊協定特定資訊的查詢。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-243">When **ProtocolTypeNVMe** is used as the **ProtocolType**, queries for protocol-specific information can be retrieved in parallel with other I/O on the NVMe drive.</span></span>

<span data-ttu-id="bf6f9-244">下列範例示範 NVMe 通訊協定特定的查詢。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-244">The following examples demonstrate NVMe protocol-specific queries.</span></span>

### <a name="example-nvme-identify-query"></a><span data-ttu-id="bf6f9-245">範例： NVMe 識別查詢</span><span class="sxs-lookup"><span data-stu-id="bf6f9-245">Example: NVMe Identify query</span></span>

<span data-ttu-id="bf6f9-246">在此範例中，會將 **識別** 要求傳送到 NVMe 磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-246">In this example, the **Identify** request is sent to an NVMe drive.</span></span> <span data-ttu-id="bf6f9-247">下列程式碼會初始化查詢資料結構，然後透過 DeviceIoControl 將命令向下傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-247">The following code initializes the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    BOOL    result;
    PVOID   buffer = NULL;
    ULONG   bufferLength = 0;
    ULONG   returnedLength = 0;

    PSTORAGE_PROPERTY_QUERY query = NULL;
    PSTORAGE_PROTOCOL_SPECIFIC_DATA protocolData = NULL;
    PSTORAGE_PROTOCOL_DATA_DESCRIPTOR protocolDataDescr = NULL;

    //
    // Allocate buffer for use.
    //
    bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_QUERY, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA) + NVME_MAX_LOG_SIZE;
    buffer = malloc(bufferLength);

    if (buffer == NULL) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: allocate buffer failed, exit.\n"));
        goto exit;
    }

    //
    // Initialize query data structure to get Identify Controller Data.
    //
    ZeroMemory(buffer, bufferLength);

    query = (PSTORAGE_PROPERTY_QUERY)buffer;
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;

    query->PropertyId = StorageAdapterProtocolSpecificProperty;
    query->QueryType = PropertyStandardQuery;

    protocolData->ProtocolType = ProtocolTypeNvme;
    protocolData->DataType = NVMeDataTypeIdentify;
    protocolData->ProtocolDataRequestValue = NVME_IDENTIFY_CNS_CONTROLLER;
    protocolData->ProtocolDataRequestSubValue = 0;
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);
    protocolData->ProtocolDataLength = NVME_MAX_LOG_SIZE;

    //
    // Send request down.
    //
    result = DeviceIoControl(DeviceList[Index].Handle,
                             IOCTL_STORAGE_QUERY_PROPERTY,
                             buffer,
                             bufferLength,
                             buffer,
                             bufferLength,
                             &returnedLength,
                             NULL
                             );

    ZeroMemory(buffer, bufferLength);
    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < NVME_MAX_LOG_SIZE)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // Identify Controller Data 
    //
    {
        PNVME_IDENTIFY_CONTROLLER_DATA identifyControllerData = (PNVME_IDENTIFY_CONTROLLER_DATA)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        if ((identifyControllerData->VID == 0) ||
            (identifyControllerData->NN == 0)) {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Identify Controller Data not valid.\n"));
            goto exit;
        } else {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Identify Controller Data succeeded_*_.\n"));
        }
    }

  
```



<span data-ttu-id="bf6f9-248">請注意，呼叫端必須配置單一緩衝區，其中包含儲存體 \_ 屬性 \_ 查詢和儲存體 \_ 通訊協定特定資料的大小 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-248">Note that the caller needs to allocate a single buffer containing STORAGE\_PROPERTY\_QUERY and the size of STORAGE\_PROTOCOL\_SPECIFIC\_DATA.</span></span> <span data-ttu-id="bf6f9-249">在此範例中，它會針對屬性查詢的輸入和輸出使用相同的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-249">In this example, it’s using the same buffer for input and output from the property query.</span></span> <span data-ttu-id="bf6f9-250">這就是為什麼配置的緩衝區大小為「欄位 \_ 位移 (儲存體 \_ 屬性 \_ 查詢，AdditionalParameters) + sizeof (儲存體 \_ 通訊協定 \_ 特定 \_ 資料) + NVME 記錄檔 \_ 大小上限」 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-250">That’s why the buffer that was allocated has a size of “FIELD\_OFFSET(STORAGE\_PROPERTY\_QUERY, AdditionalParameters) + sizeof(STORAGE\_PROTOCOL\_SPECIFIC\_DATA) + NVME\_MAX\_LOG\_SIZE”.</span></span> <span data-ttu-id="bf6f9-251">雖然可以為輸入和輸出配置不同的緩衝區，但我們建議使用單一緩衝區來查詢 NVMe 相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-251">Although separate buffers could be allocated for both input and output, we recommend using a single buffer to query NVMe related-information.</span></span>

### <a name="example-nvme-get-log-pages-query"></a><span data-ttu-id="bf6f9-252">範例： NVMe 取得記錄頁面查詢</span><span class="sxs-lookup"><span data-stu-id="bf6f9-252">Example: NVMe Get Log Pages query</span></span>

<span data-ttu-id="bf6f9-253">在此範例中，根據上一個範例，_ *取得記錄頁面*\* 要求會傳送至 NVMe 磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-253">In this example, based off of the previous one, the _ *Get Log Pages*\* request is sent to an NVMe drive.</span></span> <span data-ttu-id="bf6f9-254">下列程式碼會準備查詢資料結構，然後透過 DeviceIoControl 將命令向下傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-254">The following code prepares the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    ZeroMemory(buffer, bufferLength);  

    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  // This will be passed as the lower 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue2 = 0; // This will be passed as the higher 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue3 = 0; // This will be passed as Log Specific Identifier in CDW11.
    protocolData->ProtocolDataRequestSubValue4 = 0; // This will map to STORAGE_PROTOCOL_DATA_SUBVALUE_GET_LOG_PAGE definition, then user can pass Retain Asynchronous Event, Log Specific Field.

    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log failed. Error Code %d.\n"), GetLastError());
        goto exit;
    }

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < sizeof(NVME_HEALTH_INFO_LOG))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // SMART/Health Information Log Data 
    //
    {
        PNVME_HEALTH_INFO_LOG smartInfo = (PNVME_HEALTH_INFO_LOG)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log Data - Temperature %d.\n"), ((ULONG)smartInfo->Temperature[1] << 8 | smartInfo->Temperature[0]) - 273);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_SMART/Health Information Log succeeded_*_.\n"));
    }

```



### <a name="example-nvme-get-features-query"></a><span data-ttu-id="bf6f9-255">範例： NVMe Get Features 查詢</span><span class="sxs-lookup"><span data-stu-id="bf6f9-255">Example: NVMe Get Features query</span></span>

<span data-ttu-id="bf6f9-256">在此範例中，根據上一個範例，_ *Get Features*\* 要求會傳送至 NVMe 磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-256">In this example, based off of the previous one, the _ *Get Features*\* request is sent to an NVMe drive.</span></span> <span data-ttu-id="bf6f9-257">下列程式碼會準備查詢資料結構，然後透過 DeviceIoControl 將命令向下傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-257">The following code prepares the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    //  
    // Initialize query data structure to Volatile Cache feature.  
    //  

    ZeroMemory(buffer, bufferLength);  


    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeFeature;  
    protocolData->ProtocolDataRequestValue = NVME_FEATURE_VOLATILE_WRITE_CACHE;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = 0;  
    protocolData->ProtocolDataLength = 0;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache failed. Error Code %d.\n"), GetLastError());  
        goto exit;  
    }  

    //  
    // Validate the returned data.  
    //  

    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||  
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache  - data descriptor header not valid.\n"));  
        return;                                           
    }  

    //
    // Volatile Cache 
    //
    {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache - %x.\n"), protocolDataDescr->ProtocolSpecificData.FixedProtocolReturnData);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Get Feature - Volatile Cache succeeded_*_.\n"));
    }
```
## <a name="protocol-specific-set"></a><span data-ttu-id="bf6f9-258">通訊協定特定的集合</span><span class="sxs-lookup"><span data-stu-id="bf6f9-258">Protocol-specific set</span></span>

<span data-ttu-id="bf6f9-259">從 Windows 10 19H1，IOCTL_STORAGE_SET_PROPERTY 已增強為支援 NVMe 設定的功能。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-259">From Windows 10 19H1, the IOCTL_STORAGE_SET_PROPERTY was enhanced to support NVMe Set Features.</span></span>

<span data-ttu-id="bf6f9-260">IOCTL_STORAGE_SET_PROPERTY 的輸入緩衝區如下所示：</span><span class="sxs-lookup"><span data-stu-id="bf6f9-260">The input buffer for the IOCTL_STORAGE_SET_PROPERTY is shown here:</span></span>

```C++
typedef struct _STORAGE_PROPERTY_SET {

    //
    // ID of the property being retrieved
    //

    STORAGE_PROPERTY_ID PropertyId;

    //
    // Flags indicating the type of set property being performed
    //

    STORAGE_SET_TYPE SetType;

    //
    // Space for additional parameters if necessary
    //

    UCHAR AdditionalParameters[1];

} STORAGE_PROPERTY_SET, _PSTORAGE_PROPERTY_SET;
```

<span data-ttu-id="bf6f9-261">使用 IOCTL_STORAGE_SET_PROPERTY 設定 NVMe 功能時，請設定 STORAGE_PROPERTY_SET 結構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bf6f9-261">When using IOCTL_STORAGE_SET_PROPERTY to set NVMe feature, configure the STORAGE_PROPERTY_SET structure as follows:</span></span>

-   <span data-ttu-id="bf6f9-262">配置可同時包含 STORAGE_PROPERTY_SET 和 STORAGE_PROTOCOL_SPECIFIC_DATA_EXT 結構的緩衝區;</span><span class="sxs-lookup"><span data-stu-id="bf6f9-262">Allocate a buffer that can contains both a STORAGE_PROPERTY_SET and a STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure;</span></span>
-   <span data-ttu-id="bf6f9-263">分別將控制器或裝置/命名空間要求的 PropertyID 欄位設定為 StorageAdapterProtocolSpecificProperty 或 StorageDeviceProtocolSpecificProperty。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-263">Set the PropertyID field to StorageAdapterProtocolSpecificProperty or StorageDeviceProtocolSpecificProperty for a controller or device/namespace request, respectively.</span></span>
-   <span data-ttu-id="bf6f9-264">以所需的值填滿 STORAGE_PROTOCOL_SPECIFIC_DATA_EXT 結構。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-264">Fill the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure with the desired values.</span></span> <span data-ttu-id="bf6f9-265">STORAGE_PROTOCOL_SPECIFIC_DATA_EXT 的開頭是 STORAGE_PROPERTY_SET 的 AdditionalParameters 欄位。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-265">The start of the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT is the AdditionalParameters field of STORAGE_PROPERTY_SET.</span></span>

<span data-ttu-id="bf6f9-266">STORAGE_PROTOCOL_SPECIFIC_DATA_EXT 結構如下所示。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-266">The STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure is shown here.</span></span>

```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA_EXT {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                   // The value will be protocol specific, as defined in STORAGE_PROTOCOL_NVME_DATA_TYPE or STORAGE_PROTOCOL_ATA_DATA_TYPE.

    ULONG   ProtocolDataValue;
    ULONG   ProtocolDataSubValue;      // Data sub request value

    ULONG   ProtocolDataOffset;         // The offset of data buffer is from beginning of this data structure.
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;
    ULONG   ProtocolDataSubValue2;     // First additional data sub request value

    ULONG   ProtocolDataSubValue3;     // Second additional data sub request value
    ULONG   ProtocolDataSubValue4;     // Third additional data sub request value

    ULONG   ProtocolDataSubValue5;     // Fourth additional data sub request value
    ULONG   Reserved[5];
} STORAGE_PROTOCOL_SPECIFIC_DATA_EXT, *PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT;
```

<span data-ttu-id="bf6f9-267">若要指定要設定的 NVMe 功能類型，請設定 STORAGE_PROTOCOL_SPECIFIC_DATA_EXT 結構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bf6f9-267">To specify a type of NVMe feature to set, configure the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure as follows:</span></span>
-   <span data-ttu-id="bf6f9-268">將 ProtocolType 欄位設定為 ProtocolTypeNvme;</span><span class="sxs-lookup"><span data-stu-id="bf6f9-268">Set the ProtocolType field to ProtocolTypeNvme;</span></span>
-   <span data-ttu-id="bf6f9-269">將 DataType 欄位設定為 STORAGE_PROTOCOL_NVME_DATA_TYPE 所定義的列舉值 NVMeDataTypeFeature;</span><span class="sxs-lookup"><span data-stu-id="bf6f9-269">Set the DataType field to the enumeration value NVMeDataTypeFeature defined by STORAGE_PROTOCOL_NVME_DATA_TYPE;</span></span>

<span data-ttu-id="bf6f9-270">下列範例示範 NVMe 功能集。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-270">The following examples demonstrate NVMe feature set.</span></span>

### <a name="example-nvme-set-features"></a><span data-ttu-id="bf6f9-271">範例： NVMe 設定功能</span><span class="sxs-lookup"><span data-stu-id="bf6f9-271">Example: NVMe Set Features</span></span>

<span data-ttu-id="bf6f9-272">在此範例中，會將設定功能要求傳送到 NVMe 磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-272">In this example, the Set Features request is sent to an NVMe drive.</span></span> <span data-ttu-id="bf6f9-273">下列程式碼會準備 set 資料結構，然後透過 DeviceIoControl 將命令向下傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-273">The following code prepares the set data structure and then sends the command down to the device via DeviceIoControl.</span></span>

```C++
            PSTORAGE_PROPERTY_SET                   setProperty = NULL;
            PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT     protocolData = NULL;
            PSTORAGE_PROTOCOL_DATA_DESCRIPTOR_EXT   protocolDataDescr = NULL;

            //
            // Allocate buffer for use.
            //
            bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_SET, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA_EXT);
            bufferLength += NVME_MAX_LOG_SIZE;

            buffer = new UCHAR[bufferLength];

            //
            // Initialize query data structure to get the desired log page.
            //
            ZeroMemory(buffer, bufferLength);

            setProperty = (PSTORAGE_PROPERTY_SET)buffer;

            setProperty->PropertyId = StorageAdapterProtocolSpecificProperty;
            setProperty->SetType = PropertyStandardSet;

            protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT)setProperty->AdditionalParameters;

            protocolData->ProtocolType = ProtocolTypeNvme;
            protocolData->DataType = NVMeDataTypeFeature;
            protocolData->ProtocolDataValue = NVME_FEATURE_HOST_CONTROLLED_THERMAL_MANAGEMENT;

            protocolData->ProtocolDataSubValue = 0; // This will pass to CDW11.
            protocolData->ProtocolDataSubValue2 = 0; // This will pass to CDW12.
            protocolData->ProtocolDataSubValue3 = 0; // This will pass to CDW13.
            protocolData->ProtocolDataSubValue4 = 0; // This will pass to CDW14.
            protocolData->ProtocolDataSubValue5 = 0; // This will pass to CDW15.

            protocolData->ProtocolDataOffset = 0;
            protocolData->ProtocolDataLength = 0;

            //
            // Send request down.
            //
            result = DeviceIoControl(m_deviceHandle,
                                     IOCTL_STORAGE_SET_PROPERTY,
                                     buffer,
                                     bufferLength,
                                     buffer,
                                     bufferLength,
                                     &returnedLength,
                                     NULL
            );
```

## <a name="temperature-queries"></a><span data-ttu-id="bf6f9-274">溫度查詢</span><span class="sxs-lookup"><span data-stu-id="bf6f9-274">Temperature queries</span></span>

<span data-ttu-id="bf6f9-275">在 Windows 10 中，您也可以使用 [**IOCTL \_ 儲存體 \_ 查詢 \_ 屬性**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) ，從 NVMe 裝置查詢溫度資料。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-275">In Windows 10, [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) can also be used to query temperature data from NVMe devices.</span></span>

<span data-ttu-id="bf6f9-276">若要從 [**儲存體 \_ 溫度 \_ 資料 \_ 描述**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor)項中的 NVMe 磁片磁碟機取出溫度資訊，請依照下列方式設定 [**儲存體 \_ 屬性 \_ 查詢**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) 結構：</span><span class="sxs-lookup"><span data-stu-id="bf6f9-276">To retrieve temperature information from an NVMe drive in the [**STORAGE\_TEMPERATURE\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), configure the [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure as follows:</span></span>

-   <span data-ttu-id="bf6f9-277">配置可包含 [**儲存體 \_ 屬性 \_ 查詢**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) 結構的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-277">Allocate a buffer that can contains a [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure.</span></span>

-   <span data-ttu-id="bf6f9-278">分別將控制器或裝置/命名空間要求的 **PropertyID** 欄位設定為 **StorageAdapterTemperatureProperty** 或 **StorageDeviceTemperatureProperty** 。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-278">Set the **PropertyID** field to **StorageAdapterTemperatureProperty** or **StorageDeviceTemperatureProperty** for a controller or device/namespace request, respectively.</span></span>

-   <span data-ttu-id="bf6f9-279">將 **QueryType** 欄位設定為 **PropertyStandardQuery**。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-279">Set the **QueryType** field to **PropertyStandardQuery**.</span></span>

<span data-ttu-id="bf6f9-280">從 Windows 10)  (的 [**儲存體 \_ 溫度 \_ 資訊**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) 結構如下所示。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-280">The [**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) structure (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_TEMPERATURE_INFO {

    USHORT  Index;                      // Starts from 0. Index 0 may indicate a composite value.
    SHORT   Temperature;                // Signed value; in Celsius.
    SHORT   OverThreshold;              // Signed value; in Celsius.
    SHORT   UnderThreshold;             // Signed value; in Celsius.

    BOOLEAN OverThresholdChangable;     // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN UnderThresholdChangable;    // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN EventGenerated;             // Indicates that notification will be generated when temperature cross threshold.
    UCHAR   Reserved0;
    ULONG   Reserved1;

} STORAGE_TEMPERATURE_INFO, *PSTORAGE_TEMPERATURE_INFO;
```



## <a name="behavior-changing-commands"></a><span data-ttu-id="bf6f9-281">行為變更命令</span><span class="sxs-lookup"><span data-stu-id="bf6f9-281">Behavior changing commands</span></span>

<span data-ttu-id="bf6f9-282">操作裝置屬性或可能影響裝置行為的命令，對作業系統來說更難處理。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-282">Commands that manipulate device attributes or potentially impact device behavior are more difficult for the operating system to deal with.</span></span> <span data-ttu-id="bf6f9-283">如果在處理 i/o 時，裝置屬性在執行時間變更，則如果未正確處理，則可能會發生同步處理或資料完整性問題。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-283">If device attributes change at run-time while I/O is being processed, synchronization or data integrity issues can arise if not properly handled.</span></span>

<span data-ttu-id="bf6f9-284">NVMe **設定功能** 命令是行為變更命令的良好範例。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-284">The NVMe **Set-Features** command is a good example of a behavior changing command.</span></span> <span data-ttu-id="bf6f9-285">它可讓您變更仲裁機制和溫度臨界值的設定。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-285">It allows for the changing of the arbitration mechanism and the setting of temperature thresholds.</span></span> <span data-ttu-id="bf6f9-286">為了確保在進行行為影響的 set 命令時，進行中的資料不會有風險，Windows 會將所有 i/o 暫停至 NVMe 裝置、清空佇列，以及清除緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-286">To ensure that in-flight data is not at risk when behavior-affecting set commands are sent down, Windows will pause all I/O to the NVMe device, drain queues, and flush buffers.</span></span> <span data-ttu-id="bf6f9-287">成功執行 set 命令之後，如果可能) ，就會繼續 (i/o。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-287">Once the set command has executed successfully, I/O is resumed (if possible).</span></span> <span data-ttu-id="bf6f9-288">如果 i/o 無法繼續，可能需要重設裝置。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-288">If I/O cannot be resumed, a device reset may be required.</span></span>

### <a name="setting-temperature-thresholds"></a><span data-ttu-id="bf6f9-289">設定溫度閾值</span><span class="sxs-lookup"><span data-stu-id="bf6f9-289">Setting temperature thresholds</span></span>

<span data-ttu-id="bf6f9-290">Windows 10 引進了 [**ioctl \_ 儲存 \_ 集 \_ 溫度閾值 \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold)，這是取得和設定溫度臨界值的 ioctl。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-290">Windows 10 introduced [**IOCTL\_STORAGE\_SET\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold), an IOCTL for getting and setting temperature thresholds.</span></span> <span data-ttu-id="bf6f9-291">您也可以使用它來取得裝置目前的溫度。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-291">You can also use it to get the current temperature of the device.</span></span> <span data-ttu-id="bf6f9-292">這個 IOCTL 的輸入/輸出緩衝區是 [**儲存 \_ 溫度 \_ 資訊**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) 結構，從先前的程式碼區段。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-292">The input/output buffer for this IOCTL is the [**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) structure, from the previous code section.</span></span>

### <a name="example-setting-over-threshold-temperature"></a><span data-ttu-id="bf6f9-293">範例：設定超過閾值溫度</span><span class="sxs-lookup"><span data-stu-id="bf6f9-293">Example: Setting over-threshold temperature</span></span>

<span data-ttu-id="bf6f9-294">在此範例中，會設定 NVMe 磁片磁碟機的溫度超過閾值。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-294">In this example, an NVMe drive's over-threshold temperature is set.</span></span> <span data-ttu-id="bf6f9-295">下列程式碼會準備命令，然後透過 DeviceIoControl 將它傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-295">The following code prepares the command and then sends it down to the device via DeviceIoControl.</span></span>


```C++
    BOOL    result;  
    ULONG   returnedLength = 0;  
    
    STORAGE_TEMPERATURE_THRESHOLD setThreshold = {0};  

    setThreshold.Version = sizeof(STORAGE_TEMPERATURE_THRESHOLD); 
    setThreshold.Size = sizeof(STORAGE_TEMPERATURE_THRESHOLD);  
    setThreshold.Flags = STORAGE_TEMPERATURE_THRESHOLD_FLAG_ADAPTER_REQUEST;  
    setThreshold.Index = SensorIndex;  
    setThreshold.Threshold = Threshold;  
    setThreshold.OverThreshold = UpdateOverThreshold; 

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD,  
                             &setThreshold,  
                             sizeof(STORAGE_TEMPERATURE_THRESHOLD),  
                             NULL,  
                             0,  
                             &returnedLength,  
                             NULL  
                             ); 

```



### <a name="setting-vendor-specific-features"></a><span data-ttu-id="bf6f9-296">設定廠商特定功能</span><span class="sxs-lookup"><span data-stu-id="bf6f9-296">Setting vendor-specific features</span></span>

<span data-ttu-id="bf6f9-297">如果沒有命令效果記錄檔，驅動程式就不會知道命令的後果。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-297">Without the Command Effects Log, the driver has no knowledge of the ramifications of the command.</span></span> <span data-ttu-id="bf6f9-298">這就是為什麼需要命令效果記錄檔的原因。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-298">This is why the Command Effects Log is required.</span></span> <span data-ttu-id="bf6f9-299">它有助於作業系統判斷某個命令是否有很大的影響，以及它是否可以與其他命令平行傳送到磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-299">It helps the operating system determine if a command is high impact and if it can be sent in parallel with other commands to the drive.</span></span>

<span data-ttu-id="bf6f9-300">命令效果記錄還不夠細微，無法包含廠商專屬的 **設定功能** 命令。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-300">The Command Effects Log is not yet granular enough to encompass vendor-specific **Set-Features** commands.</span></span> <span data-ttu-id="bf6f9-301">基於這個理由，您還無法傳送廠商特有的 **設定功能** 命令。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-301">For this reason, it is not yet possible to send vendor-specific **Set-Features** commands.</span></span> <span data-ttu-id="bf6f9-302">不過，您可以使用稍早所討論的傳遞機制來傳送廠商專屬的命令。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-302">However, it is possible to use the pass-through mechanism, discussed earlier, to send vendor-specific commands.</span></span> <span data-ttu-id="bf6f9-303">如需詳細資訊，請參閱 [傳遞機制](#pass-through-mechanism)。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-303">For more info, see [Pass-through mechanism](#pass-through-mechanism).</span></span>

## <a name="header-files"></a><span data-ttu-id="bf6f9-304">標頭檔</span><span class="sxs-lookup"><span data-stu-id="bf6f9-304">Header files</span></span>

<span data-ttu-id="bf6f9-305">下列檔案與 NVMe 開發相關。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-305">The following files are relevant to NVMe development.</span></span> <span data-ttu-id="bf6f9-306">這些檔案隨附于 [Microsoft Windows 軟體開發套件 (SDK) ](https://developer.microsoft.com/windows/downloads)。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-306">These files are included with the [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads).</span></span>



| <span data-ttu-id="bf6f9-307">標頭檔</span><span class="sxs-lookup"><span data-stu-id="bf6f9-307">Header file</span></span>    | <span data-ttu-id="bf6f9-308">Description</span><span class="sxs-lookup"><span data-stu-id="bf6f9-308">Description</span></span>                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf6f9-309">**ntddstor。h**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-309">**ntddstor.h**</span></span> | <span data-ttu-id="bf6f9-310">定義常數和類型，以從核心模式存取儲存類別驅動程式。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-310">Defines constants and types for accessing the storage class drivers from kernel mode.</span></span>   |
| <span data-ttu-id="bf6f9-311">**nvme。h**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-311">**nvme.h**</span></span>     | <span data-ttu-id="bf6f9-312">適用于其他 NVMe 相關的資料結構。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-312">For other NVMe-related data-structures.</span></span>                                                 |
| <span data-ttu-id="bf6f9-313">**winioctl。h**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-313">**winioctl.h**</span></span> | <span data-ttu-id="bf6f9-314">適用于整體的 Win32 IOCTL 定義，包括使用者模式應用程式的儲存體 Api。</span><span class="sxs-lookup"><span data-stu-id="bf6f9-314">For overall Win32 IOCTL definitions, including storage APIs for user mode applications.</span></span> |



 

 

 
