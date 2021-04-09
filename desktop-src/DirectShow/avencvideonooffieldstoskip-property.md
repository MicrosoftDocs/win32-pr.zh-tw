---
description: 指定編碼期間要跳過的欄位數目。
ms.assetid: 82f2a2c1-52ff-410d-b5da-b2419c0adfe3
title: 'AVEncVideoNoOfFieldsToSkip 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708ef409fb907520d6a582599da2050a1353636c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846131"
---
# <a name="avencvideonooffieldstoskip-property"></a><span data-ttu-id="683cd-103">AVEncVideoNoOfFieldsToSkip 屬性</span><span class="sxs-lookup"><span data-stu-id="683cd-103">AVEncVideoNoOfFieldsToSkip property</span></span>

<span data-ttu-id="683cd-104">指定編碼期間要跳過的欄位數目。</span><span class="sxs-lookup"><span data-stu-id="683cd-104">Specifies the number of fields to skip during encoding.</span></span>

<span data-ttu-id="683cd-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="683cd-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="683cd-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="683cd-106">Data type</span></span>

<span data-ttu-id="683cd-107">**UINT64** (**VT \_ UI8**) </span><span class="sxs-lookup"><span data-stu-id="683cd-107">**UINT64** (**VT\_UI8**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="683cd-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="683cd-108">Property GUID</span></span>

<span data-ttu-id="683cd-109">**CODECAPI \_ AVEncVideoNoOfFieldsToSkip**</span><span class="sxs-lookup"><span data-stu-id="683cd-109">**CODECAPI\_AVEncVideoNoOfFieldsToSkip**</span></span>

## <a name="remarks"></a><span data-ttu-id="683cd-110">備註</span><span class="sxs-lookup"><span data-stu-id="683cd-110">Remarks</span></span>

<span data-ttu-id="683cd-111">若為漸進式影片，請將此屬性設定為要略過的畫面格數目的兩倍。</span><span class="sxs-lookup"><span data-stu-id="683cd-111">For progressive video, set this property to twice the number of frames to skip.</span></span>

## <a name="requirements"></a><span data-ttu-id="683cd-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="683cd-112">Requirements</span></span>



| <span data-ttu-id="683cd-113">需求</span><span class="sxs-lookup"><span data-stu-id="683cd-113">Requirement</span></span> | <span data-ttu-id="683cd-114">值</span><span class="sxs-lookup"><span data-stu-id="683cd-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="683cd-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="683cd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="683cd-116">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="683cd-116">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="683cd-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="683cd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="683cd-118">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="683cd-118">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="683cd-119">標頭</span><span class="sxs-lookup"><span data-stu-id="683cd-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="683cd-120"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="683cd-120"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="683cd-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="683cd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="683cd-122">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="683cd-122">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="683cd-123">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="683cd-123">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




