---
description: 指定密碼編譯服務提供者 (CSP) ，以及用來建立數位簽章的私密金鑰資訊。
ms.assetid: 85dc6a06-365a-4591-9d1d-117556a4417d
title: SIGNER_PROVIDER_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_PROVIDER_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 02cf4be124dd2ba1f39695bd5ca34af012cf7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978292"
---
# <a name="signer_provider_info-structure"></a><span data-ttu-id="5b3d0-103">簽署者 \_ 提供者 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="5b3d0-103">SIGNER\_PROVIDER\_INFO structure</span></span>

<span data-ttu-id="5b3d0-104">**簽署者 \_ 提供者 \_ 資訊** 結構會指定 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) ，以及用來建立數位簽章的私密金鑰資訊。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-104">The **SIGNER\_PROVIDER\_INFO** structure specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create a digital signature.</span></span>

> [!Note]  
> <span data-ttu-id="5b3d0-105">此結構未定義于任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="5b3d0-106">若要使用這個結構，您必須自行定義，如本主題所示。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5b3d0-107">語法</span><span class="sxs-lookup"><span data-stu-id="5b3d0-107">Syntax</span></span>


```C++
typedef struct _SIGNER_PROVIDER_INFO {
  DWORD   cbSize;
  LPCWSTR pwszProviderName;
  DWORD   dwProviderType;
  DWORD   dwKeySpec;
  DWORD   dwPvkChoice;
  union {
    LPWSTR pwszPvkFileName;
    LPWSTR pwszKeyContainer;
  };
} SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
```



## <a name="members"></a><span data-ttu-id="5b3d0-108">成員</span><span class="sxs-lookup"><span data-stu-id="5b3d0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5b3d0-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="5b3d0-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="5b3d0-110">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="5b3d0-111">**pwszProviderName**</span><span class="sxs-lookup"><span data-stu-id="5b3d0-111">**pwszProviderName**</span></span>
</dt> <dd>

<span data-ttu-id="5b3d0-112">用來建立數位簽章的 CSP 名稱。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-112">The name of the CSP used to create the digital signature.</span></span> <span data-ttu-id="5b3d0-113">如果這個成員的值為 **Null**，則會使用預設提供者。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-113">If the value of this member is **NULL**, the default provider is used.</span></span>

</dd> <dt>

<span data-ttu-id="5b3d0-114">**dwProviderType**</span><span class="sxs-lookup"><span data-stu-id="5b3d0-114">**dwProviderType**</span></span>
</dt> <dd>

<span data-ttu-id="5b3d0-115">**PwszProviderName** 成員所指定之 CSP 的型別。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-115">The type of the CSP specified by the **pwszProviderName** member.</span></span>

</dd> <dt>

<span data-ttu-id="5b3d0-116">**dwKeySpec**</span><span class="sxs-lookup"><span data-stu-id="5b3d0-116">**dwKeySpec**</span></span>
</dt> <dd>

<span data-ttu-id="5b3d0-117">金鑰規格。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-117">The key specification.</span></span> <span data-ttu-id="5b3d0-118">如果這個成員設定為零，則會使用 **pwszPvkFileName** 或 **pwszKeyContainer** 成員中的金鑰規格。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-118">If this member is set to zero, the key specification in the **pwszPvkFileName** or **pwszKeyContainer** member is used.</span></span> <span data-ttu-id="5b3d0-119">如果 **pwszKeyContainer** 成員中有一個 **以上的索引鍵規格，則會 \_** 使用簽章。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-119">If there is more than one key specification in the **pwszKeyContainer** member, **AT\_SIGNATURE** is used.</span></span> <span data-ttu-id="5b3d0-120">如果失敗，則會使用 **\_ KEYEXCHANGE** 。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-120">If it fails, **AT\_KEYEXCHANGE** is used.</span></span>

</dd> <dt>

<span data-ttu-id="5b3d0-121">**dwPvkChoice**</span><span class="sxs-lookup"><span data-stu-id="5b3d0-121">**dwPvkChoice**</span></span>
</dt> <dd>

<span data-ttu-id="5b3d0-122">指定私用金鑰資訊的類型。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-122">Specifies the type of private key information.</span></span> <span data-ttu-id="5b3d0-123">這個成員可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-123">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="5b3d0-124">值</span><span class="sxs-lookup"><span data-stu-id="5b3d0-124">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="5b3d0-125">意義</span><span class="sxs-lookup"><span data-stu-id="5b3d0-125">Meaning</span></span>                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="PVK_TYPE_FILE_NAME"></span><span id="pvk_type_file_name"></span><dl> <span data-ttu-id="5b3d0-126"><dt>**PVK \_輸入 \_ 檔案名 \_**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="5b3d0-126"><dt>**PVK\_TYPE\_FILE\_NAME**</dt> <dt>1 (0x1)</dt></span></span> </dl>         | <span data-ttu-id="5b3d0-127">私密金鑰資訊是檔案名。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-127">The private key information is a file name.</span></span><br/>     |
| <span id="PVK_TYPE_KEYCONTAINER"></span><span id="pvk_type_keycontainer"></span><dl> <span data-ttu-id="5b3d0-128"><dt>**PVK \_輸入 \_ KEYCONTAINER**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="5b3d0-128"><dt>**PVK\_TYPE\_KEYCONTAINER**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="5b3d0-129">私密金鑰資訊是金鑰容器。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-129">The private key information is a key container.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5b3d0-130">**pwszPvkFileName**</span><span class="sxs-lookup"><span data-stu-id="5b3d0-130">**pwszPvkFileName**</span></span>
</dt> <dd>

<span data-ttu-id="5b3d0-131">包含私用金鑰資訊的檔案名。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-131">The name of the file that contains the private key information.</span></span>

</dd> <dt>

<span data-ttu-id="5b3d0-132">**pwszKeyContainer**</span><span class="sxs-lookup"><span data-stu-id="5b3d0-132">**pwszKeyContainer**</span></span>
</dt> <dd>

<span data-ttu-id="5b3d0-133">包含私密金鑰資訊的金鑰容器名稱。</span><span class="sxs-lookup"><span data-stu-id="5b3d0-133">The name of the key container that contains the private key information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b3d0-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b3d0-134">Requirements</span></span>



| <span data-ttu-id="5b3d0-135">需求</span><span class="sxs-lookup"><span data-stu-id="5b3d0-135">Requirement</span></span> | <span data-ttu-id="5b3d0-136">值</span><span class="sxs-lookup"><span data-stu-id="5b3d0-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5b3d0-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b3d0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5b3d0-138">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b3d0-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5b3d0-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b3d0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5b3d0-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b3d0-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b3d0-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b3d0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b3d0-142">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="5b3d0-142">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="5b3d0-143">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="5b3d0-143">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
