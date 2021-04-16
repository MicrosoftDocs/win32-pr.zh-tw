---
description: 指定呼叫端是否要配置用於輸出的材質。
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: 'MF_XVP_CALLER_ALLOCATES_OUTPUT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: def1b1d138c031393e1a1b1a3832c1ad6d066306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512257"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a><span data-ttu-id="2d823-103">MF \_ XVP \_ 呼叫端配置 \_ \_ 輸出屬性</span><span class="sxs-lookup"><span data-stu-id="2d823-103">MF\_XVP\_CALLER\_ALLOCATES\_OUTPUT attribute</span></span>

<span data-ttu-id="2d823-104">指定呼叫端是否要配置用於輸出的材質。</span><span class="sxs-lookup"><span data-stu-id="2d823-104">Specifies whether that the caller will allocate the textures used for output.</span></span>

## <a name="data-type"></a><span data-ttu-id="2d823-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="2d823-105">Data type</span></span>

<span data-ttu-id="2d823-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="2d823-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2d823-107">備註</span><span class="sxs-lookup"><span data-stu-id="2d823-107">Remarks</span></span>

<span data-ttu-id="2d823-108">如果此屬性為 **TRUE**，則影片處理器預期輸出材質會由呼叫端配置，即使在 DirectX video 加速作業 (DXVA) 模式下運作。</span><span class="sxs-lookup"><span data-stu-id="2d823-108">If this attribute is **TRUE**, the video processor expect output textures to be allocated by the caller, even when operating in DirectX Video Acceleration (DXVA) mode.</span></span> <span data-ttu-id="2d823-109">如果這個屬性為 **FALSE**，則在 DXVA 模式中操作時，影片處理器會配置輸出紋理，如果提供者提供的輸出紋理，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="2d823-109">If this attribute is **FALSE**, the video processor will allocate the output textures when operating in DXVA mode, and will fail if caller provided output textures are provided.</span></span>

<span data-ttu-id="2d823-110">若要設定此屬性：</span><span class="sxs-lookup"><span data-stu-id="2d823-110">To set this attribute:</span></span>

1.  <span data-ttu-id="2d823-111">在視頻處理器上呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 。</span><span class="sxs-lookup"><span data-stu-id="2d823-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video processor.</span></span>
2.  <span data-ttu-id="2d823-112">呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="2d823-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="2d823-113">開始串流之前，請設定屬性。</span><span class="sxs-lookup"><span data-stu-id="2d823-113">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d823-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d823-114">Requirements</span></span>



| <span data-ttu-id="2d823-115">需求</span><span class="sxs-lookup"><span data-stu-id="2d823-115">Requirement</span></span> | <span data-ttu-id="2d823-116">值</span><span class="sxs-lookup"><span data-stu-id="2d823-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2d823-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d823-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2d823-118">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d823-118">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2d823-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d823-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2d823-120">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d823-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2d823-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2d823-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d823-122"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d823-122"><dt>Mfidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d823-123">Idl</span><span class="sxs-lookup"><span data-stu-id="2d823-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2d823-124"><dt>Mfidl .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d823-124"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d823-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d823-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d823-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="2d823-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




