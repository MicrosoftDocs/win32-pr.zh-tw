---
description: 包含資料流程的 pinhole 攝影機內建函式。
ms.assetid: 7E5E7C60-9C3F-406B-A7DD-A953181CD314
title: 'MFStreamExtension_PinholeCameraIntrinsics 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9ad848f0b8cc12c2496544d98b4ef17332151
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943870"
---
# <a name="mfstreamextension_pinholecameraintrinsics-attribute"></a><span data-ttu-id="3074f-103">MFStreamExtension \_ PinholeCameraIntrinsics 屬性</span><span class="sxs-lookup"><span data-stu-id="3074f-103">MFStreamExtension\_PinholeCameraIntrinsics attribute</span></span>

<span data-ttu-id="3074f-104">包含資料流程的 pinhole 攝影機內建函式。</span><span class="sxs-lookup"><span data-stu-id="3074f-104">Contains the pinhole camera intrinsics for the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="3074f-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3074f-105">Data type</span></span>

<span data-ttu-id="3074f-106">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="3074f-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="3074f-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="3074f-107">Get/set</span></span>

<span data-ttu-id="3074f-108">若要取得這個屬性，請呼叫 [**IMFMediaSourceEx：： GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes)。</span><span class="sxs-lookup"><span data-stu-id="3074f-108">To get this attribute, call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).</span></span>

## <a name="remarks"></a><span data-ttu-id="3074f-109">備註</span><span class="sxs-lookup"><span data-stu-id="3074f-109">Remarks</span></span>

<span data-ttu-id="3074f-110">屬性的值是 [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics)。</span><span class="sxs-lookup"><span data-stu-id="3074f-110">The value of the attribute is a [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span></span>

## <a name="requirements"></a><span data-ttu-id="3074f-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="3074f-111">Requirements</span></span>



| <span data-ttu-id="3074f-112">需求</span><span class="sxs-lookup"><span data-stu-id="3074f-112">Requirement</span></span> | <span data-ttu-id="3074f-113">值</span><span class="sxs-lookup"><span data-stu-id="3074f-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3074f-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3074f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3074f-115">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3074f-115">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3074f-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3074f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3074f-117">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3074f-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3074f-118">標頭</span><span class="sxs-lookup"><span data-stu-id="3074f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3074f-119"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="3074f-119"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




