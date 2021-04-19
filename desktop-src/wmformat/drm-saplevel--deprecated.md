---
title: 'DRM_SAPLEVEL (已淘汰) '
description: 指定應用程式支援的 (SAP) 層級的安全音訊路徑。
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- DRM_SAPLEVEL (已淘汰) windows Media 格式
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43711c6c394761f599271809419a46311265d8b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982058"
---
# <a name="drm_saplevel-deprecated"></a><span data-ttu-id="5564e-104">DRM \_ SAPLEVEL (已淘汰) </span><span class="sxs-lookup"><span data-stu-id="5564e-104">DRM\_SAPLEVEL (deprecated)</span></span>

<span data-ttu-id="5564e-105">\[**DRM \_SAPLEVEL** 不再適用于 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="5564e-105">\[**DRM\_SAPLEVEL** is no longer available for use as of Windows Vista.</span></span> <span data-ttu-id="5564e-106">相反地，請在媒體基礎程式庫中使用受保護的使用者模式音訊 (PUMA) 。</span><span class="sxs-lookup"><span data-stu-id="5564e-106">Instead, use Protected User Mode Audio (PUMA) in the Media Foundation library.</span></span> <span data-ttu-id="5564e-107">\]</span><span class="sxs-lookup"><span data-stu-id="5564e-107">\]</span></span>

<span data-ttu-id="5564e-108">**DRM \_ SAPLEVEL** 屬性會指定您的應用程式所支援的 (SAP) 層級的安全音訊路徑。</span><span class="sxs-lookup"><span data-stu-id="5564e-108">The **DRM\_SAPLEVEL** property specifies the secure audio path (SAP) level supported by your application.</span></span>

## <a name="global-constant"></a><span data-ttu-id="5564e-109">全域常數</span><span class="sxs-lookup"><span data-stu-id="5564e-109">Global Constant</span></span>

<span data-ttu-id="5564e-110">g \_ wszWMDRM \_ SAPLEVEL</span><span class="sxs-lookup"><span data-stu-id="5564e-110">g\_wszWMDRM\_SAPLEVEL</span></span>

## <a name="data-type"></a><span data-ttu-id="5564e-111">資料類型</span><span class="sxs-lookup"><span data-stu-id="5564e-111">Data Type</span></span>

<span data-ttu-id="5564e-112">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="5564e-112">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="5564e-113">備註</span><span class="sxs-lookup"><span data-stu-id="5564e-113">Remarks</span></span>

<span data-ttu-id="5564e-114">這是透過呼叫 [**IWMDRMReader：： SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty)所設定的僅限寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="5564e-114">This is a write-only property that is set by calling [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty).</span></span> <span data-ttu-id="5564e-115">此值是 SAP 層級的寬字元字串標記法，例如 L "200"。</span><span class="sxs-lookup"><span data-stu-id="5564e-115">The value is a wide-character string representation of the SAP level, such as L"200".</span></span> <span data-ttu-id="5564e-116">目前支援的值為200和300。</span><span class="sxs-lookup"><span data-stu-id="5564e-116">Current supported values are 200 and 300.</span></span>

## <a name="requirements"></a><span data-ttu-id="5564e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5564e-117">Requirements</span></span>



| <span data-ttu-id="5564e-118">需求</span><span class="sxs-lookup"><span data-stu-id="5564e-118">Requirement</span></span> | <span data-ttu-id="5564e-119">值</span><span class="sxs-lookup"><span data-stu-id="5564e-119">Value</span></span> |
|----------------------------------|--------------------------------|
| <span data-ttu-id="5564e-120">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5564e-120">End of client support</span></span><br/> | <span data-ttu-id="5564e-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5564e-121">Windows XP</span></span><br/>          |
| <span data-ttu-id="5564e-122">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="5564e-122">End of server support</span></span><br/> | <span data-ttu-id="5564e-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5564e-123">Windows Server 2003</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5564e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5564e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5564e-125">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="5564e-125">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 





