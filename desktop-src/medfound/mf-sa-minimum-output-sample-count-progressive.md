---
description: 指出 Microsoft 媒體基礎轉換 (MFT) 應該允許在任何指定時間1-12 的漸進樣本數目下限。
ms.assetid: C1F27F39-FADA-4644-ACD6-B02EAD9CFFE7
title: 'MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT_PROGRESSIVE 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b452f9fa4016705ed90a7f5b07abcaa6ff11983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193621"
---
# <a name="mf_sa_minimum_output_sample_count_progressive-attribute"></a><span data-ttu-id="8c9ed-103">MF \_ SA \_ 最小 \_ 輸出 \_ 範例 \_ 計數 \_ 漸進屬性</span><span class="sxs-lookup"><span data-stu-id="8c9ed-103">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT\_PROGRESSIVE attribute</span></span>

<span data-ttu-id="8c9ed-104">指出 Microsoft 媒體基礎轉換 (MFT) 應該允許在任何指定時間1-12 的漸進樣本數目下限。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-104">Indicates the minimum number of progressive samples that the Microsoft Media Foundation transform (MFT) should allow to be oustanding at any given time.</span></span>

## <a name="data-type"></a><span data-ttu-id="8c9ed-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="8c9ed-105">Data type</span></span>

<span data-ttu-id="8c9ed-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8c9ed-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="8c9ed-107">備註</span><span class="sxs-lookup"><span data-stu-id="8c9ed-107">Remarks</span></span>

<span data-ttu-id="8c9ed-108">這個屬性只適用于使用迴圈緩衝區配置其專屬輸出範例的 MFTs。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-108">This attribute applies only to MFTs that use a circular buffer to allocate their own output samples.</span></span> <span data-ttu-id="8c9ed-109">其他 MFTs 會忽略此屬性。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-109">Other MFTs ignore this attribute.</span></span>

<span data-ttu-id="8c9ed-110">若要設定此屬性：</span><span class="sxs-lookup"><span data-stu-id="8c9ed-110">To set this attribute:</span></span>

1.  <span data-ttu-id="8c9ed-111">在解碼器上呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="8c9ed-112">呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) 以加入屬性。</span><span class="sxs-lookup"><span data-stu-id="8c9ed-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c9ed-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c9ed-113">Requirements</span></span>



| <span data-ttu-id="8c9ed-114">需求</span><span class="sxs-lookup"><span data-stu-id="8c9ed-114">Requirement</span></span> | <span data-ttu-id="8c9ed-115">值</span><span class="sxs-lookup"><span data-stu-id="8c9ed-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c9ed-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c9ed-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8c9ed-117">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c9ed-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="8c9ed-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c9ed-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8c9ed-119">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c9ed-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="8c9ed-120">標頭</span><span class="sxs-lookup"><span data-stu-id="8c9ed-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c9ed-121"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c9ed-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c9ed-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c9ed-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c9ed-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="8c9ed-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




