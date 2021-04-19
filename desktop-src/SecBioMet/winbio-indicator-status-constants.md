---
title: 'WINBIO_INDICATOR_STATUS 常數 (Winbio \_ 類型 .h) '
description: 設定指標燈。
ms.assetid: 1e00ff9d-6693-4763-8ac3-b42d2a3e987d
topic_type:
- apiref
api_name:
- WINBIO_INDICATOR_ON
- WINBIO_INDICATOR_OFF
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7693fbd2b9b37067738774d172f4bb482edb06e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967770"
---
# <a name="winbio_indicator_status-constants"></a><span data-ttu-id="23576-103">WINBIO \_ 指標 \_ 狀態常數</span><span class="sxs-lookup"><span data-stu-id="23576-103">WINBIO\_INDICATOR\_STATUS Constants</span></span>

<span data-ttu-id="23576-104">您可以使用下列值來設定指標光線。</span><span class="sxs-lookup"><span data-stu-id="23576-104">The following values can be used to set an indicator light.</span></span> <span data-ttu-id="23576-105">感應器預設不會有燈亮，但應用程式可以使用這些值來啟用或停用指標燈。</span><span class="sxs-lookup"><span data-stu-id="23576-105">By default, sensors will not have a light on, but applications can use these values to enable or disable indicator lights.</span></span> <span data-ttu-id="23576-106">[ **WINBIO \_ 感應器 \_ 狀態值** ] 提供有關指標燈狀態的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="23576-106">The **WINBIO\_SENSOR\_STATUS** value provides more detail about the status of an indicator light that is on.</span></span> <span data-ttu-id="23576-107">如需詳細資訊，請參閱下列函數：</span><span class="sxs-lookup"><span data-stu-id="23576-107">For more information, see the following functions:</span></span>

-   [<span data-ttu-id="23576-108">**SensorAdapterSetIndicatorStatus**</span><span class="sxs-lookup"><span data-stu-id="23576-108">**SensorAdapterSetIndicatorStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)
-   [<span data-ttu-id="23576-109">**SensorAdapterGetIndicatorStatus**</span><span class="sxs-lookup"><span data-stu-id="23576-109">**SensorAdapterGetIndicatorStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)
-   [<span data-ttu-id="23576-110">**SensorAdapterQueryStatus**</span><span class="sxs-lookup"><span data-stu-id="23576-110">**SensorAdapterQueryStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)



| <span data-ttu-id="23576-111">常數</span><span class="sxs-lookup"><span data-stu-id="23576-111">Constant</span></span>                                                                                                                                                                            | <span data-ttu-id="23576-112">描述</span><span class="sxs-lookup"><span data-stu-id="23576-112">Description</span></span>                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="WINBIO_INDICATOR_ON"></span><span id="winbio_indicator_on"></span><dl> <span data-ttu-id="23576-113"><dt>**WINBIO \_ 指標 \_ 開啟**</dt></span><span class="sxs-lookup"><span data-stu-id="23576-113"><dt>**WINBIO\_INDICATOR\_ON**</dt></span></span> </dl>    | <span data-ttu-id="23576-114">感應器指示燈亮起。</span><span class="sxs-lookup"><span data-stu-id="23576-114">The sensor indicator light is on.</span></span><br/>  |
| <span id="WINBIO_INDICATOR_OFF"></span><span id="winbio_indicator_off"></span><dl> <span data-ttu-id="23576-115"><dt>**WINBIO \_ 指標 \_ 關閉**</dt></span><span class="sxs-lookup"><span data-stu-id="23576-115"><dt>**WINBIO\_INDICATOR\_OFF**</dt></span></span> </dl> | <span data-ttu-id="23576-116">感應器指示燈亮燈。</span><span class="sxs-lookup"><span data-stu-id="23576-116">The sensor indicator light is off.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="23576-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="23576-117">Requirements</span></span>



| <span data-ttu-id="23576-118">需求</span><span class="sxs-lookup"><span data-stu-id="23576-118">Requirement</span></span> | <span data-ttu-id="23576-119">值</span><span class="sxs-lookup"><span data-stu-id="23576-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23576-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23576-120">Minimum supported client</span></span><br/> | <span data-ttu-id="23576-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23576-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="23576-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23576-122">Minimum supported server</span></span><br/> | <span data-ttu-id="23576-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23576-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="23576-124">標頭</span><span class="sxs-lookup"><span data-stu-id="23576-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="23576-125"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="23576-125"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23576-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23576-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23576-127">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="23576-127">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





