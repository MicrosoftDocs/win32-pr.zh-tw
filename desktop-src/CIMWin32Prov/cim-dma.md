---
description: CIM \_ DMA 類別代表 (DMA) 的電腦架構直接記憶體存取。
ms.assetid: 101fa9f3-a403-487d-8482-b1e8e9f957d6
ms.tgt_platform: multiple
title: CIM_DMA 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DMA
- CIM_DMA.AddressSize
- CIM_DMA.Availability
- CIM_DMA.BurstMode
- CIM_DMA.ByteMode
- CIM_DMA.Caption
- CIM_DMA.ChannelTiming
- CIM_DMA.CreationClassName
- CIM_DMA.CSCreationClassName
- CIM_DMA.CSName
- CIM_DMA.Description
- CIM_DMA.DMAChannel
- CIM_DMA.InstallDate
- CIM_DMA.MaxTransferSize
- CIM_DMA.Name
- CIM_DMA.Status
- CIM_DMA.TransferWidths
- CIM_DMA.TypeCTiming
- CIM_DMA.WordMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71fe9c0ad29afa7be20df6fbf05c5d1183d23d13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936322"
---
# <a name="cim_dma-class"></a><span data-ttu-id="3b5d0-103">CIM \_ DMA 類別</span><span class="sxs-lookup"><span data-stu-id="3b5d0-103">CIM\_DMA class</span></span>

<span data-ttu-id="3b5d0-104">**CIM \_ DMA** 類別代表 (DMA) 的電腦架構直接記憶體存取。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-104">The **CIM\_DMA** class represents computer architecture direct memory access (DMA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b5d0-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3b5d0-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3b5d0-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3b5d0-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b5d0-109">語法</span><span class="sxs-lookup"><span data-stu-id="3b5d0-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C523-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DMA : CIM_SystemResource
{
  uint16   AddressSize;
  uint16   Availability;
  boolean  BurstMode;
  uint16   ByteMode;
  string   Caption;
  uint16   ChannelTiming;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint32   DMAChannel;
  datetime InstallDate;
  uint32   MaxTransferSize;
  string   Name;
  string   Status;
  uint16   TransferWidths[];
  uint16   TypeCTiming;
  uint16   WordMode;
};
```

## <a name="members"></a><span data-ttu-id="3b5d0-110">成員</span><span class="sxs-lookup"><span data-stu-id="3b5d0-110">Members</span></span>

<span data-ttu-id="3b5d0-111">**CIM \_ DMA** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3b5d0-111">The **CIM\_DMA** class has these types of members:</span></span>

-   [<span data-ttu-id="3b5d0-112">屬性</span><span class="sxs-lookup"><span data-stu-id="3b5d0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b5d0-113">屬性</span><span class="sxs-lookup"><span data-stu-id="3b5d0-113">Properties</span></span>

<span data-ttu-id="3b5d0-114">**CIM \_ DMA** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-114">The **CIM\_DMA** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b5d0-115">**AddressSize**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-115">**AddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-116">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-118">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。「DMTF \| 系統資源 DMA 資訊 \| 001.3」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「位」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-119">DMA 通道位址大小，以位為單位。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-119">DMA channel address size, in bits.</span></span> <span data-ttu-id="3b5d0-120">允許的值為8、16、32和64。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-120">Permissible values are 8, 16, 32, and 64.</span></span> <span data-ttu-id="3b5d0-121">如果不明，請輸入0。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-121">If unknown, enter 0.</span></span>

<dt>



 <span data-ttu-id="3b5d0-122"> (0)</span><span class="sxs-lookup"><span data-stu-id="3b5d0-122">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b5d0-123">(8)</span><span class="sxs-lookup"><span data-stu-id="3b5d0-123">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b5d0-124">(16)</span><span class="sxs-lookup"><span data-stu-id="3b5d0-124">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b5d0-125"> (32) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-125">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b5d0-126">(64)</span><span class="sxs-lookup"><span data-stu-id="3b5d0-126">(64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3b5d0-127">**可用性**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-127">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-128">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-130">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| DMA \| 001.2 ") </span><span class="sxs-lookup"><span data-stu-id="3b5d0-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-131">DMA 的可用性。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-131">Availability of the DMA.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3b5d0-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3b5d0-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-134">不明。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-134">Unknown.</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="3b5d0-135"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**可用** (3) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-135"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-136">可用。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-136">Available.</span></span>

</dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="3b5d0-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**使用中/無法使用** (4) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-138">使用中 (無法使用) 。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-138">In use (not available).</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="3b5d0-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**使用中和可用/可共用** (5) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-140">使用中，但可 (可共用的) 。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-140">In use, but available (sharable).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3b5d0-141">**BurstMode**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-141">**BurstMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-142">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-144">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| DMA \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="3b5d0-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-145">若 **為 TRUE**，DMA 通道支援高載模式。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-145">If **TRUE**, the DMA channel supports burst mode.</span></span>

</dd> <dt>

<span data-ttu-id="3b5d0-146">**ByteMode**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-146">**ByteMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-147">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-149">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統資源 DMA 資訊 \| 001.7」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-150">指出 DMA 是否可在依位元組計數的模式下執行。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-150">Indicates whether DMA can execute in count-by-byte mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3b5d0-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-152">其他。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-152">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3b5d0-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-154">不明。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-154">Unknown.</span></span>

</dd> <dt>

<span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="3b5d0-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**不是以「依位元組計數」模式執行** (3) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Not execute in 'count by byte' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-156">無法在依位元組計數的模式下執行。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-156">Cannot execute in count-by-byte mode.</span></span>

</dd> <dt>

<span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="3b5d0-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**以「依位元組計數」模式執行** (4) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Execute in 'count by byte' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-158">能夠在依位元組計數的模式下執行。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-158">Able to execute in count-by-byte mode.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3b5d0-159">**標題**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-162">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-163">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-163">Short textual description of the object.</span></span>

<span data-ttu-id="3b5d0-164">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b5d0-165">**ChannelTiming**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-165">**ChannelTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-166">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-168">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統資源 DMA 資訊 \| 001.9」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-169">DMA 通道計時。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-169">DMA channel timing.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3b5d0-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-171">其他。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-171">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3b5d0-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-173">不明。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-173">Unknown.</span></span>

</dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="3b5d0-174"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA 相容** (3) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-174"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA Compatible** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-175">ISA 相容。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-175">ISA-compatible.</span></span>

</dd> <dt>

<span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>

<span data-ttu-id="3b5d0-176"><span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>**輸入** (4) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-176"><span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>**Type A** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-177">輸入。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-177">Type A.</span></span>

</dd> <dt>

<span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>

<span data-ttu-id="3b5d0-178"><span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>**類型 B** (5) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-178"><span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>**Type B** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-179">輸入 B。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-179">Type B.</span></span>

</dd> <dt>

<span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>

<span data-ttu-id="3b5d0-180"><span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>**輸入 F** (6) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-180"><span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>**Type F** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-181">輸入 F。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-181">Type F.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3b5d0-182">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-182">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-185">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3b5d0-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-186">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-186">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3b5d0-187">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-187">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="3b5d0-188">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-188">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-191">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**CreationClassName**") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3b5d0-191">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-192">設定電腦系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-192">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="3b5d0-193">**CSName**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-193">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-196">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-196">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-197">設定電腦系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-197">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="3b5d0-198">**說明**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-201">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-201">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-202">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-202">Textual description of the object.</span></span>

<span data-ttu-id="3b5d0-203">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b5d0-204">**DMAChannel**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-204">**DMAChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-205">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-207">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| DMA \| 001.1 ") </span><span class="sxs-lookup"><span data-stu-id="3b5d0-207">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-208">DMA 頻道號碼。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-208">DMA channel number.</span></span> <span data-ttu-id="3b5d0-209">此數位是物件的索引鍵值的一部分。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-209">This number is part of the object's key value.</span></span>

</dd> <dt>

<span data-ttu-id="3b5d0-210">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-210">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-211">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-211">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-213">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="3b5d0-213">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-214">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-214">Date and time the object was installed.</span></span> <span data-ttu-id="3b5d0-215">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-215">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3b5d0-216">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-216">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b5d0-217">**MaxTransferSize**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-217">**MaxTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-218">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-218">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-220">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。「DMTF \| 系統資源 DMA 資訊 \| 001.4」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「位元組」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-220">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-221">這個 DMA 通道可以傳送的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-221">Maximum number of bytes that can be transferred by this DMA channel.</span></span> <span data-ttu-id="3b5d0-222">如果不明，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-222">If unknown, enter 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="3b5d0-223">**名稱**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-223">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-224">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-226">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-226">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-227">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-227">Label by which the object is known.</span></span> <span data-ttu-id="3b5d0-228">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-228">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="3b5d0-229">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-229">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b5d0-230">**狀態**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-230">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-231">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-233">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-233">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-234">表示物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-234">Indicates the current status of the object.</span></span>

<span data-ttu-id="3b5d0-235">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-235">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3b5d0-236">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="3b5d0-236">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3b5d0-237">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-237">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3b5d0-238">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-238">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3b5d0-239">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-239">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3b5d0-240">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-240">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3b5d0-241">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-241">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3b5d0-242">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-242">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3b5d0-243">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-243">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3b5d0-244">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-244">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3b5d0-245">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-245">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3b5d0-246">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-246">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3b5d0-247">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-247">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3b5d0-248">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-248">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3b5d0-249">**TransferWidths**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-249">**TransferWidths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-250">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="3b5d0-250">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-252">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。「DMTF \| 系統資源 DMA 資訊 \| 001.2」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「位」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-253">陣列，指出這個 DMA 通道支援的所有傳輸寬度（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-253">Array that indicates all of the transfer widths, in bits, supported by this DMA channel.</span></span> <span data-ttu-id="3b5d0-254">允許的值為8、16、32、64和128位。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-254">Permissible values are 8, 16, 32, 64, and 128 bits.</span></span> <span data-ttu-id="3b5d0-255">如果不明，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-255">If unknown, enter 0 (zero).</span></span>

<dt>



 <span data-ttu-id="3b5d0-256"> (0)</span><span class="sxs-lookup"><span data-stu-id="3b5d0-256">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b5d0-257">(8)</span><span class="sxs-lookup"><span data-stu-id="3b5d0-257">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b5d0-258">(16)</span><span class="sxs-lookup"><span data-stu-id="3b5d0-258">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b5d0-259"> (32) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-259">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b5d0-260">(64)</span><span class="sxs-lookup"><span data-stu-id="3b5d0-260">(64)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b5d0-261"> (128) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-261">(128)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3b5d0-262">**TypeCTiming**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-262">**TypeCTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-263">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-263">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-265">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統資源 DMA 資訊 \| 001.10」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-265">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-266">指出是否支援類型 C (高載) 計時。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-266">Indicates whether Type C (burst) timing is supported.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3b5d0-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-268">其他。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-268">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3b5d0-269"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-269"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-270">不明。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-270">Unknown.</span></span>

</dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="3b5d0-271"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA 相容** (3) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-271"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA Compatible** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-272">ISA 相容。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-272">ISA-compatible.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="3b5d0-273"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (4) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-273"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-274">不支援。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-274">Not supported.</span></span>

</dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="3b5d0-275"><span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>**支援** (5) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-275"><span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>**Supported** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-276">支援。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-276">Supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3b5d0-277">**WordMode**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-277">**WordMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5d0-278">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-278">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b5d0-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5d0-280">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統資源 DMA 資訊 \| 001.8」 ) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-280">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="3b5d0-281">指出 DMA 是否可以依單字的模式執行。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-281">Indicates whether DMA can execute in count-by-word mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3b5d0-282"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-282"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-283">其他。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-283">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3b5d0-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-285">不明。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-285">Unknown.</span></span>

</dd> <dt>

<span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="3b5d0-286"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**無法在「依單字計數」模式中執行** (3) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-286"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Not execute in 'count by word' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-287">無法依單字的模式執行。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-287">Cannot execute in count-by-word mode.</span></span>

</dd> <dt>

<span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="3b5d0-288"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**在 [依單字計數] 模式下執行** (4) </span><span class="sxs-lookup"><span data-stu-id="3b5d0-288"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Execute in 'count by word' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3b5d0-289">能夠依單字的模式執行。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-289">Able to execute in count-by-word mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b5d0-290">備註</span><span class="sxs-lookup"><span data-stu-id="3b5d0-290">Remarks</span></span>

<span data-ttu-id="3b5d0-291">**Cim \_ DMA** 類別衍生自 [**cim \_ SystemResource**](cim-systemresource.md)。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-291">The **CIM\_DMA** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span>

<span data-ttu-id="3b5d0-292">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-292">WMI does not implement this class.</span></span> <span data-ttu-id="3b5d0-293">針對衍生自 **CIM \_ DMA** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-293">For classes derived from **CIM\_DMA**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="3b5d0-294">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-294">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3b5d0-295">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3b5d0-295">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b5d0-296">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b5d0-296">Requirements</span></span>



| <span data-ttu-id="3b5d0-297">需求</span><span class="sxs-lookup"><span data-stu-id="3b5d0-297">Requirement</span></span> | <span data-ttu-id="3b5d0-298">值</span><span class="sxs-lookup"><span data-stu-id="3b5d0-298">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b5d0-299">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b5d0-299">Minimum supported client</span></span><br/> | <span data-ttu-id="3b5d0-300">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b5d0-300">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b5d0-301">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b5d0-301">Minimum supported server</span></span><br/> | <span data-ttu-id="3b5d0-302">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b5d0-302">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b5d0-303">命名空間</span><span class="sxs-lookup"><span data-stu-id="3b5d0-303">Namespace</span></span><br/>                | <span data-ttu-id="3b5d0-304">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3b5d0-304">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3b5d0-305">MOF</span><span class="sxs-lookup"><span data-stu-id="3b5d0-305">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b5d0-306"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b5d0-306"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b5d0-307">DLL</span><span class="sxs-lookup"><span data-stu-id="3b5d0-307">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b5d0-308"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b5d0-308"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b5d0-309">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b5d0-309">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b5d0-310">**CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="3b5d0-310">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

