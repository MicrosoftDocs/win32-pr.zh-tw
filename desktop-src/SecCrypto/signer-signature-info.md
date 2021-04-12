---
description: 包含數位簽章的相關資訊。
ms.assetid: 0b86fdf9-533f-4640-8c70-c3c8f4ef2c68
title: SIGNER_SIGNATURE_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SIGNATURE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8e2b1fa68da51a649a01d4356ebfb1519ceeffb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192947"
---
# <a name="signer_signature_info-structure"></a><span data-ttu-id="6dbc8-103">簽署人 \_ 簽名 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="6dbc8-103">SIGNER\_SIGNATURE\_INFO structure</span></span>

<span data-ttu-id="6dbc8-104">**簽署者簽章 \_ \_ 資訊** 結構包含數位簽章的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6dbc8-104">The **SIGNER\_SIGNATURE\_INFO** structure contains information about a digital signature.</span></span>

> [!Note]  
> <span data-ttu-id="6dbc8-105">此結構未定義于任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="6dbc8-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="6dbc8-106">若要使用這個結構，您必須自行定義，如本主題所示。</span><span class="sxs-lookup"><span data-stu-id="6dbc8-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6dbc8-107">語法</span><span class="sxs-lookup"><span data-stu-id="6dbc8-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SIGNATURE_INFO {
  DWORD             cbSize;
  ALG_ID            algidHash;
  DWORD             dwAttrChoice;
  union {
    SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
  };
  PCRYPT_ATTRIBUTES psAuthenticated;
  PCRYPT_ATTRIBUTES psUnauthenticated;
} SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
```



## <a name="members"></a><span data-ttu-id="6dbc8-108">成員</span><span class="sxs-lookup"><span data-stu-id="6dbc8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6dbc8-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="6dbc8-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="6dbc8-110">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6dbc8-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="6dbc8-111">**algidHash**</span><span class="sxs-lookup"><span data-stu-id="6dbc8-111">**algidHash**</span></span>
</dt> <dd>

<span data-ttu-id="6dbc8-112">用於數位簽章的雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="6dbc8-112">The hash algorithm used for the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="6dbc8-113">**dwAttrChoice**</span><span class="sxs-lookup"><span data-stu-id="6dbc8-113">**dwAttrChoice**</span></span>
</dt> <dd>

<span data-ttu-id="6dbc8-114">指定簽章是否有 [*Authenticode*](../secgloss/a-gly.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="6dbc8-114">Specifies whether the signature has [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span> <span data-ttu-id="6dbc8-115">這個成員可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="6dbc8-115">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="6dbc8-116">值</span><span class="sxs-lookup"><span data-stu-id="6dbc8-116">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="6dbc8-117">意義</span><span class="sxs-lookup"><span data-stu-id="6dbc8-117">Meaning</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_AUTHCODE_ATTR"></span><span id="signer_authcode_attr"></span><dl> <span data-ttu-id="6dbc8-118"><dt>**簽署者 \_AUTHCODE \_ ATTR**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6dbc8-118"><dt>**SIGNER\_AUTHCODE\_ATTR**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="6dbc8-119">簽名具有 [*Authenticode*](../secgloss/a-gly.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="6dbc8-119">The signature has [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span><br/>           |
| <span id="SIGNER_NO_ATTR"></span><span id="signer_no_attr"></span><dl> <span data-ttu-id="6dbc8-120"><dt>**簽署者 \_沒有 \_ ATTR**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6dbc8-120"><dt>**SIGNER\_NO\_ATTR**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="6dbc8-121">簽章沒有 [*Authenticode*](../secgloss/a-gly.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="6dbc8-121">The signature does not have [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6dbc8-122">**pAttrAuthcode**</span><span class="sxs-lookup"><span data-stu-id="6dbc8-122">**pAttrAuthcode**</span></span>
</dt> <dd>

<span data-ttu-id="6dbc8-123">指定 [*Authenticode*](../secgloss/a-gly.md) 簽章的屬性。</span><span class="sxs-lookup"><span data-stu-id="6dbc8-123">Specifies attributes for an [*Authenticode*](../secgloss/a-gly.md) signature.</span></span> <span data-ttu-id="6dbc8-124">如果 **dwAttrChoice** 成員的值為 **簽署者 \_ AUTHCODE \_ ATTR**，則需要這個成員。</span><span class="sxs-lookup"><span data-stu-id="6dbc8-124">This member is required if the value of the **dwAttrChoice** member is **SIGNER\_AUTHCODE\_ATTR**.</span></span>

</dd> <dt>

<span data-ttu-id="6dbc8-125">**psAuthenticated**</span><span class="sxs-lookup"><span data-stu-id="6dbc8-125">**psAuthenticated**</span></span>
</dt> <dd>

<span data-ttu-id="6dbc8-126">已驗證的使用者提供屬性已新增至數位簽章。</span><span class="sxs-lookup"><span data-stu-id="6dbc8-126">Authenticated user-supplied attributes added to the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="6dbc8-127">**psUnauthenticated**</span><span class="sxs-lookup"><span data-stu-id="6dbc8-127">**psUnauthenticated**</span></span>
</dt> <dd>

<span data-ttu-id="6dbc8-128">未驗證的使用者提供屬性已新增至數位簽章。</span><span class="sxs-lookup"><span data-stu-id="6dbc8-128">Unauthenticated user-supplied attributes added to the digital signature.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6dbc8-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="6dbc8-129">Requirements</span></span>



| <span data-ttu-id="6dbc8-130">需求</span><span class="sxs-lookup"><span data-stu-id="6dbc8-130">Requirement</span></span> | <span data-ttu-id="6dbc8-131">值</span><span class="sxs-lookup"><span data-stu-id="6dbc8-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6dbc8-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6dbc8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6dbc8-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dbc8-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6dbc8-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6dbc8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6dbc8-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dbc8-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6dbc8-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6dbc8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dbc8-137">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="6dbc8-137">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="6dbc8-138">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="6dbc8-138">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
