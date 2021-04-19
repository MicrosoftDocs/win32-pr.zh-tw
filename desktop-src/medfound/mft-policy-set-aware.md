---
description: 指定 IMFTransform 是否要接收 MEPolicySet 完成通知。
title: MFT_POLICY_SET_AWARE (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2effa9eab2b0b126c2849d39ce7ffe3f62d81e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977255"
---
# <a name="mft_policy_set_aware-attribute"></a><span data-ttu-id="c9c44-103">MFT \_ 原則 \_ 集 \_ 感知屬性</span><span class="sxs-lookup"><span data-stu-id="c9c44-103">MFT\_POLICY\_SET\_AWARE attribute</span></span>

<span data-ttu-id="c9c44-104">如果非零，則表示 **IMFTransform** 想要接收 [MEPolicySet](./mepolicyset.md) 完成通知。</span><span class="sxs-lookup"><span data-stu-id="c9c44-104">If non-zero, indicates that the **IMFTransform** wants to receive [MEPolicySet](./mepolicyset.md) completion notifications.</span></span>

## <a name="data-type"></a><span data-ttu-id="c9c44-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c9c44-105">Data type</span></span>

<span data-ttu-id="c9c44-106">**UINT32** (視為 **BOOL**) </span><span class="sxs-lookup"><span data-stu-id="c9c44-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="getset"></a><span data-ttu-id="c9c44-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="c9c44-107">Get/set</span></span>

<span data-ttu-id="c9c44-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="c9c44-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c9c44-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="c9c44-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c9c44-110">適用於</span><span class="sxs-lookup"><span data-stu-id="c9c44-110">Applies to</span></span>

[<span data-ttu-id="c9c44-111">**IMFInputTrustAuthority**</span><span class="sxs-lookup"><span data-stu-id="c9c44-111">**IMFInputTrustAuthority**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfinputtrustauthority)

## <a name="remarks"></a><span data-ttu-id="c9c44-112">備註</span><span class="sxs-lookup"><span data-stu-id="c9c44-112">Remarks</span></span>

<span data-ttu-id="c9c44-113">此 attributet 可供 **IMFInputTrustAuthority** decrypter 使用。</span><span class="sxs-lookup"><span data-stu-id="c9c44-113">This attributet can be used by an **IMFInputTrustAuthority** decrypter.</span></span> <span data-ttu-id="c9c44-114"> (CDM) 的內容解密模組的執行可能包括 **IMFInputTrustAuthority** 的執行。</span><span class="sxs-lookup"><span data-stu-id="c9c44-114">An implementation of a Content Decryption Module (CDM) may include an implementation of **IMFInputTrustAuthority**.</span></span> <span data-ttu-id="c9c44-115">**IMFInputTrustAuthority** 物件是透過 [IMFContentDecryptionModule：： CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput)存取。</span><span class="sxs-lookup"><span data-stu-id="c9c44-115">The **IMFInputTrustAuthority** object is accessed through [IMFContentDecryptionModule::CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).</span></span>


<span data-ttu-id="c9c44-116">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="c9c44-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9c44-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9c44-117">Requirements</span></span>



| <span data-ttu-id="c9c44-118">需求</span><span class="sxs-lookup"><span data-stu-id="c9c44-118">Requirement</span></span> | <span data-ttu-id="c9c44-119">值</span><span class="sxs-lookup"><span data-stu-id="c9c44-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9c44-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9c44-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c9c44-121">Windows 10 2020 年4月更新</span><span class="sxs-lookup"><span data-stu-id="c9c44-121">Windows 10 April 2020 Update</span></span>   <br/>                                        |
| <span data-ttu-id="c9c44-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c9c44-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9c44-123"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9c44-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9c44-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9c44-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9c44-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="c9c44-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[<span data-ttu-id="c9c44-126">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="c9c44-126">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
