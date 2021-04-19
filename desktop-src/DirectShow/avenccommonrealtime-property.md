---
description: 指定應用程式是否需要即時編碼效能。
ms.assetid: 7e98a9f4-113b-45d0-ae55-7dc3f2af099e
title: 'AVEncCommonRealTime 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a03e51da1a088603273da3d083573e5921edf7a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106997469"
---
# <a name="avenccommonrealtime-property"></a><span data-ttu-id="ed355-103">AVEncCommonRealTime 屬性</span><span class="sxs-lookup"><span data-stu-id="ed355-103">AVEncCommonRealTime property</span></span>

<span data-ttu-id="ed355-104">指定應用程式是否需要即時編碼效能。</span><span class="sxs-lookup"><span data-stu-id="ed355-104">Specifies whether the application requires real-time encoding performance.</span></span>

<span data-ttu-id="ed355-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ed355-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="ed355-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="ed355-106">Data type</span></span>

<span data-ttu-id="ed355-107">**變異 \_BOOL** (**VT \_ bool**) </span><span class="sxs-lookup"><span data-stu-id="ed355-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ed355-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="ed355-108">Property GUID</span></span>

<span data-ttu-id="ed355-109">**CODECAPI \_ AVEncCommonRealTime**</span><span class="sxs-lookup"><span data-stu-id="ed355-109">**CODECAPI\_AVEncCommonRealTime**</span></span>

## <a name="remarks"></a><span data-ttu-id="ed355-110">備註</span><span class="sxs-lookup"><span data-stu-id="ed355-110">Remarks</span></span>

<span data-ttu-id="ed355-111">若要指定必須即時執行編碼，請將此屬性設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="ed355-111">To specify that encoding must be performed in real time, set this property to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="ed355-112">編解碼器也可以傳回此屬性作為功能。</span><span class="sxs-lookup"><span data-stu-id="ed355-112">Codecs can also return this property as a capability.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed355-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed355-113">Requirements</span></span>



| <span data-ttu-id="ed355-114">需求</span><span class="sxs-lookup"><span data-stu-id="ed355-114">Requirement</span></span> | <span data-ttu-id="ed355-115">值</span><span class="sxs-lookup"><span data-stu-id="ed355-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed355-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed355-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ed355-117">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed355-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ed355-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed355-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ed355-119">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed355-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ed355-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ed355-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed355-121"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ed355-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed355-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed355-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed355-123">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="ed355-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="ed355-124">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="ed355-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




