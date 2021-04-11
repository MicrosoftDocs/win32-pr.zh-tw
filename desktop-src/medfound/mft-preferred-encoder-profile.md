---
description: 包含編碼器的設定屬性。
ms.assetid: f9bd8a50-e43e-4668-86a0-c9d5f517f4cf
title: 'MFT_PREFERRED_ENCODER_PROFILE 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfdc85ead0fe813215b3edaea14833400df5445d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943734"
---
# <a name="mft_preferred_encoder_profile-attribute"></a><span data-ttu-id="e78cc-103">MFT \_ 慣用 \_ 編碼器 \_ 配置檔案屬性</span><span class="sxs-lookup"><span data-stu-id="e78cc-103">MFT\_PREFERRED\_ENCODER\_PROFILE attribute</span></span>

<span data-ttu-id="e78cc-104">包含編碼器的設定屬性。</span><span class="sxs-lookup"><span data-stu-id="e78cc-104">Contains configuration properties for an encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="e78cc-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e78cc-105">Data type</span></span>

<span data-ttu-id="e78cc-106">**[](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) IMFAttributes \** _ 儲存為 _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="e78cc-106">**[**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="e78cc-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="e78cc-107">Get/set</span></span>

<span data-ttu-id="e78cc-108">若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。</span><span class="sxs-lookup"><span data-stu-id="e78cc-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="e78cc-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。</span><span class="sxs-lookup"><span data-stu-id="e78cc-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e78cc-110">適用於</span><span class="sxs-lookup"><span data-stu-id="e78cc-110">Applies to</span></span>

[<span data-ttu-id="e78cc-111">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="e78cc-111">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a><span data-ttu-id="e78cc-112">備註</span><span class="sxs-lookup"><span data-stu-id="e78cc-112">Remarks</span></span>

<span data-ttu-id="e78cc-113">這個屬性可以在 [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) 函數所傳回的啟用物件上設定。</span><span class="sxs-lookup"><span data-stu-id="e78cc-113">This attribute can be set on the activation object returned by the [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) function.</span></span> <span data-ttu-id="e78cc-114">只有在啟用物件設定為建立編碼器時，才會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="e78cc-114">The attribute applies only when the activation object is configured to create an encoder.</span></span> <span data-ttu-id="e78cc-115">屬性的值是屬性存放區的指標，其本身包含要在編碼器上設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="e78cc-115">The value of the attribute is a pointer to an attribute store, which itself contains properties to set on the encoder.</span></span>

<span data-ttu-id="e78cc-116">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="e78cc-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e78cc-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e78cc-117">Requirements</span></span>



| <span data-ttu-id="e78cc-118">需求</span><span class="sxs-lookup"><span data-stu-id="e78cc-118">Requirement</span></span> | <span data-ttu-id="e78cc-119">值</span><span class="sxs-lookup"><span data-stu-id="e78cc-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e78cc-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e78cc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e78cc-121">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e78cc-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e78cc-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e78cc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e78cc-123">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e78cc-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e78cc-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e78cc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e78cc-125"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="e78cc-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e78cc-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e78cc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e78cc-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e78cc-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e78cc-128">**MFCreateTransformActivate**</span><span class="sxs-lookup"><span data-stu-id="e78cc-128">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[<span data-ttu-id="e78cc-129">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="e78cc-129">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




