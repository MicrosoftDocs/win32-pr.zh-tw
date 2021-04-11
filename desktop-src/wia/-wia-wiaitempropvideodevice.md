---
description: 標準 Windows 映像取得 (WIA) video 驅動程式 (wiavusd.dll) 支援串流處理影片裝置的下列屬性。
ms.assetid: 24fa7e02-c409-49ec-b1a9-309f7c95e292
title: '影片 WIA 裝置屬性常數 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPV_LAST_PICTURE_TAKEN
- WIA_DPV_IMAGES_DIRECTORY
- WIA_DPV_DSHOW_DEVICE_PATH
- WIA_DPF_MOUNT_POINT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f02991cb5c2b8cc15eb89e335ef1e46442c89510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113260"
---
# <a name="video-wia-device-property-constants"></a><span data-ttu-id="8c1c7-103">影片 WIA 裝置屬性常數</span><span class="sxs-lookup"><span data-stu-id="8c1c7-103">Video WIA Device Property Constants</span></span>

<span data-ttu-id="8c1c7-104">標準 Windows 映像取得 (WIA) video 驅動程式 (wiavusd.dll) 支援串流處理影片裝置的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="8c1c7-104">The standard Windows Image Acquisition (WIA) video driver (wiavusd.dll) supports the following properties for streaming video devices.</span></span>

> [!Note]  
> <span data-ttu-id="8c1c7-105">WIA 不支援 Windows Server 2003、Windows Vista 或更新版本中的影片裝置。</span><span class="sxs-lookup"><span data-stu-id="8c1c7-105">WIA does not support video devices in Windows Server 2003, Windows Vista, or later.</span></span> <span data-ttu-id="8c1c7-106">針對這些版本的 Windows，請使用 [DirectShow](/previous-versions//ms783323(v=vs.85)) 從影片取得影像。</span><span class="sxs-lookup"><span data-stu-id="8c1c7-106">For those versions of the Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) to acquire images from video.</span></span>

 

<span data-ttu-id="8c1c7-107">前置詞 "WIA \_ DPV \_ " 表示影片裝置的裝置屬性，而且是 C/c + + 中使用的命名慣例。</span><span class="sxs-lookup"><span data-stu-id="8c1c7-107">The prefix "WIA\_DPV\_" indicates a Device Property for Video devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="8c1c7-108">針對腳本用途，這些常數會使用前置詞 "VideoDevice"，而且是 [WiaItemPropertyId](-wia-wiaitempropertyid.md) 列舉型別的一部分。</span><span class="sxs-lookup"><span data-stu-id="8c1c7-108">For scripting purposes these constants use the prefix "VideoDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="8c1c7-109">來自該腳本列舉的對應成員名稱，會出現在下列清單中 C/c + + 常數名稱旁邊的括弧中。</span><span class="sxs-lookup"><span data-stu-id="8c1c7-109">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



| <span data-ttu-id="8c1c7-110">常數/值</span><span class="sxs-lookup"><span data-stu-id="8c1c7-110">Constant/value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="8c1c7-111">Description</span><span class="sxs-lookup"><span data-stu-id="8c1c7-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <span data-ttu-id="8c1c7-112"><dt>**WIA \_DPV \_ 上一 \_ 張 \_ 拍攝**</dt> <dt>VideoDeviceLastPictureTaken</dt>的圖片</span><span class="sxs-lookup"><span data-stu-id="8c1c7-112"><dt>**WIA\_DPV\_LAST\_PICTURE\_TAKEN**</dt> <dt>VideoDeviceLastPictureTaken</dt></span></span> </dl> | <span data-ttu-id="8c1c7-113">這個屬性是用來通知 WIA 驅動程式已新增新的映射。</span><span class="sxs-lookup"><span data-stu-id="8c1c7-113">This property is used to notify the WIA driver that a new image has been added.</span></span> <span data-ttu-id="8c1c7-114">應用程式應該將這個屬性的值設定為成功呼叫 [**IWiaVideo：： TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) 方法所建立之影像檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c1c7-114">Applications should set the value of this property to the name of the image file created as the result of a successful call to the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method.</span></span> <br/> <span data-ttu-id="8c1c7-115">類型： VT \_ BSTR，存取：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c1c7-115">Type: VT\_BSTR, Access: Read/Write</span></span><br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <span data-ttu-id="8c1c7-116"><dt>**WIA \_DPV \_ IMAGES \_ 目錄**</dt> <dt>VideoDeviceImagesDirectory</dt></span><span class="sxs-lookup"><span data-stu-id="8c1c7-116"><dt>**WIA\_DPV\_IMAGES\_DIRECTORY**</dt> <dt>VideoDeviceImagesDirectory</dt></span></span> </dl>         | <span data-ttu-id="8c1c7-117">這個屬性是由標準的 WIA video 使用者模式驅動程式 (wiavusd.dll) 所公開。</span><span class="sxs-lookup"><span data-stu-id="8c1c7-117">This property is exposed by the standard WIA video user-mode driver (wiavusd.dll).</span></span> <span data-ttu-id="8c1c7-118">這個屬性的值是 WIA 視頻驅動程式預設放置影像的目錄完整路徑。</span><span class="sxs-lookup"><span data-stu-id="8c1c7-118">The value of this property is the full path of the directory where the WIA video driver puts images by default.</span></span> <span data-ttu-id="8c1c7-119">應用程式應該將 [**IWiaVideo：： ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) 屬性設定為此值。</span><span class="sxs-lookup"><span data-stu-id="8c1c7-119">Applications should set the [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) property to this value.</span></span> <br/> <span data-ttu-id="8c1c7-120">類型： VT \_ BSTR、Access： Read Only</span><span class="sxs-lookup"><span data-stu-id="8c1c7-120">Type: VT\_BSTR, Access: Read Only</span></span><br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <span data-ttu-id="8c1c7-121"><dt>**WIA \_DPV \_ DSHOW \_ 裝置 \_ 路徑**</dt> <dt>VideoDeviceDShowDevicePath</dt></span><span class="sxs-lookup"><span data-stu-id="8c1c7-121"><dt>**WIA\_DPV\_DSHOW\_DEVICE\_PATH**</dt> <dt>VideoDeviceDShowDevicePath</dt></span></span> </dl>     | <span data-ttu-id="8c1c7-122">DirectShow 裝置的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="8c1c7-122">The full path of the DirectShow device.</span></span> <br/> <span data-ttu-id="8c1c7-123">類型： VT \_ BSTR、Access： Read Only</span><span class="sxs-lookup"><span data-stu-id="8c1c7-123">Type: VT\_BSTR, Access: Read Only</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <span data-ttu-id="8c1c7-124"><dt>**WIA \_DPF \_ 裝入 \_ 點**</dt> <dt>FileDeviceMountPoint</dt></span><span class="sxs-lookup"><span data-stu-id="8c1c7-124"><dt>**WIA\_DPF\_MOUNT\_POINT**</dt> <dt>FileDeviceMountPoint</dt></span></span> </dl>                              | <span data-ttu-id="8c1c7-125">未實作。</span><span class="sxs-lookup"><span data-stu-id="8c1c7-125">Not implemented.</span></span> <br/> <span data-ttu-id="8c1c7-126">類型： **VT \_ I4**、存取：唯讀、有效的值： [WIA \_ 類別 \_ 無](-wia-property-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="8c1c7-126">Type: **VT\_I4**, Access: Read Only, Valid values: [WIA\_PROP\_NONE](-wia-property-attributes.md)</span></span><br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="8c1c7-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c1c7-127">Requirements</span></span>



| <span data-ttu-id="8c1c7-128">需求</span><span class="sxs-lookup"><span data-stu-id="8c1c7-128">Requirement</span></span> | <span data-ttu-id="8c1c7-129">值</span><span class="sxs-lookup"><span data-stu-id="8c1c7-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8c1c7-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c1c7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8c1c7-131">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c1c7-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="8c1c7-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c1c7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8c1c7-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c1c7-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8c1c7-134">標頭</span><span class="sxs-lookup"><span data-stu-id="8c1c7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c1c7-135"><dt>Wiadef。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c1c7-135"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
