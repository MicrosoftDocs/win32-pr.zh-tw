---
title: 'WMDRM_ENCRYPT_SCATTER_BLOCK 結構 (Wmdrmsdk .h) '
description: WMDRM \_ 加密 \_ 散佈 \_ 區塊結構包含要加密的資料區塊。
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- WMDRM_ENCRYPT_SCATTER_BLOCK 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_BLOCK
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8911ba1822b146de4a99ff1fe144afcfd8e212e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982280"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a><span data-ttu-id="a5e3d-105">WMDRM \_ 加密 \_ 散佈 \_ 區塊結構</span><span class="sxs-lookup"><span data-stu-id="a5e3d-105">WMDRM\_ENCRYPT\_SCATTER\_BLOCK structure</span></span>

<span data-ttu-id="a5e3d-106">**WMDRM \_ 加密 \_ 散佈 \_ 區塊** 結構包含要加密的資料區塊。</span><span class="sxs-lookup"><span data-stu-id="a5e3d-106">The **WMDRM\_ENCRYPT\_SCATTER\_BLOCK** structure contains a block of data to be encrypted.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5e3d-107">語法</span><span class="sxs-lookup"><span data-stu-id="a5e3d-107">Syntax</span></span>


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_BLOCK {
  DWORD dwStreamID;
  DWORD cbBlock;
  BYTE  *pbBlock;
} ;
```



## <a name="members"></a><span data-ttu-id="a5e3d-108">成員</span><span class="sxs-lookup"><span data-stu-id="a5e3d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a5e3d-109">**dwStreamID**</span><span class="sxs-lookup"><span data-stu-id="a5e3d-109">**dwStreamID**</span></span>
</dt> <dd>

<span data-ttu-id="a5e3d-110">資料區塊所屬資料流程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5e3d-110">Identifier of the stream to which the data block belongs.</span></span>

</dd> <dt>

<span data-ttu-id="a5e3d-111">**cbBlock**</span><span class="sxs-lookup"><span data-stu-id="a5e3d-111">**cbBlock**</span></span>
</dt> <dd>

<span data-ttu-id="a5e3d-112">區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a5e3d-112">Size of block in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a5e3d-113">**pbBlock**</span><span class="sxs-lookup"><span data-stu-id="a5e3d-113">**pbBlock**</span></span>
</dt> <dd>

<span data-ttu-id="a5e3d-114">包含資料區塊之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="a5e3d-114">Pointer to a buffer containing the data block.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5e3d-115">備註</span><span class="sxs-lookup"><span data-stu-id="a5e3d-115">Remarks</span></span>

<span data-ttu-id="a5e3d-116">[**IWMDRMEncryptScatter：： EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md)方法會使用此結構來識別要加密的資料區塊。</span><span class="sxs-lookup"><span data-stu-id="a5e3d-116">This structure is used by the [**IWMDRMEncryptScatter::EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) method to identify blocks of data to encrypt.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5e3d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5e3d-117">Requirements</span></span>



| <span data-ttu-id="a5e3d-118">需求</span><span class="sxs-lookup"><span data-stu-id="a5e3d-118">Requirement</span></span> | <span data-ttu-id="a5e3d-119">值</span><span class="sxs-lookup"><span data-stu-id="a5e3d-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5e3d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="a5e3d-120">Header</span></span><br/> | <dl> <span data-ttu-id="a5e3d-121"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="a5e3d-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5e3d-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5e3d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5e3d-123">**結構**</span><span class="sxs-lookup"><span data-stu-id="a5e3d-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





