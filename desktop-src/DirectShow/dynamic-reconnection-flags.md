---
description: 下列旗標指定轉譯時要使用的動態重新連接層級。
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: '動態重新連接旗標 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONNECTF_DYNAMIC_NONE
- CONNECTF_DYNAMIC_SOURCES
- CONNECTF_DYNAMIC_EFFECTS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 322c7d88cd84857ba0ebc1d19ed76a24e11cc3fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994246"
---
# <a name="dynamic-reconnection-flags"></a><span data-ttu-id="42ab7-103">動態重新連接旗標</span><span class="sxs-lookup"><span data-stu-id="42ab7-103">Dynamic Reconnection Flags</span></span>

<span data-ttu-id="42ab7-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="42ab7-104">\[Deprecated.</span></span> <span data-ttu-id="42ab7-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="42ab7-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="42ab7-106">下列旗標指定轉譯時要使用的動態重新連接層級。</span><span class="sxs-lookup"><span data-stu-id="42ab7-106">The following flags specify the level of dynamic reconnection to use during rendering.</span></span>



| <span data-ttu-id="42ab7-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="42ab7-107">Constant/value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="42ab7-108">Description</span><span class="sxs-lookup"><span data-stu-id="42ab7-108">Description</span></span>                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <span data-ttu-id="42ab7-109"><dt>**CONNECTF \_DYNAMIC \_ NONE**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="42ab7-109"><dt>**CONNECTF\_DYNAMIC\_NONE**</dt> <dt>0x00</dt></span></span> </dl>          | <span data-ttu-id="42ab7-110">無動態重新連接。</span><span class="sxs-lookup"><span data-stu-id="42ab7-110">No dynamic reconnection.</span></span> <span data-ttu-id="42ab7-111">先載入所有專案，然後再呈現專案。</span><span class="sxs-lookup"><span data-stu-id="42ab7-111">Load everything before rendering the project.</span></span><br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <span data-ttu-id="42ab7-112"><dt>**CONNECTF \_動態 \_ 來源**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="42ab7-112"><dt>**CONNECTF\_DYNAMIC\_SOURCES**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="42ab7-113">只在需要時才載入來源。</span><span class="sxs-lookup"><span data-stu-id="42ab7-113">Load sources only as needed.</span></span><br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <span data-ttu-id="42ab7-114"><dt>**CONNECTF \_動態 \_ 效果**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="42ab7-114"><dt>**CONNECTF\_DYNAMIC\_EFFECTS**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="42ab7-115">保留的。</span><span class="sxs-lookup"><span data-stu-id="42ab7-115">Reserved.</span></span> <span data-ttu-id="42ab7-116">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="42ab7-116">Do not use.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="42ab7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="42ab7-117">Requirements</span></span>



| <span data-ttu-id="42ab7-118">需求</span><span class="sxs-lookup"><span data-stu-id="42ab7-118">Requirement</span></span> | <span data-ttu-id="42ab7-119">值</span><span class="sxs-lookup"><span data-stu-id="42ab7-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="42ab7-120">標頭</span><span class="sxs-lookup"><span data-stu-id="42ab7-120">Header</span></span><br/> | <dl> <span data-ttu-id="42ab7-121"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="42ab7-121"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42ab7-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42ab7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42ab7-123">**IRenderEngine::SetDynamicReconnectLevel**</span><span class="sxs-lookup"><span data-stu-id="42ab7-123">**IRenderEngine::SetDynamicReconnectLevel**</span></span>](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




