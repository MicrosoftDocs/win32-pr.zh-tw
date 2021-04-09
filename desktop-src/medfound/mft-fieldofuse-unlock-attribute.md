---
description: 包含 IMFFieldOfUseMFTUnlock 指標，可用來解除鎖定 (MFT) 的媒體基礎轉換。 IMFFieldOfUseMFTUnlock 介面可用來解除鎖定具有使用規定限制的 MFT。
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: 'MFT_FIELDOFUSE_UNLOCK_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f02fbc032f16406a2b4407b197dc6140774001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692312"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="6b29b-104">MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性屬性</span><span class="sxs-lookup"><span data-stu-id="6b29b-104">MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="6b29b-105">包含 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) 指標，可用來解除鎖定 (MFT) 的媒體基礎轉換。</span><span class="sxs-lookup"><span data-stu-id="6b29b-105">Contains an [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer, which can be used to unlock a Media Foundation transform (MFT).</span></span> <span data-ttu-id="6b29b-106">**IMFFieldOfUseMFTUnlock** 介面可用來解除鎖定具有使用規定限制的 MFT。</span><span class="sxs-lookup"><span data-stu-id="6b29b-106">The **IMFFieldOfUseMFTUnlock** interface is used to unlock an MFT that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="6b29b-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="6b29b-107">Data type</span></span>

<span data-ttu-id="6b29b-108">**[](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) IMFFieldOfUseMFTUnlock \** _ 儲存為 _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="6b29b-108">**[**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="6b29b-109">取得/設定</span><span class="sxs-lookup"><span data-stu-id="6b29b-109">Get/set</span></span>

<span data-ttu-id="6b29b-110">若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。</span><span class="sxs-lookup"><span data-stu-id="6b29b-110">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="6b29b-111">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。</span><span class="sxs-lookup"><span data-stu-id="6b29b-111">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="6b29b-112">備註</span><span class="sxs-lookup"><span data-stu-id="6b29b-112">Remarks</span></span>

<span data-ttu-id="6b29b-113">如需此屬性的詳細資訊，請參閱 [使用限制欄位](field-of-use-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="6b29b-113">For more information about this attribute, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>

<span data-ttu-id="6b29b-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="6b29b-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b29b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b29b-115">Requirements</span></span>



| <span data-ttu-id="6b29b-116">需求</span><span class="sxs-lookup"><span data-stu-id="6b29b-116">Requirement</span></span> | <span data-ttu-id="6b29b-117">值</span><span class="sxs-lookup"><span data-stu-id="6b29b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b29b-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b29b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6b29b-119">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b29b-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="6b29b-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b29b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6b29b-121">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b29b-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6b29b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6b29b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b29b-123"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="6b29b-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b29b-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b29b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b29b-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="6b29b-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6b29b-126">使用限制領域</span><span class="sxs-lookup"><span data-stu-id="6b29b-126">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)
</dt> <dt>

[<span data-ttu-id="6b29b-127">**MFCreateTransformActivate**</span><span class="sxs-lookup"><span data-stu-id="6b29b-127">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




