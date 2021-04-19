---
description: 包含此範例的 pinhole 攝影機內建函式。
ms.assetid: AF7EA6A0-90C5-49A8-AD68-776BF770A448
title: 'MFSampleExtension_PinholeCameraIntrinsics 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb9e78641c0baab0e9eda3083aafaf8fe92229f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987467"
---
# <a name="mfsampleextension_pinholecameraintrinsics-attribute"></a><span data-ttu-id="2eab5-103">MFSampleExtension \_ PinholeCameraIntrinsics 屬性</span><span class="sxs-lookup"><span data-stu-id="2eab5-103">MFSampleExtension\_PinholeCameraIntrinsics attribute</span></span>

<span data-ttu-id="2eab5-104">包含此範例的 pinhole 攝影機內建函式。</span><span class="sxs-lookup"><span data-stu-id="2eab5-104">Contains the pinhole camera intrinsics for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="2eab5-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="2eab5-105">Data type</span></span>

<span data-ttu-id="2eab5-106">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="2eab5-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="2eab5-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="2eab5-107">Get/set</span></span>

<span data-ttu-id="2eab5-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。</span><span class="sxs-lookup"><span data-stu-id="2eab5-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="2eab5-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。</span><span class="sxs-lookup"><span data-stu-id="2eab5-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="2eab5-110">適用於</span><span class="sxs-lookup"><span data-stu-id="2eab5-110">Applies to</span></span>

[<span data-ttu-id="2eab5-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="2eab5-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="2eab5-112">備註</span><span class="sxs-lookup"><span data-stu-id="2eab5-112">Remarks</span></span>

<span data-ttu-id="2eab5-113">屬性的值是 [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics)。</span><span class="sxs-lookup"><span data-stu-id="2eab5-113">The value of the attribute is a [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span></span>

<span data-ttu-id="2eab5-114">這個屬性是選擇性的，可支援未校正的相機。</span><span class="sxs-lookup"><span data-stu-id="2eab5-114">This attribute is optional to support cameras that are not calibrated.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eab5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2eab5-115">Requirements</span></span>



| <span data-ttu-id="2eab5-116">需求</span><span class="sxs-lookup"><span data-stu-id="2eab5-116">Requirement</span></span> | <span data-ttu-id="2eab5-117">值</span><span class="sxs-lookup"><span data-stu-id="2eab5-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2eab5-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2eab5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2eab5-119">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2eab5-119">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2eab5-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2eab5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2eab5-121">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2eab5-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2eab5-122">標頭</span><span class="sxs-lookup"><span data-stu-id="2eab5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eab5-123"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="2eab5-123"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




