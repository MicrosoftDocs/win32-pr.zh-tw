---
description: 指定是否允許應用程式存取未壓縮的影片畫面。
ms.assetid: 7D2A9003-B36E-4082-877E-8AC7F5645E89
title: 'MFPROTECTION_VIDEO_FRAMES 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8ccfc56fb1c1b52b14e16d8e702111f3d8564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997512"
---
# <a name="mfprotection_video_frames-attribute"></a><span data-ttu-id="2c0d0-103">MFPROTECTION \_ 影片 \_ 畫面格屬性</span><span class="sxs-lookup"><span data-stu-id="2c0d0-103">MFPROTECTION\_VIDEO\_FRAMES attribute</span></span>

<span data-ttu-id="2c0d0-104">指定是否允許應用程式存取未壓縮的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="2c0d0-104">Specifies if an application is allowed access to uncompressed video frames.</span></span>

## <a name="data-type"></a><span data-ttu-id="2c0d0-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="2c0d0-105">Data type</span></span>

<span data-ttu-id="2c0d0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2c0d0-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2c0d0-107">備註</span><span class="sxs-lookup"><span data-stu-id="2c0d0-107">Remarks</span></span>

<span data-ttu-id="2c0d0-108">值為0表示允許應用程式存取畫面格。</span><span class="sxs-lookup"><span data-stu-id="2c0d0-108">A value of 0 indicates that the application is allowed access to the frames.</span></span> <span data-ttu-id="2c0d0-109">這可能是因為應用程式與使用中的特定內容保護系統之間的私用合約所決定。</span><span class="sxs-lookup"><span data-stu-id="2c0d0-109">This might be determined as a result of a private agreement between the application and the particular content protection system in use.</span></span>

<span data-ttu-id="2c0d0-110">如果應用程式提供有效的應用程式憑證，則值為1表示允許應用程式存取框架 (參閱 [**IMFMediaEngineProtectedContent：： SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)) 。</span><span class="sxs-lookup"><span data-stu-id="2c0d0-110">A value of 1 indicates that the application is allowed access to frames if a valid application certificate is provided by the application (see [**IMFMediaEngineProtectedContent::SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).</span></span>

<span data-ttu-id="2c0d0-111">值為0xFFFFFFFF （預設值），表示不允許任何應用程式存取未壓縮的框架。</span><span class="sxs-lookup"><span data-stu-id="2c0d0-111">A value of 0xFFFFFFFF, which is the default value, indicates no applications are allowed access to uncompressed frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c0d0-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c0d0-112">Requirements</span></span>



| <span data-ttu-id="2c0d0-113">需求</span><span class="sxs-lookup"><span data-stu-id="2c0d0-113">Requirement</span></span> | <span data-ttu-id="2c0d0-114">值</span><span class="sxs-lookup"><span data-stu-id="2c0d0-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2c0d0-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c0d0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2c0d0-116">\[僅 Windows 8 UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c0d0-116">Windows 8 \[UWP apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2c0d0-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c0d0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2c0d0-118">僅限 Windows Server 2012 \[ UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c0d0-118">Windows Server 2012 \[UWP apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2c0d0-119">標頭</span><span class="sxs-lookup"><span data-stu-id="2c0d0-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c0d0-120"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c0d0-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c0d0-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c0d0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c0d0-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="2c0d0-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2c0d0-123">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="2c0d0-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




