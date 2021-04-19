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
# <a name="working-with-nvme-drives"></a>使用 NVMe 磁片磁碟機

**適用範圍：**

-   Windows 10
-   Windows Server 2016

瞭解如何從您的 Windows 應用程式使用高速 NVMe 裝置。 您可以透過 **StorNVMe.sys** 啟用裝置存取，並在 Windows Server 2012 R2 和 Windows 8.1 中首次引進驅動程式驅動程式。 Windows 7 裝置也可以透過 KB 熱修正來取得此功能。 在 Windows 10 中引進了幾項新功能，包括廠商專屬 NVMe 命令的傳遞機制，以及現有 IOCTLs 的更新。

本主題概要說明您可以用來存取 Windows 10 中 NVMe 磁片磁碟機的一般使用 Api。 它也會說明：

-   如何使用[傳遞](#pass-through-mechanism)來傳送廠商專屬 NVMe 命令
-   如何 [傳送識別、取得功能或取得記錄頁面命令](#protocol-specific-queries) 至 NVMe 磁片磁碟機
-   如何從 NVMe 磁片磁碟機[取得溫度資訊](#temperature-queries)
-   如何執行行為變更命令，例如 [設定溫度閾值](#behavior-changing-commands)

## <a name="apis-for-working-with-nvme-drives"></a>使用 NVMe 磁片磁碟機的 Api

您可以使用下列一般用途的 Api，在 Windows 10 中存取 NVMe 磁片磁碟機。 您可以在使用者模式應用程式的 **winioctl** 中找到這些 api，並針對核心模式驅動程式使用 **ntddstor。** 如需標頭檔的詳細資訊，請參閱 [標頭檔](#header-files)。

-   [**IOCTL \_儲存體 \_ 通訊協定 \_ 命令**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) ：使用此 IOCTL 搭配 **儲存體 \_ 通訊協定 \_ 命令** 結構來發出 NVMe 命令。 這個 IOCTL 可啟用 NVMe 傳遞，並支援在 NVMe 中使用命令效果記錄檔。 您可以將它與廠商特定的命令搭配使用。 如需詳細資訊，請參閱 [傳遞機制](#pass-through-mechanism)。

-   [**儲存體 \_通訊協定 \_ 命令**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) ：此輸入緩衝區結構包含 **ReturnStatus** 欄位，可用來報告下列狀態值。
    -   **儲存體 \_ 通訊協定 \_ 狀態 \_ 暫止**
    -   **儲存體 \_ 通訊協定 \_ 狀態 \_ 成功**
    -   **儲存體 \_ 通訊協定 \_ 狀態 \_ 錯誤**
    -   **儲存體 \_ 通訊協定 \_ 狀態 \_ 不正確 \_ 要求**
    -   **儲存體 \_ 通訊協定 \_ 狀態 \_ 無 \_ 裝置**
    -   **儲存體 \_ 通訊協定 \_ 狀態 \_ 忙碌中**
    -   **儲存體 \_ 通訊協定 \_ 狀態 \_ 資料 \_ 溢出**
    -   **儲存體 \_ 通訊 \_ 協定 \_ 狀態 \_ 資源不足**
    -   **\_ \_ \_ 不支援儲存體通訊協定狀態 \_**
-   [**IOCTL \_儲存體 \_ 查詢 \_ 屬性**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) ：使用此 IOCTL 搭配 **儲存體 \_ 屬性 \_ 查詢** 結構來取得裝置資訊。 如需詳細資訊，請參閱 [通訊協定特定的查詢](#protocol-specific-queries) 和 [溫度查詢](#temperature-queries)。

-   [**儲存體 \_屬性 \_ 查詢**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) ：此結構包含 **PropertyId** 和 **AdditionalParameters** 欄位，以指定要查詢的資料。 在 [ **PropertyId** ] 欄位中，使用 [ **儲存體 \_ 屬性 \_ 識別碼** ] 列舉來指定資料類型。 您可以使用 [ **AdditionalParameters** ] 欄位來指定更多詳細資料，視資料類型而定。 針對通訊協定特定的資料，請使用 **AdditionalParameters** 欄位中的 **儲存體 \_ 通訊協定 \_ 特定 \_ 資料** 結構。 針對溫度資料，請使用 **AdditionalParameters** 欄位中的 **儲存體 \_ 溫度 \_ 資訊** 結構。
-   [**儲存體 \_屬性 \_ 識別碼**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) ：此列舉包含新的值，可讓 **IOCTL \_ 儲存體 \_ 查詢 \_ 屬性** 取得特定通訊協定和溫度資訊。

    -   **StorageAdapterProtocolSpecificProperty**
    -   **StorageDeviceProtocolSpecificProperty**

    使用這些通訊協定特定的其中一個屬性識別碼搭配 **儲存體 \_ 通訊協定 \_ 特定 \_ 資料** ，以取得 [**儲存體 \_ 通訊協定 \_ 資料 \_ 描述**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) 元結構中的通訊協定特定資料。

    -   **StorageAdapterTemperatureProperty**
    -   **StorageDeviceTemperatureProperty**

    使用其中一個溫度屬性識別碼，以取得 [**儲存體 \_ 溫度 \_ 資料 \_ 描述**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) 元結構中的溫度資料。

-   [**儲存體 \_通訊協定 \_ 特定 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data)：當此結構用於 **儲存體 \_ 屬性 \_ 查詢** 的 **AdditionalParameters** 欄位，以及指定 [**儲存體 \_ 通訊協定 \_ NVMe \_ 資料 \_ 類型**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type)列舉值時，抓取 NVMe 特定的資料。 在 **儲存體 \_ 通訊協定 \_ 特定 \_ 資料** 結構的 **DataType** 欄位中，使用下列其中一個 **儲存體 \_ 通訊協定 \_ NVME \_ 資料 \_ 類型** 值：

    -   使用 **NVMeDataTypeIdentify** 來取得識別控制器資料或識別命名空間資料。
    -   使用 **NVMeDataTypeLogPage** 取得記錄頁面 (包括智慧型/健康情況資料) 。
    -   使用 **NVMeDataTypeFeature** 取得 NVMe 磁片磁碟機的功能。

-   [**儲存體 \_溫度 \_ 資訊**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) ：此結構是用來保存特定溫度資料。 它會在 **儲存體 \_ TEMERATURE \_ 資料 \_ 描述** 元中用來傳回溫度查詢的結果。

-   [**IOCTL \_儲存體 \_ 設定 \_ 溫度 \_ 閾值**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) ：使用此 IOCTL 搭配 **儲存 \_ 溫度 \_ 閾值** 結構來設定溫度閾值。 如需詳細資訊，請參閱 [行為變更命令](#behavior-changing-commands)。

-   [**儲存體 \_溫度 \_ 閾值**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) ：此結構會用來做為輸入緩衝區，以指定溫度閾值。 **OverThreshold** 欄位 (布林值) 指定 **臨界** 值欄位是否為超過臨界值，否則為不 (; 否則為臨界值) 。

## <a name="pass-through-mechanism"></a>傳遞機制

NVMe 規格中未定義的命令是主機 OS 處理最困難的方式–主機無法深入瞭解命令可能對目標裝置造成的影響、公開的基礎結構 (命名空間/區塊大小) ，以及其行為。

為了透過 Windows 儲存體堆疊更妥善地攜帶這類裝置特定命令，新的傳遞機制可讓廠商特定的命令通過管道。 此傳遞管道也有助於開發管理和測試控管。 不過，此傳遞機制需要使用命令效果記錄檔。 此外，StoreNVMe.sys 需要在命令效果記錄檔中描述所有命令，而不只是傳遞命令。

> [!IMPORTANT]
> 如果命令效果記錄中未描述任何命令，StorNVMe.sys 和 Storport.sys 會封鎖該裝置的任何命令。

 

### <a name="supporting-the-command-effects-log"></a>支援命令效果記錄檔

命令效果記錄 (如支援和效果的命令中所述，在 [NVMe 規格 1.2](https://nvmexpress.org/specifications) 的5.10.1.5 一節中，) 可讓廠商專屬命令的效果與規格定義的命令進行描述。 這可促進命令支援驗證以及命令列為優化，因此應該針對裝置支援的整組命令來執行。 下列條件描述如何根據命令的命令效果記錄專案傳送命令的結果。

針對命令效果記錄檔中所述的任何特定命令 .。。

**While**：

-   支援的命令 (CSUPP) 設定為 ' 1 '，表示控制器 (位01所支援的命令) 

    > [!Note]  
    > 當 CSUPP 設定為 ' 0 ' 時 (表示不支援命令) 將會封鎖命令

     

**如果** 有下列任何一項設定，則為：

-   控制器功能變更 (CCC) 設定為 ' 1 '，表示命令可能會變更控制器功能 (Bit 04) 

-   命名空間清查變更 (NIC) 設定為 ' 1 '，表示命令可能會變更多個命名空間的數目或功能 (位 03) 

-   命名空間功能變更 (NCC) 設定為 ' 1 '，表示命令可能會變更單一命名空間 (位02的功能) 

-   命令提交和執行 (CSE) 設定為001b 或010b，表示當相同或任何命名空間沒有其他未完成的命令時，可能會提交命令，而且在這個命令完成 (位18:16 之前，不應將另一個命令提交至相同或任何命名空間) 

**然後** ，命令會傳送為介面卡未完成的唯一命令。

**否則** 為：

-   命令提交和執行 (CSE) 設定為001b，表示在相同的命名空間沒有其他未處理的命令時可能會提交命令，而且在此命令 18:16 (完成之前，不應將另一個命令提交至相同的命名空間) 

**然後** 命令會以唯一未完成的命令傳送給邏輯單元編號物件 (LUN) 。

**否則**，此命令會與未抑制的其他命令一起傳送。 例如，如果將廠商專屬的命令傳送至裝置，以抓取未定義規格的統計資訊，則變更裝置的行為或功能以執行 i/o 命令應該不會有任何風險。 這類要求可能會以平行方式提供給 i/o，而且不需要暫停-繼續。

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a>使用 IOCTL \_ 儲存體 \_ 通訊協定 \_ 命令傳送命令

您可以使用 Windows 10 中引進的 [**IOCTL \_ 儲存 \_ 通訊協定 \_ 命令**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command)來進行傳遞。 這個 IOCTL 的設計與現有的 SCSI 和 ATA 傳遞 IOCTLs 具有類似的行為，以將內嵌的命令傳送至目標裝置。 透過這個 IOCTL，傳遞可以傳送至存放裝置（包括 NVMe 磁片磁碟機）。

例如，在 NVMe 中，IOCTL 將允許傳送下列命令程式碼。

-   廠商特定的系統管理命令 (C0h – FFh) 
-   廠商特定 NVMe 命令 (80h – FFh) 

如同所有其他 IOCTLs，請使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 來傳送傳遞的 IOCTL。 您可以使用在 **ntddstor** 中找到的 [**儲存體 \_ 通訊協定 \_ 命令**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command)輸入緩衝區結構來填入 IOCTL。 使用廠商特定的命令填入 **命令** 欄位。


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



要傳送的廠商特定命令應該填入上面的反白顯示欄位中。 請再次注意，命令效果記錄檔必須針對傳遞命令來執行。 尤其是，這些命令必須在命令效果記錄檔中報告為支援 (如需詳細資訊) ，請參閱上一節。 另請注意，PRP 欄位是驅動程式特定的，因此傳送命令的應用程式可以將其保留為0。

最後，此傳遞 IOCTL 是為了傳送廠商特定的命令。 若要傳送其他系統管理員或非廠商特定 NVMe 命令（例如識別），則不應使用此傳遞 IOCTL。 例如，您應該使用 [ **IOCTL \_ 儲存體 \_ 查詢] \_ 屬性** 來識別或取得記錄頁面。 如需詳細資訊，請參閱下一節的 [通訊協定特定查詢](/windows)。

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a>不要透過傳遞機制更新固件

不應使用傳遞來傳送固件下載和啟用命令。 **IOCTL \_儲存體 \_ 通訊協定 \_ 命令** 只能用於廠商特定的命令。

相反地，請使用 Windows 10) 引進的下列一般儲存體 IOCTLs (，以避免使用 SCSI \_ 微型埠版本的固件 IOCTL 直接使用應用程式。 儲存體驅動程式會將 IOCTL 轉譯成 SCSI 命令，或將 IOCTL 的 SCSI \_ 微型埠版本轉譯為微型埠。

建議您在 Windows 10 和 Windows Server 2016 中開發固件升級工具，以進行這些 IOCTLs：

-   [**IOCTL \_ 儲存體 \_ 固件 \_ 取得 \_ 資訊**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [**IOCTL \_ 儲存體 \_ 固件 \_ 下載**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [**\_啟用 IOCTL 儲存體 \_ 固件 \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

為了取得儲存體資訊和更新固件，Windows 也支援 PowerShell Cmdlet 來快速進行：

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> 若要更新 Windows 8.1 中 NVMe 的固件，請使用 IOCTL \_ SCSI \_ 微型埠 \_ 固件。 這個 IOCTL 未 backport 至 Windows 7。 如需詳細資訊，請參閱 [Windows 8.1 中的升級 NVMe 裝置的固件](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device)。

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a>透過傳遞機制傳回錯誤

類似于 SCSI 和 ATA 傳遞 IOCTLs，當命令/要求傳送至微型埠或裝置時，如果成功，則會傳回 IOCTL。 在 [**儲存體 \_ 通訊協定 \_ 命令**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) 結構中，IOCTL 會透過 **ReturnStatus** 欄位傳回狀態。

### <a name="example-sending-a-vendor-specific-command"></a>範例：傳送廠商特定的命令

在此範例中，會透過傳遞到 NVMe 磁片磁碟機，將任意的廠商專屬命令 (0xFF) 傳送到 NVMe 磁片磁碟機。 下列程式碼會配置緩衝區、初始化查詢，然後透過 DeviceIoControl 將命令向下傳送至裝置。


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



在此範例中，我們會預期 `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` 命令是否成功至裝置。

## <a name="protocol-specific-queries"></a>特定通訊協定的查詢

Windows 8.1 引進了資料抓取的 [**IOCTL \_ 儲存體 \_ 查詢 \_ 屬性**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) 。 在 Windows 10 中，已增強 IOCTL 以支援一般要求的 NVMe 功能，例如 **取得記錄頁面**、 **取得功能** 和 **識別**。 這可讓您抓取 NVMe 特定資訊，以供監視和清查之用。

以下顯示 IOCTL 的輸入緩衝區、Windows 10)  ([**儲存體 \_ 屬性 \_ 查詢**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) 。


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



使用 [**IOCTL \_ 儲存體 \_ 查詢 \_ 屬性**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) 來取出 [**儲存體 \_ 通訊協定 \_ 資料 \_ 描述**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor)項中 NVMe 的通訊協定特定資訊時，請設定 [**存放裝置 \_ 屬性 \_ 查詢**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) 結構，如下所示：

-   配置可同時包含 [**儲存體 \_ 屬性 \_ 查詢**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) 和 [**儲存體 \_ 通訊協定 \_ 特定 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) 結構的緩衝區。

-   分別將控制器或裝置/命名空間要求的 **PropertyID** 欄位設定為 **StorageAdapterProtocolSpecificProperty** 或 **StorageDeviceProtocolSpecificProperty** 。

-   將 **QueryType** 欄位設定為 **PropertyStandardQuery**。

-   以所需的值填入 [**儲存體 \_ 通訊協定 \_ 特定的 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) 結構。 **儲存體 \_ 通訊協定 \_ 特定 \_ 資料** 的開始是 [**儲存體 \_ 屬性 \_ 查詢**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query)的 **AdditionalParameters** 欄位。

從 Windows 10)  ([**儲存體 \_ 通訊協定 \_ 特定的 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) 結構，如下所示。


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



若要指定 NVMe 通訊協定特定資訊的類型，請設定 [**儲存體 \_ 通訊協定 \_ 特定的 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) 結構，如下所示：

-   將 **ProtocolType** 欄位設定為 **ProtocolTypeNVMe**。

-   將 **DataType** 欄位設定為 [**儲存體 \_ 通訊協定 \_ NVME \_ 資料 \_ 類型**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type)所定義的列舉值：

    -   使用 **NVMeDataTypeIdentify** 來取得識別控制器資料或識別命名空間資料。
    -   使用 **NVMeDataTypeLogPage** 取得記錄頁面 (包括智慧型/健康情況資料) 。
    -   使用 **NVMeDataTypeFeature** 取得 NVMe 磁片磁碟機的功能。

使用 **ProtocolTypeNVMe** 做為 **ProtocolType** 時，可以使用 NVMe 磁片磁碟機上的其他 i/o 來平行抓取通訊協定特定資訊的查詢。

下列範例示範 NVMe 通訊協定特定的查詢。

### <a name="example-nvme-identify-query"></a>範例： NVMe 識別查詢

在此範例中，會將 **識別** 要求傳送到 NVMe 磁片磁碟機。 下列程式碼會初始化查詢資料結構，然後透過 DeviceIoControl 將命令向下傳送至裝置。


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



請注意，呼叫端必須配置單一緩衝區，其中包含儲存體 \_ 屬性 \_ 查詢和儲存體 \_ 通訊協定特定資料的大小 \_ \_ 。 在此範例中，它會針對屬性查詢的輸入和輸出使用相同的緩衝區。 這就是為什麼配置的緩衝區大小為「欄位 \_ 位移 (儲存體 \_ 屬性 \_ 查詢，AdditionalParameters) + sizeof (儲存體 \_ 通訊協定 \_ 特定 \_ 資料) + NVME 記錄檔 \_ 大小上限」 \_ \_ 。 雖然可以為輸入和輸出配置不同的緩衝區，但我們建議使用單一緩衝區來查詢 NVMe 相關資訊。

### <a name="example-nvme-get-log-pages-query"></a>範例： NVMe 取得記錄頁面查詢

在此範例中，根據上一個範例，_ *取得記錄頁面** 要求會傳送至 NVMe 磁片磁碟機。 下列程式碼會準備查詢資料結構，然後透過 DeviceIoControl 將命令向下傳送至裝置。


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



### <a name="example-nvme-get-features-query"></a>範例： NVMe Get Features 查詢

在此範例中，根據上一個範例，_ *Get Features** 要求會傳送至 NVMe 磁片磁碟機。 下列程式碼會準備查詢資料結構，然後透過 DeviceIoControl 將命令向下傳送至裝置。


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
## <a name="protocol-specific-set"></a>通訊協定特定的集合

從 Windows 10 19H1，IOCTL_STORAGE_SET_PROPERTY 已增強為支援 NVMe 設定的功能。

IOCTL_STORAGE_SET_PROPERTY 的輸入緩衝區如下所示：

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

使用 IOCTL_STORAGE_SET_PROPERTY 設定 NVMe 功能時，請設定 STORAGE_PROPERTY_SET 結構，如下所示：

-   配置可同時包含 STORAGE_PROPERTY_SET 和 STORAGE_PROTOCOL_SPECIFIC_DATA_EXT 結構的緩衝區;
-   分別將控制器或裝置/命名空間要求的 PropertyID 欄位設定為 StorageAdapterProtocolSpecificProperty 或 StorageDeviceProtocolSpecificProperty。
-   以所需的值填滿 STORAGE_PROTOCOL_SPECIFIC_DATA_EXT 結構。 STORAGE_PROTOCOL_SPECIFIC_DATA_EXT 的開頭是 STORAGE_PROPERTY_SET 的 AdditionalParameters 欄位。

STORAGE_PROTOCOL_SPECIFIC_DATA_EXT 結構如下所示。

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

若要指定要設定的 NVMe 功能類型，請設定 STORAGE_PROTOCOL_SPECIFIC_DATA_EXT 結構，如下所示：
-   將 ProtocolType 欄位設定為 ProtocolTypeNvme;
-   將 DataType 欄位設定為 STORAGE_PROTOCOL_NVME_DATA_TYPE 所定義的列舉值 NVMeDataTypeFeature;

下列範例示範 NVMe 功能集。

### <a name="example-nvme-set-features"></a>範例： NVMe 設定功能

在此範例中，會將設定功能要求傳送到 NVMe 磁片磁碟機。 下列程式碼會準備 set 資料結構，然後透過 DeviceIoControl 將命令向下傳送至裝置。

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

## <a name="temperature-queries"></a>溫度查詢

在 Windows 10 中，您也可以使用 [**IOCTL \_ 儲存體 \_ 查詢 \_ 屬性**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) ，從 NVMe 裝置查詢溫度資料。

若要從 [**儲存體 \_ 溫度 \_ 資料 \_ 描述**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor)項中的 NVMe 磁片磁碟機取出溫度資訊，請依照下列方式設定 [**儲存體 \_ 屬性 \_ 查詢**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) 結構：

-   配置可包含 [**儲存體 \_ 屬性 \_ 查詢**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) 結構的緩衝區。

-   分別將控制器或裝置/命名空間要求的 **PropertyID** 欄位設定為 **StorageAdapterTemperatureProperty** 或 **StorageDeviceTemperatureProperty** 。

-   將 **QueryType** 欄位設定為 **PropertyStandardQuery**。

從 Windows 10)  (的 [**儲存體 \_ 溫度 \_ 資訊**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) 結構如下所示。


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



## <a name="behavior-changing-commands"></a>行為變更命令

操作裝置屬性或可能影響裝置行為的命令，對作業系統來說更難處理。 如果在處理 i/o 時，裝置屬性在執行時間變更，則如果未正確處理，則可能會發生同步處理或資料完整性問題。

NVMe **設定功能** 命令是行為變更命令的良好範例。 它可讓您變更仲裁機制和溫度臨界值的設定。 為了確保在進行行為影響的 set 命令時，進行中的資料不會有風險，Windows 會將所有 i/o 暫停至 NVMe 裝置、清空佇列，以及清除緩衝區。 成功執行 set 命令之後，如果可能) ，就會繼續 (i/o。 如果 i/o 無法繼續，可能需要重設裝置。

### <a name="setting-temperature-thresholds"></a>設定溫度閾值

Windows 10 引進了 [**ioctl \_ 儲存 \_ 集 \_ 溫度閾值 \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold)，這是取得和設定溫度臨界值的 ioctl。 您也可以使用它來取得裝置目前的溫度。 這個 IOCTL 的輸入/輸出緩衝區是 [**儲存 \_ 溫度 \_ 資訊**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) 結構，從先前的程式碼區段。

### <a name="example-setting-over-threshold-temperature"></a>範例：設定超過閾值溫度

在此範例中，會設定 NVMe 磁片磁碟機的溫度超過閾值。 下列程式碼會準備命令，然後透過 DeviceIoControl 將它傳送至裝置。


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



### <a name="setting-vendor-specific-features"></a>設定廠商特定功能

如果沒有命令效果記錄檔，驅動程式就不會知道命令的後果。 這就是為什麼需要命令效果記錄檔的原因。 它有助於作業系統判斷某個命令是否有很大的影響，以及它是否可以與其他命令平行傳送到磁片磁碟機。

命令效果記錄還不夠細微，無法包含廠商專屬的 **設定功能** 命令。 基於這個理由，您還無法傳送廠商特有的 **設定功能** 命令。 不過，您可以使用稍早所討論的傳遞機制來傳送廠商專屬的命令。 如需詳細資訊，請參閱 [傳遞機制](#pass-through-mechanism)。

## <a name="header-files"></a>標頭檔

下列檔案與 NVMe 開發相關。 這些檔案隨附于 [Microsoft Windows 軟體開發套件 (SDK) ](https://developer.microsoft.com/windows/downloads)。



| 標頭檔    | Description                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| **ntddstor。h** | 定義常數和類型，以從核心模式存取儲存類別驅動程式。   |
| **nvme。h**     | 適用于其他 NVMe 相關的資料結構。                                                 |
| **winioctl。h** | 適用于整體的 Win32 IOCTL 定義，包括使用者模式應用程式的儲存體 Api。 |



 

 

 
