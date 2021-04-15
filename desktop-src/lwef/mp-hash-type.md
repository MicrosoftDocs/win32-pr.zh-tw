---
title: 'MP_HASH_TYPE 列舉 (MpClient .h) '
description: 可能的雜湊類型。
ms.assetid: 46432C40-6DE1-4FB8-B7C1-C2712CCEB208
keywords:
- MP_HASH_TYPE 列舉舊版 Windows 環境功能
- PMP_HASH_TYPE 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MP_HASH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40c36e709d165845b729673df4aaea1042a7ee49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466661"
---
# <a name="mp_hash_type-enumeration"></a><span data-ttu-id="28d37-105">MP \_ HASH \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="28d37-105">MP\_HASH\_TYPE enumeration</span></span>

<span data-ttu-id="28d37-106">可能的雜湊類型。</span><span class="sxs-lookup"><span data-stu-id="28d37-106">Possible hash types.</span></span>

## <a name="syntax"></a><span data-ttu-id="28d37-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="28d37-107">Syntax</span></span>


```C++
typedef enum tagMP_HASH_TYPE { 
  MP_HASH_TYPE_NONE    = 0,
  MP_HASH_TYPE_CRC32   = 2,
  MP_HASH_TYPE_MD5     = 4,
  MP_HASH_TYPE_SHA1    = 8,
  MP_HASH_TYPE_SHA256  = 16
} MP_HASH_TYPE, *PMP_HASH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="28d37-108">常數</span><span class="sxs-lookup"><span data-stu-id="28d37-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="28d37-109"><span id="MP_HASH_TYPE_NONE"></span><span id="mp_hash_type_none"></span>**MP \_ HASH \_ 類型 \_ NONE**</span><span class="sxs-lookup"><span data-stu-id="28d37-109"><span id="MP_HASH_TYPE_NONE"></span><span id="mp_hash_type_none"></span>**MP\_HASH\_TYPE\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="28d37-110">沒有雜湊。</span><span class="sxs-lookup"><span data-stu-id="28d37-110">No hash.</span></span>

</dd> <dt>

<span data-ttu-id="28d37-111"><span id="MP_HASH_TYPE_CRC32"></span><span id="mp_hash_type_crc32"></span>**MP \_ HASH \_ TYPE \_ CRC32**</span><span class="sxs-lookup"><span data-stu-id="28d37-111"><span id="MP_HASH_TYPE_CRC32"></span><span id="mp_hash_type_crc32"></span>**MP\_HASH\_TYPE\_CRC32**</span></span>
</dt> <dd>

<span data-ttu-id="28d37-112">CRC32</span><span class="sxs-lookup"><span data-stu-id="28d37-112">CRC32</span></span>

</dd> <dt>

<span data-ttu-id="28d37-113"><span id="MP_HASH_TYPE_MD5"></span><span id="mp_hash_type_md5"></span>**MP \_ HASH \_ 類型 \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="28d37-113"><span id="MP_HASH_TYPE_MD5"></span><span id="mp_hash_type_md5"></span>**MP\_HASH\_TYPE\_MD5**</span></span>
</dt> <dd>

<span data-ttu-id="28d37-114">MD5</span><span class="sxs-lookup"><span data-stu-id="28d37-114">MD5</span></span>

</dd> <dt>

<span data-ttu-id="28d37-115"><span id="MP_HASH_TYPE_SHA1"></span><span id="mp_hash_type_sha1"></span>**MP \_ HASH \_ 類型 \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="28d37-115"><span id="MP_HASH_TYPE_SHA1"></span><span id="mp_hash_type_sha1"></span>**MP\_HASH\_TYPE\_SHA1**</span></span>
</dt> <dd>

<span data-ttu-id="28d37-116">SHA1</span><span class="sxs-lookup"><span data-stu-id="28d37-116">SHA1</span></span>

</dd> <dt>

<span data-ttu-id="28d37-117"><span id="MP_HASH_TYPE_SHA256"></span><span id="mp_hash_type_sha256"></span>**MP \_ HASH \_ TYPE \_ SHA256**</span><span class="sxs-lookup"><span data-stu-id="28d37-117"><span id="MP_HASH_TYPE_SHA256"></span><span id="mp_hash_type_sha256"></span>**MP\_HASH\_TYPE\_SHA256**</span></span>
</dt> <dd>

<span data-ttu-id="28d37-118">SHA 256</span><span class="sxs-lookup"><span data-stu-id="28d37-118">SHA 256</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28d37-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="28d37-119">Requirements</span></span>



| <span data-ttu-id="28d37-120">需求</span><span class="sxs-lookup"><span data-stu-id="28d37-120">Requirement</span></span> | <span data-ttu-id="28d37-121">值</span><span class="sxs-lookup"><span data-stu-id="28d37-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28d37-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28d37-122">Minimum supported client</span></span><br/> | <span data-ttu-id="28d37-123">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28d37-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="28d37-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28d37-124">Minimum supported server</span></span><br/> | <span data-ttu-id="28d37-125">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28d37-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="28d37-126">標頭</span><span class="sxs-lookup"><span data-stu-id="28d37-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="28d37-127"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="28d37-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





