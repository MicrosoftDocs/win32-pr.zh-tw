---
description: 指定編碼器是否在資料流程結尾新增序列結束代碼。 這個屬性會套用至 MPEG 視頻編碼器。
ms.assetid: ef606207-2ee3-420b-afae-67c764e05e54
title: 'AVEncMPVAddSeqEndCode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a21adcf8b817e0049da3308760e20cdd0e9d473
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510204"
---
# <a name="avencmpvaddseqendcode-property"></a><span data-ttu-id="f1aae-104">AVEncMPVAddSeqEndCode 屬性</span><span class="sxs-lookup"><span data-stu-id="f1aae-104">AVEncMPVAddSeqEndCode property</span></span>

<span data-ttu-id="f1aae-105">指定編碼器是否在資料流程結尾新增序列結束代碼。</span><span class="sxs-lookup"><span data-stu-id="f1aae-105">Specifies whether the encoder adds a sequence end code at the end of the stream.</span></span> <span data-ttu-id="f1aae-106">這個屬性會套用至 MPEG 視頻編碼器。</span><span class="sxs-lookup"><span data-stu-id="f1aae-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="f1aae-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f1aae-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="f1aae-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="f1aae-108">Data type</span></span>

<span data-ttu-id="f1aae-109">**變異 \_BOOL** (**VT \_ bool**) </span><span class="sxs-lookup"><span data-stu-id="f1aae-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f1aae-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="f1aae-110">Property GUID</span></span>

<span data-ttu-id="f1aae-111">**CODECAPI \_ AVEncMPVAddSeqEndCode**</span><span class="sxs-lookup"><span data-stu-id="f1aae-111">**CODECAPI\_AVEncMPVAddSeqEndCode**</span></span>

## <a name="remarks"></a><span data-ttu-id="f1aae-112">備註</span><span class="sxs-lookup"><span data-stu-id="f1aae-112">Remarks</span></span>

<span data-ttu-id="f1aae-113">如果此值為 **VARIANT \_ TRUE**，編碼器會在資料流程的結尾加入序列結束代碼。</span><span class="sxs-lookup"><span data-stu-id="f1aae-113">If the value is **VARIANT\_TRUE**, the encoder adds a sequence end code at the end of the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1aae-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1aae-114">Requirements</span></span>



| <span data-ttu-id="f1aae-115">需求</span><span class="sxs-lookup"><span data-stu-id="f1aae-115">Requirement</span></span> | <span data-ttu-id="f1aae-116">值</span><span class="sxs-lookup"><span data-stu-id="f1aae-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1aae-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1aae-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f1aae-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1aae-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="f1aae-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1aae-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f1aae-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1aae-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f1aae-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f1aae-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1aae-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1aae-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1aae-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1aae-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1aae-124">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="f1aae-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="f1aae-125">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="f1aae-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




