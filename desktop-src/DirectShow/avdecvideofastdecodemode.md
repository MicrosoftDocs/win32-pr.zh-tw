---
description: 取得或設定影片解碼速度。
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: 'AVDecVideoFastDecodeMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355c085731befedbcb9245a67870d9d609a92c6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109677"
---
# <a name="avdecvideofastdecodemode-property"></a><span data-ttu-id="32718-103">AVDecVideoFastDecodeMode 屬性</span><span class="sxs-lookup"><span data-stu-id="32718-103">AVDecVideoFastDecodeMode property</span></span>

<span data-ttu-id="32718-104">取得或設定影片解碼速度。</span><span class="sxs-lookup"><span data-stu-id="32718-104">Gets or sets the video decoding speed.</span></span>

## <a name="data-type"></a><span data-ttu-id="32718-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="32718-105">Data type</span></span>

<span data-ttu-id="32718-106">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="32718-106">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="32718-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="32718-107">Property GUID</span></span>

<span data-ttu-id="32718-108">**CODECAPI \_ AVDecVideoFastDecodeMode**</span><span class="sxs-lookup"><span data-stu-id="32718-108">**CODECAPI\_AVDecVideoFastDecodeMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="32718-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="32718-109">Property value</span></span>

<span data-ttu-id="32718-110">這個屬性的值範圍從0到32，其中0表示正常解碼，而32是最快速的解碼模式。</span><span class="sxs-lookup"><span data-stu-id="32718-110">The value of this property can range from 0 to 32, where 0 indicates normal decoding and 32 is the fastest decoding mode.</span></span> <span data-ttu-id="32718-111">確切的行為取決於解碼器的執行。</span><span class="sxs-lookup"><span data-stu-id="32718-111">The exact behavior depends on the decoder implementation.</span></span> <span data-ttu-id="32718-112">並非1和32之間的每個增量都必須定義為不同的模式。</span><span class="sxs-lookup"><span data-stu-id="32718-112">Not every increment between 1 and 32 necessarily defines is a distinct mode.</span></span>

<span data-ttu-id="32718-113">[**EAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode)列舉包含這個屬性的一些預先定義模式。</span><span class="sxs-lookup"><span data-stu-id="32718-113">The [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) enumeration contains some predefined modes for this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="32718-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="32718-114">Requirements</span></span>



| <span data-ttu-id="32718-115">需求</span><span class="sxs-lookup"><span data-stu-id="32718-115">Requirement</span></span> | <span data-ttu-id="32718-116">值</span><span class="sxs-lookup"><span data-stu-id="32718-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32718-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32718-117">Minimum supported client</span></span><br/> | <span data-ttu-id="32718-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32718-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="32718-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32718-119">Minimum supported server</span></span><br/> | <span data-ttu-id="32718-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32718-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="32718-121">標頭</span><span class="sxs-lookup"><span data-stu-id="32718-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="32718-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="32718-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32718-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32718-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32718-124">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="32718-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="32718-125">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="32718-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




