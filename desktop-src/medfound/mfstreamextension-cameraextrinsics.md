---
description: 包含資料流程的相機 extrinsics。
ms.assetid: 2236C135-BA3D-4C1B-8A39-5E23EF67425A
title: 'MFStreamExtension_CameraExtrinsics 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a551aaaef48100d6104804e54f7e0ddfac3f5cb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114401"
---
# <a name="mfstreamextension_cameraextrinsics-attribute"></a><span data-ttu-id="af478-103">MFStreamExtension \_ CameraExtrinsics 屬性</span><span class="sxs-lookup"><span data-stu-id="af478-103">MFStreamExtension\_CameraExtrinsics attribute</span></span>

<span data-ttu-id="af478-104">包含資料流程的相機 extrinsics。</span><span class="sxs-lookup"><span data-stu-id="af478-104">Contains the camera extrinsics for the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="af478-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="af478-105">Data type</span></span>

<span data-ttu-id="af478-106">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="af478-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="af478-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="af478-107">Get/set</span></span>

<span data-ttu-id="af478-108">若要取得這個屬性，請呼叫 [**IMFMediaSourceEx：： GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes)。</span><span class="sxs-lookup"><span data-stu-id="af478-108">To get this attribute, call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).</span></span>

## <a name="remarks"></a><span data-ttu-id="af478-109">備註</span><span class="sxs-lookup"><span data-stu-id="af478-109">Remarks</span></span>

<span data-ttu-id="af478-110">屬性的值是 [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics)。</span><span class="sxs-lookup"><span data-stu-id="af478-110">The value of the attribute is a [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span></span>

## <a name="requirements"></a><span data-ttu-id="af478-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="af478-111">Requirements</span></span>



| <span data-ttu-id="af478-112">需求</span><span class="sxs-lookup"><span data-stu-id="af478-112">Requirement</span></span> | <span data-ttu-id="af478-113">值</span><span class="sxs-lookup"><span data-stu-id="af478-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="af478-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af478-114">Minimum supported client</span></span><br/> | <span data-ttu-id="af478-115">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af478-115">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af478-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af478-116">Minimum supported server</span></span><br/> | <span data-ttu-id="af478-117">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af478-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="af478-118">標頭</span><span class="sxs-lookup"><span data-stu-id="af478-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="af478-119"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="af478-119"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




