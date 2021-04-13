---
description: 這些 WMI 類別是在 CimWin32 中宣告。
ms.assetid: 53122499-1CC0-4B48-AEA1-B70B7BBC3A99
ms.tgt_platform: multiple
title: CIM WMI 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3249549e0915f51b6a9a6f2386c18ba695919a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510438"
---
# <a name="cim-wmi-provider"></a><span data-ttu-id="4a2aa-103">CIM WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="4a2aa-103">CIM WMI Provider</span></span>

<span data-ttu-id="4a2aa-104">這些 WMI 類別是在 CimWin32 中宣告。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-104">These WMI classes are declared in CimWin32.mof.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4a2aa-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="4a2aa-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="4a2aa-106">**CIM \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-106">**CIM\_Action**</span></span>](cim-action.md)
</dt> <dd>

<span data-ttu-id="4a2aa-107">[**CIM \_ 動作**](cim-action.md)類別是一項作業，屬於進程的一部分，可在其下一個狀態下建立軟體專案，或刪除目前狀態中的 software 元素。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-107">A [**CIM\_Action**](cim-action.md) class is an operation that is part of a process to either create a software element in its next state or to eliminate the software element in the current state.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-108">**CIM \_ ActionSequence**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-108">**CIM\_ActionSequence**</span></span>](cim-actionsequence.md)
</dt> <dd>

<span data-ttu-id="4a2aa-109">[**Cim \_ ActionSequence**](cim-actionsequence.md)關聯會定義一系列的作業，這些作業會將 [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md)) 關聯 (所參考的軟體專案轉換為下一個狀態，或從其目前的狀態中移除軟體元素。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-109">The [**CIM\_ActionSequence**](cim-actionsequence.md) association defines a series of operations that transition the software element (referenced by the [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association) to its next state, or removes the software element from its current state.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-110">**CIM \_ ActsAsSpare**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-110">**CIM\_ActsAsSpare**</span></span>](cim-actsasspare.md)
</dt> <dd>

<span data-ttu-id="4a2aa-111">[**CIM \_ ActsAsSpare**](cim-actsasspare.md)關聯會指出哪些專案可以是可替換的元素，或是取代其他匯總的元素。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-111">The [**CIM\_ActsAsSpare**](cim-actsasspare.md) association indicates which elements can be spares or replace other aggregated elements.</span></span> <span data-ttu-id="4a2aa-112">備用可以依元素個別的指定，以「熱待命」模式運作。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-112">A spare can operate in "hot-standby" mode as specified on an element-by-element basis.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-113">**CIM \_ AdjacentSlots**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-113">**CIM\_AdjacentSlots**</span></span>](cim-adjacentslots.md)
</dt> <dd>

<span data-ttu-id="4a2aa-114">[**CIM \_ AdjacentSlots**](cim-adjacentslots.md)關聯描述主控電路板或介面卡卡上的位置版面配置。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-114">The [**CIM\_AdjacentSlots**](cim-adjacentslots.md) association describes the layout of slots on a hosting board or adapter card.</span></span> <span data-ttu-id="4a2aa-115">資訊，例如位置之間的距離，以及它們是否為「共用」 (如果已填入，則無法使用另一個位置，) 會將它傳達為關聯屬性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-115">Information, such as the distance between the slots and whether they are "shared" (if one is populated, then the other slot cannot be used), is conveyed as association properties.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-116">**CIM \_ AggregatePExtent**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-116">**CIM\_AggregatePExtent**</span></span>](cim-aggregatepextent.md)
</dt> <dd>

<span data-ttu-id="4a2aa-117">[**CIM \_ AggregatePExtent**](cim-aggregatepextent.md)類別提供有關可定址邏輯區塊的摘要資訊，這些區塊位於相同的儲存體冗余群組，且位於相同的實體媒體上。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-117">The [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class provides summary information about addressable logical blocks, which are in the same storage redundancy group and located on the same physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-118">**CIM \_ AggregatePSExtent**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-118">**CIM\_AggregatePSExtent**</span></span>](cim-aggregatepsextent.md)
</dt> <dd>

<span data-ttu-id="4a2aa-119">[**CIM \_ AggregatePSExtent**](cim-aggregatepsextent.md)類別會定義單一儲存裝置上可定址的邏輯區塊數目，但不包括對應為檢查資料的邏輯區塊。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-119">The [**CIM\_AggregatePSExtent**](cim-aggregatepsextent.md) class defines the number of addressable logical blocks on a single storage device, excluding logical blocks mapped as check data.</span></span> <span data-ttu-id="4a2aa-120">如果已定義磁片區集，則邏輯區塊會包含在單一磁片區集合中。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-120">If volume sets are defined, the logical blocks are contained within a single volume set.</span></span> <span data-ttu-id="4a2aa-121">當只需要摘要資訊或使用自動設定時，這是 [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md)的替代群組。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-121">This is an alternative grouping for [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md), when only summary information is needed or when automatic configuration is used.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-122">**CIM \_ AggregateRedundancyComponent**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-122">**CIM\_AggregateRedundancyComponent**</span></span>](cim-aggregateredundancycomponent.md)
</dt> <dd>

<span data-ttu-id="4a2aa-123">[**CIM \_ AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md)類別描述儲存體冗余群組中的匯總實體範圍。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-123">The [**CIM\_AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md) class describes the aggregate physical extent in a storage redundancy group.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-124">**CIM \_ AlarmDevice**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-124">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> <dd>

<span data-ttu-id="4a2aa-125">[**CIM \_ AlarmDevice**](cim-alarmdevice.md)類別是一種警示裝置，可發出與問題狀況相關的聲音或可見指示。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-125">The [**CIM\_AlarmDevice**](cim-alarmdevice.md) class is an alarm device that emits audible or visible indications related to a problem situation.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-126">**CIM \_ AllocatedResource**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-126">**CIM\_AllocatedResource**</span></span>](cim-allocatedresource.md)
</dt> <dd>

<span data-ttu-id="4a2aa-127">[**CIM \_ AllocatedResource**](cim-allocatedresource.md)類別代表邏輯裝置與系統資源之間的關聯，並指出資源已指派給裝置。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-127">The [**CIM\_AllocatedResource**](cim-allocatedresource.md) class represents an association between logical devices and system resources and indicates that the resource is assigned to the device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-128">**CIM \_ ApplicationSystem**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-128">**CIM\_ApplicationSystem**</span></span>](cim-applicationsystem.md)
</dt> <dd>

<span data-ttu-id="4a2aa-129">[**CIM \_ ApplicationSystem**](cim-applicationsystem.md)類別代表支援特定商務功能的應用程式或軟體系統，可作為獨立的單位來管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-129">The [**CIM\_ApplicationSystem**](cim-applicationsystem.md) class represents an application or software system that supports a particular business function that can be managed as an independent unit.</span></span> <span data-ttu-id="4a2aa-130">這類系統可使用 [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) 類別分解為其功能性元件。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-130">Such a system can be decomposed into its functional components using the [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class.</span></span> <span data-ttu-id="4a2aa-131">特定應用程式或軟體系統的軟體功能位於使用 [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) 關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-131">The software features for a particular application or software system are located using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-132">**CIM \_ ApplicationSystemSoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-132">**CIM\_ApplicationSystemSoftwareFeature**</span></span>](cim-applicationsystemsoftwarefeature.md)
</dt> <dd>

<span data-ttu-id="4a2aa-133">[**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md)類別代表的關聯會識別組成特定應用程式系統的軟體功能。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-133">The [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) class represents an association that identifies the software features that make up a particular application system.</span></span> <span data-ttu-id="4a2aa-134">軟體功能可以包含在不同的產品中。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-134">The software features can be included in different products.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-135">**CIM \_ AssociatedAlarm**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-135">**CIM\_AssociatedAlarm**</span></span>](cim-associatedalarm.md)
</dt> <dd>

<span data-ttu-id="4a2aa-136">[**CIM \_ AssociatedAlarm**](cim-associatedalarm.md)相依性會將警示與邏輯裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-136">The [**CIM\_AssociatedAlarm**](cim-associatedalarm.md) dependency associates an alarm with a logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-137">**CIM \_ AssociatedBattery**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-137">**CIM\_AssociatedBattery**</span></span>](cim-associatedbattery.md)
</dt> <dd>

<span data-ttu-id="4a2aa-138">[**CIM \_ AssociatedBattery**](cim-associatedbattery.md)相依性會將電池與邏輯裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-138">The [**CIM\_AssociatedBattery**](cim-associatedbattery.md) dependency associates a battery with a logical device.</span></span> <span data-ttu-id="4a2aa-139">您可以使用此關聯來建立個別電池的模型，使其成為 (UPS) 的不斷電供應系統供應。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-139">Use this association to model individual batteries that make up an uninterruptible power supply (UPS).</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-140">**CIM \_ AssociatedCooling**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-140">**CIM\_AssociatedCooling**</span></span>](cim-associatedcooling.md)
</dt> <dd>

<span data-ttu-id="4a2aa-141">[**CIM \_ AssociatedCooling**](cim-associatedcooling.md)關聯會指出風扇或其他冷卻裝置特定于裝置 (與提供主機殼或封包冷卻) 。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-141">The [**CIM\_AssociatedCooling**](cim-associatedcooling.md) association indicates when fans or other cooling devices are specific to a device (versus providing enclosure or cabinet cooling).</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-142">**CIM \_ AssociatedMemory**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-142">**CIM\_AssociatedMemory**</span></span>](cim-associatedmemory.md)
</dt> <dd>

<span data-ttu-id="4a2aa-143">[**CIM \_ AssociateMemory**](cim-associatedmemory.md)類別會將已安裝或相關聯的記憶體（例如快取記憶體）與邏輯裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-143">The [**CIM\_AssociateMemory**](cim-associatedmemory.md) class associates installed or associated memory, such as cache memory with a logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-144">**CIM \_ AssociatedProcessorMemory**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-144">**CIM\_AssociatedProcessorMemory**</span></span>](cim-associatedprocessormemory.md)
</dt> <dd>

<span data-ttu-id="4a2aa-145">[**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md)類別會將處理器和系統記憶體或處理器的快取產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-145">The [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md) class associates the processor and system memory, or a processor's cache.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-146">**CIM \_ AssociatedSensor**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-146">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> <dd>

<span data-ttu-id="4a2aa-147">[**CIM \_ AssociatedSensor**](cim-associatedsensor.md)類別會將已安裝的感應器與邏輯裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-147">The [**CIM\_AssociatedSensor**](cim-associatedsensor.md) class associates an installed sensor with a logical device.</span></span> <span data-ttu-id="4a2aa-148">感應器會測量重要的輸入和輸出屬性，並可包含在裝置內或安裝在附近。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-148">The sensor measures critical input and output properties, and can be included with the device or installed nearby.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-149">**CIM \_ AssociatedSupplyCurrentSensor**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-149">**CIM\_AssociatedSupplyCurrentSensor**</span></span>](cim-associatedsupplycurrentsensor.md)
</dt> <dd>

<span data-ttu-id="4a2aa-150">[**CIM \_ AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md)類別會將電源供應器與目前的 (amperage) 感應器建立關聯，以監視其輸入頻率。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-150">The [**CIM\_AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md) class associates a power supply with a current (amperage) sensor that monitors its input frequency.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-151">**CIM \_ AssociatedSupplyVoltageSensor**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-151">**CIM\_AssociatedSupplyVoltageSensor**</span></span>](cim-associatedsupplyvoltagesensor.md)
</dt> <dd>

<span data-ttu-id="4a2aa-152">將電源供應器與監視其輸入電壓的電壓感應器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-152">Associates a power supply with a voltage sensor that monitors its input voltage.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-153">**CIM \_ BasedOn**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-153">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> <dd>

<span data-ttu-id="4a2aa-154">[**CIM \_ BasedOn**](cim-basedon.md)類別代表一種關聯，描述如何從較低層級的範圍組合儲存區。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-154">The [**CIM\_BasedOn**](cim-basedon.md) class represents an association that describes how storage extents can be assembled from lower-level extents.</span></span> <span data-ttu-id="4a2aa-155">例如，實體範圍包含受保護的空間範圍。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-155">For example, physical extents include protected space extents.</span></span> <span data-ttu-id="4a2aa-156">因此，系統會從一或多個實體或受保護的空間範圍組合磁片區集合。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-156">Thus, volume sets are assembled from one or more physical or protected space extents.</span></span> <span data-ttu-id="4a2aa-157">快取記憶體可以獨立定義並在實體元素中實現，也可以根據暫時性或非暫時性的儲存區。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-157">Cache memory can be defined independently and realized in a physical element, or it can be based on volatile or non-volatile storage extents.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-158">**CIM \_ 電池**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-158">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dd>

<span data-ttu-id="4a2aa-159">「 [**CIM \_ 電池**](cim-battery.md) 」類別代表電池邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-159">The [**CIM\_Battery**](cim-battery.md) class represents the capabilities and management of the battery logical device.</span></span> <span data-ttu-id="4a2aa-160">此類別適用于膝上型電腦系統中的電池，以及其他內部和外部電池。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-160">This class applies to batteries in laptop systems and other internal and external batteries.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-161">**CIM \_ BinarySensor**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-161">**CIM\_BinarySensor**</span></span>](cim-binarysensor.md)
</dt> <dd>

<span data-ttu-id="4a2aa-162">[**CIM \_ BinarySensor**](cim-binarysensor.md)類別提供布林輸出。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-162">The [**CIM\_BinarySensor**](cim-binarysensor.md) class provides a Boolean output.</span></span> <span data-ttu-id="4a2aa-163">**CurrentState** 和 **PossibleStates** 屬性已新增至 sensoring，因此不再需要 **CIM \_ BinarySensor** 子類別，不過，它是為了回溯相容性而保留。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-163">The **CurrentState** and **PossibleStates** properties were added for sensoring, thus making the **CIM\_BinarySensor** subclass no longer necessary, although, it is retained for backward compatibility.</span></span> <span data-ttu-id="4a2aa-164">您可以具現化具有兩種可能狀態的感應器，以建立二進位感應器。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-164">A binary sensor can be created by instantiating a sensor with two possible states.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-165">**CIM \_ BIOSElement**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-165">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dd>

<span data-ttu-id="4a2aa-166">[**CIM \_ BIOSElement**](cim-bioselement.md)類別代表載入至非暫時性儲存區中，用來啟動和設定電腦系統的低層級軟體。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-166">The [**CIM\_BIOSElement**](cim-bioselement.md) class represents the low-level software that is loaded into non-volatile storage and used to start and configure a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-167">**CIM \_ BIOSFeature**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-167">**CIM\_BIOSFeature**</span></span>](cim-biosfeature.md)
</dt> <dd>

<span data-ttu-id="4a2aa-168">代表用來啟動及設定電腦系統的低層級軟體的功能。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-168">represents the capabilities of the low-level software that is used to start and configure a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-169">**CIM \_ BIOSFeatureBIOSElements**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-169">**CIM\_BIOSFeatureBIOSElements**</span></span>](cim-biosfeaturebioselements.md)
</dt> <dd>

<span data-ttu-id="4a2aa-170">[**CIM \_ BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md)類別會將 BIOS 功能和其匯總的 bios 專案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-170">The [**CIM\_BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md) class associates a BIOS feature and its aggregated BIOS elements.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-171">**CIM \_ BIOSLoadedInNV**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-171">**CIM\_BIOSLoadedInNV**</span></span>](cim-biosloadedinnv.md)
</dt> <dd>

<span data-ttu-id="4a2aa-172">[**CIM \_ BIOSLoadedInNV**](cim-biosloadedinnv.md)類別會將 BIOS 元素和載入它的非暫時性儲存區產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-172">The [**CIM\_BIOSLoadedInNV**](cim-biosloadedinnv.md) class associates a BIOS element and the non-volatile storage in which it is loaded.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-173">**CIM \_ BootOSFromFS**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-173">**CIM\_BootOSFromFS**</span></span>](cim-bootosfromfs.md)
</dt> <dd>

<span data-ttu-id="4a2aa-174">[**CIM \_ BootOSFromFS**](cim-bootosfromfs.md)類別會將作業系統和載入作業系統的檔案系統產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-174">The [**CIM\_BootOSFromFS**](cim-bootosfromfs.md) class associates the operating system and the file systems from which the operating system is loaded.</span></span> <span data-ttu-id="4a2aa-175">關聯是多對多;分散式作業系統可相依于數個檔案系統，以正確且完整的載入。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-175">The association is many-to-many; a distributed operating system can depend on several file systems to load correctly and completely.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-176">**CIM \_ BootSAP**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-176">**CIM\_BootSAP**</span></span>](cim-bootsap.md)
</dt> <dd>

<span data-ttu-id="4a2aa-177">[**CIM \_ BootSAP**](cim-bootsap.md)類別代表開機服務的存取點。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-177">The [**CIM\_BootSAP**](cim-bootsap.md) class represents the access points of a boot service.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-178">**CIM \_ BootService**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-178">**CIM\_BootService**</span></span>](cim-bootservice.md)
</dt> <dd>

<span data-ttu-id="4a2aa-179">[**CIM \_ BootService**](cim-bootservice.md)類別代表裝置或軟體所提供的功能，或由網路所提供的功能，可將作業系統載入到單一電腦系統上。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-179">The [**CIM\_BootService**](cim-bootservice.md) class represents the functionality provided by a device or software, or by a network, to load an operating system on a unitary computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-180">**CIM \_ BootServiceAccessBySAP**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-180">**CIM\_BootServiceAccessBySAP**</span></span>](cim-bootserviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="4a2aa-181">[**CIM \_ BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md)類別會將開機服務及其存取點產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-181">The [**CIM\_BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md) class associates a boot service and its access points.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-182">**CIM \_ CacheMemory**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-182">**CIM\_CacheMemory**</span></span>](cim-cachememory.md)
</dt> <dd>

<span data-ttu-id="4a2aa-183">[**CIM \_ CacheMemory**](cim-cachememory.md)類別會定義快取記憶體的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-183">The [**CIM\_CacheMemory**](cim-cachememory.md) class defines the capabilities and management of cache memory.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-184">**CIM \_ 卡片**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-184">**CIM\_Card**</span></span>](cim-card.md)
</dt> <dd>

<span data-ttu-id="4a2aa-185">「 [**CIM 記憶 \_ 卡**](cim-card.md) 」類別代表一種實體容器類型，可插入另一張卡片或主控電路板，或本身是底座中的主控電路板/主機板。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-185">The [**CIM\_Card**](cim-card.md) class represents a type of physical container that can be plugged into another card or hosting board, or is itself a hosting board/motherboard in a chassis.</span></span> <span data-ttu-id="4a2aa-186">此類別包含任何能夠攜帶信號的封裝，並提供實體元件的掛接點，例如晶片或其他實體套件（例如其他卡片）。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-186">This class includes any package that is capable of carrying signals and providing a mounting point for physical components, such as chips or other physical packages, such as other cards.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-187">**CIM \_ CardInSlot**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-187">**CIM\_CardInSlot**</span></span>](cim-cardinslot.md)
</dt> <dd>

<span data-ttu-id="4a2aa-188">[**CIM \_ CardInSlot**](cim-cardinslot.md)類別會將介面卡卡片與插入它的容器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-188">The [**CIM\_CardInSlot**](cim-cardinslot.md) class associates an adapter card with the container into which it is inserted.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-189">**CIM \_ CardOnCard**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-189">**CIM\_CardOnCard**</span></span>](cim-cardoncard.md)
</dt> <dd>

<span data-ttu-id="4a2aa-190">[**CIM \_ CardOnCard**](cim-cardoncard.md)關聯描述的是可插入主機板/主機板、介面卡 daughtercards 或卡片的關聯性，以支援特殊的卡片型模組。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-190">The [**CIM\_CardOnCard**](cim-cardoncard.md) association describes relationships about cards that can be plugged into motherboards/baseboards, daughtercards of an adapter, or cards that support special card-like modules.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-191">**CIM \_ CDROMDrive**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-191">**CIM\_CDROMDrive**</span></span>](cim-cdromdrive.md)
</dt> <dd>

<span data-ttu-id="4a2aa-192">[**CIM \_ CDROMDrive**](cim-cdromdrive.md)類別代表電腦上的 cd-rom 光碟機。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-192">The [**CIM\_CDROMDrive**](cim-cdromdrive.md) class represents a CD-ROM drive on the computer.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-193">**CIM \_ 底座**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-193">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> <dd>

<span data-ttu-id="4a2aa-194">[**CIM \_ 底座**](cim-chassis.md)類別代表包含其他元素的實體元素，並提供可定義的功能，例如桌面、處理節點、UPS、磁片或磁帶存放裝置，或這些專案的組合。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-194">The [**CIM\_Chassis**](cim-chassis.md) class represents the physical elements that enclose other elements and provide definable functionality, such as a desktop, processing node, UPS, disk or tape storage, or a combination of these.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-195">**CIM \_ ChassisInRack**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-195">**CIM\_ChassisInRack**</span></span>](cim-chassisinrack.md)
</dt> <dd>

<span data-ttu-id="4a2aa-196">[**CIM \_ ChassisInRack**](cim-chassisinrack.md)關聯代表機架與其包含的底座之間的「包含」關聯性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-196">The [**CIM\_ChassisInRack**](cim-chassisinrack.md) association represents the "containing" relationship between a rack and a chassis that it contains.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-197">**CIM \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-197">**CIM\_Check**</span></span>](cim-check.md)
</dt> <dd>

<span data-ttu-id="4a2aa-198">[**Cim \_ 檢查**](cim-check.md)類別代表一種條件或特性，此條件或特性在定義的環境中應該是 true，或是由 [**cim 系統 \_ 環境**](cim-computersystem.md)類別的實例所設定的範圍。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-198">The [**CIM\_Check**](cim-check.md) class represents a condition or characteristic that is expected to be true in an environment defined or scoped by an instance of a [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span> <span data-ttu-id="4a2aa-199">與特定軟體專案相關聯的檢查會使用 [**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md)關聯的 [**階段**] 屬性組織成兩個群組的其中一個。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-199">The checks associated with a particular software element are organized into one of two groups using the **Phase** property of the [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-200">**CIM \_ 晶片**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-200">**CIM\_Chip**</span></span>](cim-chip.md)
</dt> <dd>

<span data-ttu-id="4a2aa-201">[**CIM \_ 晶片**](cim-chip.md)類別代表整合電路硬體的類型，包括 ASICs、處理器、記憶體晶片等等。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-201">The [**CIM\_Chip**](cim-chip.md) class represents the type of integrated circuit hardware, including ASICs, processors, memory chips, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-202">**CIM \_ ClusteringSAP**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-202">**CIM\_ClusteringSAP**</span></span>](cim-clusteringsap.md)
</dt> <dd>

<span data-ttu-id="4a2aa-203">[**CIM \_ ClusteringSAP**](cim-clusteringsap.md)類別代表叢集服務的存取點。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-203">The [**CIM\_ClusteringSAP**](cim-clusteringsap.md) class represents the access points of a clustering service.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-204">**CIM \_ ClusteringService**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-204">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> <dd>

<span data-ttu-id="4a2aa-205">[**CIM \_ ClusteringService**](cim-clusteringservice.md)類別代表叢集所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-205">The [**CIM\_ClusteringService**](cim-clusteringservice.md) class represents the functionality provided by a cluster.</span></span> <span data-ttu-id="4a2aa-206">例如，容錯移轉功能可以模型化為容錯移轉叢集的服務。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-206">For example, failover functionality can be modeled as a service of a failover cluster.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-207">**CIM \_ ClusterServiceAccessBySAP**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-207">**CIM\_ClusterServiceAccessBySAP**</span></span>](cim-clusterserviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="4a2aa-208">[**CIM \_ ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md)類別代表叢集服務與其存取點之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-208">The [**CIM\_ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) class represents the relationship between a clustering service and its access points.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-209">**CIM \_ CollectedCollections**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-209">**CIM\_CollectedCollections**</span></span>](cim-collectedcollections.md)
</dt> <dd>

<span data-ttu-id="4a2aa-210">[**CIM \_ CollectedCollections**](cim-collectedcollections.md)類別是一種匯總關聯，代表 mse 集合中所包含之受管理系統元素 (MSE) 。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-210">The [**CIM\_CollectedCollections**](cim-collectedcollections.md) class is an aggregation association that represents a collection of Managed System Elements (MSE) contained in a collection of MSEs.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-211">**CIM \_ CollectedMSEs**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-211">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> <dd>

<span data-ttu-id="4a2aa-212">[**CIM \_ CollectedMSEs**](cim-collectedmses.md)關聯類別代表群組物件的成員（ [**CollectionOfMSEs**](cim-collectionofmses.md)類別）。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-212">The [**CIM\_CollectedMSEs**](cim-collectedmses.md) association class represents the members of the grouping object, a [**CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-213">**CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-213">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> <dd>

<span data-ttu-id="4a2aa-214">[**Cim \_ CollectionOfMSEs**](cim-collectionofmses.md)物件允許將 [**cim \_ ManagedSystemElement**](cim-managedsystemelement.md)物件分組，以建立設定和設定的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-214">The [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object allows the grouping of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects for the purpose of associating settings and configurations.</span></span> <span data-ttu-id="4a2aa-215">它是抽象的，需要在子類別中進行進一步的定義和語義改進。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-215">It is abstract to require further definition and semantic refinement in subclasses.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-216">**CIM \_ CollectionOfSensors**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-216">**CIM\_CollectionOfSensors**</span></span>](cim-collectionofsensors.md)
</dt> <dd>

<span data-ttu-id="4a2aa-217">[**CIM \_ CollectionOfSensors**](cim-collectionofsensors.md)關聯代表組成 multistate 感應器的二元感應器。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-217">The [**CIM\_CollectionOfSensors**](cim-collectionofsensors.md) association represents the binary sensors that make up the multistate sensor.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-218">**CIM \_ CollectionSetting**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-218">**CIM\_CollectionSetting**</span></span>](cim-collectionsetting.md)
</dt> <dd>

<span data-ttu-id="4a2aa-219">[**Cim \_ CollectionSetting**](cim-collectionsetting.md)類別代表 [**cim \_ CollectionOfMSEs**](cim-collectionofmses.md)和為其定義的設定類別之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-219">The [**CIM\_CollectionSetting**](cim-collectionsetting.md) class represents the association between a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-220">**CIM \_ CompatibleProduct**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-220">**CIM\_CompatibleProduct**</span></span>](cim-compatibleproduct.md)
</dt> <dd>

<span data-ttu-id="4a2aa-221">[**CIM \_ CompatibleProduct**](cim-compatibleproduct.md)類別代表產品之間的關聯，表示兩個參考的產品是否可互通，例如是否可以一起安裝，或是可以是另一個實體容器，依此類推。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-221">The [**CIM\_CompatibleProduct**](cim-compatibleproduct.md) class represents an association between products that indicates whether two referenced products are interoperable, such as whether they can be installed together, or whether one can be the physical container for the other, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-222">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-222">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dd>

<span data-ttu-id="4a2aa-223">[**CIM \_ 元件**](cim-component.md)關聯表示 mse 之間關聯性的元件。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-223">The [**CIM\_Component**](cim-component.md) association represents the parts of a relationship between MSEs.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-224">**CIM \_ 未進行**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-224">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dd>

<span data-ttu-id="4a2aa-225">[**Cim 非 \_**](cim-computersystem.md)實例類別代表 [**cim \_ ManagedSystemElement**](cim-managedsystemelement.md)實例的特殊集合。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-225">A [**CIM\_ComputerSystem**](cim-computersystem.md) class represents a special collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) instances.</span></span> <span data-ttu-id="4a2aa-226">此集合提供電腦功能，並可做為匯總點，以建立下列一或多個專案的關聯：檔案系統、作業系統、處理器和記憶體 (volatile 和非暫時性儲存) 。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-226">This collection provides computer capabilities and serves as an aggregation point to associate one or more of the following elements: file system, operating system, processor and memory (volatile and non-volatile storage).</span></span> <span data-ttu-id="4a2aa-227">此類別衍生自 [**CIM \_ 系統**](cim-system.md)。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-227">This class is derived from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-228">**CIM \_ ComputerSystemDMA**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-228">**CIM\_ComputerSystemDMA**</span></span>](cim-computersystemdma.md)
</dt> <dd>

<span data-ttu-id="4a2aa-229">[**CIM \_ ComputerSystemDMA**](cim-computersystemdma.md)類別代表電腦系統與其可用的直接記憶體存取 (DMA) 通道之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-229">The [**CIM\_ComputerSystemDMA**](cim-computersystemdma.md) class represents an association between a computer system and its available direct memory access (DMA) channels.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-230">**CIM \_ ComputerSystemIRQ**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-230">**CIM\_ComputerSystemIRQ**</span></span>](cim-computersystemirq.md)
</dt> <dd>

<span data-ttu-id="4a2aa-231">[**CIM \_ ComputerSystemIRQ**](cim-computersystemirq.md)類別代表電腦系統與其可用的插斷要求 () 的 irq 之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-231">The [**CIM\_ComputerSystemIRQ**](cim-computersystemirq.md) class represents an association between a computer system and its available interrupt request lines (IRQs).</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-232">**CIM \_ ComputerSystemMappedIO**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-232">**CIM\_ComputerSystemMappedIO**</span></span>](cim-computersystemmappedio.md)
</dt> <dd>

<span data-ttu-id="4a2aa-233">[**CIM \_ ComputerSystemMappedIO**](cim-computersystemmappedio.md)類別代表電腦系統與其可用記憶體對應 i/o 埠之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-233">The [**CIM\_ComputerSystemMappedIO**](cim-computersystemmappedio.md) class represents an association between a computer system and its available memory-mapped I/O ports.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-234">**CIM \_ ComputerSystemPackage**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-234">**CIM\_ComputerSystemPackage**</span></span>](cim-computersystempackage.md)
</dt> <dd>

<span data-ttu-id="4a2aa-235">[**CIM \_ ComputerSystemPackage**](cim-computersystempackage.md)類別代表一種關聯，可明確定義單一電腦系統與一或多個實體套件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-235">The [**CIM\_ComputerSystemPackage**](cim-computersystempackage.md) class represents an association that explicitly defines the relationship between unitary computer systems and one or more physical packages.</span></span> <span data-ttu-id="4a2aa-236">關聯類似于實體元素實現邏輯裝置的方式。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-236">The association is similar to the way that logical devices are realized by physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-237">**CIM \_ ComputerSystemResource**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-237">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> <dd>

<span data-ttu-id="4a2aa-238">[**CIM \_ ComputerSystemResource**](cim-computersystemresource.md)類別代表電腦系統與其可用系統資源之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-238">The [**CIM\_ComputerSystemResource**](cim-computersystemresource.md) class represents an association between a computer system and its available system resources.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-239">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-239">**CIM\_Configuration**</span></span>](cim-configuration.md)
</dt> <dd>

<span data-ttu-id="4a2aa-240">Cim 設定物件允許將 [**cim \_ 設定**](cim-setting.md)物件中 (定義的參數集群組) 和一個或多個 managed 系統專案的相依性。 [**\_**](cim-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="4a2aa-240">The [**CIM\_Configuration**](cim-configuration.md) object allows the grouping of parameter sets (defined in [**CIM\_Setting**](cim-setting.md) objects) and dependencies for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-241">**CIM \_ ConnectedTo**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-241">**CIM\_ConnectedTo**</span></span>](cim-connectedto.md)
</dt> <dd>

<span data-ttu-id="4a2aa-242">[**CIM \_ ConnectedTo**](cim-connectedto.md)類別代表一種關聯，表示兩個或多個實體連接器已連線。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-242">The [**CIM\_ConnectedTo**](cim-connectedto.md) class represents an association that indicates that two or more physical connectors are connected.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-243">**CIM \_ ConnectorOnPackage**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-243">**CIM\_ConnectorOnPackage**</span></span>](cim-connectoronpackage.md)
</dt> <dd>

<span data-ttu-id="4a2aa-244">[**CIM \_ ConnectorOnPackage**](cim-connectoronpackage.md)類別代表的關聯，會明確指出連接器與封裝之間的內含專案關聯性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-244">The [**CIM\_ConnectorOnPackage**](cim-connectoronpackage.md) class represents an association that makes explicit the containment relationship between connectors and packages.</span></span> <span data-ttu-id="4a2aa-245">實體套件包含連接器和其他實體元素。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-245">Physical packages contain connectors as well as other physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-246">**CIM \_ 容器**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-246">**CIM\_Container**</span></span>](cim-container.md)
</dt> <dd>

<span data-ttu-id="4a2aa-247">[**CIM \_ 容器**](cim-container.md)類別表示包含的實體元素與包含的實體專案之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-247">The [**CIM\_Container**](cim-container.md) class represents an association between a contained and a containing physical element.</span></span> <span data-ttu-id="4a2aa-248">包含的物件必須是實體封裝。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-248">A containing object must be a physical package.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-249">**CIM \_ ControlledBy**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-249">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dd>

<span data-ttu-id="4a2aa-250">[**CIM \_ ControlledBy**](cim-controlledby.md)關聯性會指出哪些裝置是由控制器邏輯裝置所發出或存取。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-250">The [**CIM\_ControlledBy**](cim-controlledby.md) relationship indicates which devices are commanded by, or accessed through, the controller logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-251">**CIM \_ 控制器**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-251">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dd>

<span data-ttu-id="4a2aa-252">[**CIM \_ 控制器**](cim-controller.md)類別是用來分組其他控制項相關裝置的父類別。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-252">The [**CIM\_Controller**](cim-controller.md) class is a parent class for grouping miscellaneous control-related devices.</span></span> <span data-ttu-id="4a2aa-253">控制器的範例包括 SCSI 控制器、USB 控制器和串列控制器。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-253">Examples of controllers are SCSI controllers, USB controllers, and serial controllers.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-254">**CIM \_ CoolingDevice**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-254">**CIM\_CoolingDevice**</span></span>](cim-coolingdevice.md)
</dt> <dd>

<span data-ttu-id="4a2aa-255">[**CIM \_ CoolingDevice**](cim-coolingdevice.md)類別代表冷卻裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-255">The [**CIM\_CoolingDevice**](cim-coolingdevice.md) class represents the capabilities and management of cooling devices.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-256">**CIM \_ CopyFileAction**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-256">**CIM\_CopyFileAction**</span></span>](cim-copyfileaction.md)
</dt> <dd>

<span data-ttu-id="4a2aa-257">[**CIM \_ CopyFileAction**](cim-copyfileaction.md)類別代表將檔案從電腦系統移動或複製到新位置。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-257">The [**CIM\_CopyFileAction**](cim-copyfileaction.md) class represents moving or copying files from a computer system to a new location.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-258">**CIM \_ CreateDirectoryAction**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-258">**CIM\_CreateDirectoryAction**</span></span>](cim-createdirectoryaction.md)
</dt> <dd>

<span data-ttu-id="4a2aa-259">[**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md)類別會為要安裝在本機的軟體元素建立空的目錄。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-259">The [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class creates empty directories for software elements to be installed locally.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-260">**CIM \_ CurrentSensor**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-260">**CIM\_CurrentSensor**</span></span>](cim-currentsensor.md)
</dt> <dd>

<span data-ttu-id="4a2aa-261">[**Cim \_ CurrentSensor**](cim-currentsensor.md)類別存在，可回溯相容于舊版 cim 架構定義。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-261">The [**CIM\_CurrentSensor**](cim-currentsensor.md) class exists for backward compatibility to earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-262">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-262">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dd>

<span data-ttu-id="4a2aa-263">[**CIM 資料 \_ 檔**](cim-datafile.md)類別代表資料的命名集合或可執行檔程式碼。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-263">The [**CIM\_DataFile**](cim-datafile.md) class represents a named collection of data or executable code.</span></span> <span data-ttu-id="4a2aa-264">只會傳回本機固定磁片上的檔案實例</span><span class="sxs-lookup"><span data-stu-id="4a2aa-264">Only instances of files on local fixed disks will be returned</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-265">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-265">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dd>

<span data-ttu-id="4a2aa-266">[**CIM 相依 \_**](cim-dependency.md)性類別代表在物件之間建立相依性關聯性的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-266">The [**CIM\_Dependency**](cim-dependency.md) class represents an association that establishes dependency relationships between objects.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-267">**CIM \_ DependencyCoNtext**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-267">**CIM\_DependencyContext**</span></span>](cim-dependencycontext.md)
</dt> <dd>

<span data-ttu-id="4a2aa-268">[**Cim \_ DependencyCoNtext**](cim-dependencycontext.md)關聯性會將 [**cim \_**](cim-dependency.md)相依性類別與一個或多個 [**cim \_ 設定物件**](cim-configuration.md)產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-268">The [**CIM\_DependencyContext**](cim-dependencycontext.md) relationship associates a [**CIM\_Dependency**](cim-dependency.md) class with one or more [**CIM\_Configuration**](cim-configuration.md) objects.</span></span> <span data-ttu-id="4a2aa-269">例如，電腦系統的相依性可能會根據系統所連接的網路而變更。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-269">For example, a computer system's dependencies can change based on the network to which the system is attached.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-270">**CIM \_ DesktopMonitor**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-270">**CIM\_DesktopMonitor**</span></span>](cim-desktopmonitor.md)
</dt> <dd>

<span data-ttu-id="4a2aa-271">[**CIM \_ DesktopMonitor**](cim-desktopmonitor.md)類別代表桌面監視器 (CRT) 邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-271">The [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) class represents the capabilities and management of the desktop monitor (CRT) logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-272">**CIM \_ DeviceAccessedByFile**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-272">**CIM\_DeviceAccessedByFile**</span></span>](cim-deviceaccessedbyfile.md)
</dt> <dd>

<span data-ttu-id="4a2aa-273">[**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md)關聯類別會使用參考的 [**CIM \_ DeviceFile**](cim-devicefile.md)類別來指定存取的邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-273">The [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) association class specifies the logical device accessed by using the referenced [**CIM\_DeviceFile**](cim-devicefile.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-274">**CIM \_ DeviceConnection**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-274">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> <dd>

<span data-ttu-id="4a2aa-275">[**CIM \_ DeviceConnection**](cim-deviceconnection.md)關聯類別代表兩個或多個已連線的裝置。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-275">The [**CIM\_DeviceConnection**](cim-deviceconnection.md) association class represents two or more connected devices.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-276">**CIM \_ DeviceErrorCounts**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-276">**CIM\_DeviceErrorCounts**</span></span>](cim-deviceerrorcounts.md)
</dt> <dd>

<span data-ttu-id="4a2aa-277">[**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md)類別是一個統計類別，其中包含邏輯裝置的錯誤相關計數器。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-277">The [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class is a statistical class that contains error-related counters for a logical device.</span></span> <span data-ttu-id="4a2aa-278">錯誤的類型是由 CCITT (Rec 733) 和 ISO (IEC 10164-4) 所定義。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-278">The types of errors are defined by CCITT (Rec X.733) and ISO (IEC 10164-4).</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-279">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-279">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> <dd>

<span data-ttu-id="4a2aa-280">[**CIM \_ DeviceFile**](cim-devicefile.md)類別代表代表裝置的邏輯檔案類型。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-280">The [**CIM\_DeviceFile**](cim-devicefile.md) class represents a type of logical file, which represents a device.</span></span> <span data-ttu-id="4a2aa-281">此慣例適用于使用位元組串流 i/o 模型管理裝置的作業系統。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-281">This convention is useful for operating systems that manage devices using a byte stream I/O model.</span></span> <span data-ttu-id="4a2aa-282">與此檔案相關聯的邏輯裝置是使用 [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) 關聯性所指定。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-282">The logical device that is associated with this file is specified using the [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) relationship.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-283">**CIM \_ DeviceSAPImplementation**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-283">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dd>

<span data-ttu-id="4a2aa-284">[**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md)類別代表服務存取點 (SAP) 與其實作為方式之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-284">The [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) class represents an association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="4a2aa-285">當許多邏輯裝置與一個 SAP 相關聯時，這些專案會一起運作以提供存取點。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-285">When many logical devices are associated with one SAP, the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="4a2aa-286">如果有不同的 SAP 執行，每個實施都會導致 SAP 物件的個別具現化。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-286">If different implementations of a SAP exist, each implementation results in individual instantiations of the SAP object.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-287">**CIM \_ DeviceServiceImplementation**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-287">**CIM\_DeviceServiceImplementation**</span></span>](cim-deviceserviceimplementation.md)
</dt> <dd>

<span data-ttu-id="4a2aa-288">[**CIM \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md)類別代表服務與其實作為方式之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-288">The [**CIM\_DeviceServiceImplementation**](cim-deviceserviceimplementation.md) class represents an association between a service and how it is implemented.</span></span> <span data-ttu-id="4a2aa-289">當多個裝置與一個服務相關聯時，這些專案會一起運作，以提供服務。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-289">When multiple devices are associated with one service, the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="4a2aa-290">如果有不同的服務執行，則每個執行都會導致服務物件的個別具現化。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-290">If different implementations of a service exist, each implementation results in individual instantiations of the service object.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-291">**CIM \_ DeviceSoftware**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-291">**CIM\_DeviceSoftware**</span></span>](cim-devicesoftware.md)
</dt> <dd>

<span data-ttu-id="4a2aa-292">[**CIM \_ DeviceSoftware**](cim-devicesoftware.md)關聯性會識別與裝置相關聯的軟體，例如驅動程式、設定或應用程式軟體或固件。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-292">The [**CIM\_DeviceSoftware**](cim-devicesoftware.md) relationship identifies software that is associated with a device, such as drivers, configuration or application software, or firmware.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-293">**CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-293">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> <dd>

<span data-ttu-id="4a2aa-294">[**CIM \_ 目錄**](cim-directory.md)類別代表以邏輯方式分組其包含之資料檔案的檔案類型，並提供群組檔案的路徑資訊。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-294">The [**CIM\_Directory**](cim-directory.md) class represents a file type that logically groups the data files that it contains and provides path information for the grouped files.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-295">**CIM \_ DirectoryAction**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-295">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> <dd>

<span data-ttu-id="4a2aa-296">[**CIM \_ DirectoryAction**](cim-directoryaction.md)抽象類別會管理目錄。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-296">The [**CIM\_DirectoryAction**](cim-directoryaction.md) abstract class manages directories.</span></span> <span data-ttu-id="4a2aa-297">目錄建立是由 [**cim \_ CreateDirectoryAction**](cim-createdirectoryaction.md) 類別處理，而目錄移除則由 [**cim \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) 類別處理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-297">Directory creation is handled by the [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class and directory removal is handled by the [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-298">**CIM \_ DirectoryContainsFile**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-298">**CIM\_DirectoryContainsFile**</span></span>](cim-directorycontainsfile.md)
</dt> <dd>

<span data-ttu-id="4a2aa-299">[**CIM \_ DirectoryContainsFile**](cim-directorycontainsfile.md)類別代表目錄和該目錄中包含的檔案之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-299">The [**CIM\_DirectoryContainsFile**](cim-directorycontainsfile.md) class represents an association between a directory and files contained within that directory.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-300">**CIM \_ DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-300">**CIM\_DirectorySpecification**</span></span>](cim-directoryspecification.md)
</dt> <dd>

<span data-ttu-id="4a2aa-301">[**CIM \_ DirectorySpecification**](cim-directoryspecification.md)類別會捕捉 software 元素的主要目錄結構。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-301">The [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class captures the major directory structure of a software element.</span></span> <span data-ttu-id="4a2aa-302">此類別是用來將軟體專案的檔案組織成可在電腦系統上重新置放的可管理單位。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-302">This class is used to organize the files of a software element into manageable units that can be relocated on a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-303">**CIM \_ DirectorySpecificationFile**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-303">**CIM\_DirectorySpecificationFile**</span></span>](cim-directoryspecificationfile.md)
</dt> <dd>

<span data-ttu-id="4a2aa-304">[**Cim \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md)關聯代表包含透過參考 [**CIM \_ DirectorySpecification**](cim-directoryspecification.md)類別所指定之檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-304">The [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association represents the directory that contains the file specified by referencing the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-305">**CIM \_ DiscreteSensor**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-305">**CIM\_DiscreteSensor**</span></span>](cim-discretesensor.md)
</dt> <dd>

<span data-ttu-id="4a2aa-306">[**CIM \_ DiscreteSensor**](cim-discretesensor.md)類別具有一組可以報告的合法字串值。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-306">The [**CIM\_DiscreteSensor**](cim-discretesensor.md) class has a set of legal string values that it can report.</span></span> <span data-ttu-id="4a2aa-307">這些值會在感應器的 **PossibleValues** 屬性中列舉。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-307">The values are enumerated in the sensor's **PossibleValues** property.</span></span> <span data-ttu-id="4a2aa-308">離散感應器一律會有對應至其中一個列舉值的目前讀取。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-308">A discrete sensor always has a current reading that corresponds to one of the enumerated values.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-309">**CIM \_ DiskDrive**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-309">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dd>

<span data-ttu-id="4a2aa-310">[**CIM \_ DiskDrive**](cim-diskdrive.md)類別代表作業系統所見的實體磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-310">The [**CIM\_DiskDrive**](cim-diskdrive.md) class represents a physical disk drive as seen by the operating system.</span></span> <span data-ttu-id="4a2aa-311">磁片磁碟機功能對應到磁片磁碟機的邏輯和管理特性，在某些情況下，可能不會反映裝置的實體特性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-311">The disk drive features correspond to the logical and management characteristics of the drive, and in some cases, may not reflect the physical characteristics of the device.</span></span> <span data-ttu-id="4a2aa-312">實體磁片磁碟機的介面是此類別的成員。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-312">An interface to a physical drive is a member of this class.</span></span> <span data-ttu-id="4a2aa-313">不過，根據另一個邏輯裝置的物件不是此類別的成員。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-313">However, an object based on another logical device is not a member of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-314">**CIM \_ DisketteDrive**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-314">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dd>

<span data-ttu-id="4a2aa-315">[**CIM \_ DisketteDrive**](cim-diskettedrive.md)類別代表磁片磁碟機的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-315">The [**CIM\_DisketteDrive**](cim-diskettedrive.md) class represents the capabilities and management of a diskette drive.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-316">**CIM \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-316">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dd>

<span data-ttu-id="4a2aa-317">[**CIM \_ DiskPartition**](cim-diskpartition.md)類別代表由作業系統透過分割區的類型和子類型欄位識別的連續邏輯區塊範圍。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-317">The [**CIM\_DiskPartition**](cim-diskpartition.md) class represents a contiguous range of logical blocks that is identifiable by the operating system by way of the partition's type and subtype fields.</span></span> <span data-ttu-id="4a2aa-318">磁碟分割應由 [**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) 關聯) 或建立于儲存磁片區的實體媒體 (直接實現。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-318">Disk partitions should be directly realized by physical media (indicated by the [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) association) or built on storage volumes.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-319">**CIM \_ DiskSpaceCheck**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-319">**CIM\_DiskSpaceCheck**</span></span>](cim-diskspacecheck.md)
</dt> <dd>

<span data-ttu-id="4a2aa-320">[**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md)類別會檢查系統的可用磁碟空間量，並在 **AvailableDiskSpace** 屬性中指定它。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-320">The [**CIM\_DiskSpaceCheck**](cim-diskspacecheck.md) class checks the system's amount of available disk space and specifies it in the **AvailableDiskSpace** property.</span></span> <span data-ttu-id="4a2aa-321">詳細資料會 [**與 cim \_**](cim-computersystem.md) FileSystem 物件（描述系統內容）相關聯之 [**Cim \_ FileSystem**](cim-filesystem.md)物件的 **AvailableSpace** 屬性中的值進行比較。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-321">Details are compared with the value in the **AvailableSpace** property of the [**CIM\_FileSystem**](cim-filesystem.md) object that is associated with the [**CIM\_ComputerSystem**](cim-computersystem.md) object, which describes the system environment.</span></span> <span data-ttu-id="4a2aa-322">當 **AvailableSpace** 屬性的值大於或等於 **AvailableDiskSpace** 屬性中指定的值時，就會滿足條件。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-322">When the value of the **AvailableSpace** property is greater than or equal to the value specified in the **AvailableDiskSpace** property, the condition is satisfied.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-323">**CIM \_ 顯示**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-323">**CIM\_Display**</span></span>](cim-display.md)
</dt> <dd>

<span data-ttu-id="4a2aa-324">[**CIM \_ 顯示**](cim-display.md)類別是用來分組其他顯示裝置的父類別。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-324">The [**CIM\_Display**](cim-display.md) class is a parent class for grouping miscellaneous display devices.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-325">**CIM \_ DMA**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-325">**CIM\_DMA**</span></span>](cim-dma.md)
</dt> <dd>

<span data-ttu-id="4a2aa-326">[**CIM \_ DMA**](cim-dma.md)類別代表 (DMA) 的電腦架構直接記憶體存取。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-326">The [**CIM\_DMA**](cim-dma.md) class represents computer architecture direct memory access (DMA).</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-327">**CIM \_ 停駐**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-327">**CIM\_Docked**</span></span>](cim-docked.md)
</dt> <dd>

<span data-ttu-id="4a2aa-328">[**CIM 停 \_**](cim-docked.md)駐關聯表示兩個底座之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-328">The [**CIM\_Docked**](cim-docked.md) association represents the relationship between two chassis.</span></span> <span data-ttu-id="4a2aa-329">例如，膝上型電腦 (一種底座) 可停駐在銜接站 (另一種類型的底座) 。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-329">For example, a laptop (a type of chassis) can be docked in a docking station (another type of chassis).</span></span> <span data-ttu-id="4a2aa-330">這是明確描述的一般關聯性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-330">This typical relationship is explicitly described.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-331">**CIM \_ ElementCapacity**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-331">**CIM\_ElementCapacity**</span></span>](cim-elementcapacity.md)
</dt> <dd>

<span data-ttu-id="4a2aa-332">[**Cim \_ ElementCapacity**](cim-elementcapacity.md)類別會將 [**cim \_ PhysicalCapacity**](cim-physicalcapacity.md)物件與一或多個實體元素產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-332">The [**CIM\_ElementCapacity**](cim-elementcapacity.md) class associates a [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) object with one or more physical elements.</span></span> <span data-ttu-id="4a2aa-333">它會將最小和最大硬體需求的描述與所述的實體元素)  (或功能相關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-333">It associates a description of the minimum and maximum hardware requirements (or capabilities) to the physical elements being described.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-334">**CIM \_ ElementConfiguration**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-334">**CIM\_ElementConfiguration**</span></span>](cim-elementconfiguration.md)
</dt> <dd>

<span data-ttu-id="4a2aa-335">[**Cim \_ ElementConfiguration**](cim-elementconfiguration.md)關聯會將 [**cim \_ 設定**](cim-configuration.md)物件與一或多個受管理的系統元素產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-335">The [**CIM\_ElementConfiguration**](cim-elementconfiguration.md) association relates a [**CIM\_Configuration**](cim-configuration.md) object to one or more managed system elements.</span></span> <span data-ttu-id="4a2aa-336">**Cim 設定 \_** 物件代表特定的行為，或相關聯之 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)所需的功能狀態。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-336">The **CIM\_Configuration** object represents a certain behavior, or a desired functional state for the associated [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-337">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-337">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dd>

<span data-ttu-id="4a2aa-338">[**CIM \_ ElementSetting**](cim-elementsetting.md)類別代表 managed 系統專案與其定義的設定類別之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-338">The [**CIM\_ElementSetting**](cim-elementsetting.md) class represents the association between managed system elements and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-339">**CIM \_ ElementsLinked**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-339">**CIM\_ElementsLinked**</span></span>](cim-elementslinked.md)
</dt> <dd>

<span data-ttu-id="4a2aa-340">[**CIM \_ ElementsLinked**](cim-elementslinked.md)關聯表示以實體連結連接在一起的實體元素。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-340">The [**CIM\_ElementsLinked**](cim-elementslinked.md) association represents physical elements that are cabled together by a physical link.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-341">**CIM \_ ErrorCountersForDevice**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-341">**CIM\_ErrorCountersForDevice**</span></span>](cim-errorcountersfordevice.md)
</dt> <dd>

<span data-ttu-id="4a2aa-342">[**Cim \_ ErrorCountersForDevice**](cim-errorcountersfordevice.md)類別會將 [**cim \_ DeviceErrorCounts**](cim-deviceerrorcounts.md)類別與它所套用的邏輯裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-342">The [**CIM\_ErrorCountersForDevice**](cim-errorcountersfordevice.md) class associates the [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class to the logical device to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-343">**CIM \_ ExecuteProgram**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-343">**CIM\_ExecuteProgram**</span></span>](cim-executeprogram.md)
</dt> <dd>

<span data-ttu-id="4a2aa-344">[**CIM \_ ExecuteProgram**](cim-executeprogram.md)類別代表可在已安裝 software 元素的系統上執行的檔案。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-344">The [**CIM\_ExecuteProgram**](cim-executeprogram.md) class represents files that can be executed on the system where the software element is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-345">**CIM \_ 匯出**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-345">**CIM\_Export**</span></span>](cim-export.md)
</dt> <dd>

<span data-ttu-id="4a2aa-346">[**CIM \_ 匯出**](cim-export.md)類別代表本機檔案系統與其目錄之間的關聯，這表示指定的目錄可供掛接。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-346">The [**CIM\_Export**](cim-export.md) class represents an association between a local file system and its directories, which indicate that the specified directories are available for mount.</span></span> <span data-ttu-id="4a2aa-347">匯出整個檔案系統時，目錄應該參考檔案系統的最上層目錄。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-347">When exporting an entire file system, the directory should reference the topmost directory of the file system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-348">**CIM \_ ExtraCapacityGroup**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-348">**CIM\_ExtraCapacityGroup**</span></span>](cim-extracapacitygroup.md)
</dt> <dd>

<span data-ttu-id="4a2aa-349">[**CIM \_ ExtraCapacityGroup**](cim-extracapacitygroup.md)類別衍生自冗余群組，指出匯總專案的容量或功能比所需的還多。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-349">The [**CIM\_ExtraCapacityGroup**](cim-extracapacitygroup.md) class is derived from a redundancy group that indicates the aggregated elements have more capacity or capability than is needed.</span></span> <span data-ttu-id="4a2aa-350">這類冗余的範例是在系統中安裝 N + 1 電源供應器或風扇。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-350">An example of this type of redundancy is the installation of N+1 power supplies or fans in a system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-351">**CIM \_ 風扇**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-351">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> <dd>

<span data-ttu-id="4a2aa-352">[**CIM \_ 風扇**](cim-fan.md)類別代表風扇冷卻裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-352">The [**CIM\_Fan**](cim-fan.md) class represents the capabilities and management of a fan cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-353">**CIM \_ FileAction**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-353">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> <dd>

<span data-ttu-id="4a2aa-354">[**CIM \_ FileAction**](cim-fileaction.md)類別可讓作者找出使用者電腦上已存在的檔案，然後將這些檔案移動或複製到新的位置。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-354">The [**CIM\_FileAction**](cim-fileaction.md) class allows the author to locate files that already exist on a user's computer, and then move or copy those files to a new location.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-355">**CIM \_ FileSpecification**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-355">**CIM\_FileSpecification**</span></span>](cim-filespecification.md)
</dt> <dd>

<span data-ttu-id="4a2aa-356">[**CIM \_ FileSpecification**](cim-filespecification.md)類別代表系統上或關閉的檔案。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-356">The [**CIM\_FileSpecification**](cim-filespecification.md) class represents a file that is either on or off of the system.</span></span> <span data-ttu-id="4a2aa-357">檔案位於 [**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md) 關聯所識別的目錄中。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-357">The file is located in the directory identified by the [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association.</span></span> <span data-ttu-id="4a2aa-358">[**Invoke**](invoke-method-in-class-cim-filespecification.md)方法會使用此資訊來檢查檔案是否存在。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-358">The [**Invoke**](invoke-method-in-class-cim-filespecification.md) method uses the information to check for the file's existence.</span></span> <span data-ttu-id="4a2aa-359">請注意，不會檢查具有 **Null** 值的屬性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-359">Note that properties with a **Null** value are not checked.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-360">**CIM \_ FileStorage**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-360">**CIM\_FileStorage**</span></span>](cim-filestorage.md)
</dt> <dd>

<span data-ttu-id="4a2aa-361">[**CIM \_ FileStorage**](cim-filestorage.md)關聯會連結檔案系統以及透過檔案系統定址的邏輯檔案。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-361">The [**CIM\_FileStorage**](cim-filestorage.md) association links the file system and the logical files addressed through the file system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-362">**CIM \_ 檔案系統**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-362">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> <dd>

<span data-ttu-id="4a2aa-363">[**CIM \_ FileSystem**](cim-filesystem.md)類別代表電腦系統本機的檔案或資料集，或從檔案伺服器遠端掛接的檔案或資料集。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-363">The [**CIM\_FileSystem**](cim-filesystem.md) class represents a file or data set local to a computer system or remotely mounted from a file server.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-364">**CIM \_ FlatPanel**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-364">**CIM\_FlatPanel**</span></span>](cim-flatpanel.md)
</dt> <dd>

<span data-ttu-id="4a2aa-365">[**CIM \_ FlatPanel**](cim-flatpanel.md)類別代表平面化面板邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-365">The [**CIM\_FlatPanel**](cim-flatpanel.md) class represents the capabilities and management of the flat panel logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-366">**CIM \_ FromDirectoryAction**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-366">**CIM\_FromDirectoryAction**</span></span>](cim-fromdirectoryaction.md)
</dt> <dd>

<span data-ttu-id="4a2aa-367">[**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md)關聯會識別檔案動作的來原始目錄。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-367">The [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association identifies the source directory for the file action.</span></span> <span data-ttu-id="4a2aa-368">使用這個關聯時，假設來原始目錄是由先前的動作所建立。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-368">When this association is used, the assumption is that the source directory was created by a previous action.</span></span> <span data-ttu-id="4a2aa-369">此關聯無法與 [**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) 關聯存在; 檔案動作只能包含單一來原始目錄。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-369">This association cannot exist with a [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association; a file action can only involve a single source directory.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-370">**CIM \_ FromDirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-370">**CIM\_FromDirectorySpecification**</span></span>](cim-fromdirectoryspecification.md)
</dt> <dd>

<span data-ttu-id="4a2aa-371">[**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md)關聯會識別檔案動作的來原始目錄。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-371">The [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association identifies the source directory for the file action.</span></span> <span data-ttu-id="4a2aa-372">使用這個關聯時，假設來原始目錄已經存在。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-372">When this association is used, the assumption is that the source directory already exists.</span></span> <span data-ttu-id="4a2aa-373">此關聯無法與 [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) 關聯存在; 檔案動作只能包含單一來原始目錄。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-373">This association cannot exist with a [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association; a file action can only involve a single source directory.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-374">**CIM \_ FRU**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-374">**CIM\_FRU**</span></span>](cim-fru.md)
</dt> <dd>

<span data-ttu-id="4a2aa-375">[**CIM \_ FRU**](cim-fru.md)類別代表廠商定義的產品和實體元素集合，與現場可更換單元相關聯 (FRU) 在客戶的位置支援、維護或升級產品。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-375">The [**CIM\_FRU**](cim-fru.md) class represents a vendor-defined collection of products and physical elements that are associated with a field replaceable unit (FRU) to support, maintain, or upgrade a product at the customer's location.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-376">**CIM \_ FRUIncludesProduct**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-376">**CIM\_FRUIncludesProduct**</span></span>](cim-fruincludesproduct.md)
</dt> <dd>

<span data-ttu-id="4a2aa-377">[**CIM \_ FRUIncludesProduct**](cim-fruincludesproduct.md)類別指出現場可更換單元 (FRU) 可能由其他產品組成。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-377">The [**CIM\_FRUIncludesProduct**](cim-fruincludesproduct.md) class indicates that a field replaceable unit (FRU) may be composed of other products.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-378">**CIM \_ FRUPhysicalElements**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-378">**CIM\_FRUPhysicalElements**</span></span>](cim-fruphysicalelements.md)
</dt> <dd>

<span data-ttu-id="4a2aa-379">[**CIM \_ FRUPhysicalElements**](cim-fruphysicalelements.md)類別代表組成現場可更換單元 (FRU) 的實體元素。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-379">The [**CIM\_FRUPhysicalElements**](cim-fruphysicalelements.md) class represents the physical elements that make up a field replaceable unit (FRU).</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-380">**CIM \_ HeatPipe**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-380">**CIM\_HeatPipe**</span></span>](cim-heatpipe.md)
</dt> <dd>

<span data-ttu-id="4a2aa-381">[**CIM \_ HeatPipe**](cim-heatpipe.md)類別代表熱度管道冷卻裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-381">The [**CIM\_HeatPipe**](cim-heatpipe.md) class represents the capabilities and management of a heat pipe cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-382">**CIM \_ HostedAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-382">**CIM\_HostedAccessPoint**</span></span>](cim-hostedaccesspoint.md)
</dt> <dd>

<span data-ttu-id="4a2aa-383">[**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md)類別代表服務存取點 (SAP) 和提供它的系統之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-383">The [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md) class represents an association between a service access point (SAP) and the system on which it is provided.</span></span> <span data-ttu-id="4a2aa-384">每個系統可能會裝載許多 Sap。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-384">Each system may host many SAPs.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-385">**CIM \_ HostedBootSAP**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-385">**CIM\_HostedBootSAP**</span></span>](cim-hostedbootsap.md)
</dt> <dd>

<span data-ttu-id="4a2aa-386">[**Cim \_ HostedBootSAP**](cim-hostedbootsap.md)類別會定義 [**cim \_ BootSAP**](cim-bootsap.md)類別的裝載單一電腦系統。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-386">The [**CIM\_HostedBootSAP**](cim-hostedbootsap.md) class defines the hosting unitary computer system for a [**CIM\_BootSAP**](cim-bootsap.md) class.</span></span> <span data-ttu-id="4a2aa-387">由於此關聯性是從 [**cim \_ HostedAccessPoint**](cim-hostedaccesspoint.md)子類別化，因此它會繼承針對 [**cim \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)定義的範圍/命名配置，其中存取點會延遲至其主機系統。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-387">Since this relationship is subclassed from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md), it inherits the scoping/naming scheme defined for [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md), where an access point defers to its hosting system.</span></span> <span data-ttu-id="4a2aa-388">在此情況下， **CIM \_ BootSAP** 必須延後至其裝載的 [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-388">In this case, **CIM\_BootSAP** must defer to its hosting [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-389">**CIM \_ HostedBootService**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-389">**CIM\_HostedBootService**</span></span>](cim-hostedbootservice.md)
</dt> <dd>

<span data-ttu-id="4a2aa-390">[**CIM \_ HostedBootService**](cim-hostedbootservice.md)類別會將主機系統和開機服務產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-390">The [**CIM\_HostedBootService**](cim-hostedbootservice.md) class associates a hosting system and a boot service.</span></span> <span data-ttu-id="4a2aa-391">由於此關聯性是從 [**CIM \_ HostedService**](cim-hostedservice.md)子類別化，因此它會繼承為服務定義的範圍/命名配置，其中服務會延遲至其主機系統。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-391">Since this relationship is subclassed from [**CIM\_HostedService**](cim-hostedservice.md), it inherits the scoping/naming scheme defined for service, where a service defers to its hosting system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-392">**CIM \_ HostedFileSystem**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-392">**CIM\_HostedFileSystem**</span></span>](cim-hostedfilesystem.md)
</dt> <dd>

<span data-ttu-id="4a2aa-393">[**CIM \_ HostedFileSystem**](cim-hostedfilesystem.md)關聯代表電腦系統與電腦系統上所裝載之檔案系統之間的連結。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-393">The [**CIM\_HostedFileSystem**](cim-hostedfilesystem.md) association represents a link between the computer system and the file system hosted on the computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-394">**CIM \_ HostedJobDestination**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-394">**CIM\_HostedJobDestination**</span></span>](cim-hostedjobdestination.md)
</dt> <dd>

<span data-ttu-id="4a2aa-395">[**CIM \_ HostedJobDestination**](cim-hostedjobdestination.md)類別代表作業目的地與其所在系統之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-395">The [**CIM\_HostedJobDestination**](cim-hostedjobdestination.md) class represents an association between a job destination and the system on which it resides.</span></span> <span data-ttu-id="4a2aa-396">系統可能會裝載許多作業佇列。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-396">A system may host many job queues.</span></span> <span data-ttu-id="4a2aa-397">作業目的地會延後到裝載系統。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-397">Job destinations defer to the hosting system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-398">**CIM \_ HostedService**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-398">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dd>

<span data-ttu-id="4a2aa-399">[**CIM \_ HostedService**](cim-hostedservice.md)類別代表服務與功能所在系統之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-399">The [**CIM\_HostedService**](cim-hostedservice.md) class represents an association between a service and the system on which the functionality resides.</span></span> <span data-ttu-id="4a2aa-400">系統可能會裝載許多服務，而這些服務會延後到裝載系統。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-400">A system may host many services, which defer to the hosting system.</span></span> <span data-ttu-id="4a2aa-401">此模型不代表跨多個系統裝載的服務。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-401">The model does not represent services hosted across multiple systems.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-402">**CIM \_ InfraredController**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-402">**CIM\_InfraredController**</span></span>](cim-infraredcontroller.md)
</dt> <dd>

<span data-ttu-id="4a2aa-403">[**CIM \_ InfraredController**](cim-infraredcontroller.md)類別代表紅外線控制器的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-403">The [**CIM\_InfraredController**](cim-infraredcontroller.md) class represents the capabilities and management of an infrared controller.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-404">**CIM \_ InstalledOS**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-404">**CIM\_InstalledOS**</span></span>](cim-installedos.md)
</dt> <dd>

<span data-ttu-id="4a2aa-405">[**CIM \_ InstalledOS**](cim-installedos.md)關聯類別代表電腦系統與已安裝作業系統之間的連結。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-405">The [**CIM\_InstalledOS**](cim-installedos.md) association class represents a link between the computer system and the installed operating system.</span></span> <span data-ttu-id="4a2aa-406">作業系統會在電腦系統的儲存範圍內安裝 (例如，複製到磁片磁碟機或下載至記憶體) 。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-406">An operating system is installed when it is in a computer system's storage extent (for example, copied to a disk drive or downloaded to memory).</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-407">**CIM \_ InstalledSoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-407">**CIM\_InstalledSoftwareElement**</span></span>](cim-installedsoftwareelement.md)
</dt> <dd>

<span data-ttu-id="4a2aa-408">[**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md)類別會將電腦系統與已安裝的軟體元素建立關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-408">The [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) class associates a computer system with an installed software element.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-409">**CIM \_ IRQ**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-409">**CIM\_IRQ**</span></span>](cim-irq.md)
</dt> <dd>

<span data-ttu-id="4a2aa-410">[**CIM \_ IRQ**](cim-irq.md)類別代表 Intel 架構中斷要求線路 (IRQ) 。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-410">The [**CIM\_IRQ**](cim-irq.md) class represents an Intel architecture interrupt request line (IRQ).</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-411">**CIM \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-411">**CIM\_Job**</span></span>](cim-job.md)
</dt> <dd>

<span data-ttu-id="4a2aa-412">[**CIM \_ 作業**](cim-job.md)類別代表系統的工作單位，例如列印工作。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-412">The [**CIM\_Job**](cim-job.md) class represents a unit of work for a system, such as a print job.</span></span> <span data-ttu-id="4a2aa-413">作業與進程不同，因為可以排程工作。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-413">A job is distinct from a process because a job can be scheduled.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-414">**CIM \_ JobDestination**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-414">**CIM\_JobDestination**</span></span>](cim-jobdestination.md)
</dt> <dd>

<span data-ttu-id="4a2aa-415">[**CIM \_ JobDestination**](cim-jobdestination.md)類別代表提交工作以進行處理的位置。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-415">The [**CIM\_JobDestination**](cim-jobdestination.md) class represents where a job is submitted for processing.</span></span> <span data-ttu-id="4a2aa-416">它可以參考包含零或多個作業的佇列，例如包含列印工作的列印佇列。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-416">It can refer to a queue that contains zero or more jobs, such as a print queue containing print jobs.</span></span> <span data-ttu-id="4a2aa-417">作業目的地裝載于系統上，類似于在系統上託管服務的方式。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-417">Job destinations are hosted on systems, similar to the way in which services are hosted on systems.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-418">**CIM \_ JobDestinationJobs**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-418">**CIM\_JobDestinationJobs**</span></span>](cim-jobdestinationjobs.md)
</dt> <dd>

<span data-ttu-id="4a2aa-419">[**CIM \_ JobDestinationJobs**](cim-jobdestinationjobs.md)關聯描述提交作業以進行處理的位置， (也就是工作目的地) 。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-419">The [**CIM\_JobDestinationJobs**](cim-jobdestinationjobs.md) association describes where a job is submitted for processing (that is, to which job destination).</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-420">**CIM \_ 鍵盤**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-420">**CIM\_Keyboard**</span></span>](cim-keyboard.md)
</dt> <dd>

<span data-ttu-id="4a2aa-421">[**CIM \_ 鍵盤**](cim-keyboard.md)類別代表鍵盤邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-421">The [**CIM\_Keyboard**](cim-keyboard.md) class represents the capabilities and management of the keyboard logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-422">**CIM \_ LinkHasConnector**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-422">**CIM\_LinkHasConnector**</span></span>](cim-linkhasconnector.md)
</dt> <dd>

<span data-ttu-id="4a2aa-423">[**CIM \_ LinkHasConnector**](cim-linkhasconnector.md)類別會將用來作為實體連接器的纜線和連結（連接實體元素）相關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-423">The [**CIM\_LinkHasConnector**](cim-linkhasconnector.md) class associates cables and links used as physical connectors, which connect the physical elements.</span></span> <span data-ttu-id="4a2aa-424">此關聯會明確定義適用于 [**CIM \_ PhysicalLink**](cim-physicallink.md)之連接器的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-424">This association explicitly defines the relationship of connectors for [**CIM\_PhysicalLink**](cim-physicallink.md).</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-425">**CIM \_ LocalFileSystem**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-425">**CIM\_LocalFileSystem**</span></span>](cim-localfilesystem.md)
</dt> <dd>

<span data-ttu-id="4a2aa-426">[**CIM \_ LocalFileSystem**](cim-localfilesystem.md)類別代表由電腦系統透過本機所控制的檔案存放區，例如 (直接裝置驅動程式存取) 。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-426">The [**CIM\_LocalFileSystem**](cim-localfilesystem.md) class represents the file store controlled by a computer system through local means (for example, direct device-driver access).</span></span> <span data-ttu-id="4a2aa-427">檔案存放區可以直接由電腦系統管理，而不需要另一部電腦作為檔案伺服器。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-427">The file store can be managed directly by the computer system, without the need for another computer to act as a file server.</span></span> <span data-ttu-id="4a2aa-428">但是針對叢集檔案系統，檔案系統是本機的，因此會延遲到叢集。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-428">For a clustered file system, however, the file system is local and, therefore, defers to the cluster.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-429">**CIM \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-429">**CIM\_Location**</span></span>](cim-location.md)
</dt> <dd>

<span data-ttu-id="4a2aa-430">[**CIM \_ Location**](cim-location.md)類別代表實體元素的位置和位址。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-430">The [**CIM\_Location**](cim-location.md) class represents the position and address of a physical element.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-431">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-431">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dd>

<span data-ttu-id="4a2aa-432">[**CIM \_ LogicalDevice**](cim-logicaldevice.md)類別代表可能或可能不會在實體硬體中實現的硬體實體。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-432">The [**CIM\_LogicalDevice**](cim-logicaldevice.md) class represents a hardware entity that may or may not be realized in physical hardware.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-433">**CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-433">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dd>

<span data-ttu-id="4a2aa-434">[**CIM \_ LogicalDisk**](cim-logicaldisk.md)類別代表由檔案系統透過磁片 **DeviceID** (key) 欄位識別的連續邏輯區塊範圍。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-434">The [**CIM\_LogicalDisk**](cim-logicaldisk.md) class represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="4a2aa-435">例如，在 Windows 環境中， **DeviceID** 欄位包含磁碟機號;在 UNIX 環境中，它包含存取路徑;在 NetWare 環境中，它包含磁片區名稱。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-435">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-436">**CIM \_ LogicalDiskBasedOnPartition**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-436">**CIM\_LogicalDiskBasedOnPartition**</span></span>](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

<span data-ttu-id="4a2aa-437">[**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md)類別會將邏輯磁片與其所在的磁碟分割建立關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-437">The [**CIM\_LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) class associates a logical disk with the disk partition on which it resides.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-438">**CIM \_ LogicalDiskBasedOnVolumeSet**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-438">**CIM\_LogicalDiskBasedOnVolumeSet**</span></span>](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

<span data-ttu-id="4a2aa-439">[**CIM \_ LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md)關聯會將邏輯磁片與找到它們的磁片區相關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-439">The [**CIM\_LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md) association relates logical disks with the volume on which they are found.</span></span> <span data-ttu-id="4a2aa-440">邏輯磁片可根據單一磁片區 (例如，由軟體磁片區管理員) 或磁碟分割所公開。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-440">Logical disks can be based on a single volume (for example, exposed by a software volume manager) or a disk partition.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-441">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-441">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dd>

<span data-ttu-id="4a2aa-442">[**CIM \_ LogicalElement**](cim-logicalelement.md)類別是代表抽象系統元件的所有系統元件的基類，例如設定檔、進程或系統功能（以邏輯裝置的形式）。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-442">The [**CIM\_LogicalElement**](cim-logicalelement.md) class is the base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-443">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-443">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> <dd>

<span data-ttu-id="4a2aa-444">[**CIM \_ LogicalFile**](cim-logicalfile.md)類別代表資料的命名集合，可以是可執行程式碼，位於儲存區的檔案系統中。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-444">The [**CIM\_LogicalFile**](cim-logicalfile.md) class represents a named collection of data, which can be executable code, that is located in a file system on a storage extent.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-445">**CIM \_ LogicalIdentity**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-445">**CIM\_LogicalIdentity**</span></span>](cim-logicalidentity.md)
</dt> <dd>

<span data-ttu-id="4a2aa-446">[**CIM \_ LogicalIdentity**](cim-logicalidentity.md)類別是抽象和泛型關聯，表示兩個邏輯元素代表相同基礎實體的不同層面。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-446">The [**CIM\_LogicalIdentity**](cim-logicalidentity.md) class is an abstract and generic association that indicates that two logical elements represent different aspects of the same underlying entity.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-447">**CIM \_ MagnetoOpticalDrive**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-447">**CIM\_MagnetoOpticalDrive**</span></span>](cim-magnetoopticaldrive.md)
</dt> <dd>

<span data-ttu-id="4a2aa-448">[**CIM \_ MagnetoOpticalDrive**](cim-magnetoopticaldrive.md)類別代表磁光磁片磁碟機的功能和管理，也就是媒體存取裝置的子類型。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-448">The [**CIM\_MagnetoOpticalDrive**](cim-magnetoopticaldrive.md) class represents the capabilities and management of a magneto-optical drive, a subtype of the media access device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-449">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-449">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dd>

<span data-ttu-id="4a2aa-450">[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)類別是 system 元素階層的基類。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-450">The [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class is the base class for the system element hierarchy.</span></span> <span data-ttu-id="4a2aa-451">任何可辨別的系統元件都是包含在這個類別中的候選。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-451">Any distinguishable system component is a candidate for inclusion in this class.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-452">**CIM \_ ManagementController**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-452">**CIM\_ManagementController**</span></span>](cim-managementcontroller.md)
</dt> <dd>

<span data-ttu-id="4a2aa-453">[**CIM \_ ManagementController**](cim-managementcontroller.md)類別與管理控制器的功能和管理有關。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-453">The [**CIM\_ManagementController**](cim-managementcontroller.md) class relates to the capabilities and management of a management controller.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-454">**CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-454">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> <dd>

<span data-ttu-id="4a2aa-455">[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)類別代表存取一或多個媒體的能力，然後使用該媒體來儲存和取出資料。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-455">The [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) class represents the ability to access one or more media, and then use the media to store and retrieve data.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-456">**CIM \_ MediaPresent**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-456">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dd>

<span data-ttu-id="4a2aa-457">[**CIM \_ MediaPresent**](cim-mediapresent.md)關聯描述必須透過媒體存取裝置存取儲存區的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-457">The [**CIM\_MediaPresent**](cim-mediapresent.md) association describes a relationship where a storage extent must be accessed through a media access device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-458">**CIM \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-458">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> <dd>

<span data-ttu-id="4a2aa-459">[**CIM \_ 記憶體**](cim-memory.md)類別代表記憶體相關邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-459">The [**CIM\_Memory**](cim-memory.md) class represents the capabilities and management of memory-related logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-460">**CIM \_ MemoryCapacity**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-460">**CIM\_MemoryCapacity**</span></span>](cim-memorycapacity.md)
</dt> <dd>

<span data-ttu-id="4a2aa-461">[**CIM \_ MemoryCapacity**](cim-memorycapacity.md)類別代表可以安裝在實體元素上的記憶體，以及最小和最大的設定。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-461">The [**CIM\_MemoryCapacity**](cim-memorycapacity.md) class represents memory that can be installed on a physical element and its minimum and maximum configurations.</span></span> <span data-ttu-id="4a2aa-462">目前已安裝的記憶體和元素的最小和最大需求的資訊位於 [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) 類別的實例中。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-462">Information on memory that is currently installed and an element's minimum and maximum requirements is located in instances of the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-463">**CIM \_ MemoryCheck**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-463">**CIM\_MemoryCheck**</span></span>](cim-memorycheck.md)
</dt> <dd>

<span data-ttu-id="4a2aa-464">[**CIM \_ MemoryCheck**](cim-memorycheck.md)類別會指定系統上必須可用的最小記憶體數量的條件。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-464">The [**CIM\_MemoryCheck**](cim-memorycheck.md) class specifies a condition for the minimum amount of memory that must be available on a system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-465">**CIM \_ MemoryMappedIO**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-465">**CIM\_MemoryMappedIO**</span></span>](cim-memorymappedio.md)
</dt> <dd>

<span data-ttu-id="4a2aa-466">[**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)類別代表電腦架構記憶體對應 i/o。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-466">The [**CIM\_MemoryMappedIO**](cim-memorymappedio.md) class represents computer architecture memory-mapped I/O.</span></span> <span data-ttu-id="4a2aa-467">此類別會解決記憶體和埠 i/o 資源。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-467">This class addresses memory and port I/O resources.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-468">**CIM \_ MemoryOnCard**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-468">**CIM\_MemoryOnCard**</span></span>](cim-memoryoncard.md)
</dt> <dd>

<span data-ttu-id="4a2aa-469">[**CIM \_ MemoryOnCard**](cim-memoryoncard.md)類別會將位於主機板、介面卡等上的實體記憶體相關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-469">The [**CIM\_MemoryOnCard**](cim-memoryoncard.md) class associates physical memory located on hosting boards, adapter cards, and so on.</span></span> <span data-ttu-id="4a2aa-470">此關聯會明確定義記憶體與卡片之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-470">This association explicitly defines the relationship of memory to cards.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-471">**CIM \_ MemoryWithMedia**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-471">**CIM\_MemoryWithMedia**</span></span>](cim-memorywithmedia.md)
</dt> <dd>

<span data-ttu-id="4a2aa-472">[**CIM \_ MemoryWithMedia**](cim-memorywithmedia.md)類別會將實體記憶體與實體媒體和其墨水匣產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-472">The [**CIM\_MemoryWithMedia**](cim-memorywithmedia.md) class associates physical memory with a physical media and its cartridge.</span></span> <span data-ttu-id="4a2aa-473">記憶體會提供媒體識別，並儲存使用者專屬的資料。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-473">The memory provides media identification and stores user-specific data.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-474">**CIM \_ ModifySettingAction**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-474">**CIM\_ModifySettingAction**</span></span>](cim-modifysettingaction.md)
</dt> <dd>

<span data-ttu-id="4a2aa-475">[**CIM \_ ModifySettingAction**](cim-modifysettingaction.md)類別代表針對特定專案（具有特定值）修改特定設定檔案的資訊。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-475">The [**CIM\_ModifySettingAction**](cim-modifysettingaction.md) class represents the information for modifying a specific setting file, for a specific entry, with a specific value.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-476">**CIM \_ MonitorResolution**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-476">**CIM\_MonitorResolution**</span></span>](cim-monitorresolution.md)
</dt> <dd>

<span data-ttu-id="4a2aa-477">[**CIM \_ MonitorResolution**](cim-monitorresolution.md)類別代表水準和垂直解析度之間的關聯性，以及桌面監視器的重新整理頻率和掃描模式。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-477">The [**CIM\_MonitorResolution**](cim-monitorresolution.md) class represents the relationship between horizontal and vertical resolutions and the refresh rate and scan mode for a desktop monitor.</span></span> <span data-ttu-id="4a2aa-478">影片控制器物件中指定了值。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-478">Values are specified in the video controller object.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-479">**CIM \_ MonitorSetting**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-479">**CIM\_MonitorSetting**</span></span>](cim-monitorsetting.md)
</dt> <dd>

<span data-ttu-id="4a2aa-480">[**CIM \_ MonitorSetting**](cim-monitorsetting.md)類別會將監視器解析度與其套用的桌面監視器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-480">The [**CIM\_MonitorSetting**](cim-monitorsetting.md) class associates the monitor resolution with the desktop monitor to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-481">**CIM \_ 掛接**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-481">**CIM\_Mount**</span></span>](cim-mount.md)
</dt> <dd>

<span data-ttu-id="4a2aa-482">[**CIM \_ 裝載**](cim-mount.md)類別代表檔案系統與其附加目錄之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-482">The [**CIM\_Mount**](cim-mount.md) class represents an association between a file system and a directory to which it is attached.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-483">**CIM \_ MultiStateSensor**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-483">**CIM\_MultiStateSensor**</span></span>](cim-multistatesensor.md)
</dt> <dd>

<span data-ttu-id="4a2aa-484">[**CIM \_ MultiStateSensor**](cim-multistatesensor.md)類別代表一組二元感應器的多重成員，其中每個二進位感應器都會報告布林結果。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-484">The [**CIM\_MultiStateSensor**](cim-multistatesensor.md) class represents a multi-member set of binary sensors where each binary sensor reports a Boolean result.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-485">**CIM \_ NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-485">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> <dd>

<span data-ttu-id="4a2aa-486">[**CIM \_ NetworkAdapter**](cim-networkadapter.md)類別是一個抽象類別，用來定義一般網路硬體概念 (例如，) 的永久位址或速度。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-486">The [**CIM\_NetworkAdapter**](cim-networkadapter.md) class is an abstract class that defines general networking hardware concepts (for example, permanent address or speed of operation).</span></span> <span data-ttu-id="4a2aa-487">這項資訊是使用 [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) 關聯來傳達。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-487">The information is conveyed using the [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-488">**CIM \_ NFS**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-488">**CIM\_NFS**</span></span>](cim-nfs.md)
</dt> <dd>

<span data-ttu-id="4a2aa-489">[**CIM \_ NFS**](cim-nfs.md)類別代表從電腦系統使用網路檔案系統 (NFS) 通訊協定掛接的遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-489">The [**CIM\_NFS**](cim-nfs.md) class represents a remote file system that is mounted, using the network file system (NFS) protocol, from a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-490">**CIM \_ NonVolatileStorage**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-490">**CIM\_NonVolatileStorage**</span></span>](cim-nonvolatilestorage.md)
</dt> <dd>

<span data-ttu-id="4a2aa-491">[**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md)類別代表非暫時性儲存的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-491">The [**CIM\_NonVolatileStorage**](cim-nonvolatilestorage.md) class represents the capabilities and management of non-volatile storage.</span></span> <span data-ttu-id="4a2aa-492">靜態記憶體原生包含 flash 和 ROM 存放裝置。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-492">Nonvolatile memory natively includes flash and ROM storage.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-493">**CIM \_ NumericSensor**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-493">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> <dd>

<span data-ttu-id="4a2aa-494">[**CIM \_ NumericSensor**](cim-numericsensor.md)類別代表會傳回數值讀數並選擇性支援臨界值設定的數值感應器。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-494">The [**CIM\_NumericSensor**](cim-numericsensor.md) class represents a numeric sensor that returns numeric readings and optionally supports thresholds settings.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-495">**CIM \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-495">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> <dd>

<span data-ttu-id="4a2aa-496">[**CIM 作業系統 \_**](cim-operatingsystem.md)類別代表電腦作業系統，由軟體和固件組成，可讓電腦系統的硬體可用。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-496">The [**CIM\_OperatingSystem**](cim-operatingsystem.md) class represents a computer operating system, which is made up of software and firmware that make a computer system's hardware usable.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-497">**CIM \_ OperatingSystemSoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-497">**CIM\_OperatingSystemSoftwareFeature**</span></span>](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

<span data-ttu-id="4a2aa-498">[**CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md)類別代表組成作業系統的軟體功能。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-498">The [**CIM\_OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) class represents the software features that make up the operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-499">**CIM \_ OSProcess**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-499">**CIM\_OSProcess**</span></span>](cim-osprocess.md)
</dt> <dd>

<span data-ttu-id="4a2aa-500">[**CIM \_ OSProcess**](cim-osprocess.md)類別會將作業系統以及在作業系統環境中執行的一或多個處理常式產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-500">The [**CIM\_OSProcess**](cim-osprocess.md) class associates the operating system and one or more processes running in the context of the operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-501">**CIM \_ OSVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-501">**CIM\_OSVersionCheck**</span></span>](cim-osversioncheck.md)
</dt> <dd>

<span data-ttu-id="4a2aa-502">[**CIM \_ OSVersionCheck**](cim-osversioncheck.md)類別會指定可支援軟體元素的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-502">The [**CIM\_OSVersionCheck**](cim-osversioncheck.md) class specifies the versions of the operating system that can support a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-503">**CIM \_ PackageAlarm**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-503">**CIM\_PackageAlarm**</span></span>](cim-packagealarm.md)
</dt> <dd>

<span data-ttu-id="4a2aa-504">[**CIM \_ PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum)關聯代表將警示裝置安裝為套件一部分的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-504">The [**CIM\_PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) association represents the relationship in which an alarm device is installed as part of a package.</span></span> <span data-ttu-id="4a2aa-505">此安裝指出封裝環境的問題，也就是其安全性狀態或其整體健全狀況。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-505">The installation indicates issues with the package's environment—its security state or its overall health.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-506">**CIM \_ PackageCooling**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-506">**CIM\_PackageCooling**</span></span>](cim-packagecooling.md)
</dt> <dd>

<span data-ttu-id="4a2aa-507">[**CIM \_ PackageCooling**](cim-packagecooling.md)關聯代表在套件中安裝冷卻裝置的關聯性（例如底座或機架），以協助封裝的冷卻。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-507">The [**CIM\_PackageCooling**](cim-packagecooling.md) association represents the relationship in which a cooling device is installed in a package, such as a chassis or rack, to assist with the package's cooling.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-508">**CIM \_ PackagedComponent**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-508">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> <dd>

<span data-ttu-id="4a2aa-509">[**CIM \_ PackagedComponent**](cim-packagedcomponent.md)關聯表示一個明確的關聯性，其中元件通常包含在實體封裝中，例如底座或卡片。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-509">The [**CIM\_PackagedComponent**](cim-packagedcomponent.md) association represents an explicit relationship in which a component is typically contained by a physical package, such as a chassis or card.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-510">**CIM \_ PackageInChassis**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-510">**CIM\_PackageInChassis**</span></span>](cim-packageinchassis.md)
</dt> <dd>

<span data-ttu-id="4a2aa-511">[**CIM \_ PackageInChassis**](cim-packageinchassis.md)關聯代表底座可包含其他套件的關聯性，例如其他底座和卡片。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-511">The [**CIM\_PackageInChassis**](cim-packageinchassis.md) association represents the relationship in which a chassis can contain other packages, such as other chassis and cards.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-512">**CIM \_ PackageInSlot**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-512">**CIM\_PackageInSlot**</span></span>](cim-packageinslot.md)
</dt> <dd>

<span data-ttu-id="4a2aa-513">[**CIM \_ PackageInSlot**](cim-packageinslot.md)關聯代表裝置卡與其掛接之底座之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-513">The [**CIM\_PackageInSlot**](cim-packageinslot.md) association represents the relationship between device cards and the chassis in which they are mounted.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-514">**CIM \_ PackageTempSensor**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-514">**CIM\_PackageTempSensor**</span></span>](cim-packagetempsensor.md)
</dt> <dd>

<span data-ttu-id="4a2aa-515">[**CIM \_ PackageTempSensor**](cim-packagetempsensor.md)關聯表示通常會在套件中安裝溫度感應器的關聯性，例如底座或機架，以監視封裝的環境。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-515">The [**CIM\_PackageTempSensor**](cim-packagetempsensor.md) association represents the relationship in which a temperature sensor is often installed in a package, such as a chassis or a rack, to monitor the package's environment.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-516">**CIM \_ ParallelController**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-516">**CIM\_ParallelController**</span></span>](cim-parallelcontroller.md)
</dt> <dd>

<span data-ttu-id="4a2aa-517">[**CIM \_ ParallelController**](cim-parallelcontroller.md)關聯與平行埠邏輯裝置的功能和管理有關。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-517">The [**CIM\_ParallelController**](cim-parallelcontroller.md) association relates to the capabilities and management of the parallel port logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-518">**CIM \_ ParticipatesInSet**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-518">**CIM\_ParticipatesInSet**</span></span>](cim-participatesinset.md)
</dt> <dd>

<span data-ttu-id="4a2aa-519">[**CIM \_ ParticipatesInSet**](cim-participatesinset.md)類別會識別應該一起取代的實體元素。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-519">The [**CIM\_ParticipatesInSet**](cim-participatesinset.md) class identifies physical elements that should be replaced together.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-520">**CIM \_ PCIController**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-520">**CIM\_PCIController**</span></span>](cim-pcicontroller.md)
</dt> <dd>

<span data-ttu-id="4a2aa-521">[**CIM \_ PCIController**](cim-pcicontroller.md)類別代表 PCI 控制器的屬性和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-521">The [**CIM\_PCIController**](cim-pcicontroller.md) class represents the properties and management of a PCI controller.</span></span> <span data-ttu-id="4a2aa-522">此類別中的屬性及其子類別會定義于 PCI SIG 所發佈的各種 PCI 規格中。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-522">The properties in this class and its subclasses are defined in the various PCI specifications published by the PCI SIG.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-523">**CIM \_ PCMCIAController**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-523">**CIM\_PCMCIAController**</span></span>](cim-pcmciacontroller.md)
</dt> <dd>

<span data-ttu-id="4a2aa-524">[**CIM \_ PCMCIAController**](cim-pcmciacontroller.md)類別代表個人電腦記憶卡國際協會 (PCMCIA) 控制器的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-524">The [**CIM\_PCMCIAController**](cim-pcmciacontroller.md) class represents the capabilities and management of a Personal Computer Memory Card International Association (PCMCIA) controller.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-525">**CIM \_ PCVideoController**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-525">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> <dd>

<span data-ttu-id="4a2aa-526">[**CIM \_ PCVideoController**](cim-pcvideocontroller.md)代表個人電腦影片控制器的功能和管理，也就是影片控制器的子類型。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-526">The [**CIM\_PCVideoController**](cim-pcvideocontroller.md) represents the capabilities and management of a personal computer video controller, a subtype of a video controller.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-527">**CIM \_ PExtentRedundancyComponent**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-527">**CIM\_PExtentRedundancyComponent**</span></span>](cim-pextentredundancycomponent.md)
</dt> <dd>

<span data-ttu-id="4a2aa-528">[**CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md)類別代表參與儲存體冗余群組的實體範圍。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-528">The [**CIM\_PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) class represents the physical extents that participate in a storage redundancy group.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-529">**CIM \_ PhysicalCapacity**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-529">**CIM\_PhysicalCapacity**</span></span>](cim-physicalcapacity.md)
</dt> <dd>

<span data-ttu-id="4a2aa-530">[**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md)類別是一種抽象類別，代表實體元素的最小和最大需求，以及其支援不同硬體類型的能力。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-530">The [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) class is an abstract class that represents a physical element's minimum and maximum requirements and its ability to support different types of hardware.</span></span> <span data-ttu-id="4a2aa-531">例如，最小和最大記憶體需求可以模型化為 **CIM \_ PhysicalCapacity** 的子類別。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-531">For example, minimum and maximum memory requirements can be modeled as a subclass of **CIM\_PhysicalCapacity**.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-532">**CIM \_ PhysicalComponent**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-532">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> <dd>

<span data-ttu-id="4a2aa-533">[**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)類別代表封裝內的低層級或基本元件。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-533">The [**CIM\_PhysicalComponent**](cim-physicalcomponent.md) class represents a low-level or basic component within a package.</span></span> <span data-ttu-id="4a2aa-534">不是連結、連接器或封裝的實體元素是此類別 (或成員) 的子系。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-534">A physical element that is not a link, connector, or package is a descendant (or member) of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-535">**CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-535">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> <dd>

<span data-ttu-id="4a2aa-536">[**CIM \_ PhysicalConnector**](cim-physicalconnector.md)類別代表用來連接到其他元素的任何實體元素。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-536">The [**CIM\_PhysicalConnector**](cim-physicalconnector.md) class represents any physical element that is used to connect to other elements.</span></span> <span data-ttu-id="4a2aa-537">任何可以連接及傳輸兩個或多個實體元素之間的信號或電源的物件，都是此類別的子系 (或成員) 。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-537">Any object that can connect and transmit signals or power between two or more physical elements is a descendant (or member) of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-538">**CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-538">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> <dd>

<span data-ttu-id="4a2aa-539">[**CIM \_ PhysicalElement**](cim-physicalelement.md)子類別會定義具有不同實體身分識別之系統的任何元件。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-539">The [**CIM\_PhysicalElement**](cim-physicalelement.md) subclasses define any component of a system that has a distinct physical identity.</span></span> <span data-ttu-id="4a2aa-540">可以實體附加至物件的標籤可以定義這個類別的實例。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-540">Instances of this class can be defined in terms of labels that can be physically attached to the object.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-541">**CIM \_ PhysicalElementLocation**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-541">**CIM\_PhysicalElementLocation**</span></span>](cim-physicalelementlocation.md)
</dt> <dd>

<span data-ttu-id="4a2aa-542">[**Cim \_ PhysicalElementLocation**](cim-physicalelementlocation.md)類別會將實體元素與 [**CIM \_ 位置**](cim-location.md)物件產生關聯，以供清查或取代之用。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-542">The [**CIM\_PhysicalElementLocation**](cim-physicalelementlocation.md) class associates a physical element with a [**CIM\_Location**](cim-location.md) object for inventory or replacement purposes.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-543">**CIM \_ PhysicalExtent**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-543">**CIM\_PhysicalExtent**</span></span>](cim-physicalextent.md)
</dt> <dd>

<span data-ttu-id="4a2aa-544">[**CIM \_ PhysicalExtent**](cim-physicalextent.md)類別代表 SCC RAID 的執行。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-544">The [**CIM\_PhysicalExtent**](cim-physicalextent.md) class represents an SCC RAID implementation.</span></span> <span data-ttu-id="4a2aa-545">它會在單一存放裝置上定義連續可定址的區塊位址，這些位址會被視為相同 [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) 類別中的單一儲存區。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-545">It defines the consecutive addressable block addresses on a single storage device that are treated as a single storage extent in the same [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class.</span></span> <span data-ttu-id="4a2aa-546">替代方式是使用自動設定時，是要具現化或擴充 [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-546">An alternative, when automatic configuration is used, is to instantiate or extend the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-547">**CIM \_ PhysicalFrame**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-547">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> <dd>

<span data-ttu-id="4a2aa-548">[**CIM \_ PhysicalFrame**](cim-physicalframe.md)類別是機架、底座和其他框架主機殼的父類別，因為它們是在擴充類別中定義的。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-548">The [**CIM\_PhysicalFrame**](cim-physicalframe.md) class is a parent class of rack, chassis, and other frame enclosures as they are defined in extension classes.</span></span> <span data-ttu-id="4a2aa-549">**VisibleAlarm** 和 **AudibleAlarm** 等屬性，以及與安全性缺口相關的資料會包含在這個父類別中。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-549">Properties such as **VisibleAlarm** and **AudibleAlarm**, and data related to security breaches are included in this parent class.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-550">**CIM \_ PhysicalLink**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-550">**CIM\_PhysicalLink**</span></span>](cim-physicallink.md)
</dt> <dd>

<span data-ttu-id="4a2aa-551">[**CIM \_ PhysicalLink**](cim-physicallink.md)類別代表實體元素的纜線。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-551">The [**CIM\_PhysicalLink**](cim-physicallink.md) class represents the cabling of physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-552">**CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-552">**CIM\_PhysicalMedia**</span></span>](cim-physicalmedia.md)
</dt> <dd>

<span data-ttu-id="4a2aa-553">[**CIM \_ PhysicalMedia**](cim-physicalmedia.md)類別代表檔和儲存媒體的類型，例如磁帶、CD rom 等等。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-553">The [**CIM\_PhysicalMedia**](cim-physicalmedia.md) class represents types of documentation and storage medium, such as tapes, CD ROMs, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-554">**CIM \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-554">**CIM\_PhysicalMemory**</span></span>](cim-physicalmemory.md)
</dt> <dd>

<span data-ttu-id="4a2aa-555">[**CIM \_ PhysicalMemory**](cim-physicalmemory.md)類別代表低層級的記憶體裝置，例如 simm、dimm、原始記憶體晶片等等。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-555">The [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class represents low-level memory devices, such as SIMMS, DIMMs, raw memory chips, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-556">**CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-556">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> <dd>

<span data-ttu-id="4a2aa-557">[**CIM \_ PhysicalPackage**](cim-physicalpackage.md)類別代表包含或裝載其他元件的實體元素。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-557">The [**CIM\_PhysicalPackage**](cim-physicalpackage.md) class represents physical elements that contain or host other components.</span></span> <span data-ttu-id="4a2aa-558">範例包括機架主機殼或介面卡。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-558">Examples are a rack enclosure or an adapter card.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-559">**CIM \_ PointingDevice**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-559">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dd>

<span data-ttu-id="4a2aa-560">[**CIM \_ PointingDevice**](cim-pointingdevice.md)類別代表指向顯示區域的裝置。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-560">The [**CIM\_PointingDevice**](cim-pointingdevice.md) class represents a device that points to regions on the display.</span></span> <span data-ttu-id="4a2aa-561">任何操作指標的裝置，或指向視覺效果顯示器上的區域，都是此類別的成員。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-561">Any device that manipulates a pointer, or points to regions on a visual display, is a member of this class.</span></span> <span data-ttu-id="4a2aa-562">例如，滑鼠、手寫筆、觸控板或平板電腦。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-562">For example, a mouse, stylus, touch pad, or tablet.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-563">**CIM \_ POTSModem**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-563">**CIM\_POTSModem**</span></span>](cim-potsmodem.md)
</dt> <dd>

<span data-ttu-id="4a2aa-564">[**CIM \_ POTSModem**](cim-potsmodem.md)類別代表一種裝置，可透過連接到單純的舊電話系統 (POTS) 網路，將二進位資料轉譯成 wave modulations 進行音效型傳輸。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-564">The [**CIM\_POTSModem**](cim-potsmodem.md) class represents a device that translates binary data into wave modulations for sound-based transmission by connecting to the Plain Old Telephone System (POTS) network.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-565">**CIM \_ 電源**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-565">**CIM\_PowerSupply**</span></span>](cim-powersupply.md)
</dt> <dd>

<span data-ttu-id="4a2aa-566">[**CIM 電源 \_ 供應器**](cim-powersupply.md)類別代表電源供應器邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-566">The [**CIM\_PowerSupply**](cim-powersupply.md) class represents the capabilities and management of the power supply logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-567">**CIM \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-567">**CIM\_Printer**</span></span>](cim-printer.md)
</dt> <dd>

<span data-ttu-id="4a2aa-568">[**CIM \_ 印表機**](cim-printer.md)類別代表印表機邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-568">The [**CIM\_Printer**](cim-printer.md) class represents the capabilities and management of the printer logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-569">**CIM \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-569">**CIM\_Process**</span></span>](cim-process.md)
</dt> <dd>

<span data-ttu-id="4a2aa-570">[**CIM \_ 進程**](cim-process.md)類別代表執行中程式的單一實例。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-570">The [**CIM\_Process**](cim-process.md) class represents a single instance of a running program.</span></span> <span data-ttu-id="4a2aa-571">使用者通常會將進程視為應用程式或工作。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-571">A user typically sees a process as an application or task.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-572">**CIM \_ ProcessExecutable**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-572">**CIM\_ProcessExecutable**</span></span>](cim-processexecutable.md)
</dt> <dd>

<span data-ttu-id="4a2aa-573">[**CIM \_ ProcessExecutable**](cim-processexecutable.md)類別代表進程和資料檔之間的連結，表示檔案參與處理常式的執行。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-573">The [**CIM\_ProcessExecutable**](cim-processexecutable.md) class represents a link between a process and data file, and indicates that the file participates in the execution of the process.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-574">**CIM \_ 處理器**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-574">**CIM\_Processor**</span></span>](cim-processor.md)
</dt> <dd>

<span data-ttu-id="4a2aa-575">[**CIM \_ 處理器**](cim-processor.md)類別代表處理器邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-575">The [**CIM\_Processor**](cim-processor.md) class represents the capabilities and management of the processor logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-576">**CIM \_ ProcessThread**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-576">**CIM\_ProcessThread**</span></span>](cim-processthread.md)
</dt> <dd>

<span data-ttu-id="4a2aa-577">[**CIM \_ ProcessThread**](cim-processthread.md)類別代表進程與進程內容中執行之執行緒之間的連結。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-577">The [**CIM\_ProcessThread**](cim-processthread.md) class represents a link between a process and the threads running in the context of the process.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-578">**CIM \_ 產品**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-578">**CIM\_Product**</span></span>](cim-product.md)
</dt> <dd>

<span data-ttu-id="4a2aa-579">[**CIM \_ Product**](cim-product.md)類別是代表實體元素集合、軟體功能和其他產品（以單位形式取得）的實體類別。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-579">The [**CIM\_Product**](cim-product.md) class is a concrete class that represents a collection of physical elements, software features and, other products, acquired as a unit.</span></span> <span data-ttu-id="4a2aa-580">取得意味著供應商與消費者之間的合約，可能會影響產品授權、支援和擔保。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-580">Acquisition implies an agreement between the supplier and consumer, which can have implications on product licensing, support, and warranty.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-581">**CIM \_ ProductFRU**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-581">**CIM\_ProductFRU**</span></span>](cim-productfru.md)
</dt> <dd>

<span data-ttu-id="4a2aa-582">[**CIM \_ ProductFRU**](cim-productfru.md)類別代表產品與現場可更換單元之間的關聯 (FRU) ，其提供已被取代之產品元件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-582">The [**CIM\_ProductFRU**](cim-productfru.md) class represents an association between the product and a field replaceable unit (FRU), which provides information about product components that have been, or are being replaced.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-583">**CIM \_ ProductParentChild**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-583">**CIM\_ProductParentChild**</span></span>](cim-productparentchild.md)
</dt> <dd>

<span data-ttu-id="4a2aa-584">[**CIM \_ ProductParentChild**](cim-productparentchild.md)關聯會定義產品之間的父子式階層。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-584">The [**CIM\_ProductParentChild**](cim-productparentchild.md) association defines a parent-child hierarchy among products.</span></span> <span data-ttu-id="4a2aa-585">例如，產品可以與其他產品配套。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-585">For example, a product can come bundled with other products.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-586">**CIM \_ ProductPhysicalElements**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-586">**CIM\_ProductPhysicalElements**</span></span>](cim-productphysicalelements.md)
</dt> <dd>

<span data-ttu-id="4a2aa-587">[**CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md)類別代表組成產品的實體元素。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-587">The [**CIM\_ProductPhysicalElements**](cim-productphysicalelements.md) class represents the physical elements that make up a product.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-588">**CIM \_ ProductProductDependency**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-588">**CIM\_ProductProductDependency**</span></span>](cim-productproductdependency.md)
</dt> <dd>

<span data-ttu-id="4a2aa-589">[**CIM \_ ProductProductDependency**](cim-productproductdependency.md)類別代表兩項產品之間的關聯，這表示必須安裝或不存在才能讓另一個產品運作。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-589">The [**CIM\_ProductProductDependency**](cim-productproductdependency.md) class represents an association between two products, which indicates that one must be installed or absent for the other to function.</span></span> <span data-ttu-id="4a2aa-590">這在概念上相當於 [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) 關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-590">This is conceptually equivalent to the [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-591">**CIM \_ ProductSoftwareFeatures**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-591">**CIM\_ProductSoftwareFeatures**</span></span>](cim-productsoftwarefeatures.md)
</dt> <dd>

<span data-ttu-id="4a2aa-592">[**CIM \_ ProductSoftwareFeatures**](cim-productsoftwarefeatures.md)關聯會識別特定產品的軟體功能。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-592">The [**CIM\_ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) association identifies the software features for a particular product.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-593">**CIM \_ ProductSupport**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-593">**CIM\_ProductSupport**</span></span>](cim-productsupport.md)
</dt> <dd>

<span data-ttu-id="4a2aa-594">[**CIM \_ ProductSupport**](cim-productsupport.md)類別代表產品與支援存取之間的關聯，可傳達如何取得產品的支援。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-594">The [**CIM\_ProductSupport**](cim-productsupport.md) class represents an association between product and support access that conveys how support is obtained for the product.</span></span> <span data-ttu-id="4a2aa-595">產品有各種類型的支援，相同的支持對象可以提供多項產品的協助。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-595">Various types of support are available for a product; the same support object can provide assistance for multiple products.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-596">**CIM \_ ProtectedSpaceExtent**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-596">**CIM\_ProtectedSpaceExtent**</span></span>](cim-protectedspaceextent.md)
</dt> <dd>

<span data-ttu-id="4a2aa-597">[**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md)類別代表可定址的邏輯區塊位址，這些位址會被視為單一儲存範圍，但位於單一實體範圍。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-597">The [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) class represents addressable logical-block addresses, which are treated as a single storage extent, but are located on a single physical extent.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-598">**CIM \_ PSExtentBasedOnPExtent**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-598">**CIM\_PSExtentBasedOnPExtent**</span></span>](cim-psextentbasedonpextent.md)
</dt> <dd>

<span data-ttu-id="4a2aa-599">[**CIM \_ PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md)類別會將以實體範圍為基礎的受保護空間範圍產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-599">The [**CIM\_PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md) class associates protected space extents that are based on a physical extent.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-600">**CIM \_ 機架**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-600">**CIM\_Rack**</span></span>](cim-rack.md)
</dt> <dd>

<span data-ttu-id="4a2aa-601">[**CIM \_ 機架**](cim-rack.md)類別代表機架 (實體框架或主機殼) 在其中儲存底座。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-601">The [**CIM\_Rack**](cim-rack.md) class represents a rack (a physical frame or enclosure) in which chassis are stored.</span></span> <span data-ttu-id="4a2aa-602">通常，機架代表主機殼;所有運作中的元件都會封裝在底座中。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-602">Typically, a rack represents the enclosure; all functioning components are packaged in the chassis.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-603">**CIM \_ 意識**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-603">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dd>

<span data-ttu-id="4a2aa-604">[**CIM \_ 認識**](cim-realizes.md)類別代表定義邏輯裝置與執行裝置之實體元件之間對應的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-604">The [**CIM\_Realizes**](cim-realizes.md) class represents the association that defines the mapping between a logical device and the physical component that implements the device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-605">**CIM \_ RealizesAggregatePExtent**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-605">**CIM\_RealizesAggregatePExtent**</span></span>](cim-realizesaggregatepextent.md)
</dt> <dd>

<span data-ttu-id="4a2aa-606">[**Cim \_ RealizesAggregatePExtent**](cim-realizesaggregatepextent.md)關聯表示在實體媒體上實現 [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md)類別的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-606">The [**CIM\_RealizesAggregatePExtent**](cim-realizesaggregatepextent.md) association represents the relationship in which the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class is realized on a physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-607">**CIM \_ RealizesDiskPartition**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-607">**CIM\_RealizesDiskPartition**</span></span>](cim-realizesdiskpartition.md)
</dt> <dd>

<span data-ttu-id="4a2aa-608">[**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md)類別代表實體媒體上的磁碟分割，此磁碟分割會建立原始 SCSI 或 IDE 磁片磁碟機上磁碟分割的建立模型。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-608">The [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) class represents a disk partition on a physical media that models the creation of partitions on a raw SCSI or IDE drive.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-609">**CIM \_ RealizesPExtent**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-609">**CIM\_RealizesPExtent**</span></span>](cim-realizespextent.md)
</dt> <dd>

<span data-ttu-id="4a2aa-610">[**CIM \_ RealizesPExtent**](cim-realizespextent.md)關聯表示在實體媒體上實現實體範圍的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-610">The [**CIM\_RealizesPExtent**](cim-realizespextent.md) association represents the relationship in which physical extents are realized on a physical media.</span></span> <span data-ttu-id="4a2aa-611">此外，也會指定實體媒體上實體範圍的起始位址。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-611">In addition, the starting address of the physical extent on the physical media is specified.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-612">**CIM \_ RebootAction**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-612">**CIM\_RebootAction**</span></span>](cim-rebootaction.md)
</dt> <dd>

<span data-ttu-id="4a2aa-613">[**CIM \_ RebootAction**](cim-rebootaction.md)類別會導致系統重新開機，其中安裝了 software 元素。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-613">The [**CIM\_RebootAction**](cim-rebootaction.md) class causes a system reboot where the software element is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-614">**CIM \_ RedundancyComponent**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-614">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> <dd>

<span data-ttu-id="4a2aa-615">[**CIM \_ RedundancyComponent**](cim-redundancycomponent.md)類別會將由受管理系統專案組成的複製群組產生關聯，並指出這些元素一起提供冗余。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-615">The [**CIM\_RedundancyComponent**](cim-redundancycomponent.md) class associates a redundancy group composed of managed system elements and indicates that, together, the elements provide redundancy.</span></span> <span data-ttu-id="4a2aa-616">在冗余群組中匯總的所有元素都應該是相同物件類別的具現化。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-616">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-617">**CIM \_ RedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-617">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> <dd>

<span data-ttu-id="4a2aa-618">[**CIM \_ RedundancyGroup**](cim-redundancygroup.md)類別代表 managed 系統專案的集合，這些元素表示匯總的元件會一起提供冗余。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-618">The [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class represents a collection of managed system elements, which indicates that the aggregated components, together, provide redundancy.</span></span> <span data-ttu-id="4a2aa-619">在冗余群組中匯總的所有元素都應該是相同物件類別的具現化。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-619">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-620">**CIM \_ 冷藏庫取出**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-620">**CIM\_Refrigeration**</span></span>](cim-refrigeration.md)
</dt> <dd>

<span data-ttu-id="4a2aa-621">[**CIM \_ 冷藏庫取出**](cim-refrigeration.md)類別代表冷藏庫取出冷卻裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-621">The [**CIM\_Refrigeration**](cim-refrigeration.md) class represents the capabilities and management of a refrigeration cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-622">**CIM \_ RelatedStatistics**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-622">**CIM\_RelatedStatistics**</span></span>](cim-relatedstatistics.md)
</dt> <dd>

<span data-ttu-id="4a2aa-623">[**Cim \_ RelatedStatistics**](cim-relatedstatistics.md)關聯表示階層以及相關 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)類別的相依性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-623">The [**CIM\_RelatedStatistics**](cim-relatedstatistics.md) association represents hierarchies and dependencies of related [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) classes.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-624">**CIM \_ RemoteFileSystem**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-624">**CIM\_RemoteFileSystem**</span></span>](cim-remotefilesystem.md)
</dt> <dd>

<span data-ttu-id="4a2aa-625">[**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md)類別代表透過網路相關服務來存取的遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-625">The [**CIM\_RemoteFileSystem**](cim-remotefilesystem.md) class represents a remote file system that is accessed by way of a network-related service.</span></span> <span data-ttu-id="4a2aa-626">在此情況下，檔案存放區是由電腦主控，作為檔案伺服器。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-626">In this case, the file store is hosted by a computer, which acts as a file server.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-627">**CIM \_ RemoveDirectoryAction**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-627">**CIM\_RemoveDirectoryAction**</span></span>](cim-removedirectoryaction.md)
</dt> <dd>

<span data-ttu-id="4a2aa-628">[**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md)類別會移除軟體元素的目錄。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-628">The [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class removes directories for software elements.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-629">**CIM \_ RemoveFileAction**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-629">**CIM\_RemoveFileAction**</span></span>](cim-removefileaction.md)
</dt> <dd>

<span data-ttu-id="4a2aa-630">[**CIM \_ RemoveFileAction**](cim-removefileaction.md)類別會卸載檔案。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-630">The [**CIM\_RemoveFileAction**](cim-removefileaction.md) class uninstalls files.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-631">**CIM \_ ReplacementSet**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-631">**CIM\_ReplacementSet**</span></span>](cim-replacementset.md)
</dt> <dd>

<span data-ttu-id="4a2aa-632">[**CIM \_ ReplacementSet**](cim-replacementset.md)類別會匯總必須一起取代的實體元素。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-632">The [**CIM\_ReplacementSet**](cim-replacementset.md) class aggregates physical elements that must be replaced together.</span></span> <span data-ttu-id="4a2aa-633">例如，更換記憶卡時，也可以移除並取代元件記憶體晶片。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-633">For example, when replacing a memory card, the component memory chips can also be removed and replaced.</span></span> <span data-ttu-id="4a2aa-634">或者，這個關聯可以用來取代或升級一組記憶體晶片。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-634">Or, this association can be used to replace or upgrade a set of memory chips.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-635">**CIM \_ ResidesOnExtent**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-635">**CIM\_ResidesOnExtent**</span></span>](cim-residesonextent.md)
</dt> <dd>

<span data-ttu-id="4a2aa-636">[**CIM \_ ResidesOnExtent**](cim-residesonextent.md)類別代表檔案系統與其所在儲存區之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-636">The [**CIM\_ResidesOnExtent**](cim-residesonextent.md) class represents an association between a file system and the storage extent where it is located.</span></span> <span data-ttu-id="4a2aa-637">一般而言，檔案系統位於邏輯磁片上。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-637">Typically, a file system resides on a logical disk.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-638">**CIM \_ RunningOS**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-638">**CIM\_RunningOS**</span></span>](cim-runningos.md)
</dt> <dd>

<span data-ttu-id="4a2aa-639">[**CIM \_ RunningOS**](cim-runningos.md)類別代表目前正在執行的作業系統。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-639">The [**CIM\_RunningOS**](cim-runningos.md) class represents the currently executing operating system.</span></span> <span data-ttu-id="4a2aa-640">電腦系統上的任何時間最多可以執行一個作業系統;電腦系統目前可能無法開機，或其作業系統可能不明。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-640">At most, one operating system can execute at any time on a computer system; the computer system may not be currently booted, or its operating system may be unknown.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-641">**CIM \_ SAPSAPDependency**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-641">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> <dd>

<span data-ttu-id="4a2aa-642">[**CIM \_ SAPSAPDependency**](cim-sapsapdependency.md)類別是 (sap) 的兩個服務存取點之間的關聯，這表示第一個 sap 需要第二個 sap 才能與其服務連接。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-642">The [**CIM\_SAPSAPDependency**](cim-sapsapdependency.md) class is an association between two service access points (SAPs), which indicates that the second SAP is required for the first SAP to connect with its service.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-643">**CIM \_ 掃描器**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-643">**CIM\_Scanner**</span></span>](cim-scanner.md)
</dt> <dd>

<span data-ttu-id="4a2aa-644">[**CIM \_ 掃描器**](cim-scanner.md)代表掃描器邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-644">The [**CIM\_Scanner**](cim-scanner.md) represents the capabilities and management of the scanner logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-645">**CIM \_ microsoft.hyperv.powershell.scsicontroller**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-645">**CIM\_SCSIController**</span></span>](cim-scsicontroller.md)
</dt> <dd>

<span data-ttu-id="4a2aa-646">[**CIM \_ microsoft.hyperv.powershell.scsicontroller**](cim-scsicontroller.md)類別代表 SCSI 控制器邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-646">The [**CIM\_SCSIController**](cim-scsicontroller.md) class represents the capabilities and management of the SCSI controller logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-647">**CIM \_ SCSIInterface**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-647">**CIM\_SCSIInterface**</span></span>](cim-scsiinterface.md)
</dt> <dd>

<span data-ttu-id="4a2aa-648">代表 [**CIM \_ ControlledBy**](cim-controlledby.md) 關聯性，指出哪些裝置可透過 SCSI 控制器和存取特性來存取。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-648">represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through a SCSI controller and the access characteristics.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-649">**CIM \_ 感應器**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-649">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> <dd>

<span data-ttu-id="4a2aa-650">[**CIM \_ 感應器**](cim-sensor.md)類別代表能夠測量實體屬性特性的硬體裝置 (例如，單一電腦系統) 的溫度或電壓特性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-650">The [**CIM\_Sensor**](cim-sensor.md) class represents a hardware device that is capable of measuring the characteristics of a physical property (for example, the temperature or voltage characteristics of a unitary computer system).</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-651">**CIM \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-651">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dd>

<span data-ttu-id="4a2aa-652">[**CIM \_ SerialController**](cim-serialcontroller.md)類別代表序列埠邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-652">The [**CIM\_SerialController**](cim-serialcontroller.md) class represents the capabilities and management of the serial port logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-653">**CIM \_ SerialInterface**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-653">**CIM\_SerialInterface**</span></span>](cim-serialinterface.md)
</dt> <dd>

<span data-ttu-id="4a2aa-654">[**Cim \_ SerialInterface**](cim-serialinterface.md)類別代表 [**cim \_ ControlledBy**](cim-controlledby.md)關聯性，指出哪些裝置可透過序列控制器存取，以及存取的特性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-654">The [**CIM\_SerialInterface**](cim-serialinterface.md) class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through the serial controller and the characteristics of the access.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-655">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-655">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dd>

<span data-ttu-id="4a2aa-656">[**CIM \_ 服務**](cim-service.md)類別代表邏輯元素，其中包含的資訊可代表和管理裝置或軟體功能所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-656">The [**CIM\_Service**](cim-service.md) class represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="4a2aa-657">服務是一般用途的物件，用來設定及管理功能的執行;這並不是功能本身。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-657">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-658">**CIM \_ ServiceAccessBySAP**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-658">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="4a2aa-659">[**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md)關聯類別代表服務的存取點。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-659">The [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md) association class represents the access points for a service.</span></span> <span data-ttu-id="4a2aa-660">例如，您可以透過 NetWare、Macintosh 或 Windows 服務存取點來存取印表機 (Sap) ，這些都可能裝載在不同的系統上。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-660">For example, a printer can be accessed by NetWare, Macintosh, or Windows service access points (SAPs), which are potentially hosted on different systems.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-661">**CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-661">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> <dd>

<span data-ttu-id="4a2aa-662">[**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)類別代表使用或叫用服務的能力。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-662">The [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) class represents the ability to use or invoke a service.</span></span> <span data-ttu-id="4a2aa-663">存取點代表可供其他實體使用的服務。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-663">Access points represent services that are available for use by other entities.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-664">**CIM \_ ServiceSAPDependency**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-664">**CIM\_ServiceSAPDependency**</span></span>](cim-servicesapdependency.md)
</dt> <dd>

<span data-ttu-id="4a2aa-665">[**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md)類別代表服務與服務存取點之間的關聯 (SAP) ，這表示服務會使用參考的 SAP 來提供其功能。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-665">The [**CIM\_ServiceSAPDependency**](cim-servicesapdependency.md) class represents an association between a service and a service access point (SAP), which indicates that the referenced SAP is used by the service to provide its functionality.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-666">**CIM \_ ServiceServiceDependency**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-666">**CIM\_ServiceServiceDependency**</span></span>](cim-serviceservicedependency.md)
</dt> <dd>

<span data-ttu-id="4a2aa-667">[**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md)類別代表兩個服務之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-667">The [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) class represents an association between two services.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-668">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-668">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dd>

<span data-ttu-id="4a2aa-669">[**CIM \_ 設定**](cim-setting.md)類別代表一或多個受管理系統元素的設定相關和指令引數。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-669">The [**CIM\_Setting**](cim-setting.md) class represents configuration-related and operational parameters for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-670">**CIM \_ SettingCheck**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-670">**CIM\_SettingCheck**</span></span>](cim-settingcheck.md)
</dt> <dd>

<span data-ttu-id="4a2aa-671">[**CIM \_ SettingCheck**](cim-settingcheck.md)類別會指定針對包含值等於指定值的特定專案檢查特定設定檔案所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-671">The [**CIM\_SettingCheck**](cim-settingcheck.md) class specifies information needed to check a particular setting file for a specific entry that contains a value equal to the value specified.</span></span> <span data-ttu-id="4a2aa-672">所有的比較都會假設為不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-672">All comparisons are assumed to be case insensitive.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-673">**CIM \_ SettingCoNtext**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-673">**CIM\_SettingContext**</span></span>](cim-settingcontext.md)
</dt> <dd>

<span data-ttu-id="4a2aa-674">[**CIM \_ SettingCoNtext**](cim-settingcontext.md)類別會將設定物件與設定物件建立關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-674">The [**CIM\_SettingContext**](cim-settingcontext.md) class associates configuration objects with setting objects.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-675">**CIM \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-675">**CIM\_Slot**</span></span>](cim-slot.md)
</dt> <dd>

<span data-ttu-id="4a2aa-676">[**CIM 位置 \_**](cim-slot.md)類別代表要插入封裝的連接器。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-676">The [**CIM\_Slot**](cim-slot.md) class represents connectors into which packages are inserted.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-677">**CIM \_ SlotInSlot**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-677">**CIM\_SlotInSlot**</span></span>](cim-slotinslot.md)
</dt> <dd>

<span data-ttu-id="4a2aa-678">[**CIM \_ SlotInSlot**](cim-slotinslot.md)關聯性代表特殊介面卡擴充現有插槽結構的能力，以啟用其他不相容的卡片來插入框架或主控面板。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-678">The [**CIM\_SlotInSlot**](cim-slotinslot.md) relationship represents the ability of a special adapter to extend the existing slot structure to enable otherwise incompatible cards to be plugged into a frame or hosting board.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-679">**CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-679">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> <dd>

<span data-ttu-id="4a2aa-680">[**Cim \_ SoftwareElement**](cim-softwareelement.md)類別會將 [**cim \_ SoftwareFeature**](cim-softwarefeature.md)物件分解至特定平臺的一組個別可管理或可部署的元件中。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-680">The [**CIM\_SoftwareElement**](cim-softwareelement.md) class decomposes a [**CIM\_SoftwareFeature**](cim-softwarefeature.md) object into a set of individually manageable or deployable parts for a particular platform.</span></span> <span data-ttu-id="4a2aa-681">軟體專案的平臺是由其基礎硬體架構和作業系統來唯一識別。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-681">A software element's platform is uniquely identified by its underlying hardware architecture and operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-682">**CIM \_ SoftwareElementActions**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-682">**CIM\_SoftwareElementActions**</span></span>](cim-softwareelementactions.md)
</dt> <dd>

<span data-ttu-id="4a2aa-683">[**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md)關聯會識別 software 元素的動作。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-683">The [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association identifies the actions for a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-684">**CIM \_ SoftwareElementChecks**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-684">**CIM\_SoftwareElementChecks**</span></span>](cim-softwareelementchecks.md)
</dt> <dd>

<span data-ttu-id="4a2aa-685">[**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md)關聯類別會將 software 元素與功能可能需要的條件或位置資訊產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-685">The [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association class relates a software element with condition or location information that a feature may require.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-686">**CIM \_ SoftwareElementVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-686">**CIM\_SoftwareElementVersionCheck**</span></span>](cim-softwareelementversioncheck.md)
</dt> <dd>

<span data-ttu-id="4a2aa-687">[**CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md)類別代表必須存在於環境中的 software 元素類型。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-687">The [**CIM\_SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) class represents a type of software element that must exist in the environment.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-688">**CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-688">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> <dd>

<span data-ttu-id="4a2aa-689">[**CIM \_ SoftwareFeature**](cim-softwarefeature.md)類別代表產品或應用程式系統的特定功能或功能。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-689">The [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class represents a particular function or capability of a product or application system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-690">**CIM \_ SoftwareFeatureSAPImplementation**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-690">**CIM\_SoftwareFeatureSAPImplementation**</span></span>](cim-softwarefeaturesapimplementation.md)
</dt> <dd>

<span data-ttu-id="4a2aa-691">[**CIM \_ SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md)類別代表服務存取點之間的關聯 (SAP) 以及如何在軟體中執行。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-691">The [**CIM\_SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) class represents an association between a service access point (SAP) and how it is implemented in software.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-692">**CIM \_ SoftwareFeatureServiceImplementation**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-692">**CIM\_SoftwareFeatureServiceImplementation**</span></span>](cim-softwarefeatureserviceimplementation.md)
</dt> <dd>

<span data-ttu-id="4a2aa-693">[**CIM \_ SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md)類別代表服務之間的關聯，以及它在軟體中的執行方式。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-693">The [**CIM\_SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) class represents an association between a service and how it is implemented in software.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-694">**CIM \_ SoftwareFeatureSoftwareElements**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-694">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> <dd>

<span data-ttu-id="4a2aa-695">[**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md)關聯會識別組成特定軟體功能的軟體元素。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-695">The [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) association identifies the software elements that make up a specific software feature.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-696">**CIM \_ SpareGroup**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-696">**CIM\_SpareGroup**</span></span>](cim-sparegroup.md)
</dt> <dd>

<span data-ttu-id="4a2aa-697">[**Cim \_ SpareGroup**](cim-sparegroup.md)類別衍生自 [**cim \_ RedundancyGroup**](cim-redundancygroup.md)類別，並指出一或多個匯總的元素可以被用。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-697">The [**CIM\_SpareGroup**](cim-sparegroup.md) class is derived from the [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class and indicates that one or more of the aggregated elements can be spared.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-698">**CIM \_ StatisticalInformation**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-698">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> <dd>

<span data-ttu-id="4a2aa-699">[**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)類別是適用于一或多個 managed 系統專案之統計資料或計量的任意集合的根類別。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-699">The [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) class is a root class for the arbitrary collection of statistical data or metrics applicable to one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-700">**CIM \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-700">**CIM\_Statistics**</span></span>](cim-statistics.md)
</dt> <dd>

<span data-ttu-id="4a2aa-701">[**CIM \_ Statistics**](cim-statistics.md)類別代表關聯，可將 managed 系統專案與套用至這些專案的統計群組產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-701">The [**CIM\_Statistics**](cim-statistics.md) class represents an association that relates managed system elements to the statistical groups that apply to them.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-702">**CIM \_ StorageDefect**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-702">**CIM\_StorageDefect**</span></span>](cim-storagedefect.md)
</dt> <dd>

<span data-ttu-id="4a2aa-703">[**CIM \_ StorageDefect**](cim-storagedefect.md)匯總會收集儲存區的儲存錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-703">The [**CIM\_StorageDefect**](cim-storagedefect.md) aggregation collects the storage errors for a storage extent.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-704">**CIM \_ StorageError**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-704">**CIM\_StorageError**</span></span>](cim-storageerror.md)
</dt> <dd>

<span data-ttu-id="4a2aa-705">[**CIM \_ StorageError**](cim-storageerror.md)類別代表因為錯誤而對應于使用中的媒體或記憶體空間區塊。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-705">The [**CIM\_StorageError**](cim-storageerror.md) class represents blocks of media or memory space that are mapped out-of-use due to errors.</span></span> <span data-ttu-id="4a2aa-706">類別的索引鍵是錯誤中位元組的 **StartingAddress** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-706">The key of the class is the **StartingAddress** property of the bytes in error.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-707">**CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-707">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dd>

<span data-ttu-id="4a2aa-708">[**CIM \_ StorageExtent**](cim-storageextent.md)類別代表各種媒體的功能和管理，該媒體存在於儲存資料和允許資料抓取。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-708">The [**CIM\_StorageExtent**](cim-storageextent.md) class represents the capabilities and management of the various media that exist to store data and allow data retrieval.</span></span> <span data-ttu-id="4a2aa-709">此父類別可代表 RAID (硬體或軟體) 的各種元件，或實體媒體上的原始邏輯範圍。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-709">This parent class can represent the various components of RAID (hardware or software) or a raw logical extent on top of physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-710">**CIM \_ StorageRedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-710">**CIM\_StorageRedundancyGroup**</span></span>](cim-storageredundancygroup.md)
</dt> <dd>

<span data-ttu-id="4a2aa-711">[**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md)類別代表大量儲存體相關的重複資訊。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-711">The [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class represents mass storage-related redundancy information.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-712">**CIM \_ SupportAccess**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-712">**CIM\_SupportAccess**</span></span>](cim-supportaccess.md)
</dt> <dd>

<span data-ttu-id="4a2aa-713">[**CIM \_ SupportAccess**](cim-supportaccess.md)類別定義了如何取得產品的協助。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-713">The [**CIM\_SupportAccess**](cim-supportaccess.md) class defines how to obtain assistance for a product.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-714">**CIM \_ SwapSpaceCheck**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-714">**CIM\_SwapSpaceCheck**</span></span>](cim-swapspacecheck.md)
</dt> <dd>

<span data-ttu-id="4a2aa-715">[**CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md)類別會指定系統上必須可用的交換空間量。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-715">The [**CIM\_SwapSpaceCheck**](cim-swapspacecheck.md) class specifies the amount of swap space that must be available on the system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-716">**CIM \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-716">**CIM\_System**</span></span>](cim-system.md)
</dt> <dd>

<span data-ttu-id="4a2aa-717">[**CIM \_ 系統**](cim-system.md)類別會匯總 managed 系統專案的可列舉集合。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-717">The [**CIM\_System**](cim-system.md) class aggregates an enumerable set of managed system elements.</span></span> <span data-ttu-id="4a2aa-718">匯總會以整體功能的形式運作。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-718">The aggregation operates as a functional whole.</span></span> <span data-ttu-id="4a2aa-719">在系統的任何特定子類別內，都有一個定義完善的 managed 系統專案類別清單，這些類別的實例必須加以匯總。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-719">Within any particular subclass of the system, there is a well-defined list of managed system element classes whose instances must be aggregated.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-720">**CIM \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-720">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dd>

<span data-ttu-id="4a2aa-721">通用訊息模型 (CIM) 關聯類別，可建立系統與其組成之 managed 系統元素之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-721">a Common Information Model (CIM) association class that establishes relationships between a system and the managed system elements of which it is composed.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-722">**CIM \_ SystemDevice**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-722">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dd>

<span data-ttu-id="4a2aa-723">[**CIM \_ SystemDevice**](cim-systemdevice.md)關聯代表明確的關聯性，可讓系統匯總邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-723">The [**CIM\_SystemDevice**](cim-systemdevice.md) association represents an explicit relationship in which logical devices can be aggregated by a system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-724">**CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-724">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> <dd>

<span data-ttu-id="4a2aa-725">[**CIM \_ SystemResource**](cim-systemresource.md)類別代表 BIOS 所管理的實體，或是可供軟體和邏輯裝置使用的作業系統。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-725">The [**CIM\_SystemResource**](cim-systemresource.md) class represents an entity managed by BIOS, or an operating system that is available for use by software and logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-726">**CIM \_ 流速**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-726">**CIM\_Tachometer**</span></span>](cim-tachometer.md)
</dt> <dd>

<span data-ttu-id="4a2aa-727">[**Cim \_ 轉速計**](cim-tachometer.md)類別存在，可回溯相容于舊版 CIM 架構定義。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-727">The [**CIM\_Tachometer**](cim-tachometer.md) class exists for backward compatibility with earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-728">**CIM \_ disable-tapedrive**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-728">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> <dd>

<span data-ttu-id="4a2aa-729">[**CIM \_ disable-tapedrive**](cim-tapedrive.md)類別代表系統上的磁帶機。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-729">The [**CIM\_TapeDrive**](cim-tapedrive.md) class represents a tape drive on the system.</span></span> <span data-ttu-id="4a2aa-730">磁帶機主要是用來區別，因為它們只能依序存取。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-730">Tape drives are primarily distinguished in that they can only be accessed sequentially.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-731">**CIM \_ 溫度感應器**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-731">**CIM\_TemperatureSensor**</span></span>](cim-temperaturesensor.md)
</dt> <dd>

<span data-ttu-id="4a2aa-732">[**Cim \_ 溫度感應器**](cim-temperaturesensor.md)類別存在，可回溯相容于舊版 cim 架構定義。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-732">The [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) class exists for backward compatibility with earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-733">**CIM \_ 執行緒**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-733">**CIM\_Thread**</span></span>](cim-thread.md)
</dt> <dd>

<span data-ttu-id="4a2aa-734">[**CIM \_ 執行緒**](cim-thread.md)類別代表能夠以平行方式執行進程或工作的單位。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-734">The [**CIM\_Thread**](cim-thread.md) class represents the ability to execute units of a process or task, in parallel.</span></span> <span data-ttu-id="4a2aa-735">一個處理常式可以有許多執行緒，每個執行緒都是進程的弱式。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-735">A process can have many threads, each of which is weak to the process.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-736">**CIM \_ ToDirectoryAction**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-736">**CIM\_ToDirectoryAction**</span></span>](cim-todirectoryaction.md)
</dt> <dd>

<span data-ttu-id="4a2aa-737">[**CIM \_ ToDirectoryAction**](cim-todirectoryaction.md)關聯會識別檔案動作的目標目錄。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-737">The [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) association identifies the target directory for the file action.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-738">**CIM \_ ToDirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-738">**CIM\_ToDirectorySpecification**</span></span>](cim-todirectoryspecification.md)
</dt> <dd>

<span data-ttu-id="4a2aa-739">[**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md)關聯會識別檔案動作的目標目錄。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-739">The [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) association identifies the target directory for the file action.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-740">**CIM \_ UninterruptiblePowerSupply**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-740">**CIM\_UninterruptiblePowerSupply**</span></span>](cim-uninterruptiblepowersupply.md)
</dt> <dd>

<span data-ttu-id="4a2aa-741">[**CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md)類別代表 (UPS) 的不斷電供應系統供應器的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-741">The [**CIM\_UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) class represents the capabilities and management of an uninterruptible power supply (UPS).</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-742">**CIM \_ UnitaryComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-742">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> <dd>

<span data-ttu-id="4a2aa-743">[**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)類別代表桌上型電腦、行動裝置、網路電腦、伺服器或其他類型的單一節點電腦系統。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-743">The [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class represents a desktop, mobile, network computer, server, or other type of single-node computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-744">**CIM \_ USBController**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-744">**CIM\_USBController**</span></span>](cim-usbcontroller.md)
</dt> <dd>

<span data-ttu-id="4a2aa-745">[**CIM \_ USBController**](cim-usbcontroller.md)類別代表 USB 控制器的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-745">The [**CIM\_USBController**](cim-usbcontroller.md) class represents the capabilities and management of a USB controller.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-746">**CIM \_ USBControllerHasHub**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-746">**CIM\_USBControllerHasHub**</span></span>](cim-usbcontrollerhashub.md)
</dt> <dd>

<span data-ttu-id="4a2aa-747">[**CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md)類別定義了 USB 控制器下游的中樞。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-747">The [**CIM\_USBControllerHasHub**](cim-usbcontrollerhashub.md) class defines the hubs that are downstream of the USB controller.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-748">**CIM \_ USBDevice**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-748">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> <dd>

<span data-ttu-id="4a2aa-749">[**CIM \_ USBDevice**](cim-usbdevice.md)類別代表 USB 裝置的管理特性。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-749">The [**CIM\_USBDevice**](cim-usbdevice.md) class represents the management characteristics of a USB device.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-750">**CIM \_ USBHub**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-750">**CIM\_USBHub**</span></span>](cim-usbhub.md)
</dt> <dd>

<span data-ttu-id="4a2aa-751">[**CIM \_ USBHub**](cim-usbhub.md)類別代表 USB 集線器的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-751">The [**CIM\_USBHub**](cim-usbhub.md) class represents the capabilities and management of a USB hub.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-752">**CIM \_ UserDevice**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-752">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> <dd>

<span data-ttu-id="4a2aa-753">[**Cim \_ UserDevice**](cim-userdevice.md)類別是其他類別（例如 [**CIM \_ 鍵盤**](cim-keyboard.md)或 [**cim \_ DesktopMonitor**](cim-desktopmonitor.md)）下降的父類別。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-753">The [**CIM\_UserDevice**](cim-userdevice.md) class is a parent class from which other classes, such as [**CIM\_Keyboard**](cim-keyboard.md) or [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), descend.</span></span> <span data-ttu-id="4a2aa-754">使用者裝置是邏輯裝置，可讓電腦系統的使用者輸入、查看或聽到資料。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-754">User devices are logical devices that allow a computer system's user to input, view, or hear data.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-755">**CIM \_ VersionCompatibilityCheck**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-755">**CIM\_VersionCompatibilityCheck**</span></span>](cim-versioncompatibilitycheck.md)
</dt> <dd>

<span data-ttu-id="4a2aa-756">[**CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md)類別會指定是否允許建立軟體元素的下一個狀態。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-756">The [**CIM\_VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) class specifies whether it is permissible to create the next state of a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-757">**CIM \_ VideoBIOSElement**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-757">**CIM\_VideoBIOSElement**</span></span>](cim-videobioselement.md)
</dt> <dd>

<span data-ttu-id="4a2aa-758">[**CIM \_ VideoBIOSElement**](cim-videobioselement.md)類別代表載入至非暫時性存放裝置的低層級軟體，可用來設定及存取電腦系統的視訊控制器和顯示器。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-758">The [**CIM\_VideoBIOSElement**](cim-videobioselement.md) class represents the low-level software that is loaded into non-volatile storage and used to configure and access a computer system's video controller and display.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-759">**CIM \_ VideoBIOSFeature**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-759">**CIM\_VideoBIOSFeature**</span></span>](cim-videobiosfeature.md)
</dt> <dd>

<span data-ttu-id="4a2aa-760">[**CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md)類別代表用來設定及存取電腦系統之視訊控制器和顯示器的低層級軟體的功能。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-760">The [**CIM\_VideoBIOSFeature**](cim-videobiosfeature.md) class represents the capabilities of the low-level software used to configure and access a computer system's video controller and display.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-761">**CIM \_ VideoBIOSFeatureVideoBIOSElements**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-761">**CIM\_VideoBIOSFeatureVideoBIOSElements**</span></span>](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

<span data-ttu-id="4a2aa-762">[**CIM \_ VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md)類別會將影片 bios 功能與其匯總的影片 bios 專案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-762">The [**CIM\_VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md) class associates a video BIOS feature and its aggregated video BIOS elements.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-763">**CIM \_ VideoController**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-763">**CIM\_VideoController**</span></span>](cim-videocontroller.md)
</dt> <dd>

<span data-ttu-id="4a2aa-764">[**CIM \_ VideoController**](cim-videocontroller.md)類別代表影片控制器的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-764">The [**CIM\_VideoController**](cim-videocontroller.md) class represents the capabilities and management of the video controller.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-765">**CIM \_ VideoControllerResolution**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-765">**CIM\_VideoControllerResolution**</span></span>](cim-videocontrollerresolution.md)
</dt> <dd>

<span data-ttu-id="4a2aa-766">[**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)類別代表影片控制器可支援的各種影片模式。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-766">The [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) class represents the various video modes that a video controller can support.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-767">**CIM \_ VideoSetting**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-767">**CIM\_VideoSetting**</span></span>](cim-videosetting.md)
</dt> <dd>

<span data-ttu-id="4a2aa-768">[**Cim \_ VideoSetting**](cim-videosetting.md)類別會將 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)設定物件與其套用的控制器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-768">The [**CIM\_VideoSetting**](cim-videosetting.md) class associates the [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) setting object with the controller to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-769">**CIM \_ VolatileStorage**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-769">**CIM\_VolatileStorage**</span></span>](cim-volatilestorage.md)
</dt> <dd>

<span data-ttu-id="4a2aa-770">[**CIM \_ VolatileStorage**](cim-volatilestorage.md)類別代表 volatile 儲存體的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-770">The [**CIM\_VolatileStorage**](cim-volatilestorage.md) class represents the capabilities and management of volatile storage.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-771">**CIM \_ 電壓感應器**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-771">**CIM\_VoltageSensor**</span></span>](cim-voltagesensor.md)
</dt> <dd>

<span data-ttu-id="4a2aa-772">[**Cim \_ 電壓感應器**](cim-voltagesensor.md)類別存在，可回溯相容于舊版 cim 架構定義。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-772">The [**CIM\_VoltageSensor**](cim-voltagesensor.md) class exists for backward compatibility to earlier CIM schema definitions.</span></span> <span data-ttu-id="4a2aa-773">在2.2 版中，有 [**cim \_ 感應器**](cim-sensor.md) 和 [**cim \_ NumericSensor**](cim-numericsensor.md) 類別的新增功能，不再需要。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-773">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-774">**CIM \_ VolumeSet**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-774">**CIM\_VolumeSet**</span></span>](cim-volumeset.md)
</dt> <dd>

<span data-ttu-id="4a2aa-775">[**CIM \_ VolumeSet**](cim-volumeset.md)類別代表針對讀取和寫入使用者資料的作業環境所呈現的連續邏輯區塊範圍。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-775">The [**CIM\_VolumeSet**](cim-volumeset.md) class represents a contiguous range of logical blocks presented to the operating environment for reading and writing user data.</span></span>

</dd> <dt>

[<span data-ttu-id="4a2aa-776">**CIM \_ WORMDrive**</span><span class="sxs-lookup"><span data-stu-id="4a2aa-776">**CIM\_WORMDrive**</span></span>](cim-wormdrive.md)
</dt> <dd>

<span data-ttu-id="4a2aa-777">[**CIM \_ WORMDrive**](cim-wormdrive.md)類別代表 WORM 磁片磁碟機（媒體存取裝置的子類型）的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4a2aa-777">The [**CIM\_WORMDrive**](cim-wormdrive.md) class represents the capabilities and management of a WORM drive, a subtype of the media access device.</span></span>

</dd> </dl>

 

 
