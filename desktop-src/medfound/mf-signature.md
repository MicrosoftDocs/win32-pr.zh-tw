---
description: 包含 (GRL) 簽章的全域撤銷清單。
ms.assetid: 388a901c-6202-41cf-9c3d-f29d8ccca76b
title: MF_SIGNATURE 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_SIGNATURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4827fea8e4259609cbb54f2b58a3d1c88ad6c23e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194861"
---
# <a name="mf_signature-structure"></a><span data-ttu-id="2f080-103">MF \_ 簽名結構</span><span class="sxs-lookup"><span data-stu-id="2f080-103">MF\_SIGNATURE structure</span></span>

<span data-ttu-id="2f080-104">包含 (GRL) 簽章的全域撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="2f080-104">Contains a global revocation list (GRL) signature.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f080-105">語法</span><span class="sxs-lookup"><span data-stu-id="2f080-105">Syntax</span></span>


```C++
typedef struct _MF_SIGNATURE {
  DWORD dwSignVer;
  DWORD cbSign;
  BYTE  rgSign[1];
} MF_SIGNATURE;
```



## <a name="members"></a><span data-ttu-id="2f080-106">成員</span><span class="sxs-lookup"><span data-stu-id="2f080-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2f080-107">**dwSignVer**</span><span class="sxs-lookup"><span data-stu-id="2f080-107">**dwSignVer**</span></span>
</dt> <dd>

<span data-ttu-id="2f080-108">簽章版本號碼。</span><span class="sxs-lookup"><span data-stu-id="2f080-108">The signature version number.</span></span>

</dd> <dt>

<span data-ttu-id="2f080-109">**cbSign**</span><span class="sxs-lookup"><span data-stu-id="2f080-109">**cbSign**</span></span>
</dt> <dd>

<span data-ttu-id="2f080-110">簽章的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f080-110">The size of the signature in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2f080-111">**rgSign**</span><span class="sxs-lookup"><span data-stu-id="2f080-111">**rgSign**</span></span>
</dt> <dd>

<span data-ttu-id="2f080-112">**CbSign** 大小的位元組陣列，其中包含簽章。</span><span class="sxs-lookup"><span data-stu-id="2f080-112">A byte array of size **cbSign** that contains the signature.</span></span> <span data-ttu-id="2f080-113">實際的陣列大小大於結構宣告中指定的大小。</span><span class="sxs-lookup"><span data-stu-id="2f080-113">The actual array size is larger than the size given in the structure declaration.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f080-114">備註</span><span class="sxs-lookup"><span data-stu-id="2f080-114">Remarks</span></span>

<span data-ttu-id="2f080-115">SDK 標頭中未宣告此結構。</span><span class="sxs-lookup"><span data-stu-id="2f080-115">This structure is not declared in an SDK header.</span></span> <span data-ttu-id="2f080-116">若要使用此結構，請將此處顯示的宣告新增至您的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="2f080-116">To use this structure, add the declaration shown here to your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f080-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f080-117">Requirements</span></span>



| <span data-ttu-id="2f080-118">需求</span><span class="sxs-lookup"><span data-stu-id="2f080-118">Requirement</span></span> | <span data-ttu-id="2f080-119">值</span><span class="sxs-lookup"><span data-stu-id="2f080-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2f080-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f080-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2f080-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f080-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2f080-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f080-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2f080-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f080-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f080-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f080-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f080-125">OPM 憑證撤銷</span><span class="sxs-lookup"><span data-stu-id="2f080-125">OPM Certificate Revocation</span></span>](opm-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="2f080-126">OPM 結構</span><span class="sxs-lookup"><span data-stu-id="2f080-126">OPM Structures</span></span>](opm-structures.md)
</dt> </dl>

 

 




