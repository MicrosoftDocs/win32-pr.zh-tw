---
title: 'WMDRM_ENCRYPT_SCATTER_INFO 結構 (Wmdrmsdk .h) '
description: WMDRM \_ 加密 \_ 散佈 \_ 資訊結構包含設定 IWMDRMEncryptScatter 介面以供使用所需的資訊。
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- WMDRM_ENCRYPT_SCATTER_INFO 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_INFO
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500012231f6860fd94038b240355eda9aa2aee44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982980"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a><span data-ttu-id="c17b1-105">WMDRM \_ 加密 \_ 散佈 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="c17b1-105">WMDRM\_ENCRYPT\_SCATTER\_INFO structure</span></span>

<span data-ttu-id="c17b1-106">**WMDRM \_ 加密 \_ 散佈 \_ 資訊** 結構包含設定 [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)介面以供使用所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="c17b1-106">The **WMDRM\_ENCRYPT\_SCATTER\_INFO** structure contains information needed to configure the [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) interface for use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c17b1-107">語法</span><span class="sxs-lookup"><span data-stu-id="c17b1-107">Syntax</span></span>


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_INFO {
  DWORD dwStreamID;
  DWORD dwSampleProtectionVersion;
  DWORD cbProtectionInfo;
  BYTE  *pbProtectionInfo;
} ;
```



## <a name="members"></a><span data-ttu-id="c17b1-108">成員</span><span class="sxs-lookup"><span data-stu-id="c17b1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c17b1-109">**dwStreamID**</span><span class="sxs-lookup"><span data-stu-id="c17b1-109">**dwStreamID**</span></span>
</dt> <dd>

<span data-ttu-id="c17b1-110">要加密之資料流程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c17b1-110">Identifier of the stream to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="c17b1-111">**dwSampleProtectionVersion**</span><span class="sxs-lookup"><span data-stu-id="c17b1-111">**dwSampleProtectionVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c17b1-112">用來從指定的資料流程編碼資料的範例保護版本。</span><span class="sxs-lookup"><span data-stu-id="c17b1-112">Sample protection version to be used to encode data from the specified stream.</span></span>

</dd> <dt>

<span data-ttu-id="c17b1-113">**cbProtectionInfo**</span><span class="sxs-lookup"><span data-stu-id="c17b1-113">**cbProtectionInfo**</span></span>
</dt> <dd>

<span data-ttu-id="c17b1-114">**PbProtectionInfo** 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c17b1-114">Size of the **pbProtectionInfo** buffer in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c17b1-115">**pbProtectionInfo**</span><span class="sxs-lookup"><span data-stu-id="c17b1-115">**pbProtectionInfo**</span></span>
</dt> <dd>

<span data-ttu-id="c17b1-116">包含額外保護資訊的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c17b1-116">Buffer containing additional protection information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c17b1-117">備註</span><span class="sxs-lookup"><span data-stu-id="c17b1-117">Remarks</span></span>

<span data-ttu-id="c17b1-118">此結構是由 [**IWMDRMEncryptScatter：： InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) 方法所使用。</span><span class="sxs-lookup"><span data-stu-id="c17b1-118">This structure is used by the [**IWMDRMEncryptScatter::InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c17b1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c17b1-119">Requirements</span></span>



| <span data-ttu-id="c17b1-120">需求</span><span class="sxs-lookup"><span data-stu-id="c17b1-120">Requirement</span></span> | <span data-ttu-id="c17b1-121">值</span><span class="sxs-lookup"><span data-stu-id="c17b1-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c17b1-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c17b1-122">Header</span></span><br/> | <dl> <span data-ttu-id="c17b1-123"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="c17b1-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c17b1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c17b1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c17b1-125">**結構**</span><span class="sxs-lookup"><span data-stu-id="c17b1-125">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





