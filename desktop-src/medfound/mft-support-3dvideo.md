---
description: 指定媒體基礎轉換 (MFT) 是否支援 3D stereoscopic 影片。
ms.assetid: DE96FD14-5C7E-4560-99AC-B1EBDA1EBB2B
title: 'MFT_SUPPORT_3DVIDEO 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdbc7208f9bbcf2c638ae83e988c6e541a4be2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992426"
---
# <a name="mft_support_3dvideo-attribute"></a><span data-ttu-id="b79fe-103">MFT \_ 支援 \_ 3DVIDEO 屬性</span><span class="sxs-lookup"><span data-stu-id="b79fe-103">MFT\_SUPPORT\_3DVIDEO attribute</span></span>

<span data-ttu-id="b79fe-104">指定媒體基礎轉換 (MFT) 是否支援 3D stereoscopic 影片。</span><span class="sxs-lookup"><span data-stu-id="b79fe-104">Specifies whether a Media Foundation transform (MFT) supports 3D stereoscopic video.</span></span>

## <a name="data-type"></a><span data-ttu-id="b79fe-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b79fe-105">Data type</span></span>

<span data-ttu-id="b79fe-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="b79fe-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b79fe-107">備註</span><span class="sxs-lookup"><span data-stu-id="b79fe-107">Remarks</span></span>

<span data-ttu-id="b79fe-108">若要查詢這個屬性，請呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 MFT 的全域屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="b79fe-108">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span> <span data-ttu-id="b79fe-109">如果 **GetAttributes** 成功，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="b79fe-109">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b79fe-110">這個屬性的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="b79fe-110">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="b79fe-111">將此屬性視為唯讀。</span><span class="sxs-lookup"><span data-stu-id="b79fe-111">Treat this attribute as read-only.</span></span> <span data-ttu-id="b79fe-112">請勿變更值;MFT 會忽略值的任何變更。</span><span class="sxs-lookup"><span data-stu-id="b79fe-112">Do not change the value; the MFT will ignore any changes to the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b79fe-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b79fe-113">Requirements</span></span>



| <span data-ttu-id="b79fe-114">需求</span><span class="sxs-lookup"><span data-stu-id="b79fe-114">Requirement</span></span> | <span data-ttu-id="b79fe-115">值</span><span class="sxs-lookup"><span data-stu-id="b79fe-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b79fe-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b79fe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b79fe-117">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b79fe-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b79fe-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b79fe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b79fe-119">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b79fe-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b79fe-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b79fe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b79fe-121"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="b79fe-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b79fe-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b79fe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b79fe-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="b79fe-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




