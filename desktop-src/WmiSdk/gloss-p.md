---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d426673b-dea2-4f8b-9259-6a17543f70c0
ms.tgt_platform: multiple
title: 'P (WMI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd72fca871352f8a31652eb72f693da43d1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945229"
---
# <a name="p-wmi"></a><span data-ttu-id="2f1b4-103">P (WMI) </span><span class="sxs-lookup"><span data-stu-id="2f1b4-103">P (WMI)</span></span>

<span data-ttu-id="2f1b4-104">[B](gloss-a.md) [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="2f1b4-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="2f1b4-105"><span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**效能計數器**</span><span class="sxs-lookup"><span data-stu-id="2f1b4-105"><span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**performance counter**</span></span>
</dt> <dd>

<span data-ttu-id="2f1b4-106">性能類別中的屬性，此屬性衍生自儲存效能資料的 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-106">A property in a performance class that is derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) that stores performance data.</span></span>

</dd> <dt>

<span data-ttu-id="2f1b4-107"><span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**效能物件**</span><span class="sxs-lookup"><span data-stu-id="2f1b4-107"><span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**performance object**</span></span>
</dt> <dd>

<span data-ttu-id="2f1b4-108">效能程式庫中的物件，可將資料儲存在計數器中。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-108">An object in a performance library that stores data in counters.</span></span> <span data-ttu-id="2f1b4-109">這些物件會顯示在 [*系統監視器*](gloss-s.md) 公用程式中。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-109">These objects are visible in the [*System Monitor*](gloss-s.md) utility.</span></span> <span data-ttu-id="2f1b4-110">範例包括 Cache 和 Logical Disk 物件。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-110">Examples are Cache and Logical Disk objects.</span></span> <span data-ttu-id="2f1b4-111">由 [*ADAP*](gloss-a.md) 進程傳送至 WMI 時，每個物件都會變成兩個 WMI 效能類別。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-111">When transferred into WMI by the [*ADAP*](gloss-a.md) process, each object becomes two WMI performance classes.</span></span> <span data-ttu-id="2f1b4-112">一個包含原始資料的類別，衍生自 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-112">One class, containing raw data, derives from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span> <span data-ttu-id="2f1b4-113">另一個類別衍生自 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) ，且包含在系統監視器中可見的相同資料，如同處理後計數器提供者所計算。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-113">The other class derives from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) and contains the same data visible in System Monitor as calculated by the Cooked Counter provider.</span></span>

</dd> <dt>

<span data-ttu-id="2f1b4-114"><span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**永久取用者**</span><span class="sxs-lookup"><span data-stu-id="2f1b4-114"><span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**permanent consumer**</span></span>
</dt> <dd>

<span data-ttu-id="2f1b4-115">其註冊會一直持續到被明確取消為止的 [*事件取用者*](gloss-e.md) 。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-115">An [*event consumer*](gloss-e.md) whose registration lasts until it is explicitly canceled.</span></span> <span data-ttu-id="2f1b4-116">另請參閱 [*暫時取用者*](gloss-t.md)。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-116">Also see [*temporary consumer*](gloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f1b4-117"><span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**實體取用者**</span><span class="sxs-lookup"><span data-stu-id="2f1b4-117"><span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**physical consumer**</span></span>
</dt> <dd>

<span data-ttu-id="2f1b4-118">由 [*事件*](gloss-e.md)取用者提供者所執行的 COM 物件，其中包含接收事件通知 [*的接收。*](gloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="2f1b4-118">A COM object that is implemented by an [*event consumer provider*](gloss-e.md) that includes a [*sink*](gloss-s.md) for receiving event notifications.</span></span>

</dd> <dt>

<span data-ttu-id="2f1b4-119"><span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**財產**</span><span class="sxs-lookup"><span data-stu-id="2f1b4-119"><span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="2f1b4-120">描述類別資料單位的名稱/值組。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-120">A name/value pair that describes a unit of data for a class.</span></span> <span data-ttu-id="2f1b4-121">屬性值必須具有有效的 [*受控物件格式 (MOF)*](gloss-m.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-121">Property values must have a valid [*Managed Object Format (MOF)*](gloss-m.md) data type.</span></span> <span data-ttu-id="2f1b4-122">另請參閱 [*參考屬性*](gloss-r.md)。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-122">Also see [*reference property*](gloss-r.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f1b4-123"><span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**屬性提供者**</span><span class="sxs-lookup"><span data-stu-id="2f1b4-123"><span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**property provider**</span></span>
</dt> <dd>

<span data-ttu-id="2f1b4-124">支援對 WMI 屬性進行抓取和修改的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-124">A COM server that supports the retrieval and modification of WMI properties.</span></span> <span data-ttu-id="2f1b4-125">屬性提供者會執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 和 [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) 介面。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-125">Property providers implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="2f1b4-126"><span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**供應商**</span><span class="sxs-lookup"><span data-stu-id="2f1b4-126"><span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="2f1b4-127">與受管理物件通訊以存取資料和事件通知（例如登錄或 SNMP 裝置）的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-127">A COM server that communicates with managed objects to access data and event notifications, such as the registry or an SNMP device.</span></span> <span data-ttu-id="2f1b4-128">提供者將此資料轉送至 [*CIM 物件管理員*](gloss-c.md) ，以進行整合和轉譯。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-128">Providers forward this data to the [*CIM Object Manager*](gloss-c.md) for integration and interpretation.</span></span>

</dd> <dt>

<span data-ttu-id="2f1b4-129"><span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**提供者方法**</span><span class="sxs-lookup"><span data-stu-id="2f1b4-129"><span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**provider method**</span></span>
</dt> <dd>

<span data-ttu-id="2f1b4-130">WMI *提供者* 所實行的方法。</span><span class="sxs-lookup"><span data-stu-id="2f1b4-130">A method that a WMI *provider* implements.</span></span>

</dd> </dl>

 

 
