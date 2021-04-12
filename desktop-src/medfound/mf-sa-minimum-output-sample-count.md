---
description: 指定 Microsoft 媒體基礎轉換 (MFT) 在管線中隨時都未完成之輸出樣本的最大數目。
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: 'MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf168158fd6a5f9a173d4d5d25dda3fa5b16d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191628"
---
# <a name="mf_sa_minimum_output_sample_count-attribute"></a><span data-ttu-id="0a959-103">MF \_ SA \_ 最小 \_ 輸出 \_ 範例 \_ 計數屬性</span><span class="sxs-lookup"><span data-stu-id="0a959-103">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT attribute</span></span>

<span data-ttu-id="0a959-104">指定 Microsoft 媒體基礎轉換 (MFT) 在管線中隨時都未完成之輸出樣本的最大數目。</span><span class="sxs-lookup"><span data-stu-id="0a959-104">Specifies the maximum number of output samples that a Microsoft Media Foundation transform (MFT) will have outstanding in the pipeline at any time.</span></span>

## <a name="data-type"></a><span data-ttu-id="0a959-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="0a959-105">Data type</span></span>

<span data-ttu-id="0a959-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0a959-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0a959-107">備註</span><span class="sxs-lookup"><span data-stu-id="0a959-107">Remarks</span></span>

<span data-ttu-id="0a959-108">這個屬性只適用于使用迴圈緩衝區配置其專屬輸出範例的 MFTs。</span><span class="sxs-lookup"><span data-stu-id="0a959-108">This attribute applies only to MFTs that use a circular buffer to allocate their own output samples.</span></span> <span data-ttu-id="0a959-109">其他 MFTs 會忽略此屬性。</span><span class="sxs-lookup"><span data-stu-id="0a959-109">Other MFTs ignore this attribute.</span></span>

<span data-ttu-id="0a959-110">若要設定此屬性：</span><span class="sxs-lookup"><span data-stu-id="0a959-110">To set this attribute:</span></span>

1.  <span data-ttu-id="0a959-111">在解碼器上呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。</span><span class="sxs-lookup"><span data-stu-id="0a959-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="0a959-112">呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) 以加入屬性。</span><span class="sxs-lookup"><span data-stu-id="0a959-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a959-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a959-113">Requirements</span></span>



| <span data-ttu-id="0a959-114">需求</span><span class="sxs-lookup"><span data-stu-id="0a959-114">Requirement</span></span> | <span data-ttu-id="0a959-115">值</span><span class="sxs-lookup"><span data-stu-id="0a959-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a959-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a959-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0a959-117">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a959-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0a959-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a959-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0a959-119">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a959-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0a959-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0a959-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a959-121"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a959-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a959-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a959-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a959-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="0a959-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0a959-124">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="0a959-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




