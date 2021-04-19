---
description: 指出 NALU 長度資訊將會以 BLOB 的形式傳送至每個壓縮的 h.264 範例。
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: 'MF_NALU_LENGTH_SET 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a01034cf62758787747882da40ac703d205fa55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997975"
---
# <a name="mf_nalu_length_set-attribute"></a><span data-ttu-id="4a298-103">MF \_ NALU \_ LENGTH \_ SET 屬性</span><span class="sxs-lookup"><span data-stu-id="4a298-103">MF\_NALU\_LENGTH\_SET attribute</span></span>

<span data-ttu-id="4a298-104">指出 NALU 長度資訊將會以 **BLOB** 的形式傳送至每個壓縮的 h.264 範例。</span><span class="sxs-lookup"><span data-stu-id="4a298-104">Indicates that NALU length information will be sent as a **BLOB** with each compressed H.264 sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="4a298-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="4a298-105">Data type</span></span>

<span data-ttu-id="4a298-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4a298-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4a298-107">備註</span><span class="sxs-lookup"><span data-stu-id="4a298-107">Remarks</span></span>

<span data-ttu-id="4a298-108">在 MEDIASUBTYPE H264 的輸入媒體類型上設定此屬性 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4a298-108">Set this attribute on the input media type of MEDIASUBTYPE\_H264.</span></span>

<span data-ttu-id="4a298-109">\_ \_ \_ 在輸入媒體類型的 h.264 解碼器上設定 MF NALU 長度，指出每個輸入範例都有可用的 NALU 長度，而每個輸入範例都包含一個完整的主要圖片。</span><span class="sxs-lookup"><span data-stu-id="4a298-109">Set MF\_NALU\_LENGTH\_SET on input media type of H.264 decoder, indicating each input sample will have a NALU length available and each input sample contains one complete primary picture.</span></span>

<span data-ttu-id="4a298-110">您可以從輸入範例上的 [MF \_ NALU \_ 長度 \_ 資訊](mf-nalu-length-information.md)屬性，取出包含 NALU 長度資訊的 **BLOB** 。</span><span class="sxs-lookup"><span data-stu-id="4a298-110">The **BLOB** containing the NALU length information can be retrieved from [MF\_NALU\_LENGTH\_INFORMATION](mf-nalu-length-information.md) attribute on the input sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a298-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a298-111">Requirements</span></span>



| <span data-ttu-id="4a298-112">需求</span><span class="sxs-lookup"><span data-stu-id="4a298-112">Requirement</span></span> | <span data-ttu-id="4a298-113">值</span><span class="sxs-lookup"><span data-stu-id="4a298-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a298-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a298-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4a298-115">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a298-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4a298-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a298-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4a298-117">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a298-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4a298-118">標頭</span><span class="sxs-lookup"><span data-stu-id="4a298-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a298-119"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a298-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a298-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a298-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a298-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="4a298-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4a298-122">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="4a298-122">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




