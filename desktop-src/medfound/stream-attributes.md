---
description: 資料流程屬性
ms.assetid: 83b64ad8-2552-41d1-bc61-20361831020b
title: 資料流程屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a25de9ae6cf769268b3868d36bac2e293cfd8d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512544"
---
# <a name="stream-attributes"></a><span data-ttu-id="f2898-103">資料流程屬性</span><span class="sxs-lookup"><span data-stu-id="f2898-103">Stream Attributes</span></span>

<span data-ttu-id="f2898-104">下列屬性適用于媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="f2898-104">The following attributes apply to media streams.</span></span> <span data-ttu-id="f2898-105">若要從媒體範例取得屬性，請使用 [**IMFMediaSourceEx：： GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) 方法。</span><span class="sxs-lookup"><span data-stu-id="f2898-105">To get the attributes from a media sample, use the [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) method.</span></span>



| <span data-ttu-id="f2898-106">屬性</span><span class="sxs-lookup"><span data-stu-id="f2898-106">Attribute</span></span>                                                                                   | <span data-ttu-id="f2898-107">描述</span><span class="sxs-lookup"><span data-stu-id="f2898-107">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="f2898-108">MFStreamExtension \_ CameraExtrinsics</span><span class="sxs-lookup"><span data-stu-id="f2898-108">MFStreamExtension\_CameraExtrinsics</span></span>](mfstreamextension-cameraextrinsics.md)               | <span data-ttu-id="f2898-109">資料流程的相機 extrinsics。</span><span class="sxs-lookup"><span data-stu-id="f2898-109">The camera extrinsics for the stream.</span></span>         |
| [<span data-ttu-id="f2898-110">MFStreamExtension \_ PinholeCameraIntrinsics</span><span class="sxs-lookup"><span data-stu-id="f2898-110">MFStreamExtension\_PinholeCameraIntrinsics</span></span>](mfstreamextension-pinholecameraintrinsics.md) | <span data-ttu-id="f2898-111">資料流程的 pinhole 攝影機內建函式。</span><span class="sxs-lookup"><span data-stu-id="f2898-111">The pinhole camera intrinsics for the stream.</span></span> |



 

<span data-ttu-id="f2898-112">並非每個媒體資料流程都包含此處所列的每個屬性。</span><span class="sxs-lookup"><span data-stu-id="f2898-112">Not every media stream contains every attribute listed here.</span></span> <span data-ttu-id="f2898-113">在某些情況下，屬性只適用于特定類型的資料。</span><span class="sxs-lookup"><span data-stu-id="f2898-113">In some cases, an attribute applies only to certain kinds of data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2898-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2898-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2898-115">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="f2898-115">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="f2898-116">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="f2898-116">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f2898-117">媒體範例</span><span class="sxs-lookup"><span data-stu-id="f2898-117">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 



