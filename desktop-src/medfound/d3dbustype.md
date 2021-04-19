---
description: 指定圖形介面卡所使用的 i/o 匯流排類型。
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
title: 'D3DBUSTYPE 列舉 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBUSTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 807e5a57c4abbf57c241643a3e7fea47606fbf75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973987"
---
# <a name="d3dbustype-enumeration"></a><span data-ttu-id="4696c-103">D3DBUSTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="4696c-103">D3DBUSTYPE enumeration</span></span>

<span data-ttu-id="4696c-104">指定圖形介面卡所使用的 i/o 匯流排類型。</span><span class="sxs-lookup"><span data-stu-id="4696c-104">Specifies the type of I/O bus used by the graphics adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4696c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4696c-105">Syntax</span></span>


```C++
typedef enum  { 
  D3DBUSTYPE_OTHER                                             = 0x00000000,
  D3DBUSTYPE_PCI                                               = 0x00000001,
  D3DBUSTYPE_PCIX                                              = 0x00000002,
  D3DBUSTYPE_PCIEXPRESS                                        = 0x00000003,
  D3DBUSTYPE_AGP                                               = 0x00000004,
  D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET                        = 0x00010000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP           = 0x00020000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET         = 0x00030000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR                 = 0x00040000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE  = 0x00050000,
  D3DBUSIMPL_MODIFIER_NON_STANDARD                             = 0x80000000
} D3DBUSTYPE;
```



## <a name="constants"></a><span data-ttu-id="4696c-106">常數</span><span class="sxs-lookup"><span data-stu-id="4696c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4696c-107"><span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_ 其他**</span><span class="sxs-lookup"><span data-stu-id="4696c-107"><span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE\_OTHER**</span></span>
</dt> <dd>

<span data-ttu-id="4696c-108">指出此處所列類型以外的匯流排類型。</span><span class="sxs-lookup"><span data-stu-id="4696c-108">Indicates a type of bus other than the types listed here.</span></span>

</dd> <dt>

<span data-ttu-id="4696c-109"><span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="4696c-109"><span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE\_PCI**</span></span>
</dt> <dd>

<span data-ttu-id="4696c-110">PCI 匯流排。</span><span class="sxs-lookup"><span data-stu-id="4696c-110">PCI bus.</span></span>

</dd> <dt>

<span data-ttu-id="4696c-111"><span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE \_ PCIX**</span><span class="sxs-lookup"><span data-stu-id="4696c-111"><span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE\_PCIX**</span></span>
</dt> <dd>

<span data-ttu-id="4696c-112">PCI X 匯流排。</span><span class="sxs-lookup"><span data-stu-id="4696c-112">PCI-X bus.</span></span>

</dd> <dt>

<span data-ttu-id="4696c-113"><span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE \_ PCIEXPRESS**</span><span class="sxs-lookup"><span data-stu-id="4696c-113"><span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE\_PCIEXPRESS**</span></span>
</dt> <dd>

<span data-ttu-id="4696c-114">PCI Express 匯流排。</span><span class="sxs-lookup"><span data-stu-id="4696c-114">PCI Express bus.</span></span>

</dd> <dt>

<span data-ttu-id="4696c-115"><span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE \_ AGP**</span><span class="sxs-lookup"><span data-stu-id="4696c-115"><span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE\_AGP**</span></span>
</dt> <dd>

<span data-ttu-id="4696c-116">高速圖形連接埠 (AGP) 匯流排。</span><span class="sxs-lookup"><span data-stu-id="4696c-116">Accelerated Graphics Port (AGP) bus.</span></span>

</dd> <dt>

<span data-ttu-id="4696c-117"><span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**\_ \_ 在晶片內部 \_ D3DBUSIMPL 修飾詞 \_**</span><span class="sxs-lookup"><span data-stu-id="4696c-117"><span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**D3DBUSIMPL\_MODIFIER\_INSIDE\_OF\_CHIPSET**</span></span>
</dt> <dd>

<span data-ttu-id="4696c-118">圖形介面卡的執行是在主機板晶片的北方 bridge 中。</span><span class="sxs-lookup"><span data-stu-id="4696c-118">The implementation for the graphics adapter is in a motherboard chipset's north bridge.</span></span> <span data-ttu-id="4696c-119">此旗標表示資料永遠不會超出展開匯流排 (例如 PCI 或 AGP) 從主儲存體傳輸到圖形介面卡時。</span><span class="sxs-lookup"><span data-stu-id="4696c-119">This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4696c-120"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**D3DBUSIMPL \_ 修飾 \_ 詞 \_ 在 \_ \_ 主機板 \_ 到 \_ 晶片的軌跡**</span><span class="sxs-lookup"><span data-stu-id="4696c-120"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**D3DBUSIMPL\_MODIFIER\_TRACKS\_ON\_MOTHER\_BOARD\_TO\_CHIP**</span></span>
</dt> <dd>

<span data-ttu-id="4696c-121">指出圖形介面卡已透過板上的曲目，連接至主機板晶片的北方橋接器，而所有圖形介面卡的晶片都會焊接到主機板上。</span><span class="sxs-lookup"><span data-stu-id="4696c-121">Indicates that the graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard and all of the graphics adapter's chips are soldered to the motherboard.</span></span> <span data-ttu-id="4696c-122">此旗標表示資料永遠不會超出展開匯流排 (例如 PCI 或 AGP) 從主儲存體傳輸到圖形介面卡時。</span><span class="sxs-lookup"><span data-stu-id="4696c-122">This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4696c-123"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**將 D3DBUSIMPL 修飾詞從 \_ \_ \_ \_ \_ 主機板 \_ 到 \_ 通訊端的追蹤**</span><span class="sxs-lookup"><span data-stu-id="4696c-123"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**D3DBUSIMPL\_MODIFIER\_TRACKS\_ON\_MOTHER\_BOARD\_TO\_SOCKET**</span></span>
</dt> <dd>

<span data-ttu-id="4696c-124">圖形介面卡會透過在主機板上進行追蹤，連接至主機板晶片的北方橋接器，而所有圖形介面卡的晶片都會透過通訊端連接至主機板。</span><span class="sxs-lookup"><span data-stu-id="4696c-124">The graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard, and all of the graphics adapter's chips are connected through sockets to the motherboard.</span></span>

</dd> <dt>

<span data-ttu-id="4696c-125"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**D3DBUSIMPL \_ 修飾詞 \_ 子 \_ 面板 \_ 連接器**</span><span class="sxs-lookup"><span data-stu-id="4696c-125"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**D3DBUSIMPL\_MODIFIER\_DAUGHTER\_BOARD\_CONNECTOR**</span></span>
</dt> <dd>

<span data-ttu-id="4696c-126">圖形介面卡透過 daughterboard 連接器連線至主機板。</span><span class="sxs-lookup"><span data-stu-id="4696c-126">The graphics adapter is connected to the motherboard through a daughterboard connector.</span></span>

</dd> <dt>

<span data-ttu-id="4696c-127"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**\_ \_ \_ \_ \_ \_ NUAE 內的 \_ D3DBUSIMPL 修飾詞子面板連接器**</span><span class="sxs-lookup"><span data-stu-id="4696c-127"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**D3DBUSIMPL\_MODIFIER\_DAUGHTER\_BOARD\_CONNECTOR\_INSIDE\_OF\_NUAE**</span></span>
</dt> <dd>

<span data-ttu-id="4696c-128">圖形介面卡透過 daughterboard 連接器連線至主機板，而圖形介面卡位於無法存取使用者的主機殼內。</span><span class="sxs-lookup"><span data-stu-id="4696c-128">The graphics adapter is connected to the motherboard through a daughterboard connector, and the graphics adapter is inside an enclosure that is not user accessible.</span></span>

</dd> <dt>

<span data-ttu-id="4696c-129"><span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**D3DBUSIMPL \_ 修飾詞 \_ 非 \_ 標準**</span><span class="sxs-lookup"><span data-stu-id="4696c-129"><span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**D3DBUSIMPL\_MODIFIER\_NON\_STANDARD**</span></span>
</dt> <dd>

<span data-ttu-id="4696c-130">其中一個 D3DBUSIMPL \_ 修飾詞 \_ 修飾詞 \_ Xxx 旗標已設定。</span><span class="sxs-lookup"><span data-stu-id="4696c-130">One of the D3DBUSIMPL\_MODIFIER\_MODIFIER\_Xxx flags is set.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4696c-131">備註</span><span class="sxs-lookup"><span data-stu-id="4696c-131">Remarks</span></span>

<span data-ttu-id="4696c-132">最多可以設定三個旗標。</span><span class="sxs-lookup"><span data-stu-id="4696c-132">As many as three flags can be set.</span></span> <span data-ttu-id="4696c-133">範圍從0x00 到0x04 的旗標 (**D3DBUSTYPE \_ Xxx**) 提供基本的匯流排類型。</span><span class="sxs-lookup"><span data-stu-id="4696c-133">Flags in the range 0x00 through 0x04 (**D3DBUSTYPE\_Xxx**) provide the basic bus type.</span></span> <span data-ttu-id="4696c-134">範圍0x10000 到 0x50000 (**D3DBUSIMPL \_ 修飾詞 \_ Xxx** 的旗標，) 修改基本描述。</span><span class="sxs-lookup"><span data-stu-id="4696c-134">Flags in the range 0x10000 through 0x50000 (**D3DBUSIMPL\_MODIFIER\_Xxx**) modify the basic description.</span></span> <span data-ttu-id="4696c-135">驅動程式會設定一個匯流排類型旗標，而且可以設定零或一個修飾詞旗標。</span><span class="sxs-lookup"><span data-stu-id="4696c-135">The driver sets one bus-type flag, and can set zero or one modifier flag.</span></span> <span data-ttu-id="4696c-136">如果驅動程式設定了修飾詞旗標，也會設定 **D3DBUSIMPL \_ 修飾詞 \_ 非 \_ 標準** 旗標。</span><span class="sxs-lookup"><span data-stu-id="4696c-136">If the driver sets a modifier flag, it also sets the **D3DBUSIMPL\_MODIFIER\_NON\_STANDARD** flag.</span></span> <span data-ttu-id="4696c-137">旗標會與位 **or** 合併。</span><span class="sxs-lookup"><span data-stu-id="4696c-137">Flags are combined with a bitwise **OR**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4696c-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="4696c-138">Requirements</span></span>



| <span data-ttu-id="4696c-139">需求</span><span class="sxs-lookup"><span data-stu-id="4696c-139">Requirement</span></span> | <span data-ttu-id="4696c-140">值</span><span class="sxs-lookup"><span data-stu-id="4696c-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4696c-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4696c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4696c-142">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4696c-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4696c-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4696c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4696c-144">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4696c-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4696c-145">標頭</span><span class="sxs-lookup"><span data-stu-id="4696c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="4696c-146"><dt>D3d9types (包含 D3d9) </dt></span><span class="sxs-lookup"><span data-stu-id="4696c-146"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4696c-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4696c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4696c-148">Direct3D 影片列舉</span><span class="sxs-lookup"><span data-stu-id="4696c-148">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> </dl>

 

 




