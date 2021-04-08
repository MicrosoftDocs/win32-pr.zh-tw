---
title: 'WINBIO_SENSOR_MODE 常數 (Winbio \_ 類型 .h) '
description: 設定感應器介面卡模式。
ms.assetid: fceaed5c-de59-4da7-9d7a-adeef353292f
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_UNKNOWN_MODE
- WINBIO_SENSOR_BASIC_MODE
- WINBIO_SENSOR_ADVANCED_MODE
- WINBIO_SENSOR_NAVIGATION_MODE
- WINBIO_SENSOR_SLEEP_MODE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fedf419a64b3629d0cccbcb3d56de31a4adf383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686512"
---
# <a name="winbio_sensor_mode-constants"></a><span data-ttu-id="e33ea-103">WINBIO \_ 感應器 \_ 模式常數</span><span class="sxs-lookup"><span data-stu-id="e33ea-103">WINBIO\_SENSOR\_MODE Constants</span></span>

<span data-ttu-id="e33ea-104">[**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn)函式中使用下列值來設定感應器介面卡模式。</span><span class="sxs-lookup"><span data-stu-id="e33ea-104">The following values are used in the [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) function to set the sensor adapter mode.</span></span>



| <span data-ttu-id="e33ea-105">常數</span><span class="sxs-lookup"><span data-stu-id="e33ea-105">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="e33ea-106">描述</span><span class="sxs-lookup"><span data-stu-id="e33ea-106">Description</span></span>                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <span data-ttu-id="e33ea-107"><dt>**WINBIO \_ 感應器 \_ 不明 \_ 模式**</dt></span><span class="sxs-lookup"><span data-stu-id="e33ea-107"><dt>**WINBIO\_SENSOR\_UNKNOWN\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="e33ea-108">作業模式未知。</span><span class="sxs-lookup"><span data-stu-id="e33ea-108">The operating mode is not known.</span></span><br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <span data-ttu-id="e33ea-109"><dt>**WINBIO \_ 感應器 \_ 基本 \_ 模式**</dt></span><span class="sxs-lookup"><span data-stu-id="e33ea-109"><dt>**WINBIO\_SENSOR\_BASIC\_MODE**</dt></span></span> </dl>                | <span data-ttu-id="e33ea-110">在基本模式下操作感應器。</span><span class="sxs-lookup"><span data-stu-id="e33ea-110">Operate the sensor in basic mode.</span></span> <span data-ttu-id="e33ea-111">感應器只能做為捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="e33ea-111">The sensor acts only as a capture device.</span></span> <span data-ttu-id="e33ea-112">不會使用任何存在的上架處理或儲存功能。</span><span class="sxs-lookup"><span data-stu-id="e33ea-112">Any onboard processing or storage capabilities that exist are not used.</span></span><br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <span data-ttu-id="e33ea-113"><dt>**WINBIO \_ 感應器 \_ ADVANCED \_ 模式**</dt></span><span class="sxs-lookup"><span data-stu-id="e33ea-113"><dt>**WINBIO\_SENSOR\_ADVANCED\_MODE**</dt></span></span> </dl>       | <span data-ttu-id="e33ea-114">以 advanced 模式操作感應器。</span><span class="sxs-lookup"><span data-stu-id="e33ea-114">Operate the sensor in advanced mode.</span></span> <span data-ttu-id="e33ea-115">感應器可以捕獲範例，並執行相符和儲存功能。</span><span class="sxs-lookup"><span data-stu-id="e33ea-115">The sensor can capture samples and perform matching and storage functions.</span></span><br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <span data-ttu-id="e33ea-116"><dt>**WINBIO \_ 感應器 \_ 流覽 \_ 模式**</dt></span><span class="sxs-lookup"><span data-stu-id="e33ea-116"><dt>**WINBIO\_SENSOR\_NAVIGATION\_MODE**</dt></span></span> </dl> | <span data-ttu-id="e33ea-117">以滑鼠墊的形式操作感應器。</span><span class="sxs-lookup"><span data-stu-id="e33ea-117">Operate the sensor as a mouse pad.</span></span> <span data-ttu-id="e33ea-118">目前不受支援。</span><span class="sxs-lookup"><span data-stu-id="e33ea-118">This is not currently supported.</span></span><br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <span data-ttu-id="e33ea-119"><dt>**WINBIO \_ 感應器 \_ 睡眠 \_ 模式**</dt></span><span class="sxs-lookup"><span data-stu-id="e33ea-119"><dt>**WINBIO\_SENSOR\_SLEEP\_MODE**</dt></span></span> </dl>                | <span data-ttu-id="e33ea-120">以睡眠模式操作感應器。</span><span class="sxs-lookup"><span data-stu-id="e33ea-120">Operate the sensor in sleep mode.</span></span><br/>                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="e33ea-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e33ea-121">Requirements</span></span>



| <span data-ttu-id="e33ea-122">需求</span><span class="sxs-lookup"><span data-stu-id="e33ea-122">Requirement</span></span> | <span data-ttu-id="e33ea-123">值</span><span class="sxs-lookup"><span data-stu-id="e33ea-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e33ea-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e33ea-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e33ea-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e33ea-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="e33ea-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e33ea-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e33ea-127">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e33ea-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e33ea-128">標頭</span><span class="sxs-lookup"><span data-stu-id="e33ea-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e33ea-129"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e33ea-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e33ea-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e33ea-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e33ea-131">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="e33ea-131">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





