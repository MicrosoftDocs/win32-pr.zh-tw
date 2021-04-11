---
description: 指定要略過的影片畫面格數目，因為它們與先前的畫面格重複。
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: 'MFPKEY_ZEROBYTEFRAMES 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffcf29d099b3a3fb27a307e970af7af1a5c3d58b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848448"
---
# <a name="mfpkey_zerobyteframes-property"></a><span data-ttu-id="607a0-103">MFPKEY \_ ZEROBYTEFRAMES 屬性</span><span class="sxs-lookup"><span data-stu-id="607a0-103">MFPKEY\_ZEROBYTEFRAMES Property</span></span>

<span data-ttu-id="607a0-104">指定要略過的影片畫面格數目，因為它們與先前的畫面格重複。</span><span class="sxs-lookup"><span data-stu-id="607a0-104">Specifies the number of video frames that are skipped because they were duplicates of previous frames.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="607a0-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="607a0-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="607a0-106">g \_ wszWMVCZeroByteFrames</span><span class="sxs-lookup"><span data-stu-id="607a0-106">g\_wszWMVCZeroByteFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="607a0-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="607a0-107">Data Type</span></span>

<span data-ttu-id="607a0-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="607a0-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="607a0-109">備註</span><span class="sxs-lookup"><span data-stu-id="607a0-109">Remarks</span></span>

<span data-ttu-id="607a0-110">在計算編碼的畫面格數目 ([MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md)) 時，不會從傳遞的框架總數 ([MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md)) 減去此值。</span><span class="sxs-lookup"><span data-stu-id="607a0-110">This value is not subtracted from the total number of frames passed ([MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md)) when calculating the number of encoded frames ([MFPKEY\_CODEDFRAMES](mfpkey-codedframesproperty.md)).</span></span>

<span data-ttu-id="607a0-111">您可以將 [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) 設定為 VARIANT TRUE，以防止編解碼器略過重複的畫面格 \_ 。</span><span class="sxs-lookup"><span data-stu-id="607a0-111">You can stop the codec from skipping duplicate frames by setting [MFPKEY\_PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) to VARIANT\_TRUE.</span></span>

<span data-ttu-id="607a0-112">完成傳遞範例之後，您可以取得此值。</span><span class="sxs-lookup"><span data-stu-id="607a0-112">You can get this value after you are finished passing samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="607a0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="607a0-113">Requirements</span></span>



| <span data-ttu-id="607a0-114">需求</span><span class="sxs-lookup"><span data-stu-id="607a0-114">Requirement</span></span> | <span data-ttu-id="607a0-115">值</span><span class="sxs-lookup"><span data-stu-id="607a0-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="607a0-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="607a0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="607a0-117">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="607a0-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="607a0-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="607a0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="607a0-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="607a0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="607a0-120">標頭</span><span class="sxs-lookup"><span data-stu-id="607a0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="607a0-121"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="607a0-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="607a0-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="607a0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="607a0-123">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="607a0-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




