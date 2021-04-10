---
description: 啟用或停用影片解碼中的縮圖產生模式。
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: 'AVDecVideoThumbnailGenerationMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a9c8b095c0fdb0d44a5a12fdfe954b89ba49
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935981"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a><span data-ttu-id="d802b-103">AVDecVideoThumbnailGenerationMode 屬性</span><span class="sxs-lookup"><span data-stu-id="d802b-103">AVDecVideoThumbnailGenerationMode property</span></span>

<span data-ttu-id="d802b-104">啟用或停用影片解碼中的縮圖產生模式。</span><span class="sxs-lookup"><span data-stu-id="d802b-104">Enables or disables thumbnail generation mode in a video decoder.</span></span>

<span data-ttu-id="d802b-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d802b-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d802b-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="d802b-106">Data type</span></span>

<span data-ttu-id="d802b-107">**變異 \_BOOL** (**VT \_ bool**) </span><span class="sxs-lookup"><span data-stu-id="d802b-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d802b-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="d802b-108">Property GUID</span></span>

<span data-ttu-id="d802b-109">**CODECAPI \_ AVDecVideoThumbnailGenerationMode**</span><span class="sxs-lookup"><span data-stu-id="d802b-109">**CODECAPI\_AVDecVideoThumbnailGenerationMode**</span></span>

## <a name="remarks"></a><span data-ttu-id="d802b-110">備註</span><span class="sxs-lookup"><span data-stu-id="d802b-110">Remarks</span></span>

<span data-ttu-id="d802b-111">如果值為 **VARIANT \_ TRUE**，則此解碼器會使用已優化的設定來快速產生縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="d802b-111">If the value is **VARIANT\_TRUE**, the decoder uses a setting that is optimized to generate thumbnail images quickly.</span></span> <span data-ttu-id="d802b-112"> (例如，它可能會略過 B 或 P 框架。 ) 否則，如果值為 **VARIANT \_ FALSE**，則會使用其一般解碼設定。</span><span class="sxs-lookup"><span data-stu-id="d802b-112">(For example, it might skip B or P frames.) Otherwise, if the value is **VARIANT\_FALSE**, the decoder uses its normal decoding settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="d802b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d802b-113">Requirements</span></span>



| <span data-ttu-id="d802b-114">需求</span><span class="sxs-lookup"><span data-stu-id="d802b-114">Requirement</span></span> | <span data-ttu-id="d802b-115">值</span><span class="sxs-lookup"><span data-stu-id="d802b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d802b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d802b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d802b-117">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d802b-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d802b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d802b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d802b-119">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d802b-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d802b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d802b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d802b-121"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="d802b-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d802b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d802b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d802b-123">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="d802b-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d802b-124">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="d802b-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




