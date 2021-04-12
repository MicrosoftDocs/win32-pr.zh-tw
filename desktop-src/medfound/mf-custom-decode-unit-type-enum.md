---
description: 指定 IMFSample 在 MFSampleExtension ForwardedDecodeUnits 集合中包含的單位類型 \_ 。
ms.assetid: B74890ED-9586-475B-8C77-457ECB893980
title: 'MF_CUSTOM_DECODE_UNIT_TYPE 列舉 (Mfapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_CUSTOM_DECODE_UNIT_TYPE
api_type:
- HeaderDef
api_location:
- mfapi.h
ms.openlocfilehash: 406f6b3f6b93ced212ccf06910b69761ac0dfd9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191897"
---
# <a name="mf_custom_decode_unit_type-enumeration"></a><span data-ttu-id="8c73c-103">MF \_ 自訂解碼 \_ \_ 單位 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="8c73c-103">MF\_CUSTOM\_DECODE\_UNIT\_TYPE enumeration</span></span>

<span data-ttu-id="8c73c-104">指定 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 在 [MFSampleExtension \_ ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md) 集合中包含的單位類型。</span><span class="sxs-lookup"><span data-stu-id="8c73c-104">Specifies the type of unit contained in an [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in a [MFSampleExtension\_ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md) collection.</span></span>

## <a name="members"></a><span data-ttu-id="8c73c-105">成員</span><span class="sxs-lookup"><span data-stu-id="8c73c-105">Members</span></span>



| <span data-ttu-id="8c73c-106">member</span><span class="sxs-lookup"><span data-stu-id="8c73c-106">Member</span></span>                    | <span data-ttu-id="8c73c-107">描述</span><span class="sxs-lookup"><span data-stu-id="8c73c-107">Description</span></span>                                                             | <span data-ttu-id="8c73c-108">值</span><span class="sxs-lookup"><span data-stu-id="8c73c-108">Value</span></span> |
|---------------------------|-------------------------------------------------------------------------|-------|
| <span data-ttu-id="8c73c-109">**MF \_ 解碼 \_ 單位 \_ NAL**</span><span class="sxs-lookup"><span data-stu-id="8c73c-109">**MF\_DECODE\_UNIT\_NAL**</span></span> | <span data-ttu-id="8c73c-110">單位類型是網路抽象層單位， (NALU) 。</span><span class="sxs-lookup"><span data-stu-id="8c73c-110">The unit type is network abstraction layer unit (NALU).</span></span> <br/>     | <span data-ttu-id="8c73c-111">0</span><span class="sxs-lookup"><span data-stu-id="8c73c-111">0</span></span>     |
| <span data-ttu-id="8c73c-112">**MF \_ 解碼 \_ 單位 \_ SEI**</span><span class="sxs-lookup"><span data-stu-id="8c73c-112">**MF\_DECODE\_UNIT\_SEI**</span></span> | <span data-ttu-id="8c73c-113">單位類型為補充增強資訊 (SEI) 。</span><span class="sxs-lookup"><span data-stu-id="8c73c-113">The unit type is Supplemental Enhancement Information (SEI).</span></span><br/> | <span data-ttu-id="8c73c-114">1</span><span class="sxs-lookup"><span data-stu-id="8c73c-114">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="8c73c-115">備註</span><span class="sxs-lookup"><span data-stu-id="8c73c-115">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8c73c-116">需求</span><span class="sxs-lookup"><span data-stu-id="8c73c-116">Requirements</span></span>



| <span data-ttu-id="8c73c-117">需求</span><span class="sxs-lookup"><span data-stu-id="8c73c-117">Requirement</span></span> | <span data-ttu-id="8c73c-118">值</span><span class="sxs-lookup"><span data-stu-id="8c73c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8c73c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c73c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8c73c-120">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c73c-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8c73c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c73c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8c73c-122">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c73c-122">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8c73c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="8c73c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c73c-124"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c73c-124"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




