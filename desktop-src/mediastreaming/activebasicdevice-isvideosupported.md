---
title: 'ActiveBasicDevice IsVideoSupported 屬性 (PlayToDevice .h) '
description: 取得值，這個值會指出裝置是否支援影片。
ms.assetid: E8D33A04-748D-42F8-878F-35D973A6B559
keywords:
- IsVideoSupported 屬性媒體串流 API
- IsVideoSupported 屬性媒體串流 API，ActiveBasicDevice 介面
- ActiveBasicDevice 介面媒體串流 API，IsVideoSupported 屬性
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsVideoSupported
- ActiveBasicDevice.get_IsVideoSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be369b34355b199cd47518065724242b9a422e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106980293"
---
# <a name="activebasicdeviceisvideosupported-property"></a><span data-ttu-id="46c33-106">ActiveBasicDevice：： IsVideoSupported 屬性</span><span class="sxs-lookup"><span data-stu-id="46c33-106">ActiveBasicDevice::IsVideoSupported property</span></span>

<span data-ttu-id="46c33-107">取得值，這個值會指出裝置是否支援影片。</span><span class="sxs-lookup"><span data-stu-id="46c33-107">Gets a value that indicates if the device supports video.</span></span>

<span data-ttu-id="46c33-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="46c33-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="46c33-109">語法</span><span class="sxs-lookup"><span data-stu-id="46c33-109">Syntax</span></span>


```C++
HRESULT get_IsVideoSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="46c33-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="46c33-110">Property value</span></span>

<span data-ttu-id="46c33-111">**布林值** 的指標，指出裝置是否支援影片。</span><span class="sxs-lookup"><span data-stu-id="46c33-111">A pointer to a **boolean** that indicates if the device supports video.</span></span>

<span data-ttu-id="46c33-112">如果裝置支援影片，則 **為 true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="46c33-112">**true** if the device supports video; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="46c33-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="46c33-113">Requirements</span></span>



| <span data-ttu-id="46c33-114">需求</span><span class="sxs-lookup"><span data-stu-id="46c33-114">Requirement</span></span> | <span data-ttu-id="46c33-115">值</span><span class="sxs-lookup"><span data-stu-id="46c33-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="46c33-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46c33-116">Minimum supported client</span></span><br/> | <span data-ttu-id="46c33-117">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46c33-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="46c33-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46c33-118">Minimum supported server</span></span><br/> | <span data-ttu-id="46c33-119">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46c33-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="46c33-120">標頭</span><span class="sxs-lookup"><span data-stu-id="46c33-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="46c33-121"><dt>PlayToDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="46c33-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="46c33-122">Idl</span><span class="sxs-lookup"><span data-stu-id="46c33-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46c33-123"><dt>PlayToDevice .idl</dt></span><span class="sxs-lookup"><span data-stu-id="46c33-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="46c33-124">DLL</span><span class="sxs-lookup"><span data-stu-id="46c33-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46c33-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46c33-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46c33-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46c33-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="46c33-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="46c33-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

