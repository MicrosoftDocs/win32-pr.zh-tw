---
description: WPD \_ 裝置 \_ 類型列舉類型說明不同的 Windows 可攜式裝置 (WPD) 類型通常用來判斷可攜式裝置的基本分類和視覺外觀。
ms.assetid: 51714e0f-e9b7-4474-a8bb-da3875ef5399
title: 'WPD_DEVICE_TYPES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3e71acf200a95bba05b7298a5824bfa353e4a90b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999078"
---
# <a name="wpd_device_types-enumeration"></a><span data-ttu-id="c396a-103">WPD \_ 裝置 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="c396a-103">WPD\_DEVICE\_TYPES enumeration</span></span>

<span data-ttu-id="c396a-104">**WPD \_ 裝置 \_ 類型** 列舉類型說明不同的 WINDOWS 可攜式裝置 (WPD) 類型通常用來判斷可攜式裝置的基本分類和視覺外觀。</span><span class="sxs-lookup"><span data-stu-id="c396a-104">The **WPD\_DEVICE\_TYPES** enumeration type describes the different Windows Portable Device (WPD) types commonly used to determine the basic classification and visual appearance of a portable device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c396a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c396a-105">Syntax</span></span>


```C++
typedef enum tagWPD_DEVICE_TYPES { 
  WPD_DEVICE_TYPE_GENERIC                       = 0,
  WPD_DEVICE_TYPE_CAMERA                        = 1,
  WPD_DEVICE_TYPE_MEDIA_PLAYER                  = 2,
  WPD_DEVICE_TYPE_PHONE                         = 3,
  WPD_DEVICE_TYPE_VIDEO                         = 4,
  WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER  = 5,
  WPD_DEVICE_TYPE_AUDIO_RECORDER                = 6
} WPD_DEVICE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="c396a-106">常數</span><span class="sxs-lookup"><span data-stu-id="c396a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c396a-107"><span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**WPD \_ 裝置 \_ 類型 \_ 泛型**</span><span class="sxs-lookup"><span data-stu-id="c396a-107"><span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**WPD\_DEVICE\_TYPE\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="c396a-108">泛型 WPD，包含不屬於其他 [**WPD \_ 裝置 \_ 類型**](wpd-device-types.md) 列舉值的多功能裝置。</span><span class="sxs-lookup"><span data-stu-id="c396a-108">A generic WPD that includes multifunction devices that do not fall into one of the other [**WPD\_DEVICE\_TYPES**](wpd-device-types.md) enumeration values.</span></span>

</dd> <dt>

<span data-ttu-id="c396a-109"><span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**WPD \_ 裝置 \_ 類型 \_ 相機**</span><span class="sxs-lookup"><span data-stu-id="c396a-109"><span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**WPD\_DEVICE\_TYPE\_CAMERA**</span></span>
</dt> <dd>

<span data-ttu-id="c396a-110">攝影機裝置，例如數位靜止相機。</span><span class="sxs-lookup"><span data-stu-id="c396a-110">A camera device, such as a digital still camera.</span></span>

</dd> <dt>

<span data-ttu-id="c396a-111"><span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**WPD \_ 裝置 \_ 類型 \_ 媒體 \_ 播放機**</span><span class="sxs-lookup"><span data-stu-id="c396a-111"><span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER**</span></span>
</dt> <dd>

<span data-ttu-id="c396a-112">支援播放音訊、影片或觀賞圖片的 media player 裝置，例如便攜音樂播放機或便攜媒體中心。</span><span class="sxs-lookup"><span data-stu-id="c396a-112">A media player device that supports playing audio, video, or viewing pictures, such as a portable music player or portable media center.</span></span> <span data-ttu-id="c396a-113">並非所有這項功能都分類為 WPD \_ 裝置 \_ 類型的 \_ MEDIA \_ PLAYER。</span><span class="sxs-lookup"><span data-stu-id="c396a-113">Not all of this functionally is classified as a WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER.</span></span> <span data-ttu-id="c396a-114">例如，可移植音樂播放機裝置會分類為 WPD \_ 裝置 \_ 類型 \_ 媒體 \_ 播放機。</span><span class="sxs-lookup"><span data-stu-id="c396a-114">For example, portable music player devices are classified as WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER.</span></span>

</dd> <dt>

<span data-ttu-id="c396a-115"><span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**WPD \_ 裝置 \_ 類型 \_ 電話**</span><span class="sxs-lookup"><span data-stu-id="c396a-115"><span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**WPD\_DEVICE\_TYPE\_PHONE**</span></span>
</dt> <dd>

<span data-ttu-id="c396a-116">電話裝置，例如行動電話。</span><span class="sxs-lookup"><span data-stu-id="c396a-116">A phone device, such as a mobile phone.</span></span>

</dd> <dt>

<span data-ttu-id="c396a-117"><span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**WPD \_ 裝置 \_ 類型 \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="c396a-117"><span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**WPD\_DEVICE\_TYPE\_VIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="c396a-118">影片裝置。</span><span class="sxs-lookup"><span data-stu-id="c396a-118">A video device.</span></span>

</dd> <dt>

<span data-ttu-id="c396a-119"><span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**WPD \_ 裝置 \_ 類型 \_ 個人 \_ 資訊 \_ 管理員**</span><span class="sxs-lookup"><span data-stu-id="c396a-119"><span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**WPD\_DEVICE\_TYPE\_PERSONAL\_INFORMATION\_MANAGER**</span></span>
</dt> <dd>

<span data-ttu-id="c396a-120">個人資訊管理員裝置。</span><span class="sxs-lookup"><span data-stu-id="c396a-120">A personal information manager device.</span></span>

</dd> <dt>

<span data-ttu-id="c396a-121"><span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**WPD \_ 裝置 \_ 類型 \_ 音訊 \_ 錄製器**</span><span class="sxs-lookup"><span data-stu-id="c396a-121"><span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**WPD\_DEVICE\_TYPE\_AUDIO\_RECORDER**</span></span>
</dt> <dd>

<span data-ttu-id="c396a-122">音訊錄製器裝置。</span><span class="sxs-lookup"><span data-stu-id="c396a-122">An audio recorder device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c396a-123">備註</span><span class="sxs-lookup"><span data-stu-id="c396a-123">Remarks</span></span>

<span data-ttu-id="c396a-124">**WPD \_裝置 \_ 類型** 會使用 [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) 介面來讀取。</span><span class="sxs-lookup"><span data-stu-id="c396a-124">**WPD\_DEVICE\_TYPES** are read using the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface.</span></span> <span data-ttu-id="c396a-125">WPD 應用程式可能會使用這些值來判斷裝置的一般視覺外觀。</span><span class="sxs-lookup"><span data-stu-id="c396a-125">WPD applications may use these values to determine the generic visual appearance of the device.</span></span> <span data-ttu-id="c396a-126">也就是，針對類似相機的裝置會顯示相機圖片，會針對類似電話的裝置顯示行動電話圖片等等。</span><span class="sxs-lookup"><span data-stu-id="c396a-126">That is, a camera picture is displayed for camera-like devices, a mobile phone picture is displayed for phone-like devices, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="c396a-127">WPD 應用程式必須使用可攜式裝置的功能來判斷功能，而不是 **WPD \_ 裝置 \_ 類型** 值。</span><span class="sxs-lookup"><span data-stu-id="c396a-127">WPD applications must use the capabilities of the portable device to determine functionally, not the **WPD\_DEVICE\_TYPES** value.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c396a-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="c396a-128">Requirements</span></span>



| <span data-ttu-id="c396a-129">需求</span><span class="sxs-lookup"><span data-stu-id="c396a-129">Requirement</span></span> | <span data-ttu-id="c396a-130">值</span><span class="sxs-lookup"><span data-stu-id="c396a-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c396a-131">標頭</span><span class="sxs-lookup"><span data-stu-id="c396a-131">Header</span></span><br/> | <dl> <span data-ttu-id="c396a-132"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="c396a-132"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c396a-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c396a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c396a-134">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="c396a-134">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




