---
description: 停止目前的編碼階段，或查詢目前的編碼傳遞是否為最後一次。
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: 'AVEncCommonPassEnd 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026b20cf0c13536403e7ccf32b160e8c6fc08141
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467890"
---
# <a name="avenccommonpassend-property"></a><span data-ttu-id="6e3a3-103">AVEncCommonPassEnd 屬性</span><span class="sxs-lookup"><span data-stu-id="6e3a3-103">AVEncCommonPassEnd property</span></span>

<span data-ttu-id="6e3a3-104">停止目前的編碼階段，或查詢目前的編碼傳遞是否為最後一次。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-104">Stops the current encoding pass, or queries whether the current encoding pass is the last one.</span></span>

<span data-ttu-id="6e3a3-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="6e3a3-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="6e3a3-106">Data type</span></span>

<span data-ttu-id="6e3a3-107">**變異 \_BOOL** (**VT \_ bool**) </span><span class="sxs-lookup"><span data-stu-id="6e3a3-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6e3a3-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="6e3a3-108">Property GUID</span></span>

<span data-ttu-id="6e3a3-109">**CODECAPI \_ AVEncCommonPassEnd**</span><span class="sxs-lookup"><span data-stu-id="6e3a3-109">**CODECAPI\_AVEncCommonPassEnd**</span></span>

## <a name="remarks"></a><span data-ttu-id="6e3a3-110">備註</span><span class="sxs-lookup"><span data-stu-id="6e3a3-110">Remarks</span></span>

<span data-ttu-id="6e3a3-111">將此屬性設定為 **VARIANT \_ TRUE** 會結束目前的編碼傳遞。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-111">Setting this property to **VARIANT\_TRUE** ends the current encoding pass.</span></span> <span data-ttu-id="6e3a3-112">將這個屬性設定為 **VARIANT \_ FALSE** 會終止 multipass 編碼。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-112">Setting this property to **VARIANT\_FALSE** terminates multipass encoding.</span></span>

<span data-ttu-id="6e3a3-113">讀取此屬性會查詢目前的編碼傳遞是否為最後一次。</span><span class="sxs-lookup"><span data-stu-id="6e3a3-113">Reading this property queries whether the current encoding pass is the last one.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e3a3-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e3a3-114">Requirements</span></span>



| <span data-ttu-id="6e3a3-115">需求</span><span class="sxs-lookup"><span data-stu-id="6e3a3-115">Requirement</span></span> | <span data-ttu-id="6e3a3-116">值</span><span class="sxs-lookup"><span data-stu-id="6e3a3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e3a3-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e3a3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6e3a3-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e3a3-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="6e3a3-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e3a3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6e3a3-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e3a3-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6e3a3-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6e3a3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e3a3-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e3a3-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e3a3-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e3a3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e3a3-124">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="6e3a3-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="6e3a3-125">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="6e3a3-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




