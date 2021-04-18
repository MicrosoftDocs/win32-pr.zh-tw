---
description: Windows 8 和 Windows Server 2012 引進在虛擬機器上執行之軟體的功能，以偵測可能發生時間移位事件。
ms.assetid: 0793E46B-8464-425E-8C5B-77C14DA90004
title: 虛擬機器世代識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df6ecbb600dbc7ae2efe14d36cb17cc75816444
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971572"
---
# <a name="virtual-machine-generation-identifier"></a><span data-ttu-id="44804-103">虛擬機器世代識別碼</span><span class="sxs-lookup"><span data-stu-id="44804-103">Virtual machine generation identifier</span></span>

<span data-ttu-id="44804-104">Windows 8 和 Windows Server 2012 引進在虛擬機器上執行之軟體的功能，以偵測可能發生時間移位事件。</span><span class="sxs-lookup"><span data-stu-id="44804-104">Windows 8 and Windows Server 2012 introduce the ability for software that is running on a virtual machine to detect that a time shift event may have occurred.</span></span> <span data-ttu-id="44804-105">由於虛擬機器快照集的應用程式或虛擬機器備份的還原，可能會發生時間移位事件。</span><span class="sxs-lookup"><span data-stu-id="44804-105">Time shift events can occur as a result of an application of a virtual machine snapshot or the restoration of a virtual machine backup.</span></span> <span data-ttu-id="44804-106">如需此功能的詳細資訊，請參閱 [虛擬機器世代識別碼白皮書](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx)。</span><span class="sxs-lookup"><span data-stu-id="44804-106">For more information about this functionality, see the [Virtual Machine Generation ID white paper](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="44804-107">必要條件</span><span class="sxs-lookup"><span data-stu-id="44804-107">Prerequisites</span></span>

<span data-ttu-id="44804-108">若要在虛擬機器內使用虛擬機器世代識別碼，您的虛擬機器必須符合下列各項。</span><span class="sxs-lookup"><span data-stu-id="44804-108">To use the virtual machine generation identifier from inside a virtual machine your virtual machine must conform to the following.</span></span>

-   <span data-ttu-id="44804-109">虛擬機器必須在執行虛擬機器世代識別碼支援的虛擬程式上執行。</span><span class="sxs-lookup"><span data-stu-id="44804-109">The virtual machine must be running on a hypervisor that implements support for virtual machine generation identifiers.</span></span> <span data-ttu-id="44804-110">目前，這些如下：</span><span class="sxs-lookup"><span data-stu-id="44804-110">Currently, these are the following:</span></span>
    -   <span data-ttu-id="44804-111">Windows 8</span><span class="sxs-lookup"><span data-stu-id="44804-111">Windows 8</span></span>
    -   <span data-ttu-id="44804-112">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="44804-112">Windows Server 2012</span></span>
    -   <span data-ttu-id="44804-113">Microsoft Hyper-V Server 2012</span><span class="sxs-lookup"><span data-stu-id="44804-113">Microsoft Hyper-V Server 2012</span></span>
-   <span data-ttu-id="44804-114">虛擬機器必須正在執行支援虛擬機器世代識別碼的客體作業系統。</span><span class="sxs-lookup"><span data-stu-id="44804-114">The virtual machine must be running a guest operating system that has support for the virtual machine generation identifier.</span></span> <span data-ttu-id="44804-115">目前，這些如下所示。</span><span class="sxs-lookup"><span data-stu-id="44804-115">Currently, these are the following.</span></span>

    <span data-ttu-id="44804-116">下列作業系統擁有虛擬機器世代識別碼的原生支援。</span><span class="sxs-lookup"><span data-stu-id="44804-116">The following operating systems have native support for the virtual machine generation identifier.</span></span>

    -   <span data-ttu-id="44804-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="44804-117">Windows 8</span></span>
    -   <span data-ttu-id="44804-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="44804-118">Windows Server 2012</span></span>
    -   

    <span data-ttu-id="44804-119">如果已安裝 Windows 8 或 Windows Server 2012 中的 Hyper-v integration services，則可以使用下列操作作為客體作業系統。</span><span class="sxs-lookup"><span data-stu-id="44804-119">The following operating can be used as the guest operating system if the Hyper-V integration services from Windows 8 or Windows Server 2012 are installed.</span></span>

    -   <span data-ttu-id="44804-120">Windows Server 2008 R2 包含 Service Pack 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="44804-120">Windows Server 2008 R2 with Service Pack 1 (SP1)</span></span>
    -   <span data-ttu-id="44804-121">Windows 7 含 Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="44804-121">Windows 7 with Service Pack 1 (SP1)</span></span>
    -   <span data-ttu-id="44804-122">Windows Server 2008 Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="44804-122">Windows Server 2008 with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="44804-123">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="44804-123">Windows Server 2003 R2</span></span>
    -   <span data-ttu-id="44804-124">Windows Server 2003 Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="44804-124">Windows Server 2003 with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="44804-125">Windows Vista (含 Service Pack 2，SP2)</span><span class="sxs-lookup"><span data-stu-id="44804-125">Windows Vista with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="44804-126">Windows XP (含 Service Pack 3，SP3)</span><span class="sxs-lookup"><span data-stu-id="44804-126">Windows XP with Service Pack 3 (SP3)</span></span>

## <a name="obtaining-the-virtual-machine-generation-identifier"></a><span data-ttu-id="44804-127">取得虛擬機器世代識別碼</span><span class="sxs-lookup"><span data-stu-id="44804-127">Obtaining the virtual machine generation identifier</span></span>

<span data-ttu-id="44804-128">若要以程式設計方式取得虛擬機器世代識別碼，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="44804-128">To programmatically obtain the virtual machine generation identifier, perform the following steps.</span></span>

> [!Note]  
> <span data-ttu-id="44804-129">您必須以系統管理員或系統許可權來執行下列各項，才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="44804-129">The following must be run with administrator or system privileges to function correctly.</span></span>

 

1.  <span data-ttu-id="44804-130">在您的應用程式中包含標頭檔 "vmgenerationcounter .h"。</span><span class="sxs-lookup"><span data-stu-id="44804-130">Include header file "vmgenerationcounter.h" in your app.</span></span> <span data-ttu-id="44804-131">標頭檔包含下列定義：</span><span class="sxs-lookup"><span data-stu-id="44804-131">The header file contains these definitions:</span></span>
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

    

2.  <span data-ttu-id="44804-132">開啟的控制碼 \\ \\ 。 \\VmGenerationCounter "裝置使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)函式。</span><span class="sxs-lookup"><span data-stu-id="44804-132">Open a handle to the "\\\\.\\VmGenerationCounter" device using the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="44804-133">或者，您可以使用 PnP 管理員來取用裝置介面 **GUID \_ DEVINTERFACE \_ VM \_ GENCOUNTER** ( {3ff2c92b-6598-4e60-8e1c-0ccf4927e319} ) 。</span><span class="sxs-lookup"><span data-stu-id="44804-133">Alternatively, you can use the PnP manager to consume the device interface **GUID\_DEVINTERFACE\_VM\_GENCOUNTER** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}).</span></span> <span data-ttu-id="44804-134">如果應用程式不是在虛擬機器中執行，則不會出現這些物件。</span><span class="sxs-lookup"><span data-stu-id="44804-134">These objects will not be present if the app is not running in a virtual machine.</span></span>
3.  <span data-ttu-id="44804-135">將 [**ioctl \_ Vmgencounter.sys \_ READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) ioctl 傳送至驅動程式，以取出世代識別碼。</span><span class="sxs-lookup"><span data-stu-id="44804-135">Send the [**IOCTL\_VMGENCOUNTER\_READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL to the driver to retrieve the generation identifier.</span></span>

    <span data-ttu-id="44804-136">[**Ioctl \_ Vmgencounter.sys \_ READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) ioctl 會以兩種模式、*輪詢* 和 *事件驅動* 的其中一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="44804-136">The [**IOCTL\_VMGENCOUNTER\_READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL operates in one of two modes, *polling*, and *event driven*.</span></span>

    <span data-ttu-id="44804-137">若要在輪詢模式中發出 IOCTL，您可以提交輸入緩衝區長度為零的 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="44804-137">To issue the IOCTL in polling mode, you submit the IOCTL with an input buffer of zero length.</span></span> <span data-ttu-id="44804-138">為了回應這一點，驅動程式會抓取目前的世代識別碼、將它寫入輸出緩衝區，然後完成 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="44804-138">In response to this, the driver retrieves the current generation identifier, writes it to the output buffer, and completes the IOCTL.</span></span>

    <span data-ttu-id="44804-139">若要在事件驅動模式下發出 IOCTL，請提交包含現有世代識別碼之輸入緩衝區的 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="44804-139">To issue the IOCTL in event driven mode, submit the IOCTL with an input buffer that contains an existing generation identifier.</span></span> <span data-ttu-id="44804-140">為了回應這一點，驅動程式會等到目前的世代識別碼與傳入的世代識別碼不同。</span><span class="sxs-lookup"><span data-stu-id="44804-140">In response to this, the driver waits until the current generation identifier becomes different from the generation identifier that was passed in.</span></span> <span data-ttu-id="44804-141">當世代識別碼變更時，驅動程式會將目前的世代識別碼寫入輸出緩衝區，並完成 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="44804-141">When the generation identifier changes, the driver writes the current generation identifier to the output buffer and completes the IOCTL.</span></span>

    <span data-ttu-id="44804-142">在這兩種模式中，輸出緩衝區的格式和長度都是由 [**VM \_ GENCOUNTER**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) 結構所決定。</span><span class="sxs-lookup"><span data-stu-id="44804-142">In both modes, the format and length of the output buffer is dictated by the [**VM\_GENCOUNTER**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) structure.</span></span>

    <span data-ttu-id="44804-143">上面所列的所有客體作業系統都支援輪詢模式。</span><span class="sxs-lookup"><span data-stu-id="44804-143">Polling mode is supported on all of the guest operating systems listed above.</span></span> <span data-ttu-id="44804-144">只有在 Windows Vista SP2、Windows Server 2008 SP2 和更新版本的作業系統上才支援事件驅動模式。</span><span class="sxs-lookup"><span data-stu-id="44804-144">Event driven mode is supported only on Windows Vista with SP2, Windows Server 2008 with SP2, and later operating systems.</span></span> <span data-ttu-id="44804-145">在舊版作業系統上，IOCTL 會失敗，並在事件驅動模式下發出錯誤代碼 **錯誤 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="44804-145">On earlier operating systems, the IOCTL will fail with the error code **ERROR\_NOT\_SUPPORTED** when issued in event driven mode.</span></span>

    <span data-ttu-id="44804-146">產生識別碼有可能在驅動程式抓取時間與完成 IOCTL 的時間之間變更的時間。</span><span class="sxs-lookup"><span data-stu-id="44804-146">It is possible for the generation identifier to change between the time that it is retrieved by the driver and the time the IOCTL is completed.</span></span> <span data-ttu-id="44804-147">這可能會導致用戶端應用程式接收到過時的資料。</span><span class="sxs-lookup"><span data-stu-id="44804-147">This can result in the client app receiving stale data.</span></span> <span data-ttu-id="44804-148">為了避免這種情況，用戶端應用程式可以使用事件驅動模式，以確保最終會瞭解世代識別碼的任何更新。</span><span class="sxs-lookup"><span data-stu-id="44804-148">To avoid this, the client app can use event driven mode to ensure that it will eventually learn about any updates to the generation identifier.</span></span> <span data-ttu-id="44804-149">藉由將用戶端應用程式的目前識別碼做為輸入，事件驅動模式可避免可能導致呼叫者遺漏通知的潛在競爭情形。</span><span class="sxs-lookup"><span data-stu-id="44804-149">By taking the client app's current identifier as input, event driven mode avoids potential race conditions that would cause the caller to miss notifications.</span></span>

<span data-ttu-id="44804-150">下列程式碼範例示範如何執行上述動作，以取得虛擬機器世代識別碼。</span><span class="sxs-lookup"><span data-stu-id="44804-150">The following code example shows how to perform the above actions to obtain the virtual machine generation identifier.</span></span>

> [!Note]  
> <span data-ttu-id="44804-151">下列程式碼必須以系統管理員或系統許可權執行，才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="44804-151">The following code must be run with administrator or system privileges to function correctly.</span></span>

 


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



## <a name="determining-if-a-time-shift-event-has-occurred"></a><span data-ttu-id="44804-152">判斷是否發生時間移位事件</span><span class="sxs-lookup"><span data-stu-id="44804-152">Determining if a time shift event has occurred</span></span>

<span data-ttu-id="44804-153">取得虛擬機器世代識別碼之後，您應該加以儲存，以供日後使用。</span><span class="sxs-lookup"><span data-stu-id="44804-153">After you have obtained the virtual machine generation identifier, you should store it for future use.</span></span> <span data-ttu-id="44804-154">在您的應用程式執行時間緊迫的作業（例如認可資料庫）之前，您應該重新取得世代識別碼，並將其與儲存的值進行比較。</span><span class="sxs-lookup"><span data-stu-id="44804-154">Before your app performs a time-sensitive operation, such as committing to a database, you should re-obtain the generation identifier and compare it to the stored value.</span></span> <span data-ttu-id="44804-155">如果識別碼已變更，這表示已發生時間移位事件，而且您的應用程式必須適當地執行動作。</span><span class="sxs-lookup"><span data-stu-id="44804-155">If the identifier has changed, that means that a time shift event has occurred, and your app must act appropriately.</span></span>

 

 
