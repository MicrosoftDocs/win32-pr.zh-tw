---
description: 指定編解碼器編碼的影片框架數目。
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: 'MFPKEY_CODEDFRAMES 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708bb6c200701cdf48fa8407108be2161fdb4f61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984568"
---
# <a name="mfpkey_codedframes-property"></a><span data-ttu-id="fcd7e-103">MFPKEY \_ CODEDFRAMES 屬性</span><span class="sxs-lookup"><span data-stu-id="fcd7e-103">MFPKEY\_CODEDFRAMES Property</span></span>

<span data-ttu-id="fcd7e-104">指定編解碼器編碼的影片框架數目。</span><span class="sxs-lookup"><span data-stu-id="fcd7e-104">Specifies the number of video frames encoded by the codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="fcd7e-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="fcd7e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="fcd7e-106">g \_ wszWMVCCodedFrames</span><span class="sxs-lookup"><span data-stu-id="fcd7e-106">g\_wszWMVCCodedFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="fcd7e-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="fcd7e-107">Data Type</span></span>

<span data-ttu-id="fcd7e-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="fcd7e-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="fcd7e-109">備註</span><span class="sxs-lookup"><span data-stu-id="fcd7e-109">Remarks</span></span>

<span data-ttu-id="fcd7e-110">這個值等於 [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) 減去由於位速率限制而捨棄的任何框架。</span><span class="sxs-lookup"><span data-stu-id="fcd7e-110">This value is equal to [MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) minus any frames that were dropped due to bit-rate constraints.</span></span> <span data-ttu-id="fcd7e-111">完成傳遞範例之後，您可以取得此值。</span><span class="sxs-lookup"><span data-stu-id="fcd7e-111">You can get this value after you are finished passing samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcd7e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="fcd7e-112">Requirements</span></span>



| <span data-ttu-id="fcd7e-113">需求</span><span class="sxs-lookup"><span data-stu-id="fcd7e-113">Requirement</span></span> | <span data-ttu-id="fcd7e-114">值</span><span class="sxs-lookup"><span data-stu-id="fcd7e-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcd7e-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fcd7e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fcd7e-116">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fcd7e-116">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fcd7e-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fcd7e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fcd7e-118">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fcd7e-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fcd7e-119">標頭</span><span class="sxs-lookup"><span data-stu-id="fcd7e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcd7e-120"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fcd7e-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcd7e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fcd7e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcd7e-122">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="fcd7e-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




