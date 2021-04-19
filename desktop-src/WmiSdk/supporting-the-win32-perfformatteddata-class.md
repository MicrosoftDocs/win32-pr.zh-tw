---
description: 撰寫從 Win32 PerfFormattedData 衍生類別的高效能提供者時 \_ ，您必須遵循特定慣例，讓 WMI 可以計算屬性值。
ms.assetid: 57912f6f-45ca-491c-8a6c-77e2a6937ccc
ms.tgt_platform: multiple
title: 支援 Win32_PerfFormattedData 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54911105f5c485d3a80ddb93b96f0af2637c9506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106995866"
---
# <a name="supporting-the-win32_perfformatteddata-class"></a><span data-ttu-id="321ab-103">支援 Win32 \_ PerfFormattedData 類別</span><span class="sxs-lookup"><span data-stu-id="321ab-103">Supporting the Win32\_PerfFormattedData Class</span></span>

<span data-ttu-id="321ab-104">撰寫從 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)衍生類別的高效能提供者時，您必須遵循特定慣例，讓 WMI 可以計算屬性值。</span><span class="sxs-lookup"><span data-stu-id="321ab-104">When writing a high-performance provider that derives classes from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), you must follow specific conventions so that WMI can calculate the property values.</span></span>

> [!Note]  
> <span data-ttu-id="321ab-105">不建議在任何版本的 Windows 作業系統上撰寫 WMI 高效能提供者來建立效能計數器。</span><span class="sxs-lookup"><span data-stu-id="321ab-105">Writing a WMI high-performance provider to create performance counters is not recommended on any version of the Windows operating system.</span></span> <span data-ttu-id="321ab-106">如需詳細資訊，請參閱 [讓執行個體提供者成為 High-Performance 提供者](making-an-instance-provider-into-a-high-performance-provider.md)和 [效能程式庫和 WMI](performance-libraries-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="321ab-106">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

 

<span data-ttu-id="321ab-107">下列程式描述如何支援 Win32 \_ PerfFormattedData 類別。</span><span class="sxs-lookup"><span data-stu-id="321ab-107">The following procedure describes how to support the Win32\_PerfFormattedData class.</span></span>

<span data-ttu-id="321ab-108">**支援 Win32 \_ PerfFormattedData 類別**</span><span class="sxs-lookup"><span data-stu-id="321ab-108">**To support the Win32\_PerfFormattedData class**</span></span>

1.  <span data-ttu-id="321ab-109">在與對應的原始類別相同的命名空間中建立您的類別。</span><span class="sxs-lookup"><span data-stu-id="321ab-109">Create your class in the same namespace as the corresponding raw class.</span></span> <span data-ttu-id="321ab-110">類別必須衍生自 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) ，並將 **HiPerf** 辨識符號設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="321ab-110">The class must be derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) and have the **HiPerf** qualifier set to **TRUE**.</span></span> <span data-ttu-id="321ab-111">如需建立自己的 WMI 類別的詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="321ab-111">For more information about creating your own class for WMI, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="321ab-112">\_在 [**提供者**](class-qualifiers-for-performance-counter-classes.md)辨識符號中指定 "HiPerfCooker v1"。</span><span class="sxs-lookup"><span data-stu-id="321ab-112">Specify "HiPerfCooker\_v1" in the [**Provider**](class-qualifiers-for-performance-counter-classes.md) qualifier.</span></span>
3.  <span data-ttu-id="321ab-113">除了用於原始類別的限定詞之外，請指定下列類別層級限定詞：</span><span class="sxs-lookup"><span data-stu-id="321ab-113">Specify the following class-level qualifiers in addition to the qualifiers used for the raw classes:</span></span>

    -   [<span data-ttu-id="321ab-114">**AutoCook**</span><span class="sxs-lookup"><span data-stu-id="321ab-114">**AutoCook**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="321ab-115">**Autocook \_ RawClass**</span><span class="sxs-lookup"><span data-stu-id="321ab-115">**Autocook\_RawClass**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="321ab-116">**熟**</span><span class="sxs-lookup"><span data-stu-id="321ab-116">**Cooked**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="321ab-117">**昂貴**</span><span class="sxs-lookup"><span data-stu-id="321ab-117">**Costly**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="321ab-118">**動態**</span><span class="sxs-lookup"><span data-stu-id="321ab-118">**Dynamic**</span></span>](dynamic-qualifier.md)
    -   [<span data-ttu-id="321ab-119">**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="321ab-119">**HiPerf**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="321ab-120">**Locale**</span><span class="sxs-lookup"><span data-stu-id="321ab-120">**Locale**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="321ab-121">**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="321ab-121">**PerfDefault**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="321ab-122">**提供者**</span><span class="sxs-lookup"><span data-stu-id="321ab-122">**Provider**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="321ab-123">**單身 人士**</span><span class="sxs-lookup"><span data-stu-id="321ab-123">**Singleton**</span></span>](standard-wmi-qualifiers.md)

    > [!Note]  
    > <span data-ttu-id="321ab-124">請勿為 **GenericPerfCtr**、 **PerfIndex** 或 **HelpIndex** 設定任何值，因為 ADAP 進程會設定這些值。</span><span class="sxs-lookup"><span data-stu-id="321ab-124">Do not set any value for **GenericPerfCtr**, **PerfIndex**, or **HelpIndex** because these will be set by the ADAP process.</span></span> <span data-ttu-id="321ab-125">如需詳細資訊，請參閱 [**效能計數器類別的類別限定詞**](class-qualifiers-for-performance-counter-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="321ab-125">For more information, see [**Class Qualifiers for Performance Counter Classes**](class-qualifiers-for-performance-counter-classes.md).</span></span>

     

4.  <span data-ttu-id="321ab-126">在您的類別中包含名為 **Name** 的索引鍵屬性 (單一類別) 不需要此屬性。</span><span class="sxs-lookup"><span data-stu-id="321ab-126">Include a key property called **Name** in your class (this property is not required for singleton classes).</span></span>

    <span data-ttu-id="321ab-127">**Name** 屬性的值必須與對應的原始類別相同。</span><span class="sxs-lookup"><span data-stu-id="321ab-127">The value of the **Name** property must be the same as the corresponding raw class.</span></span> <span data-ttu-id="321ab-128">您不能在類別上使用 **名稱** 以外的任何索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="321ab-128">You must not use any key property other than **Name** on your class.</span></span>

5.  <span data-ttu-id="321ab-129">建立屬性資料類型為 **DWORD** (**Uint32**) 或 **QWORD** (**uint64**) 。</span><span class="sxs-lookup"><span data-stu-id="321ab-129">Create properties data typed as either **DWORD** (**uint32**) or **QWORD** (**uint64**).</span></span>

    <span data-ttu-id="321ab-130">屬性必須對應至原始類別中的屬性，或是您要建立之類別中的屬性。</span><span class="sxs-lookup"><span data-stu-id="321ab-130">The properties must correspond either to a property in the raw class or a property in the class you are creating.</span></span>

6.  <span data-ttu-id="321ab-131">除了用於原始類別屬性的 **PerfIndex** 和 **PerfDetail** 限定詞之外，請為類別中的所有屬性指定下列屬性層級限定詞：</span><span class="sxs-lookup"><span data-stu-id="321ab-131">Specify the following property level qualifiers for all properties in your class in addition to the **PerfIndex** and **PerfDetail** qualifiers used for the raw class properties:</span></span>

    -   [<span data-ttu-id="321ab-132">**基本**</span><span class="sxs-lookup"><span data-stu-id="321ab-132">**Base**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="321ab-133">**CookingType**</span><span class="sxs-lookup"><span data-stu-id="321ab-133">**CookingType**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="321ab-134">**計數器**</span><span class="sxs-lookup"><span data-stu-id="321ab-134">**Counter**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="321ab-135">**PerfTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="321ab-135">**PerfTimeStamp**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="321ab-136">**PerfTimeFreq**</span><span class="sxs-lookup"><span data-stu-id="321ab-136">**PerfTimeFreq**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="321ab-137">**SampleWindow**</span><span class="sxs-lookup"><span data-stu-id="321ab-137">**SampleWindow**</span></span>](property-qualifiers-for-performance-counter-classes.md)

    <span data-ttu-id="321ab-138">如需詳細資訊，請參閱 [**效能計數器類別的屬性限定詞**](property-qualifiers-for-performance-counter-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="321ab-138">For more information, see [**Property Qualifiers for Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="321ab-139">此外，Winperf 標頭檔包含您可以針對 **PerfDetail** 和 **CounterType** 指定的值。</span><span class="sxs-lookup"><span data-stu-id="321ab-139">In addition, the Winperf.h header file contains values that you can specify for **PerfDetail** and **CounterType**.</span></span>

7.  <span data-ttu-id="321ab-140">請確定您的提供者符合 [效能需求](#performance-requirements)。</span><span class="sxs-lookup"><span data-stu-id="321ab-140">Make sure your provider meets the [performance requirements](#performance-requirements).</span></span>

## <a name="performance-requirements"></a><span data-ttu-id="321ab-141">效能需求</span><span class="sxs-lookup"><span data-stu-id="321ab-141">Performance Requirements</span></span>

<span data-ttu-id="321ab-142">當您撰寫高效能的提供者時，其效能必須符合下列需求：</span><span class="sxs-lookup"><span data-stu-id="321ab-142">When you write a high-performance provider, its performance must meet the following requirements:</span></span>

-   <span data-ttu-id="321ab-143">開啟高效能 DLL 檔案的時間不能超過100毫秒。</span><span class="sxs-lookup"><span data-stu-id="321ab-143">Opening the high-performance DLL file can take no more than 100 milliseconds.</span></span> <span data-ttu-id="321ab-144">整體來說，開啟每個高效能提供者和效能程式庫的速度不能超過5秒。</span><span class="sxs-lookup"><span data-stu-id="321ab-144">Overall, opening each the high-performance provider and performance library cannot exceed 5 seconds.</span></span>
-   <span data-ttu-id="321ab-145">每次收集時，資料重新整理不會超過10毫秒。</span><span class="sxs-lookup"><span data-stu-id="321ab-145">Data refresh can take no more than 10 milliseconds per collect.</span></span> <span data-ttu-id="321ab-146">在整體重新整理和收集作業中，所有高效能的提供者都不能超過800毫秒的時間。</span><span class="sxs-lookup"><span data-stu-id="321ab-146">On an overall refresh and collect operation, all the high-performance providers together cannot take more than 800 milliseconds.</span></span>
-   <span data-ttu-id="321ab-147">所有高效能提供者的整體 CPU 負載，都不能以互動方式超過 6-7% CPU 負擔，也不能以5% 來進行記錄。</span><span class="sxs-lookup"><span data-stu-id="321ab-147">The overall CPU load for all high-performance providers cannot exceed 6-7% CPU overhead interactively or 5% for logging.</span></span>

## <a name="related-topics"></a><span data-ttu-id="321ab-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="321ab-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="321ab-149">讓執行個體提供者成為 High-Performance 提供者</span><span class="sxs-lookup"><span data-stu-id="321ab-149">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
