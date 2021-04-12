---
description: Wmiadap 是在 Windows 上執行的應用程式，可更新 WMI 儲存機制中的效能資訊。
ms.assetid: 459fe19e-3e2e-4a58-b3e7-75fd285f7389
ms.tgt_platform: multiple
title: wmiadap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5d2de65e8566283b341c5af52048cc79cc0299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195216"
---
# <a name="wmiadap"></a><span data-ttu-id="39137-103">wmiadap</span><span class="sxs-lookup"><span data-stu-id="39137-103">wmiadap</span></span>

<span data-ttu-id="39137-104">Wmiadap 是在 Windows 上執行的應用程式，可更新 WMI 儲存機制中的效能資訊。</span><span class="sxs-lookup"><span data-stu-id="39137-104">Wmiadap is a application that runs on Windows that can update performance information in the WMI repository.</span></span> <span data-ttu-id="39137-105">一般而言，這可讓開發人員和 IT 系統管理員建立腳本來存取效能資訊，例如應用程式所使用的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="39137-105">Generally, this allows developers and IT Administrators to create scripts that access performance information, such as the amount of memory used by an application.</span></span> <span data-ttu-id="39137-106">下列主題描述您可以用來控制 wmiadap 如何捕獲資訊的命令列介面。</span><span class="sxs-lookup"><span data-stu-id="39137-106">The following topic describes the command-line interface you can use to control how wmiadap retrieves information.</span></span>

<span data-ttu-id="39137-107">Wmiadap 是與大部分系統上的作業系統一起安裝，位於 C： \\ Windows \\ System32 \\ wbem 目錄中。</span><span class="sxs-lookup"><span data-stu-id="39137-107">Wmiadap is installed with the operating system on most systems, in the C:\\Windows\\System32\\wbem directory.</span></span> <span data-ttu-id="39137-108">如果您看到有關 wmiadap.exe 的錯誤訊息，請搜尋 [Microsoft 支援服務](https://support.microsoft.com/)。</span><span class="sxs-lookup"><span data-stu-id="39137-108">If you are seeing error messages concerning wmiadap.exe, search [Microsoft Support](https://support.microsoft.com/).</span></span> <span data-ttu-id="39137-109">一般而言，除非另有指示，否則您不應該刪除系統中的 wmiadap.exe。</span><span class="sxs-lookup"><span data-stu-id="39137-109">Generally, you should not delete wmiadap.exe from your system, unless otherwise instructed.</span></span>

<span data-ttu-id="39137-110">從效能程式庫傳輸資料以及從 [**win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 和 [**win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) 衍生的類別重新整理，是由 [WmiPerfClass](wmi-providers.md) 和 [WMIPerfInst](wmi-providers.md) 提供者完成。</span><span class="sxs-lookup"><span data-stu-id="39137-110">The transfer of data from the performance libraries and the refresh of classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) is done by the [WmiPerfClass](wmi-providers.md) and [WMIPerfInst](wmi-providers.md) providers.</span></span> <span data-ttu-id="39137-111">只有在加入新的效能物件時，WmiPerfClass 提供者才會更新 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes) 。</span><span class="sxs-lookup"><span data-stu-id="39137-111">The WmiPerfClass provider updates WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) only when a new performance object is added.</span></span> <span data-ttu-id="39137-112">您仍然可以使用 **/r** 參數執行 Wmiadap，以剖析 Windows Driver Model 驅動程式來建立效能物件。</span><span class="sxs-lookup"><span data-stu-id="39137-112">You still can run Wmiadap with the **/r** switch to parse the Windows Driver Model drivers to create performance objects.</span></span> <span data-ttu-id="39137-113">**/F** 參數仍然會從效能程式庫強制更新 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="39137-113">The **/f** switch still forces an update of the WMI classes from the performance libraries.</span></span>

<span data-ttu-id="39137-114">您可以在命令提示字元中使用下列參數。</span><span class="sxs-lookup"><span data-stu-id="39137-114">The following switches are available at the command prompt.</span></span>

<span data-ttu-id="39137-115">**wmiadap** \[ \] /f \[**/r**\]</span><span class="sxs-lookup"><span data-stu-id="39137-115">**wmiadap** \[**/f**\]\[**/r**\]</span></span>

## <a name="switches"></a><span data-ttu-id="39137-116">交換器</span><span class="sxs-lookup"><span data-stu-id="39137-116">Switches</span></span>

<dl> <dt>

<span data-ttu-id="39137-117"><span id="_f"></span><span id="_F"></span>**/f**</span><span class="sxs-lookup"><span data-stu-id="39137-117"><span id="_f"></span><span id="_F"></span>**/f**</span></span>
</dt> <dd>

<span data-ttu-id="39137-118">剖析系統上的所有效能程式庫，並重新整理衍生自 [**win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 和 [**win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)的類別。</span><span class="sxs-lookup"><span data-stu-id="39137-118">Parses all the performance libraries on the system and refreshes the classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

</dd> <dt>

<span data-ttu-id="39137-119"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="39137-119"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="39137-120">剖析系統上的所有 Windows Driver Model 驅動程式，以建立效能物件。</span><span class="sxs-lookup"><span data-stu-id="39137-120">Parses all the Windows Driver Model drivers on the system to create performance objects.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="39137-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39137-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39137-122">效能程式庫和 WMI</span><span class="sxs-lookup"><span data-stu-id="39137-122">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="39137-123">**winmgmt**</span><span class="sxs-lookup"><span data-stu-id="39137-123">**winmgmt**</span></span>](winmgmt.md)
</dt> </dl>

 

 
