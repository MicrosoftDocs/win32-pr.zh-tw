---
description: 指定此解碼器的電源等級。
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: 'MFPKEY_AVDecVideoSWPowerLevel 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2180e26d3e14263c14f2f3603c8c92cf8c11daec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974525"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a><span data-ttu-id="d83bf-103">MFPKEY \_ AVDecVideoSWPowerLevel 屬性</span><span class="sxs-lookup"><span data-stu-id="d83bf-103">MFPKEY\_AVDecVideoSWPowerLevel Property</span></span>

<span data-ttu-id="d83bf-104">指定此解碼器的電源等級。</span><span class="sxs-lookup"><span data-stu-id="d83bf-104">Specifies the power level for the decoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d83bf-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="d83bf-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d83bf-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="d83bf-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="d83bf-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="d83bf-107">Data Type</span></span>

<span data-ttu-id="d83bf-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="d83bf-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="d83bf-109">預設值</span><span class="sxs-lookup"><span data-stu-id="d83bf-109">Default Value</span></span>

<span data-ttu-id="d83bf-110">**100**</span><span class="sxs-lookup"><span data-stu-id="d83bf-110">**100**</span></span>

## <a name="remarks"></a><span data-ttu-id="d83bf-111">備註</span><span class="sxs-lookup"><span data-stu-id="d83bf-111">Remarks</span></span>

<span data-ttu-id="d83bf-112">這個屬性必須設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d83bf-112">This property must be set to one of the following values.</span></span>



| <span data-ttu-id="d83bf-113">值</span><span class="sxs-lookup"><span data-stu-id="d83bf-113">Value</span></span> | <span data-ttu-id="d83bf-114">意義</span><span class="sxs-lookup"><span data-stu-id="d83bf-114">Meaning</span></span>                                                             |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="d83bf-115">0</span><span class="sxs-lookup"><span data-stu-id="d83bf-115">0</span></span>     | <span data-ttu-id="d83bf-116">此解碼器使用已針對電池壽命優化的電源等級。</span><span class="sxs-lookup"><span data-stu-id="d83bf-116">The decoder uses a power level that is optimized for battery life.</span></span>  |
| <span data-ttu-id="d83bf-117">50</span><span class="sxs-lookup"><span data-stu-id="d83bf-117">50</span></span>    | <span data-ttu-id="d83bf-118">此解碼器使用平衡的電源等級。</span><span class="sxs-lookup"><span data-stu-id="d83bf-118">The decoder uses a balanced power level.</span></span>                            |
| <span data-ttu-id="d83bf-119">100</span><span class="sxs-lookup"><span data-stu-id="d83bf-119">100</span></span>   | <span data-ttu-id="d83bf-120">此解碼器會使用針對影片品質優化的電源等級。</span><span class="sxs-lookup"><span data-stu-id="d83bf-120">The decoder uses a power level that is optimized for video quality.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d83bf-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d83bf-121">Requirements</span></span>



| <span data-ttu-id="d83bf-122">需求</span><span class="sxs-lookup"><span data-stu-id="d83bf-122">Requirement</span></span> | <span data-ttu-id="d83bf-123">值</span><span class="sxs-lookup"><span data-stu-id="d83bf-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d83bf-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d83bf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d83bf-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d83bf-125">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="d83bf-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d83bf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d83bf-127">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d83bf-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d83bf-128">標頭</span><span class="sxs-lookup"><span data-stu-id="d83bf-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d83bf-129"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d83bf-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d83bf-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d83bf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d83bf-131">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="d83bf-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
