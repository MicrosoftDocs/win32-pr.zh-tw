---
description: Windows 8 和 Windows Server 2012 引進在虛擬機器上執行之軟體的功能，以偵測可能發生時間移位事件。
ms.assetid: 0793E46B-8464-425E-8C5B-77C14DA90004
title: 虛擬機器世代識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d810a1a65e95f4dde0ccf9779b1e955f2630623e362ffbf94ab8ca36d51d116e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899008"
---
# <a name="virtual-machine-generation-identifier"></a>虛擬機器世代識別碼

Windows 8 和 Windows Server 2012 引進在虛擬機器上執行之軟體的功能，以偵測可能發生時間移位事件。 由於虛擬機器快照集的應用程式或虛擬機器備份的還原，可能會發生時間移位事件。 如需此功能的詳細資訊，請參閱 [虛擬機器世代識別碼白皮書](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx)。

## <a name="prerequisites"></a>必要條件

若要在虛擬機器內使用虛擬機器世代識別碼，您的虛擬機器必須符合下列各項。

-   虛擬機器必須在執行虛擬機器世代識別碼支援的虛擬程式上執行。 目前，這些如下：
    -   Windows 8
    -   Windows Server 2012
    -   Microsoft Hyper-V Server 2012
-   虛擬機器必須正在執行支援虛擬機器世代識別碼的客體作業系統。 目前，這些如下所示。

    下列作業系統擁有虛擬機器世代識別碼的原生支援。

    -   Windows 8
    -   Windows Server 2012
    -   

    如果已安裝 Windows 8 或 Windows Server 2012 的 hyper-v integration services，則可以使用下列操作作為客體作業系統。

    -   Windows Server 2008 R2 包含 Service Pack 1 (SP1))
    -   Windows 7 含 Service Pack 1 (SP1)
    -   Windows Server 2008 Service Pack 2 (SP2)
    -   Windows Server 2003 R2
    -   Windows Server 2003 Service Pack 2 (SP2)
    -   Windows Vista (含 Service Pack 2，SP2)
    -   Windows XP (含 Service Pack 3，SP3)

## <a name="obtaining-the-virtual-machine-generation-identifier"></a>取得虛擬機器世代識別碼

若要以程式設計方式取得虛擬機器世代識別碼，請執行下列步驟。

> [!Note]  
> 您必須以系統管理員或系統許可權來執行下列各項，才能正確運作。

 

1.  在您的應用程式中包含標頭檔 "vmgenerationcounter .h"。 標頭檔包含下列定義：
    ```C++
    DEFINE_GUID(
        GUID_DEVINTERFACE_VM_GENCOUNTER,
        0x3ff2c92b, 
        0x6598, 
        0x4e60, 
        0x8e, 
        0x1c, 
        0x0c, 
        0xcf, 
        0x49, 
        0x27, 
        0xe3, 
        0x19);

    #define VM_GENCOUNTER_SYMBOLIC_LINK_NAME L"VmGenerationCounter"

    #define IOCTL_VMGENCOUNTER_READ CTL_CODE( \
        FILE_DEVICE_ACPI, \
        0x1, METHOD_BUFFERED, \
        FILE_READ_ACCESS | FILE_WRITE_ACCESS)

    typedef struct _VM_GENCOUNTER
    {
        ULONGLONG GenerationCount;
        ULONGLONG GenerationCountHigh;
    } VM_GENCOUNTER, *PVM_GENCOUNTER;
    ```

    

2.  開啟的控制碼 \\ \\ 。 \\VmGenerationCounter "裝置使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)函式。 或者，您可以使用 PnP 管理員來取用裝置介面 **GUID \_ DEVINTERFACE \_ VM \_ GENCOUNTER** ( {3ff2c92b-6598-4e60-8e1c-0ccf4927e319} ) 。 如果應用程式不是在虛擬機器中執行，則不會出現這些物件。
3.  將 [**ioctl \_ Vmgencounter.sys \_ READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) ioctl 傳送至驅動程式，以取出世代識別碼。

    [**Ioctl \_ Vmgencounter.sys \_ READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) ioctl 會以兩種模式、*輪詢* 和 *事件驅動* 的其中一種方式運作。

    若要在輪詢模式中發出 IOCTL，您可以提交輸入緩衝區長度為零的 IOCTL。 為了回應這一點，驅動程式會抓取目前的世代識別碼、將它寫入輸出緩衝區，然後完成 IOCTL。

    若要在事件驅動模式下發出 IOCTL，請提交包含現有世代識別碼之輸入緩衝區的 IOCTL。 為了回應這一點，驅動程式會等到目前的世代識別碼與傳入的世代識別碼不同。 當世代識別碼變更時，驅動程式會將目前的世代識別碼寫入輸出緩衝區，並完成 IOCTL。

    在這兩種模式中，輸出緩衝區的格式和長度都是由 [**VM \_ GENCOUNTER**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) 結構所決定。

    上面所列的所有客體作業系統都支援輪詢模式。 只有 Windows Vista sp2、Windows Server 2008 sp2 和更新版本的作業系統才支援事件驅動模式。 在舊版作業系統上，IOCTL 會失敗，並在事件驅動模式下發出錯誤代碼 **錯誤 \_ \_** 。

    產生識別碼有可能在驅動程式抓取時間與完成 IOCTL 的時間之間變更的時間。 這可能會導致用戶端應用程式接收到過時的資料。 為了避免這種情況，用戶端應用程式可以使用事件驅動模式，以確保最終會瞭解世代識別碼的任何更新。 藉由將用戶端應用程式的目前識別碼做為輸入，事件驅動模式可避免可能導致呼叫者遺漏通知的潛在競爭情形。

下列程式碼範例示範如何執行上述動作，以取得虛擬機器世代識別碼。

> [!Note]  
> 下列程式碼必須以系統管理員或系統許可權執行，才能正確運作。

 


```C++
HRESULT GetVmCounter(bool fWaitForChange)
{
    BOOL success = FALSE;
    DWORD error = ERROR_SUCCESS;
    VM_GENCOUNTER vmCounterOutput = {0};
    DWORD size = 0;
    HANDLE handle = INVALID_HANDLE_VALUE;
    HRESULT hr = S_OK;

    handle = CreateFile(
        L"\\\\.\\" VM_GENCOUNTER_SYMBOLIC_LINK_NAME,
        GENERIC_READ | GENERIC_WRITE,
        FILE_SHARE_READ | FILE_SHARE_WRITE,
        NULL,
        OPEN_EXISTING,
        0,
        NULL);

    if (handle == INVALID_HANDLE_VALUE)
    {
        error = GetLastError();

        wprintf(
            L"Unable to open device %s. Error code = %d.", 
            VM_GENCOUNTER_SYMBOLIC_LINK_NAME, 
            error);

        hr = HRESULT_FROM_WIN32(error);

        goto Cleanup;
    }

    /*
    Call into the driver. 

    Because the 4th parameter to DeviceIoControl (nInBufferSize) is zero, this 
    is a polling request rather than an event-driven request.
    */
    success = DeviceIoControl(
        handle,
        IOCTL_VMGENCOUNTER_READ,
        NULL,
        0,
        &vmCounterOutput,
        sizeof(vmCounterOutput),
        &size,
        NULL);

    if (!success)
    {
        error = GetLastError();

        wprintf(L"Call IOCTL_VMGENCOUNTER_READ failed with %d.", error);

        hr = HRESULT_FROM_WIN32(error);

        goto Cleanup;
    }

    wprintf(
        L"VmCounterValue: %I64x:%I64x",
        vmCounterOutput.GenerationCount,
        vmCounterOutput.GenerationCountHigh);

    if (fWaitForChange)
    {
        /*
        Call into the driver again in event-driven mode. DeviceIoControl won't 
        return until the generation identifier has changed.
        */
        success = DeviceIoControl(
            handle,
            IOCTL_VMGENCOUNTER_READ,
            &vmCounterOutput,
            sizeof(vmCounterOutput),
            &vmCounterOutput,
            sizeof(vmCounterOutput),
            &size,
            NULL);

        if (!success)
        {
            error = GetLastError();

            wprintf(L"Call IOCTL_VMGENCOUNTER_READ failed with %d.", error);

            hr = HRESULT_FROM_WIN32(error);

            goto Cleanup;
        }

        wprintf(
            L"VmCounterValue changed to: %I64x:%I64x",
            vmCounterOutput.GenerationCount,
            vmCounterOutput.GenerationCountHigh);
    }

Cleanup:

    if (handle != INVALID_HANDLE_VALUE)
    {
        CloseHandle(handle);
    }

    return hr;
};
```



## <a name="determining-if-a-time-shift-event-has-occurred"></a>判斷是否發生時間移位事件

取得虛擬機器世代識別碼之後，您應該加以儲存，以供日後使用。 在您的應用程式執行時間緊迫的作業（例如認可資料庫）之前，您應該重新取得世代識別碼，並將其與儲存的值進行比較。 如果識別碼已變更，這表示已發生時間移位事件，而且您的應用程式必須適當地執行動作。

 

 
