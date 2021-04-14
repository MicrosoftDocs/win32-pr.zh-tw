---
title: 'WINBIO_PRESENCE_PROPERTIES 聯集 (Winbio \_ 類型 .h) '
description: 包含 Windows 生物特徵辨識架構用來判斷是否有個人的生物特徵辨識值。
ms.assetid: 596CAA7F-35D2-442A-8041-BA1010DF5BAD
keywords:
- WINBIO_PRESENCE_PROPERTIES 聯集 Windows 生物特徵辨識架構 API
- PWINBIO_PRESENCE_PROPERTIES 聯集指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_PROPERTIES
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0568008b870953c34205706acc90cb22a2c0e92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464605"
---
# <a name="winbio_presence_properties-union"></a><span data-ttu-id="c80e8-105">WINBIO \_ 狀態 \_ 屬性聯集</span><span class="sxs-lookup"><span data-stu-id="c80e8-105">WINBIO\_PRESENCE\_PROPERTIES union</span></span>

<span data-ttu-id="c80e8-106">包含 Windows 生物特徵辨識架構用來判斷是否有個人的生物特徵辨識值。</span><span class="sxs-lookup"><span data-stu-id="c80e8-106">Contains biometric values that the Windows Biometric Framework used to determine that an individual was present.</span></span>

## <a name="syntax"></a><span data-ttu-id="c80e8-107">語法</span><span class="sxs-lookup"><span data-stu-id="c80e8-107">Syntax</span></span>


```C++
typedef union _WINBIO_PRESENCE_PROPERTIES {
  struct {
    RECT BoundingBox;
    LONG Distance;
  } FacialFeatures;
  struct {
    RECT  EyeBoundingBox_1;
    RECT  EyeBoundingBox_2;
    POINT PupilCenter_1;
    POINT PupilCenter_2;
    LONG  Distance;
  } Iris;
} WINBIO_PRESENCE_PROPERTIES, *PWINBIO_PRESENCE_PROPERTIES;
```



## <a name="members"></a><span data-ttu-id="c80e8-108">成員</span><span class="sxs-lookup"><span data-stu-id="c80e8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c80e8-109">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="c80e8-109">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="c80e8-110">Windows 生物特徵辨識架構用來判斷是否有個人的臉部特徵位置值。</span><span class="sxs-lookup"><span data-stu-id="c80e8-110">Values for the location of facial features that the Windows Biometric Framework used to determine that an individual was present.</span></span>

<dl> <dt>

<span data-ttu-id="c80e8-111">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="c80e8-111">**BoundingBox**</span></span>
</dt> <dd>

<span data-ttu-id="c80e8-112">以圖元為單位之臉部的相機框架內的位置。</span><span class="sxs-lookup"><span data-stu-id="c80e8-112">The position within the camera frame of the face of the individual, in pixels.</span></span> <span data-ttu-id="c80e8-113">相機框架的大小會決定這個位置的圖元數上限。</span><span class="sxs-lookup"><span data-stu-id="c80e8-113">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="c80e8-114">取得 [ **WINBIO \_ 屬性 \_ 擴充 \_ 感應器 \_ 資訊** ] 屬性，以決定相機框架的大小。</span><span class="sxs-lookup"><span data-stu-id="c80e8-114">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="c80e8-115">使用狀態監視器的用戶端必須執行調整作業，以將位置對應至相機框架。</span><span class="sxs-lookup"><span data-stu-id="c80e8-115">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame .</span></span>

</dd> <dt>

<span data-ttu-id="c80e8-116">**距離**</span><span class="sxs-lookup"><span data-stu-id="c80e8-116">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="c80e8-117">臉部的實際位置與臉部的理想焦距之間的距離。</span><span class="sxs-lookup"><span data-stu-id="c80e8-117">The distance between the actual location of the face and the ideal focal distance for the face.</span></span> <span data-ttu-id="c80e8-118">此值範圍從-100 到100。</span><span class="sxs-lookup"><span data-stu-id="c80e8-118">This value ranges from -100 to 100.</span></span> <span data-ttu-id="c80e8-119">0表示理想的距離，正值表示臉部的實際位置太遠，負值表示實際位置太近。</span><span class="sxs-lookup"><span data-stu-id="c80e8-119">0 indicates the ideal distance, positive values indicate that the actual location of the face is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c80e8-120">**虹膜**</span><span class="sxs-lookup"><span data-stu-id="c80e8-120">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="c80e8-121">Windows 生物特徵辨識架構用來判斷是否有個人的鳶尾花位置值。</span><span class="sxs-lookup"><span data-stu-id="c80e8-121">Values for iris location that the Windows Biometric Framework used to determine that an individual was present.</span></span>

<dl> <dt>

<span data-ttu-id="c80e8-122">**EyeBoundingBox \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c80e8-122">**EyeBoundingBox\_1**</span></span>
</dt> <dd>

<span data-ttu-id="c80e8-123">要註冊之個人 irises 的相機框架內的位置（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="c80e8-123">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="c80e8-124">如果鳶尾花辨識系統只監視一眼，這個位置就是該眼睛的鳶尾花。</span><span class="sxs-lookup"><span data-stu-id="c80e8-124">If the iris-recognition system is only monitoring one eye, this position is of the iris of that eye.</span></span> <span data-ttu-id="c80e8-125">如果鳶尾花辨識系統同時監視這兩眼，但攝影機框架中只會有一眼，這個位置就是相機框架中的眼睛鳶尾花。</span><span class="sxs-lookup"><span data-stu-id="c80e8-125">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the iris of the eye in the camera frame.</span></span> <span data-ttu-id="c80e8-126">如果鳶尾花辨識系統同時監視這兩個眼睛，而兩個眼睛都在攝影機框架中，則這個位置可能是個人的正確眼睛鳶尾花。</span><span class="sxs-lookup"><span data-stu-id="c80e8-126">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the iris of the right eye of the individual.</span></span>

<span data-ttu-id="c80e8-127">相機框架的大小會決定這個位置的圖元數上限。</span><span class="sxs-lookup"><span data-stu-id="c80e8-127">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="c80e8-128">取得 [ **WINBIO \_ 屬性 \_ 擴充 \_ 感應器 \_ 資訊** ] 屬性，以決定相機框架的大小。</span><span class="sxs-lookup"><span data-stu-id="c80e8-128">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="c80e8-129">使用狀態監視器的用戶端必須執行調整作業，以將位置對應至相機框架。</span><span class="sxs-lookup"><span data-stu-id="c80e8-129">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="c80e8-130">**EyeBoundingBox \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c80e8-130">**EyeBoundingBox\_2**</span></span>
</dt> <dd>

<span data-ttu-id="c80e8-131">要註冊之個人 irises 的相機框架內的位置（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="c80e8-131">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="c80e8-132">如果鳶尾花辨識系統只監視一眼，或是攝影機框架中只有一眼，則這個值是空的。</span><span class="sxs-lookup"><span data-stu-id="c80e8-132">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="c80e8-133">如果鳶尾花辨識系統同時監視這兩眼，而兩眼都在攝影機框架中，則這個位置可能是個人的最左邊鳶尾花。</span><span class="sxs-lookup"><span data-stu-id="c80e8-133">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of iris of the left eye of the individual.</span></span>

<span data-ttu-id="c80e8-134">相機框架的大小會決定這個位置的圖元數上限。</span><span class="sxs-lookup"><span data-stu-id="c80e8-134">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="c80e8-135">取得 [ **WINBIO \_ 屬性 \_ 擴充 \_ 感應器 \_ 資訊** ] 屬性，以決定相機框架的大小。</span><span class="sxs-lookup"><span data-stu-id="c80e8-135">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="c80e8-136">使用狀態監視器的用戶端必須執行調整作業，以將位置對應至相機框架。</span><span class="sxs-lookup"><span data-stu-id="c80e8-136">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="c80e8-137">**PupilCenter \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c80e8-137">**PupilCenter\_1**</span></span>
</dt> <dd>

<span data-ttu-id="c80e8-138">要註冊之個人的其中一個瞳孔中心位置。</span><span class="sxs-lookup"><span data-stu-id="c80e8-138">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="c80e8-139">如果鳶尾花辨識系統只監控一眼，這個位置就是該眼睛小學生的中心。</span><span class="sxs-lookup"><span data-stu-id="c80e8-139">If the iris-recognition system is only monitoring one eye, this position is of the center of the pupil of that eye.</span></span> <span data-ttu-id="c80e8-140">如果鳶尾花辨識系統同時監視這兩種情況，但攝影機框架中只會有一眼，這個位置就是相機框架中的眼睛小學生中心。</span><span class="sxs-lookup"><span data-stu-id="c80e8-140">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the center of the pupil of the eye in the camera frame.</span></span> <span data-ttu-id="c80e8-141">如果鳶尾花辨識系統同時監視這兩眼，而兩眼都在攝影機框架中，則這個位置可能是個人的適當眼睛小學生中心。</span><span class="sxs-lookup"><span data-stu-id="c80e8-141">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the right eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="c80e8-142">**PupilCenter \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c80e8-142">**PupilCenter\_2**</span></span>
</dt> <dd>

<span data-ttu-id="c80e8-143">要註冊之個人的其中一個瞳孔中心位置。</span><span class="sxs-lookup"><span data-stu-id="c80e8-143">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="c80e8-144">如果鳶尾花辨識系統只監視一眼，或是攝影機框架中只有一眼，則這個值是空的。</span><span class="sxs-lookup"><span data-stu-id="c80e8-144">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="c80e8-145">如果鳶尾花辨識系統同時監視這兩眼，而兩眼都在攝影機框架中，則這個位置可能是個人左側的小學生中心。</span><span class="sxs-lookup"><span data-stu-id="c80e8-145">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the left eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="c80e8-146">**距離**</span><span class="sxs-lookup"><span data-stu-id="c80e8-146">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="c80e8-147">鳶尾花的實際位置與鳶尾花的理想焦距距離之間的距離。</span><span class="sxs-lookup"><span data-stu-id="c80e8-147">The distance between the actual location of the iris and the ideal focal distance for the iris.</span></span> <span data-ttu-id="c80e8-148">此值範圍從-100 到100。</span><span class="sxs-lookup"><span data-stu-id="c80e8-148">This value ranges from -100 to 100.</span></span> <span data-ttu-id="c80e8-149">0表示理想的距離，正值表示鳶尾花的實際位置太遠，負值則表示實際位置太近。</span><span class="sxs-lookup"><span data-stu-id="c80e8-149">0 indicates the ideal distance, positive values indicate that the actual location of the iris is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c80e8-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="c80e8-150">Requirements</span></span>



| <span data-ttu-id="c80e8-151">需求</span><span class="sxs-lookup"><span data-stu-id="c80e8-151">Requirement</span></span> | <span data-ttu-id="c80e8-152">值</span><span class="sxs-lookup"><span data-stu-id="c80e8-152">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c80e8-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c80e8-153">Minimum supported client</span></span><br/> | <span data-ttu-id="c80e8-154">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c80e8-154">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="c80e8-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c80e8-155">Minimum supported server</span></span><br/> | <span data-ttu-id="c80e8-156">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c80e8-156">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="c80e8-157">標頭</span><span class="sxs-lookup"><span data-stu-id="c80e8-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="c80e8-158"><dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt></span><span class="sxs-lookup"><span data-stu-id="c80e8-158"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





