---
title: 'WINBIO_ORIENTATION 常數 (Winbio \_ 類型 .h) '
description: 下列常數指定感應器元件指定為強制的可能相機方向。
ms.assetid: E44A6F17-5F38-47C7-947B-FB6FB79B1217
topic_type:
- apiref
api_name:
- WINBIO_ORIENTATION_UNSPECIFIED
- WINBIO_ORIENTATION_LANDSCAPE
- WINBIO_ORIENTATION_PORTRAIT
- WINBIO_ORIENTATION_ANY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e5c3a3150819eff6311c03b8cd279fad7dcf398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844383"
---
# <a name="winbio_orientation-constants"></a><span data-ttu-id="3fe0d-103">WINBIO \_ 方向常數</span><span class="sxs-lookup"><span data-stu-id="3fe0d-103">WINBIO\_ORIENTATION Constants</span></span>

<span data-ttu-id="3fe0d-104">下列常數指定感應器元件指定為強制的可能相機方向。</span><span class="sxs-lookup"><span data-stu-id="3fe0d-104">The following constants specify the possible camera orientations that the sensor component specifies as mandatory.</span></span>



| <span data-ttu-id="3fe0d-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="3fe0d-105">Constant/value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="3fe0d-106">Description</span><span class="sxs-lookup"><span data-stu-id="3fe0d-106">Description</span></span>                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| <span id="WINBIO_ORIENTATION_UNSPECIFIED"></span><span id="winbio_orientation_unspecified"></span><dl> <span data-ttu-id="3fe0d-107"><dt>**WINBIO \_\_未指定方向**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3fe0d-107"><dt>**WINBIO\_ORIENTATION\_UNSPECIFIED**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="3fe0d-108">未指定相機的強制方向。</span><span class="sxs-lookup"><span data-stu-id="3fe0d-108">A mandatory orientation for the camera is not specified.</span></span><br/> |
| <span id="WINBIO_ORIENTATION_LANDSCAPE"></span><span id="winbio_orientation_landscape"></span><dl> <span data-ttu-id="3fe0d-109"><dt>**WINBIO \_方向 \_ 橫向**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3fe0d-109"><dt>**WINBIO\_ORIENTATION\_LANDSCAPE**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="3fe0d-110">相機需要橫向方向。</span><span class="sxs-lookup"><span data-stu-id="3fe0d-110">The landscape orientation is required for the camera.</span></span><br/>    |
| <span id="WINBIO_ORIENTATION_PORTRAIT"></span><span id="winbio_orientation_portrait"></span><dl> <span data-ttu-id="3fe0d-111"><dt>**WINBIO \_方向 \_**</dt>直向 <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3fe0d-111"><dt>**WINBIO\_ORIENTATION\_PORTRAIT**</dt> <dt>2</dt></span></span> </dl>          | <span data-ttu-id="3fe0d-112">攝影機需要縱向方向。</span><span class="sxs-lookup"><span data-stu-id="3fe0d-112">The portrait orientation is required for the camera.</span></span><br/>     |
| <span id="WINBIO_ORIENTATION_ANY"></span><span id="winbio_orientation_any"></span><dl> <span data-ttu-id="3fe0d-113"><dt>**WINBIO \_\_任意**</dt> <dt>3</dt>方向</span><span class="sxs-lookup"><span data-stu-id="3fe0d-113"><dt>**WINBIO\_ORIENTATION\_ANY**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="3fe0d-114">相機允許任何方向。</span><span class="sxs-lookup"><span data-stu-id="3fe0d-114">Any orientation is permitted for the camera.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="3fe0d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fe0d-115">Requirements</span></span>



| <span data-ttu-id="3fe0d-116">需求</span><span class="sxs-lookup"><span data-stu-id="3fe0d-116">Requirement</span></span> | <span data-ttu-id="3fe0d-117">值</span><span class="sxs-lookup"><span data-stu-id="3fe0d-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fe0d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3fe0d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3fe0d-119">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fe0d-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="3fe0d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3fe0d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3fe0d-121">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fe0d-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="3fe0d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3fe0d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fe0d-123"><dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt></span><span class="sxs-lookup"><span data-stu-id="3fe0d-123"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fe0d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3fe0d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fe0d-125">**WINBIO \_ 擴充的 \_ 感應器 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="3fe0d-125">**WINBIO\_EXTENDED\_SENSOR\_INFO**</span></span>](winbio-extended-sensor-info.md)
</dt> </dl>

 

 





