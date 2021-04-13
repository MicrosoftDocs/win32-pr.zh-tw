---
description: 包含128位進階加密標準 CTR 模式 (CTR) 區塊加密加密 (IV) 的初始化向量。
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: 'D3DAES_CTR_IV 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAES_CTR_IV
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6e0d543fb0e57ae34f181e7ff0f40a1a1f8222b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317992"
---
# <a name="d3daes_ctr_iv-structure"></a><span data-ttu-id="59168-103">D3DAES \_ CTR \_ IV 結構</span><span class="sxs-lookup"><span data-stu-id="59168-103">D3DAES\_CTR\_IV structure</span></span>

<span data-ttu-id="59168-104">包含128位進階加密標準 CTR 模式 (CTR) 區塊加密加密 (IV) 的初始化向量。</span><span class="sxs-lookup"><span data-stu-id="59168-104">Contains an initialization vector (IV) for 128-bit Advanced Encryption Standard CTR mode (AES-CTR) block cipher encryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="59168-105">語法</span><span class="sxs-lookup"><span data-stu-id="59168-105">Syntax</span></span>


```C++
typedef struct _D3DAES_CTR_IV {
  UINT64 IV;
  UINT64 Count;
} D3DAES_CTR_IV;
```



## <a name="members"></a><span data-ttu-id="59168-106">成員</span><span class="sxs-lookup"><span data-stu-id="59168-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="59168-107">**IV**</span><span class="sxs-lookup"><span data-stu-id="59168-107">**IV**</span></span>
</dt> <dd>

<span data-ttu-id="59168-108">以位元組由大到小的格式的 IV。</span><span class="sxs-lookup"><span data-stu-id="59168-108">The IV, in big-endian format.</span></span>

</dd> <dt>

<span data-ttu-id="59168-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="59168-109">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="59168-110">以位元組由大到小的格式的區塊計數。</span><span class="sxs-lookup"><span data-stu-id="59168-110">The block count, in big-endian format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59168-111">備註</span><span class="sxs-lookup"><span data-stu-id="59168-111">Remarks</span></span>

<span data-ttu-id="59168-112">**D3DAES \_ CTR \_ Iv** 結構和 [**DXVA2 \_ AES \_ CTR \_ iv**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv)結構是相等的。</span><span class="sxs-lookup"><span data-stu-id="59168-112">The **D3DAES\_CTR\_IV** structure and the [**DXVA2\_AES\_CTR\_IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) structure are equivalent.</span></span>

<span data-ttu-id="59168-113">如需詳細資訊，請參閱 [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv)。</span><span class="sxs-lookup"><span data-stu-id="59168-113">For details, see [**DXVA2\_AES\_CTR\_IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).</span></span>

## <a name="requirements"></a><span data-ttu-id="59168-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="59168-114">Requirements</span></span>



| <span data-ttu-id="59168-115">需求</span><span class="sxs-lookup"><span data-stu-id="59168-115">Requirement</span></span> | <span data-ttu-id="59168-116">值</span><span class="sxs-lookup"><span data-stu-id="59168-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59168-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59168-117">Minimum supported client</span></span><br/> | <span data-ttu-id="59168-118">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59168-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="59168-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59168-119">Minimum supported server</span></span><br/> | <span data-ttu-id="59168-120">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59168-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="59168-121">標頭</span><span class="sxs-lookup"><span data-stu-id="59168-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="59168-122"><dt>D3d9types (包含 D3d9) </dt></span><span class="sxs-lookup"><span data-stu-id="59168-122"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59168-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59168-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59168-124">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="59168-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




