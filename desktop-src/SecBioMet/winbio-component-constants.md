---
title: 'WINBIO_COMPONENT 常數 (Winbio \_ 類型 .h) '
description: 指定要使用的介面卡類型。
ms.assetid: f920788b-2175-4c01-81b5-e7b49111a7ac
topic_type:
- apiref
api_name:
- WINBIO_COMPONENT_SENSOR
- WINBIO_COMPONENT_ENGINE
- WINBIO_COMPONENT_STORAGE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07afe4fac08632133d4fa755717d83475b78c675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384246"
---
# <a name="winbio_component-constants"></a><span data-ttu-id="63eb3-103">WINBIO \_ 元件常數</span><span class="sxs-lookup"><span data-stu-id="63eb3-103">WINBIO\_COMPONENT Constants</span></span>

<span data-ttu-id="63eb3-104">呼叫 [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit) 或 [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged) 來指定所使用的介面卡類型時，可以使用下列常數。</span><span class="sxs-lookup"><span data-stu-id="63eb3-104">The following constants can be used when calling [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit) or [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged) to specify the type of adapter being used.</span></span>



| <span data-ttu-id="63eb3-105">常數</span><span class="sxs-lookup"><span data-stu-id="63eb3-105">Constant</span></span>                                                                                                                                                                                        | <span data-ttu-id="63eb3-106">描述</span><span class="sxs-lookup"><span data-stu-id="63eb3-106">Description</span></span>                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------|
| <span id="WINBIO_COMPONENT_SENSOR"></span><span id="winbio_component_sensor"></span><dl> <span data-ttu-id="63eb3-107"><dt>**WINBIO \_ 元件 \_ 感應器**</dt></span><span class="sxs-lookup"><span data-stu-id="63eb3-107"><dt>**WINBIO\_COMPONENT\_SENSOR**</dt></span></span> </dl>    | <span data-ttu-id="63eb3-108">指定感應器介面卡。</span><span class="sxs-lookup"><span data-stu-id="63eb3-108">Specifies a sensor adapter.</span></span><br/>  |
| <span id="WINBIO_COMPONENT_ENGINE"></span><span id="winbio_component_engine"></span><dl> <span data-ttu-id="63eb3-109"><dt>**WINBIO \_ 元件 \_ 引擎**</dt></span><span class="sxs-lookup"><span data-stu-id="63eb3-109"><dt>**WINBIO\_COMPONENT\_ENGINE**</dt></span></span> </dl>    | <span data-ttu-id="63eb3-110">指定引擎介面卡。</span><span class="sxs-lookup"><span data-stu-id="63eb3-110">Specifies an engine adapter.</span></span><br/> |
| <span id="WINBIO_COMPONENT_STORAGE"></span><span id="winbio_component_storage"></span><dl> <span data-ttu-id="63eb3-111"><dt>**WINBIO \_ 元件 \_ 儲存體**</dt></span><span class="sxs-lookup"><span data-stu-id="63eb3-111"><dt>**WINBIO\_COMPONENT\_STORAGE**</dt></span></span> </dl> | <span data-ttu-id="63eb3-112">指定存放裝置介面卡。</span><span class="sxs-lookup"><span data-stu-id="63eb3-112">Specifies a storage adapter.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="63eb3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="63eb3-113">Requirements</span></span>



| <span data-ttu-id="63eb3-114">需求</span><span class="sxs-lookup"><span data-stu-id="63eb3-114">Requirement</span></span> | <span data-ttu-id="63eb3-115">值</span><span class="sxs-lookup"><span data-stu-id="63eb3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63eb3-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63eb3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="63eb3-117">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63eb3-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="63eb3-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63eb3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="63eb3-119">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63eb3-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="63eb3-120">標頭</span><span class="sxs-lookup"><span data-stu-id="63eb3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="63eb3-121"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="63eb3-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63eb3-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63eb3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63eb3-123">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="63eb3-123">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





