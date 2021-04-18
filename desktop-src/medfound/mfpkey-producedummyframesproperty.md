---
description: 指定編碼器是否會在位流中產生重複框架的虛擬框架專案。
ms.assetid: dc09cecb-98c0-40bb-9e5d-f4661bf98522
title: 'MFPKEY_PRODUCEDUMMYFRAMES 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b40bdaa54b3dc14a2b4ef44235d7f87cab5b905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192245"
---
# <a name="mfpkey_producedummyframes-property"></a><span data-ttu-id="57a38-103">MFPKEY \_ PRODUCEDUMMYFRAMES 屬性</span><span class="sxs-lookup"><span data-stu-id="57a38-103">MFPKEY\_PRODUCEDUMMYFRAMES Property</span></span>

<span data-ttu-id="57a38-104">指定編碼器是否會在位流中產生重複框架的虛擬框架專案。</span><span class="sxs-lookup"><span data-stu-id="57a38-104">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="57a38-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="57a38-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="57a38-106">g \_ wszWMVCProduceDummyFrames</span><span class="sxs-lookup"><span data-stu-id="57a38-106">g\_wszWMVCProduceDummyFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="57a38-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="57a38-107">Data Type</span></span>

<span data-ttu-id="57a38-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="57a38-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="57a38-109">預設值</span><span class="sxs-lookup"><span data-stu-id="57a38-109">Default Value</span></span>

<span data-ttu-id="57a38-110">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="57a38-110">VARIANT\_FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="57a38-111">備註</span><span class="sxs-lookup"><span data-stu-id="57a38-111">Remarks</span></span>

<span data-ttu-id="57a38-112">如果此值為 VARIANT \_ FALSE，則編解碼器不會將任何資料放在位資料流程中，以供重複的畫面格之用。</span><span class="sxs-lookup"><span data-stu-id="57a38-112">If this value is VARIANT\_FALSE, the codec will not put any data in the bit stream for duplicate frames.</span></span>

<span data-ttu-id="57a38-113">在保存框架編號的應用程式中，虛擬框架可能很重要。</span><span class="sxs-lookup"><span data-stu-id="57a38-113">Dummy frames can be important in applications where frame numbers are persisted.</span></span> <span data-ttu-id="57a38-114">常見的範例是針對編碼的內容維護 SMPTE 時間代碼。</span><span class="sxs-lookup"><span data-stu-id="57a38-114">A common example is when SMPTE time codes are maintained for encoded content.</span></span>

## <a name="requirements"></a><span data-ttu-id="57a38-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="57a38-115">Requirements</span></span>



| <span data-ttu-id="57a38-116">需求</span><span class="sxs-lookup"><span data-stu-id="57a38-116">Requirement</span></span> | <span data-ttu-id="57a38-117">值</span><span class="sxs-lookup"><span data-stu-id="57a38-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57a38-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57a38-118">Minimum supported client</span></span><br/> | <span data-ttu-id="57a38-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57a38-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="57a38-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57a38-120">Minimum supported server</span></span><br/> | <span data-ttu-id="57a38-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57a38-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="57a38-122">標頭</span><span class="sxs-lookup"><span data-stu-id="57a38-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="57a38-123"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="57a38-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57a38-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57a38-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57a38-125">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="57a38-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




