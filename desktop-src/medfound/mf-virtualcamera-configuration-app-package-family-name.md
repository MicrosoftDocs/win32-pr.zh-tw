---
description: 指定虛擬攝影機設定應用程式的應用程式套件系列名稱。
title: 'MF_VIRTUALCAMERA_APP_PACKAGE_FAMILY_NAME 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/24/2021
ms.openlocfilehash: e821a273c44b1d5c9e654e34bbfb928ea707cdc0
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691845"
---
# <a name="mf_virtualcamera_app_package_family_name-attribute"></a><span data-ttu-id="f406c-103">MF \_ VIRTUALCAMERA \_ 應用程式 \_ 套件 \_ 系列 \_ 名稱屬性</span><span class="sxs-lookup"><span data-stu-id="f406c-103">MF\_VIRTUALCAMERA\_APP\_PACKAGE\_FAMILY\_NAME attribute</span></span>

<span data-ttu-id="f406c-104">指定虛擬攝影機設定應用程式的應用程式套件系列名稱。</span><span class="sxs-lookup"><span data-stu-id="f406c-104">Specifies the app package family name for a virtual camera configuration application.</span></span> <span data-ttu-id="f406c-105">提供時，管線會將設定應用程式與虛擬攝影機建立關聯，並在相機設定頁面中提供啟動點。</span><span class="sxs-lookup"><span data-stu-id="f406c-105">When provided, the pipeline will associate the configuration application with the virtual camera and provide a launch point within the Camera Settings page.</span></span>

## <a name="data-type"></a><span data-ttu-id="f406c-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="f406c-106">Data type</span></span>

[<span data-ttu-id="f406c-107">MF_ATTRIBUTE_STRING</span><span class="sxs-lookup"><span data-stu-id="f406c-107">MF_ATTRIBUTE_STRING</span></span>](/windows/win32/api/mfobjects/ne-mfobjects-mf_attribute_type)

## <a name="remarks"></a><span data-ttu-id="f406c-108">備註</span><span class="sxs-lookup"><span data-stu-id="f406c-108">Remarks</span></span>

<span data-ttu-id="f406c-109">虛擬攝影機自訂媒體來源會從媒體來源屬性存放區 [IMFMediaSourceEx：： GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource)公開此屬性。</span><span class="sxs-lookup"><span data-stu-id="f406c-109">This attribute may be exposed by the virtual camera custom media source from the media source attribute store [IMFMediaSourceEx::GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).</span></span>  

<span data-ttu-id="f406c-110">如果電腦上還沒有安裝設定應用程式，則會啟動存放區應用程式，並流覽至套件系列名稱所指定的應用程式頁面。</span><span class="sxs-lookup"><span data-stu-id="f406c-110">If the configuration application is not yet installed on the machine, the Store application will be launched and navigated to the application page specified by the package family name.</span></span> <span data-ttu-id="f406c-111">否則，系統會為使用者啟動已安裝的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f406c-111">Otherwise, the installed application will be launched for the user.</span></span>


## <a name="requirements"></a><span data-ttu-id="f406c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f406c-112">Requirements</span></span>



| <span data-ttu-id="f406c-113">需求</span><span class="sxs-lookup"><span data-stu-id="f406c-113">Requirement</span></span> | <span data-ttu-id="f406c-114">值</span><span class="sxs-lookup"><span data-stu-id="f406c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f406c-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f406c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f406c-116">Windows組建22000</span><span class="sxs-lookup"><span data-stu-id="f406c-116">Windows Build 22000</span></span><br/>                          |
| <span data-ttu-id="f406c-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f406c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f406c-118">Windows組建22000</span><span class="sxs-lookup"><span data-stu-id="f406c-118">Windows Build 22000</span></span><br/>                      |
| <span data-ttu-id="f406c-119">標頭</span><span class="sxs-lookup"><span data-stu-id="f406c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f406c-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="f406c-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f406c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f406c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f406c-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="f406c-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f406c-123">**IMFAttributes：： GetString**</span><span class="sxs-lookup"><span data-stu-id="f406c-123">**IMFAttributes::GetString**</span></span>](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="f406c-124">**IMFAttributes：： SetString**</span><span class="sxs-lookup"><span data-stu-id="f406c-124">**IMFAttributes::SetString**</span></span>](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> 
</dl>
 




