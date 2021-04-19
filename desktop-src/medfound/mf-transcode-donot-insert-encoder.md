---
description: 指定編碼器是否必須包含在轉碼拓撲中。
ms.assetid: 73f23aed-d1b9-4821-b1ca-0a07f02b6913
title: 'MF_TRANSCODE_DONOT_INSERT_ENCODER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d3f8fc5dabfd3e4c55c6242ba9b8f52b6f5c2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973887"
---
# <a name="mf_transcode_donot_insert_encoder-attribute"></a><span data-ttu-id="fa2b8-103">MF \_ 轉碼 \_ 沒有 \_ 插入 \_ 編碼器屬性</span><span class="sxs-lookup"><span data-stu-id="fa2b8-103">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER attribute</span></span>

<span data-ttu-id="fa2b8-104">指定編碼器是否必須包含在轉碼拓撲中。</span><span class="sxs-lookup"><span data-stu-id="fa2b8-104">Specifies whether an encoder must be included in the transcode topology.</span></span>

<span data-ttu-id="fa2b8-105">[**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology)函式會在拓撲建立期間檢查這個屬性。</span><span class="sxs-lookup"><span data-stu-id="fa2b8-105">The [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function checks this attribute during topology building.</span></span> <span data-ttu-id="fa2b8-106">如果未設定此屬性，則會將編碼器插入轉碼拓撲中。</span><span class="sxs-lookup"><span data-stu-id="fa2b8-106">If this attribute is not set, an encoder is inserted in the transcode topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="fa2b8-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="fa2b8-107">Data type</span></span>

<span data-ttu-id="fa2b8-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fa2b8-108">**UINT32**</span></span>



| <span data-ttu-id="fa2b8-109">值</span><span class="sxs-lookup"><span data-stu-id="fa2b8-109">Value</span></span>                                                                        | <span data-ttu-id="fa2b8-110">意義</span><span class="sxs-lookup"><span data-stu-id="fa2b8-110">Meaning</span></span>                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fa2b8-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fa2b8-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="fa2b8-112">編碼器會插入轉碼拓撲中。</span><span class="sxs-lookup"><span data-stu-id="fa2b8-112">An encoder is inserted in the transcode topology.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="fa2b8-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fa2b8-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="fa2b8-114">編碼器不會包含在轉碼拓撲中。</span><span class="sxs-lookup"><span data-stu-id="fa2b8-114">An encoder is not included in the transcode topology.</span></span> <span data-ttu-id="fa2b8-115">來源節點連接至輸出節點。</span><span class="sxs-lookup"><span data-stu-id="fa2b8-115">The source node is connected to the output node.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fa2b8-116">備註</span><span class="sxs-lookup"><span data-stu-id="fa2b8-116">Remarks</span></span>

<span data-ttu-id="fa2b8-117">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="fa2b8-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa2b8-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa2b8-118">Requirements</span></span>



| <span data-ttu-id="fa2b8-119">需求</span><span class="sxs-lookup"><span data-stu-id="fa2b8-119">Requirement</span></span> | <span data-ttu-id="fa2b8-120">值</span><span class="sxs-lookup"><span data-stu-id="fa2b8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fa2b8-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa2b8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fa2b8-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa2b8-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fa2b8-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa2b8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fa2b8-124">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa2b8-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="fa2b8-125">標頭</span><span class="sxs-lookup"><span data-stu-id="fa2b8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa2b8-126"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa2b8-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa2b8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa2b8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa2b8-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="fa2b8-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fa2b8-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="fa2b8-129">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




