---
title: 'WINBIO_BIOMETRIC_SENSOR_SUBTYPE 常數 (Winbio \_ 類型 .h) '
description: 指定用來上架感應器功能的位元遮罩。
ms.assetid: ED2A26BC-AED4-4304-9A17-A9BA126B0AFC
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_SUBTYPE_UNKNOWN
- WINBIO_FP_SENSOR_SUBTYPE_SWIPE
- WINBIO_FP_SENSOR_SUBTYPE_TOUCH
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26229634f3d404921f877bb65d83f7d75634ecbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384378"
---
# <a name="winbio_biometric_sensor_subtype-constants"></a><span data-ttu-id="62b0c-103">WINBIO \_ 生物特徵辨識 \_ 感應器 \_ 子類型常數</span><span class="sxs-lookup"><span data-stu-id="62b0c-103">WINBIO\_BIOMETRIC\_SENSOR\_SUBTYPE Constants</span></span>

<span data-ttu-id="62b0c-104">下列常數可用來當做 [**WINBIO \_ 單元 \_ 架構**](winbio-unit-schema.md)之 *功能* 參數的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="62b0c-104">The following constants can be used as a bitmask for the *Capabilities* parameter of the [**WINBIO\_UNIT\_SCHEMA**](winbio-unit-schema.md) structure.</span></span> <span data-ttu-id="62b0c-105">這些是指上架的感應器功能。</span><span class="sxs-lookup"><span data-stu-id="62b0c-105">These refer to the onboard sensor capabilities.</span></span>



| <span data-ttu-id="62b0c-106">常數</span><span class="sxs-lookup"><span data-stu-id="62b0c-106">Constant</span></span>                                                                                                                                                                                                            | <span data-ttu-id="62b0c-107">描述</span><span class="sxs-lookup"><span data-stu-id="62b0c-107">Description</span></span>                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="WINBIO_SENSOR_SUBTYPE_UNKNOWN"></span><span id="winbio_sensor_subtype_unknown"></span><dl> <span data-ttu-id="62b0c-108"><dt>**WINBIO \_ 感應器 \_ 子類型 \_ 不明**</dt></span><span class="sxs-lookup"><span data-stu-id="62b0c-108"><dt>**WINBIO\_SENSOR\_SUBTYPE\_UNKNOWN**</dt></span></span> </dl>     | <span data-ttu-id="62b0c-109">感應器子類型未知。</span><span class="sxs-lookup"><span data-stu-id="62b0c-109">The sensor sub types is not known.</span></span><br/>      |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_SWIPE"></span><span id="winbio_fp_sensor_subtype_swipe"></span><dl> <span data-ttu-id="62b0c-110"><dt>**WINBIO \_ FP \_ 感應器 \_ 子類型 \_ 滑動**</dt></span><span class="sxs-lookup"><span data-stu-id="62b0c-110"><dt>**WINBIO\_FP\_SENSOR\_SUBTYPE\_SWIPE**</dt></span></span> </dl> | <span data-ttu-id="62b0c-111">感應器支援指紋撥動。</span><span class="sxs-lookup"><span data-stu-id="62b0c-111">The sensor supports fingerprint swipes.</span></span><br/> |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_TOUCH"></span><span id="winbio_fp_sensor_subtype_touch"></span><dl> <span data-ttu-id="62b0c-112"><dt>**WINBIO \_ FP \_ 感應器 \_ 子類型 \_ 觸控**</dt></span><span class="sxs-lookup"><span data-stu-id="62b0c-112"><dt>**WINBIO\_FP\_SENSOR\_SUBTYPE\_TOUCH**</dt></span></span> </dl> | <span data-ttu-id="62b0c-113">感應器支援手指觸控。</span><span class="sxs-lookup"><span data-stu-id="62b0c-113">The sensor supports finger touches.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="62b0c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="62b0c-114">Requirements</span></span>



| <span data-ttu-id="62b0c-115">需求</span><span class="sxs-lookup"><span data-stu-id="62b0c-115">Requirement</span></span> | <span data-ttu-id="62b0c-116">值</span><span class="sxs-lookup"><span data-stu-id="62b0c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b0c-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62b0c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="62b0c-118">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62b0c-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="62b0c-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62b0c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="62b0c-120">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62b0c-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="62b0c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="62b0c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="62b0c-122"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="62b0c-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62b0c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62b0c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62b0c-124">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="62b0c-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="62b0c-125">**WINBIO \_ 單元 \_ 架構**</span><span class="sxs-lookup"><span data-stu-id="62b0c-125">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





