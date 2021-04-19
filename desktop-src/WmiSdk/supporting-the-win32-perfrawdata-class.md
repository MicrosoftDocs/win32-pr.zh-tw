---
description: 撰寫從 Win32 PerfRawData 衍生類別的高效能提供者時 \_ ，您必須遵循特定慣例，讓 WMI 可以提供資料給屬性值。
ms.assetid: 04abb2f9-800f-497a-ac8f-8ef210746273
ms.tgt_platform: multiple
title: 支援 Win32_PerfRawData 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 835815c9171097bfe088d22e4154ac668d790c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983552"
---
# <a name="supporting-the-win32_perfrawdata-class"></a><span data-ttu-id="35353-103">支援 Win32 \_ PerfRawData 類別</span><span class="sxs-lookup"><span data-stu-id="35353-103">Supporting the Win32\_PerfRawData Class</span></span>

<span data-ttu-id="35353-104">撰寫從 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)衍生類別的高效能提供者時，您必須遵循特定慣例，讓 WMI 可以提供資料給屬性值。</span><span class="sxs-lookup"><span data-stu-id="35353-104">When writing a high-performance provider that derives classes from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), you must follow specific conventions so that WMI can supply data to the property values.</span></span>

> [!Note]  
> <span data-ttu-id="35353-105">不建議在任何版本的 Windows 作業系統上撰寫 WMI 高效能提供者來建立效能計數器。</span><span class="sxs-lookup"><span data-stu-id="35353-105">Writing a WMI high-performance provider to create performance counters is not recommended on any version of the Windows operating system.</span></span> <span data-ttu-id="35353-106">如需詳細資訊，請參閱 [讓執行個體提供者成為 High-Performance 提供者](making-an-instance-provider-into-a-high-performance-provider.md)和 [效能程式庫和 WMI](performance-libraries-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="35353-106">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

 

<span data-ttu-id="35353-107">下列程式說明如何使用高效能提供者來支援 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 類別。</span><span class="sxs-lookup"><span data-stu-id="35353-107">The following procedure describes how to support the [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class with your high-performance provider.</span></span>

<span data-ttu-id="35353-108">**支援 Win32 \_ PerfRawData 類別**</span><span class="sxs-lookup"><span data-stu-id="35353-108">**To support the Win32\_PerfRawData class**</span></span>

1.  <span data-ttu-id="35353-109">在根 CIMv2 命名空間中建立您的類別 \\ 。</span><span class="sxs-lookup"><span data-stu-id="35353-109">Create your class in the Root\\CIMv2 namespace.</span></span>

    <span data-ttu-id="35353-110">類別必須衍生自 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) ，並將 **Hiperf** 辨識符號設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="35353-110">The class must be derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and have the **Hiperf** qualifier set to **TRUE**.</span></span> <span data-ttu-id="35353-111">您也可以將 WDM (驅動程式) 效能資料類別新增至根 \\ wmi 命名空間。</span><span class="sxs-lookup"><span data-stu-id="35353-111">You can also add WDM (driver) performance data classes to the root\\wmi namespace.</span></span> <span data-ttu-id="35353-112">如需建立自己的 WMI 類別的詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="35353-112">For more information about creating your own class for WMI, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

2.  <span data-ttu-id="35353-113">在提供者辨識符號中，將提供者指定為 "NT5 \_ GenericPerfProvider \_ V1"。 </span><span class="sxs-lookup"><span data-stu-id="35353-113">Specify the provider as "NT5\_GenericPerfProvider\_V1" in the **Provider** qualifier.</span></span>
3.  <span data-ttu-id="35353-114">指定下列類別層級的限定詞：</span><span class="sxs-lookup"><span data-stu-id="35353-114">Specify the following class-level qualifiers:</span></span>

    -   <span data-ttu-id="35353-115">**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="35353-115">**HiPerf**</span></span>
    -   <span data-ttu-id="35353-116">**地區設定**</span><span class="sxs-lookup"><span data-stu-id="35353-116">**Locale**</span></span>
    -   <span data-ttu-id="35353-117">**PerfDetail**</span><span class="sxs-lookup"><span data-stu-id="35353-117">**PerfDetail**</span></span>
    -   <span data-ttu-id="35353-118">**提供者**</span><span class="sxs-lookup"><span data-stu-id="35353-118">**Provider**</span></span>

    <span data-ttu-id="35353-119">如需詳細資訊，請參閱 [**效能計數器類別的類別限定詞**](class-qualifiers-for-performance-counter-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="35353-119">For more information, see [**Class Qualifiers for Performance Counter Classes**](class-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="35353-120">請勿定義 **GenericPerfCtr** 限定詞，因為它是針對將效能程式庫資料傳輸至 WMI 類別的 ADAP 進程所保留的。</span><span class="sxs-lookup"><span data-stu-id="35353-120">Do not define the **GenericPerfCtr** qualifier because that is reserved for the ADAP process that transfers performance library data into WMI classes.</span></span>

4.  <span data-ttu-id="35353-121">填入適當的 timestamp 和 frequency 屬性，以用來計算計數器類型公式。</span><span class="sxs-lookup"><span data-stu-id="35353-121">Populate the appropriate timestamp and frequency properties used to compute counter-type formulas.</span></span>

    <span data-ttu-id="35353-122">這些屬性是從 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 繼承而來，如果您要撰寫高效能的提供者，就必須填滿這些屬性，才能在 [系統監視器] 中顯示該類別。</span><span class="sxs-lookup"><span data-stu-id="35353-122">These properties are inherited from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and, if you are writing a high-performance provider, you must fill these out for the class to be displayed in System Monitor.</span></span>

5.  <span data-ttu-id="35353-123">在您的類別中包含名為 **Name** 的索引鍵屬性 (單一類別) 不需要此屬性。</span><span class="sxs-lookup"><span data-stu-id="35353-123">Include a key property called **Name** in your class (this property is not required for singleton classes).</span></span>

    <span data-ttu-id="35353-124">您不能在類別上使用 **名稱** 以外的任何索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="35353-124">You must not use any key property other than **Name** on your class.</span></span>

6.  <span data-ttu-id="35353-125">建立屬性資料類型為 **DWORD** (**Uint32**) 或 **QWORD** (**uint64**) 。</span><span class="sxs-lookup"><span data-stu-id="35353-125">Create properties data-typed as either **DWORD** (**uint32**) or **QWORD** (**uint64**).</span></span> <span data-ttu-id="35353-126">這些屬性會在傳輸至效能程式庫時成為效能計數器。</span><span class="sxs-lookup"><span data-stu-id="35353-126">These properties become performance counters when transferred to the performance libraries.</span></span>
7.  <span data-ttu-id="35353-127">針對您類別中的所有屬性指定下列屬性層級限定詞：</span><span class="sxs-lookup"><span data-stu-id="35353-127">Specify the following property level qualifiers for all properties in your class:</span></span>

    -   <span data-ttu-id="35353-128">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="35353-128">**DisplayName**</span></span>
    -   <span data-ttu-id="35353-129">**CounterType**</span><span class="sxs-lookup"><span data-stu-id="35353-129">**CounterType**</span></span>
    -   <span data-ttu-id="35353-130">**DefaultScale**</span><span class="sxs-lookup"><span data-stu-id="35353-130">**DefaultScale**</span></span>
    -   <span data-ttu-id="35353-131">**說明**</span><span class="sxs-lookup"><span data-stu-id="35353-131">**Description**</span></span>
    -   <span data-ttu-id="35353-132">**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="35353-132">**PerfDefault**</span></span>
    -   <span data-ttu-id="35353-133">**PerfDetail**</span><span class="sxs-lookup"><span data-stu-id="35353-133">**PerfDetail**</span></span>

    <span data-ttu-id="35353-134">如需詳細資訊，請參閱 [**效能計數器類別的屬性限定詞**](property-qualifiers-for-performance-counter-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="35353-134">For more information, see [**Property Qualifiers for Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="35353-135">此外，Winperf 標頭檔包含您可以針對 **PerfDetail** 和 **CounterType** 指定的值。</span><span class="sxs-lookup"><span data-stu-id="35353-135">In addition, the Winperf.h header file contains values that you can specify for **PerfDetail** and **CounterType**.</span></span>

    <span data-ttu-id="35353-136">WMI 使用 **DisplayName**、 **Locale** 和 **Description** 限定詞進行當地語系化。</span><span class="sxs-lookup"><span data-stu-id="35353-136">WMI uses the **DisplayName**, **Locale**, and **Description** qualifiers for localization.</span></span> <span data-ttu-id="35353-137">您必須將修改過的限定詞新增至 MS \_ 409 (英文) 命名空間，讓系統監視器可以適當地顯示您的類別資料。</span><span class="sxs-lookup"><span data-stu-id="35353-137">You must add amended qualifiers to the MS\_409 (English) namespace so that System Monitor can properly display your class data.</span></span> <span data-ttu-id="35353-138">這表示您可以藉由新增具有解說文字的 **描述** 辨識符號，並填入 **DisplayName** 值來修改屬性定義。</span><span class="sxs-lookup"><span data-stu-id="35353-138">This means that you amend the property definition by adding a **Description** qualifier with explanatory text and fill in the **DisplayName** value.</span></span> <span data-ttu-id="35353-139">您也必須將修改過的限定詞新增至類別所支援的任何其他地區設定命名空間。</span><span class="sxs-lookup"><span data-stu-id="35353-139">You must also add amended qualifiers to any other locale namespace that your class supports.</span></span> <span data-ttu-id="35353-140">如果使用者從您未提供修改過的限定詞的地區設定要求資料，WMI 會預設為 MS 409 命名空間中指定的定義 \_ 。</span><span class="sxs-lookup"><span data-stu-id="35353-140">If a user requests data from a locale for which you do not provide amended qualifiers, WMI defaults to the definitions specified in the MS\_409 namespace.</span></span>

8.  <span data-ttu-id="35353-141">針對具有應基底值之計數器類型的任何屬性，建立基底屬性。</span><span class="sxs-lookup"><span data-stu-id="35353-141">Create a base property for any property that has a counter type expecting a base value.</span></span>

    <span data-ttu-id="35353-142">這個屬性會緊接在屬性之後，並且命名為 \* propertyname \***\_ Base**。</span><span class="sxs-lookup"><span data-stu-id="35353-142">This property immediately follows the property and is named \*propertyname\***\_Base**.</span></span> <span data-ttu-id="35353-143">例如，在 [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)類別中 **AvgDiskBytesPerRead** 的 average 屬性，需要名為 **AvgDiskBytesPerRead \_ base** 的基底屬性來計算樣本數。</span><span class="sxs-lookup"><span data-stu-id="35353-143">For example, the average property **AvgDiskBytesPerRead** in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class requires a base property named **AvgDiskBytesPerRead\_Base** to count the number of samples.</span></span> <span data-ttu-id="35353-144">若要判斷您想要使用的計數器類型是否需要基底屬性，請在 [WMI 效能計數器類型](wmi-performance-counter-types.md)中依名稱或十進位值找出計數器類型。</span><span class="sxs-lookup"><span data-stu-id="35353-144">To determine if the counter type you want to use requires a base property, locate the counter type by name or decimal value in [WMI Performance Counter Types](wmi-performance-counter-types.md).</span></span>

9.  <span data-ttu-id="35353-145">請確定您的提供者符合 [效能需求](supporting-the-win32-perfformatteddata-class.md)。</span><span class="sxs-lookup"><span data-stu-id="35353-145">Make sure your provider meets the [performance requirements](supporting-the-win32-perfformatteddata-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="35353-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="35353-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35353-147">讓執行個體提供者成為 High-Performance 提供者</span><span class="sxs-lookup"><span data-stu-id="35353-147">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
