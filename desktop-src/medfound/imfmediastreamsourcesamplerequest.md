---
description: 表示來自 >mediastreamsource 的範例要求。
ms.assetid: 43617cda-84b1-405f-8a20-be793413c186
title: IMFMediaStreamSourceSampleRequest 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: fa159727c6e13a894148391b9508afad4b8dacfc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321580"
---
# <a name="imfmediastreamsourcesamplerequest-interface"></a><span data-ttu-id="a7351-103">IMFMediaStreamSourceSampleRequest 介面</span><span class="sxs-lookup"><span data-stu-id="a7351-103">IMFMediaStreamSourceSampleRequest interface</span></span>

<span data-ttu-id="a7351-104">表示來自 >mediastreamsource 的範例要求。</span><span class="sxs-lookup"><span data-stu-id="a7351-104">Represents a request for a sample from a MediaStreamSource.</span></span>

## <a name="members"></a><span data-ttu-id="a7351-105">成員</span><span class="sxs-lookup"><span data-stu-id="a7351-105">Members</span></span>

<span data-ttu-id="a7351-106">**IMFMediaStreamSourceSampleRequest** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="a7351-106">The **IMFMediaStreamSourceSampleRequest** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a7351-107">**IMFMediaStreamSourceSampleRequest** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a7351-107">**IMFMediaStreamSourceSampleRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="a7351-108">方法</span><span class="sxs-lookup"><span data-stu-id="a7351-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a7351-109">方法</span><span class="sxs-lookup"><span data-stu-id="a7351-109">Methods</span></span>

<span data-ttu-id="a7351-110">**IMFMediaStreamSourceSampleRequest** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a7351-110">The **IMFMediaStreamSourceSampleRequest** interface has these methods.</span></span>



| <span data-ttu-id="a7351-111">方法</span><span class="sxs-lookup"><span data-stu-id="a7351-111">Method</span></span>                                                           | <span data-ttu-id="a7351-112">描述</span><span class="sxs-lookup"><span data-stu-id="a7351-112">Description</span></span>                                             |
|:-----------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="a7351-113">**SetSample**</span><span class="sxs-lookup"><span data-stu-id="a7351-113">**SetSample**</span></span>](imfmediastreamsourcesamplerequest-setsample.md) | <span data-ttu-id="a7351-114">設定媒體資料流程來源的範例。</span><span class="sxs-lookup"><span data-stu-id="a7351-114">Sets the sample for the media stream source.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a7351-115">備註</span><span class="sxs-lookup"><span data-stu-id="a7351-115">Remarks</span></span>

<span data-ttu-id="a7351-116">**MFMediaStreamSourceSampleRequest** 是由 [**MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) 執行時間類別所執行。</span><span class="sxs-lookup"><span data-stu-id="a7351-116">**MFMediaStreamSourceSampleRequest** is implemented by the [**Windows.Media.Core.MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) runtime class.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7351-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7351-117">Requirements</span></span>



| <span data-ttu-id="a7351-118">需求</span><span class="sxs-lookup"><span data-stu-id="a7351-118">Requirement</span></span> | <span data-ttu-id="a7351-119">值</span><span class="sxs-lookup"><span data-stu-id="a7351-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a7351-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7351-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a7351-121">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7351-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="a7351-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7351-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a7351-123">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7351-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="a7351-124">Idl</span><span class="sxs-lookup"><span data-stu-id="a7351-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7351-125"><dt>Mfidl .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7351-125"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7351-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7351-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7351-127">媒體基礎介面</span><span class="sxs-lookup"><span data-stu-id="a7351-127">Media Foundation Interfaces</span></span>](media-foundation-interfaces.md)
</dt> </dl>

 

 
