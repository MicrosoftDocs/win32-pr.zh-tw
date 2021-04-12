---
description: 指示影片範例配置器使用索引 mutex 將材質建立為可共用。
ms.assetid: 798CA474-3B1A-4795-81B7-563749197104
title: 'MF_SA_D3D11_SHARED 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff6ecb23a99a732e183bc16942e33bbb4f8e3a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193013"
---
# <a name="mf_sa_d3d11_shared-attribute"></a><span data-ttu-id="4e0c6-103">MF \_ SA \_ D3D11 \_ 共用屬性</span><span class="sxs-lookup"><span data-stu-id="4e0c6-103">MF\_SA\_D3D11\_SHARED attribute</span></span>

<span data-ttu-id="4e0c6-104">指示影片範例配置器使用索引 mutex 將材質建立為可共用。</span><span class="sxs-lookup"><span data-stu-id="4e0c6-104">Indicates to the video sample allocator to create textures as shareable using keyed-mutex.</span></span>

## <a name="data-type"></a><span data-ttu-id="4e0c6-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="4e0c6-105">Data type</span></span>

<span data-ttu-id="4e0c6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4e0c6-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4e0c6-107">備註</span><span class="sxs-lookup"><span data-stu-id="4e0c6-107">Remarks</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="4e0c6-108">範例配置器</span><span class="sxs-lookup"><span data-stu-id="4e0c6-108">Sample Allocator</span></span>

<span data-ttu-id="4e0c6-109">您可以在影片範例配置器的 [**IMFVideoSampleAllocatorEx：： InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) 方法中設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4e0c6-109">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e0c6-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e0c6-110">Requirements</span></span>



| <span data-ttu-id="4e0c6-111">需求</span><span class="sxs-lookup"><span data-stu-id="4e0c6-111">Requirement</span></span> | <span data-ttu-id="4e0c6-112">值</span><span class="sxs-lookup"><span data-stu-id="4e0c6-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e0c6-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e0c6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4e0c6-114">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e0c6-114">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="4e0c6-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e0c6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4e0c6-116">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e0c6-116">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="4e0c6-117">標頭</span><span class="sxs-lookup"><span data-stu-id="4e0c6-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e0c6-118"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="4e0c6-118"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e0c6-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e0c6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e0c6-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="4e0c6-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4e0c6-121">**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**</span><span class="sxs-lookup"><span data-stu-id="4e0c6-121">**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)
</dt> <dt>

[<span data-ttu-id="4e0c6-122">未搭配 MUTEX 的 MF \_ SA \_ D3D11 \_ 共用 \_ \_</span><span class="sxs-lookup"><span data-stu-id="4e0c6-122">MF\_SA\_D3D11\_SHARED\_WITHOUT\_MUTEX</span></span>](mf-sa-d3d11-shared-without-mutex.md)
</dt> </dl>

 

 




