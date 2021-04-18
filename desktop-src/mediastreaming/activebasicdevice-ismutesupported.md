---
title: 'ActiveBasicDevice IsMuteSupported 屬性 (PlayToDevice .h) '
description: 取得值，這個值會指出裝置是否支援將音訊靜音。
ms.assetid: FF4B533F-B416-4DBE-BF86-FA34E785FFA2
keywords:
- IsMuteSupported 屬性媒體串流 API
- IsMuteSupported 屬性媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，IsMuteSupported 屬性
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsMuteSupported
- ActiveBasicDevice.get_IsMuteSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcec2e4520bd3b15b715c01e4369da87887355e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465744"
---
# <a name="activebasicdeviceismutesupported-property"></a><span data-ttu-id="0d412-106">ActiveBasicDevice：： IsMuteSupported 屬性</span><span class="sxs-lookup"><span data-stu-id="0d412-106">ActiveBasicDevice::IsMuteSupported property</span></span>

<span data-ttu-id="0d412-107">取得值，這個值會指出裝置是否支援將音訊靜音。</span><span class="sxs-lookup"><span data-stu-id="0d412-107">Gets a value that indicates if the device supports muting the audio.</span></span>

<span data-ttu-id="0d412-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="0d412-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d412-109">語法</span><span class="sxs-lookup"><span data-stu-id="0d412-109">Syntax</span></span>


```C++
HRESULT get_IsMuteSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="0d412-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="0d412-110">Property value</span></span>

<span data-ttu-id="0d412-111">**布林值** 的指標，指出裝置是否支援將音訊靜音。</span><span class="sxs-lookup"><span data-stu-id="0d412-111">A pointer to a **boolean** that indicates if the device supports muting the audio.</span></span>

<span data-ttu-id="0d412-112">如果裝置支援音訊靜音，則 **為 true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="0d412-112">**true** if the device supports muting the audio; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d412-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d412-113">Requirements</span></span>



| <span data-ttu-id="0d412-114">需求</span><span class="sxs-lookup"><span data-stu-id="0d412-114">Requirement</span></span> | <span data-ttu-id="0d412-115">值</span><span class="sxs-lookup"><span data-stu-id="0d412-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d412-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d412-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0d412-117">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d412-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0d412-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d412-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0d412-119">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d412-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0d412-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0d412-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d412-121"><dt>PlayToDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d412-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d412-122">Idl</span><span class="sxs-lookup"><span data-stu-id="0d412-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0d412-123"><dt>PlayToDevice .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d412-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="0d412-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0d412-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d412-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d412-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d412-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d412-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="0d412-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0d412-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

