---
title: 如何呼叫 WMI 方法
description: WMI 的主要用途是提供類別和實例的存取權，以代表網路上的物件。
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 892561785280e78ecf29da1030883994990fc822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513697"
---
# <a name="how-to-call-a-wmi-method"></a><span data-ttu-id="c7113-103">如何呼叫 WMI 方法</span><span class="sxs-lookup"><span data-stu-id="c7113-103">How to call a WMI method</span></span>

<span data-ttu-id="c7113-104">WMI 的主要用途是提供類別和實例的存取權，以代表網路上的物件。</span><span class="sxs-lookup"><span data-stu-id="c7113-104">The main purpose of WMI is to provide access to classes and instances that represent objects on your network.</span></span> <span data-ttu-id="c7113-105">提供者支援這些類別和實例。</span><span class="sxs-lookup"><span data-stu-id="c7113-105">These classes and instances are supported by providers.</span></span> <span data-ttu-id="c7113-106">例如，所有代表您企業上標準硬體裝置的實例（例如 [**win32 \_ PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) 或 [**win32 \_ 印表機**](/windows/desktop/CIMWin32Prov/win32-printer)）都受到 win32 提供者的支援。</span><span class="sxs-lookup"><span data-stu-id="c7113-106">For example, all of the instances that represent standard hardware devices on your enterprise, such as [**Win32\_PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) or [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer), are supported by the Win32 provider.</span></span> <span data-ttu-id="c7113-107">同樣地，您可以透過事件記錄檔提供者，以及透過登錄提供者的登錄來存取事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c7113-107">Similarly, you can access the event log through the Event Log provider, and the registry through the Registry provider.</span></span>

<span data-ttu-id="c7113-108">WMI 在介面（例如 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 或腳本物件，例如 [**SWbemServices**](swbemservices.md)）中所實行的方法，主要是用來一般取得和操作任何提供者所提供的資料。</span><span class="sxs-lookup"><span data-stu-id="c7113-108">The methods that WMI implements in interfaces such as [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) or scripting objects such as [**SWbemServices**](swbemservices.md), are primarily for generically obtaining and manipulating data supplied by any provider.</span></span> <span data-ttu-id="c7113-109">例如，您可以使用 [**SWbemServices InstancesOf**](swbemservices-instancesof.md) ，在企業電腦的子集中取得 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 的所有實例。</span><span class="sxs-lookup"><span data-stu-id="c7113-109">For example, use [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) to obtain all the instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) in a subset of enterprise computers.</span></span> <span data-ttu-id="c7113-110">然後，您可以在每個 **win32 \_ 處理** 程式物件上呼叫 Win32 提供者方法 [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) 。</span><span class="sxs-lookup"><span data-stu-id="c7113-110">You can then call the Win32 provider method [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) on each **Win32\_Process** object.</span></span>

<span data-ttu-id="c7113-111">在下列範例中， [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) 方法會在處理常式物件上被稱為 automation 方法。</span><span class="sxs-lookup"><span data-stu-id="c7113-111">In the following example, the [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) method is called as an automation method on the Process object.</span></span> <span data-ttu-id="c7113-112">WMI 方法（例如針對 [**SWbemObject**](swbemobject.md)所定義的 [**路徑 \_**](swbemobject-path-.md)方法）也可以在 **處理** 程式物件上呼叫。</span><span class="sxs-lookup"><span data-stu-id="c7113-112">A WMI method, such as the [**Path\_**](swbemobject-path-.md) method defined for [**SWbemObject**](swbemobject.md) could also be called on the **Process** object.</span></span>


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



<span data-ttu-id="c7113-113">使用 WMI 方法的實際處理方式，與使用任何其他 Windows COM 或 automation 介面相同。</span><span class="sxs-lookup"><span data-stu-id="c7113-113">The actual process of using the WMI methods is identical to using any other Windows COM or automation interface.</span></span> <span data-ttu-id="c7113-114">如需詳細資訊，請參閱 [COM](../cossdk/component-services-portal.md) 和 [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)。</span><span class="sxs-lookup"><span data-stu-id="c7113-114">For more information, see [COM](../cossdk/component-services-portal.md) and [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span> <span data-ttu-id="c7113-115">如需 WMI 所支援介面的詳細資訊，請參閱適用于 wmi 的 [COM api](com-api-for-wmi.md) 和 [適用于 WMI 的腳本 API](scripting-api-for-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="c7113-115">For more information about the interfaces that WMI supports, see [COM API for WMI](com-api-for-wmi.md) and [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

<span data-ttu-id="c7113-116">如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。</span><span class="sxs-lookup"><span data-stu-id="c7113-116">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7113-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7113-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7113-118">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="c7113-118">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
