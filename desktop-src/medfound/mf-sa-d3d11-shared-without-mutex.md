---
description: 指示影片範例配置器使用舊版機制，將材質建立為可共用。
ms.assetid: A9F4D4AF-BB47-48E2-B40A-D0245FD61FAF
title: 'MF_SA_D3D11_SHARED_WITHOUT_MUTEX 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9139328c9d272007be6e5cd9434614cb1de8c9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973686"
---
# <a name="mf_sa_d3d11_shared_without_mutex-attribute"></a><span data-ttu-id="2bc75-103">\_未搭配 \_ \_ \_ \_ MUTEX 屬性共用的 MF SA D3D11</span><span class="sxs-lookup"><span data-stu-id="2bc75-103">MF\_SA\_D3D11\_SHARED\_WITHOUT\_MUTEX attribute</span></span>

<span data-ttu-id="2bc75-104">指示影片範例配置器使用舊版機制，將材質建立為可共用。</span><span class="sxs-lookup"><span data-stu-id="2bc75-104">Indicates to the video sample allocator to create textures as shareable using the legacy mechanism.</span></span>

## <a name="data-type"></a><span data-ttu-id="2bc75-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="2bc75-105">Data type</span></span>

<span data-ttu-id="2bc75-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2bc75-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2bc75-107">備註</span><span class="sxs-lookup"><span data-stu-id="2bc75-107">Remarks</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="2bc75-108">範例配置器</span><span class="sxs-lookup"><span data-stu-id="2bc75-108">Sample Allocator</span></span>

<span data-ttu-id="2bc75-109">您可以在影片範例配置器的 [**IMFVideoSampleAllocatorEx：： InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) 方法中設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2bc75-109">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bc75-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bc75-110">Requirements</span></span>



| <span data-ttu-id="2bc75-111">需求</span><span class="sxs-lookup"><span data-stu-id="2bc75-111">Requirement</span></span> | <span data-ttu-id="2bc75-112">值</span><span class="sxs-lookup"><span data-stu-id="2bc75-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc75-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2bc75-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2bc75-114">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bc75-114">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="2bc75-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2bc75-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2bc75-116">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bc75-116">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="2bc75-117">標頭</span><span class="sxs-lookup"><span data-stu-id="2bc75-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bc75-118"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="2bc75-118"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bc75-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bc75-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bc75-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="2bc75-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2bc75-121">**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**</span><span class="sxs-lookup"><span data-stu-id="2bc75-121">**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)
</dt> <dt>

[<span data-ttu-id="2bc75-122">MF \_ SA \_ D3D11 \_ 共用</span><span class="sxs-lookup"><span data-stu-id="2bc75-122">MF\_SA\_D3D11\_SHARED</span></span>](mf-sa-d3d11-shared.md)
</dt> </dl>

 

 




