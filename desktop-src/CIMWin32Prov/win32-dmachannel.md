---
description: Win32 \_ DMACHANNEL WMI 類別代表在執行 Windows 的電腦系統上 (DMA) 通道的直接記憶體存取。
ms.assetid: cc517aac-7bd4-4937-8b07-2597076fca2c
ms.tgt_platform: multiple
title: Win32_DMAChannel 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DMAChannel
- Win32_DMAChannel.AddressSize
- Win32_DMAChannel.Availability
- Win32_DMAChannel.BurstMode
- Win32_DMAChannel.ByteMode
- Win32_DMAChannel.Caption
- Win32_DMAChannel.ChannelTiming
- Win32_DMAChannel.CreationClassName
- Win32_DMAChannel.CSCreationClassName
- Win32_DMAChannel.CSName
- Win32_DMAChannel.Description
- Win32_DMAChannel.DMAChannel
- Win32_DMAChannel.InstallDate
- Win32_DMAChannel.MaxTransferSize
- Win32_DMAChannel.Name
- Win32_DMAChannel.Port
- Win32_DMAChannel.Status
- Win32_DMAChannel.TransferWidths
- Win32_DMAChannel.TypeCTiming
- Win32_DMAChannel.WordMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0c2b36ff17931133d0dc4529e34f31ac24e00653
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847485"
---
# <a name="win32_dmachannel-class"></a><span data-ttu-id="43634-103">Win32 \_ DMAChannel 類別</span><span class="sxs-lookup"><span data-stu-id="43634-103">Win32\_DMAChannel class</span></span>

<span data-ttu-id="43634-104">**Win32 \_ DMAChannel** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表在執行 Windows 的電腦系統上 (DMA) 通道的直接記憶體存取。</span><span class="sxs-lookup"><span data-stu-id="43634-104">The **Win32\_DMAChannel** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a direct memory access (DMA) channel on a computer system running Windows.</span></span> <span data-ttu-id="43634-105">DMA 是一種將資料從裝置移至記憶體 (或反之亦然) ，而不需要微處理器協助的方法。</span><span class="sxs-lookup"><span data-stu-id="43634-105">DMA is a method of moving data from a device to memory (or vice versa) without the help of the microprocessor.</span></span> <span data-ttu-id="43634-106">系統面板會使用 DMA 控制器來處理固定數目的通道，其中每一個都只能由一個 (使用，一次只能使用一個) 裝置。</span><span class="sxs-lookup"><span data-stu-id="43634-106">The system board uses a DMA controller to handle a fixed number of channels, each of which can be used by one (and only one) device at a time.</span></span>

<span data-ttu-id="43634-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="43634-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="43634-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="43634-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="43634-109">語法</span><span class="sxs-lookup"><span data-stu-id="43634-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DMAChannel : CIM_DMA
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
  uint32   Port;
  string   Status;
  uint16   TransferWidths[];
  uint16   TypeCTiming;
  uint16   WordMode;
};
```

## <a name="members"></a><span data-ttu-id="43634-110">成員</span><span class="sxs-lookup"><span data-stu-id="43634-110">Members</span></span>

<span data-ttu-id="43634-111">**Win32 \_ DMAChannel** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="43634-111">The **Win32\_DMAChannel** class has these types of members:</span></span>

-   [<span data-ttu-id="43634-112">屬性</span><span class="sxs-lookup"><span data-stu-id="43634-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43634-113">屬性</span><span class="sxs-lookup"><span data-stu-id="43634-113">Properties</span></span>

<span data-ttu-id="43634-114">**Win32 \_ DMAChannel** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="43634-114">The **Win32\_DMAChannel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43634-115">**AddressSize**</span><span class="sxs-lookup"><span data-stu-id="43634-115">**AddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-116">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="43634-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43634-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-118">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。「DMTF \| 系統資源 DMA 資訊 \| 001.3」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「位」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="43634-119">DMA 通道位址大小（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="43634-119">DMA channel address size in bits.</span></span> <span data-ttu-id="43634-120">允許的值為8、16、32或64位。</span><span class="sxs-lookup"><span data-stu-id="43634-120">Permissible values are 8, 16, 32, or 64 bits.</span></span> <span data-ttu-id="43634-121">如果不明，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="43634-121">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="43634-122">這個屬性繼承自 [**CIM \_ DMA**](cim-dma.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-122">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>



 <span data-ttu-id="43634-123"> (0)</span><span class="sxs-lookup"><span data-stu-id="43634-123">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="43634-124">(8)</span><span class="sxs-lookup"><span data-stu-id="43634-124">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="43634-125">(16)</span><span class="sxs-lookup"><span data-stu-id="43634-125">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="43634-126"> (32) </span><span class="sxs-lookup"><span data-stu-id="43634-126">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="43634-127">(64)</span><span class="sxs-lookup"><span data-stu-id="43634-127">(64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43634-128">**可用性**</span><span class="sxs-lookup"><span data-stu-id="43634-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-129">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="43634-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43634-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-131">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| DMA \| 001.2 ") </span><span class="sxs-lookup"><span data-stu-id="43634-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="43634-132">DMA 的可用性。</span><span class="sxs-lookup"><span data-stu-id="43634-132">Availability of the DMA.</span></span> <span data-ttu-id="43634-133">這個屬性繼承自 [**CIM \_ DMA**](cim-dma.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-133">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="43634-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="43634-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43634-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="43634-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="43634-136"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**可用** (3) </span><span class="sxs-lookup"><span data-stu-id="43634-136"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="43634-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**使用中/無法使用** (4) </span><span class="sxs-lookup"><span data-stu-id="43634-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="43634-138">使用中或無法使用</span><span class="sxs-lookup"><span data-stu-id="43634-138">In Use or Not Available</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="43634-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**使用中和可用/可共用** (5) </span><span class="sxs-lookup"><span data-stu-id="43634-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="43634-140">使用中和可用或可共用</span><span class="sxs-lookup"><span data-stu-id="43634-140">In Use and Available or Sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="43634-141">**BurstMode**</span><span class="sxs-lookup"><span data-stu-id="43634-141">**BurstMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-142">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="43634-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43634-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-144">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| DMA \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="43634-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="43634-145">指出 DMA 通道是否支援高載模式。</span><span class="sxs-lookup"><span data-stu-id="43634-145">Indicates whether or not the DMA channel supports burst mode.</span></span>

<span data-ttu-id="43634-146">這個屬性繼承自 [**CIM \_ DMA**](cim-dma.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-146">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="43634-147">**ByteMode**</span><span class="sxs-lookup"><span data-stu-id="43634-147">**ByteMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-148">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="43634-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43634-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-150">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統資源 DMA 資訊 \| 001.7」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="43634-151">DMA 執行模式。</span><span class="sxs-lookup"><span data-stu-id="43634-151">DMA execution mode.</span></span>

<span data-ttu-id="43634-152">這個屬性繼承自 [**CIM \_ DMA**](cim-dma.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-152">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="43634-153"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="43634-153"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43634-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="43634-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="43634-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**不是以「依位元組計數」模式執行** (3) </span><span class="sxs-lookup"><span data-stu-id="43634-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Not execute in 'count by byte' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="43634-156">不會在「依位元組計數」模式中執行</span><span class="sxs-lookup"><span data-stu-id="43634-156">Does not execute in "count by byte" mode</span></span>

</dd> <dt>

<span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="43634-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**以「依位元組計數」模式執行** (4) </span><span class="sxs-lookup"><span data-stu-id="43634-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Execute in 'count by byte' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="43634-158">以「依位元組計數」模式執行</span><span class="sxs-lookup"><span data-stu-id="43634-158">Execute in "count by byte" mode</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="43634-159">**標題**</span><span class="sxs-lookup"><span data-stu-id="43634-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="43634-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43634-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-162">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="43634-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="43634-163">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="43634-163">Short description of the object a one-line string.</span></span>

<span data-ttu-id="43634-164">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="43634-165">**ChannelTiming**</span><span class="sxs-lookup"><span data-stu-id="43634-165">**ChannelTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-166">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="43634-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43634-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-168">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統資源 DMA 資訊 \| 001.9」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="43634-169">DMA 通道計時。</span><span class="sxs-lookup"><span data-stu-id="43634-169">DMA channel timing.</span></span>

<span data-ttu-id="43634-170">這個屬性繼承自 [**CIM \_ DMA**](cim-dma.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-170">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="43634-171">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="43634-171">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43634-172">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="43634-172">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="43634-173">**ISA 相容** (3) </span><span class="sxs-lookup"><span data-stu-id="43634-173">**ISA Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>

<span data-ttu-id="43634-174">**輸入** (4) </span><span class="sxs-lookup"><span data-stu-id="43634-174">**Type A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>

<span data-ttu-id="43634-175">**類型 B** (5) </span><span class="sxs-lookup"><span data-stu-id="43634-175">**Type B** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>

<span data-ttu-id="43634-176">**輸入 F** (6) </span><span class="sxs-lookup"><span data-stu-id="43634-176">**Type F** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43634-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="43634-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="43634-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43634-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-180">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="43634-180">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="43634-181">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="43634-181">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="43634-182">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="43634-182">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="43634-183">這個屬性繼承自 [**CIM \_ DMA**](cim-dma.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-183">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="43634-184">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="43634-184">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="43634-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43634-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-187">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**CreationClassName**") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="43634-187">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="43634-188">範圍電腦系統建立類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="43634-188">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="43634-189">這個屬性繼承自 [**CIM \_ DMA**](cim-dma.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-189">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="43634-190">**CSName**</span><span class="sxs-lookup"><span data-stu-id="43634-190">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="43634-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43634-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-193">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="43634-193">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="43634-194">範圍電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="43634-194">Name of the scoping computer system.</span></span>

<span data-ttu-id="43634-195">這個屬性繼承自 [**CIM \_ DMA**](cim-dma.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-195">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="43634-196">**說明**</span><span class="sxs-lookup"><span data-stu-id="43634-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="43634-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43634-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-199">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="43634-199">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="43634-200">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="43634-200">Description of the object.</span></span>

<span data-ttu-id="43634-201">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="43634-202">**DMAChannel**</span><span class="sxs-lookup"><span data-stu-id="43634-202">**DMAChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-203">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="43634-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43634-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-205">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| DMA \| 001.1 ") </span><span class="sxs-lookup"><span data-stu-id="43634-205">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="43634-206">DMA 通道編號，物件的索引鍵值的一部分。</span><span class="sxs-lookup"><span data-stu-id="43634-206">DMA channel number, part of the object's key value.</span></span>

<span data-ttu-id="43634-207">這個屬性繼承自 [**CIM \_ DMA**](cim-dma.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-207">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="43634-208">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="43634-208">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-209">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="43634-209">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="43634-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-211">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="43634-211">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="43634-212">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="43634-212">Date and time the object was installed.</span></span> <span data-ttu-id="43634-213">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="43634-213">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="43634-214">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="43634-215">**MaxTransferSize**</span><span class="sxs-lookup"><span data-stu-id="43634-215">**MaxTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-216">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="43634-216">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43634-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-218">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。「DMTF \| 系統資源 DMA 資訊 \| 001.4」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「位元組」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-218">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="43634-219">這個 DMA 通道可以傳送的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="43634-219">Maximum number of bytes that can be transferred by this DMA channel.</span></span> <span data-ttu-id="43634-220">如果不明，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="43634-220">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="43634-221">這個屬性繼承自 [**CIM \_ DMA**](cim-dma.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-221">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="43634-222">**名稱**</span><span class="sxs-lookup"><span data-stu-id="43634-222">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-223">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="43634-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43634-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-225">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="43634-225">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="43634-226">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="43634-226">Label by which the object is known.</span></span> <span data-ttu-id="43634-227">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="43634-227">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="43634-228">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-228">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="43634-229">**通訊埠**</span><span class="sxs-lookup"><span data-stu-id="43634-229">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-230">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="43634-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43634-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-232">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 系統結構 \| [**CM \_ 部分 \_ 資源 \_ 描述**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)項 \| Dma \| 埠」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-232">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|[**CM\_PARTIAL\_RESOURCE\_DESCRIPTOR**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)\|Dma\|Port")</span></span>
</dt> </dl>

<span data-ttu-id="43634-233">主機匯流排介面卡所使用的 DMA 埠。</span><span class="sxs-lookup"><span data-stu-id="43634-233">DMA port used by the host bus adapter.</span></span> <span data-ttu-id="43634-234">這對 MCA 型別匯流排而言有意義。</span><span class="sxs-lookup"><span data-stu-id="43634-234">This is meaningful for MCA-type buses.</span></span>

<span data-ttu-id="43634-235">範例: 12</span><span class="sxs-lookup"><span data-stu-id="43634-235">Example: 12</span></span>

</dd> <dt>

<span data-ttu-id="43634-236">**狀態**</span><span class="sxs-lookup"><span data-stu-id="43634-236">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="43634-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43634-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-239">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="43634-239">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="43634-240">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="43634-240">Current status of the object.</span></span> <span data-ttu-id="43634-241">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="43634-241">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="43634-242">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="43634-242">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="43634-243">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="43634-243">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="43634-244">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="43634-244">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="43634-245">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="43634-245">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="43634-246">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-246">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="43634-247">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="43634-247">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="43634-248">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="43634-248">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="43634-249">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-249">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="43634-250">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-250">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43634-251">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-251">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="43634-252">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-252">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="43634-253">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-253">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="43634-254">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-254">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="43634-255">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-255">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="43634-256">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-256">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="43634-257">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="43634-257">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="43634-258">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-258">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="43634-259">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-259">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43634-260">**TransferWidths**</span><span class="sxs-lookup"><span data-stu-id="43634-260">**TransferWidths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-261">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="43634-261">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="43634-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-263">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。「DMTF \| 系統資源 DMA 資訊 \| 001.2」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「位」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-263">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="43634-264">此 DMA 通道支援的所有傳輸寬度陣列 (位) 。</span><span class="sxs-lookup"><span data-stu-id="43634-264">Array of all the transfer widths (in bits) supported by this DMA channel.</span></span> <span data-ttu-id="43634-265">如果不明，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="43634-265">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="43634-266">這個屬性繼承自 [**CIM \_ DMA**](cim-dma.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-266">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>



 <span data-ttu-id="43634-267"> (0)</span><span class="sxs-lookup"><span data-stu-id="43634-267">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="43634-268">(8)</span><span class="sxs-lookup"><span data-stu-id="43634-268">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="43634-269">(16)</span><span class="sxs-lookup"><span data-stu-id="43634-269">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="43634-270"> (32) </span><span class="sxs-lookup"><span data-stu-id="43634-270">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="43634-271">(64)</span><span class="sxs-lookup"><span data-stu-id="43634-271">(64)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="43634-272"> (128) </span><span class="sxs-lookup"><span data-stu-id="43634-272">(128)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43634-273">**TypeCTiming**</span><span class="sxs-lookup"><span data-stu-id="43634-273">**TypeCTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-274">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="43634-274">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43634-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-276">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統資源 DMA 資訊 \| 001.10」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-276">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="43634-277">支援 C 類型 (高載) 計時。</span><span class="sxs-lookup"><span data-stu-id="43634-277">Support for C type (burst) timing.</span></span>

<span data-ttu-id="43634-278">這個屬性繼承自 [**CIM \_ DMA**](cim-dma.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-278">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="43634-279">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="43634-279">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43634-280">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="43634-280">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="43634-281">**ISA 相容** (3) </span><span class="sxs-lookup"><span data-stu-id="43634-281">**ISA Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="43634-282">**不支援** (4) </span><span class="sxs-lookup"><span data-stu-id="43634-282">**Not Supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="43634-283">**支援** (5) </span><span class="sxs-lookup"><span data-stu-id="43634-283">**Supported** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43634-284">**WordMode**</span><span class="sxs-lookup"><span data-stu-id="43634-284">**WordMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43634-285">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="43634-285">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43634-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="43634-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43634-287">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統資源 DMA 資訊 \| 001.8」 ) </span><span class="sxs-lookup"><span data-stu-id="43634-287">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="43634-288">DMA 執行模式。</span><span class="sxs-lookup"><span data-stu-id="43634-288">DMA execution mode.</span></span>

<span data-ttu-id="43634-289">這個屬性繼承自 [**CIM \_ DMA**](cim-dma.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-289">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="43634-290"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="43634-290"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43634-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="43634-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="43634-292"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**無法在「依單字計數」模式中執行** (3) </span><span class="sxs-lookup"><span data-stu-id="43634-292"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Not execute in 'count by word' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="43634-293">不會在「依單字計數」模式中執行</span><span class="sxs-lookup"><span data-stu-id="43634-293">Does not execute in "count by word" mode</span></span>

</dd> <dt>

<span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="43634-294"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**在 [依單字計數] 模式下執行** (4) </span><span class="sxs-lookup"><span data-stu-id="43634-294"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Execute in 'count by word' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="43634-295">在「依單字計數」模式中執行</span><span class="sxs-lookup"><span data-stu-id="43634-295">Execute in "count by word" mode</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43634-296">備註</span><span class="sxs-lookup"><span data-stu-id="43634-296">Remarks</span></span>

<span data-ttu-id="43634-297">**Win32 \_ DMAChannel** 類別衍生自 [**CIM \_ DMA**](cim-dma.md)。</span><span class="sxs-lookup"><span data-stu-id="43634-297">The **Win32\_DMAChannel** class is derived from [**CIM\_DMA**](cim-dma.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43634-298">規格需求</span><span class="sxs-lookup"><span data-stu-id="43634-298">Requirements</span></span>



| <span data-ttu-id="43634-299">需求</span><span class="sxs-lookup"><span data-stu-id="43634-299">Requirement</span></span> | <span data-ttu-id="43634-300">值</span><span class="sxs-lookup"><span data-stu-id="43634-300">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43634-301">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43634-301">Minimum supported client</span></span><br/> | <span data-ttu-id="43634-302">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43634-302">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43634-303">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43634-303">Minimum supported server</span></span><br/> | <span data-ttu-id="43634-304">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43634-304">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43634-305">命名空間</span><span class="sxs-lookup"><span data-stu-id="43634-305">Namespace</span></span><br/>                | <span data-ttu-id="43634-306">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="43634-306">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="43634-307">MOF</span><span class="sxs-lookup"><span data-stu-id="43634-307">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43634-308"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="43634-308"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="43634-309">DLL</span><span class="sxs-lookup"><span data-stu-id="43634-309">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43634-310"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43634-310"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43634-311">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43634-311">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43634-312">**CIM \_ DMA**</span><span class="sxs-lookup"><span data-stu-id="43634-312">**CIM\_DMA**</span></span>](cim-dma.md)
</dt> <dt>

[<span data-ttu-id="43634-313">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="43634-313">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

