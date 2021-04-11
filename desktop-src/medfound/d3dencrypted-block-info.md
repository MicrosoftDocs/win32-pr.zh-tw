---
description: 指定要在受保護的視頻界面中加密的位元組。
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: 'D3DENCRYPTED_BLOCK_INFO 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DENCRYPTED_BLOCK_INFO
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21864dcc41ce86f139361af4357810137acf7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111801"
---
# <a name="d3dencrypted_block_info-structure"></a><span data-ttu-id="1855c-103">D3DENCRYPTED \_ 區塊 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="1855c-103">D3DENCRYPTED\_BLOCK\_INFO structure</span></span>

<span data-ttu-id="1855c-104">指定要在受保護的視頻界面中加密的位元組。</span><span class="sxs-lookup"><span data-stu-id="1855c-104">Specifies which bytes are encrypted in a protected video surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1855c-105">語法</span><span class="sxs-lookup"><span data-stu-id="1855c-105">Syntax</span></span>


```C++
typedef struct _D3DENCRYPTED_BLOCK_INFO {
  UINT NumEncryptedBytesAtBeginning;
  UINT NumBytesInSkipPattern;
  UINT NumBytesInEncryptPattern;
} D3DENCRYPTED_BLOCK_INFO;
```



## <a name="members"></a><span data-ttu-id="1855c-106">成員</span><span class="sxs-lookup"><span data-stu-id="1855c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1855c-107">**NumEncryptedBytesAtBeginning**</span><span class="sxs-lookup"><span data-stu-id="1855c-107">**NumEncryptedBytesAtBeginning**</span></span>
</dt> <dd>

<span data-ttu-id="1855c-108">在緩衝區開頭加密的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="1855c-108">The number of bytes that are encrypted at the start of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1855c-109">**NumBytesInSkipPattern**</span><span class="sxs-lookup"><span data-stu-id="1855c-109">**NumBytesInSkipPattern**</span></span>
</dt> <dd>

<span data-ttu-id="1855c-110">在第一個 **NumEncryptedBytesAtBeginning** 的位元組之後，以及每個 **NumBytesInEncryptPattern** 位元組區塊之後略過的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="1855c-110">The number of bytes that are skipped after the first **NumEncryptedBytesAtBeginning** bytes, and then after each block of **NumBytesInEncryptPattern** bytes.</span></span> <span data-ttu-id="1855c-111">略過的位元組不會加密。</span><span class="sxs-lookup"><span data-stu-id="1855c-111">Skipped bytes are not encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="1855c-112">**NumBytesInEncryptPattern**</span><span class="sxs-lookup"><span data-stu-id="1855c-112">**NumBytesInEncryptPattern**</span></span>
</dt> <dd>

<span data-ttu-id="1855c-113">在每個略過的位元組區塊之後加密的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="1855c-113">The number of bytes that are encrypted after each block of skipped bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1855c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1855c-114">Requirements</span></span>



| <span data-ttu-id="1855c-115">需求</span><span class="sxs-lookup"><span data-stu-id="1855c-115">Requirement</span></span> | <span data-ttu-id="1855c-116">值</span><span class="sxs-lookup"><span data-stu-id="1855c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1855c-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1855c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1855c-118">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1855c-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1855c-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1855c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1855c-120">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1855c-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1855c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="1855c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1855c-122"><dt>D3d9types (包含 D3d9) </dt></span><span class="sxs-lookup"><span data-stu-id="1855c-122"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1855c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1855c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1855c-124">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="1855c-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




