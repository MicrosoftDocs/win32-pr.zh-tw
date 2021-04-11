---
description: 指定軟體發行者憑證 (SPC) ，以及用來簽署檔的憑證鏈。
ms.assetid: b65b4129-df92-410c-b372-b0c004f8bb03
title: SIGNER_SPC_CHAIN_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SPC_CHAIN_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60279a60e6cdfbf43a1e2d9c45735b885d97a055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115533"
---
# <a name="signer_spc_chain_info-structure"></a><span data-ttu-id="886f8-103">簽署者 \_ SPC \_ 連鎖 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="886f8-103">SIGNER\_SPC\_CHAIN\_INFO structure</span></span>

<span data-ttu-id="886f8-104">**簽署者的 \_ spc \_ 鏈 \_ 資訊** 結構會指定 [*軟體發行者憑證*](../secgloss/s-gly.md) (SPC) ，以及用來簽署檔的憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="886f8-104">The **SIGNER\_SPC\_CHAIN\_INFO** structure specifies a [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) and certificate chain used to sign a document.</span></span>

> [!Note]  
> <span data-ttu-id="886f8-105">此結構未定義于任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="886f8-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="886f8-106">若要使用這個結構，您必須自行定義，如本主題所示。</span><span class="sxs-lookup"><span data-stu-id="886f8-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="886f8-107">語法</span><span class="sxs-lookup"><span data-stu-id="886f8-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SPC_CHAIN_INFO {
  DWORD      cbSize;
  LPCWSTR    pwszSpcFile;
  DWORD      dwCertPolicy;
  HCERTSTORE hCertStore;
} SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
```



## <a name="members"></a><span data-ttu-id="886f8-108">成員</span><span class="sxs-lookup"><span data-stu-id="886f8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="886f8-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="886f8-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="886f8-110">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="886f8-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="886f8-111">**pwszSpcFile**</span><span class="sxs-lookup"><span data-stu-id="886f8-111">**pwszSpcFile**</span></span>
</dt> <dd>

<span data-ttu-id="886f8-112">用來簽署檔的 SPC 檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="886f8-112">The name of the SPC file to use to sign a document.</span></span>

</dd> <dt>

<span data-ttu-id="886f8-113">**dwCertPolicy**</span><span class="sxs-lookup"><span data-stu-id="886f8-113">**dwCertPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="886f8-114">指定如何將憑證加入至簽章。</span><span class="sxs-lookup"><span data-stu-id="886f8-114">Specifies how certificates are added to the signature.</span></span> <span data-ttu-id="886f8-115">若要尋找憑證鏈，除了 **hCertStore** 成員所指定的存放區之外，還會檢查「我的」、「CA」、「根」和「SPC」存放區。</span><span class="sxs-lookup"><span data-stu-id="886f8-115">To find the certificate chain, the MY, CA, ROOT, and SPC stores, in addition to the store specified by the **hCertStore** member, are checked.</span></span> <span data-ttu-id="886f8-116">這個成員可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="886f8-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="886f8-117">值</span><span class="sxs-lookup"><span data-stu-id="886f8-117">Value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="886f8-118">意義</span><span class="sxs-lookup"><span data-stu-id="886f8-118">Meaning</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <span data-ttu-id="886f8-119"><dt>**簽署者 \_CERT \_ POLICY \_ CHAIN**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="886f8-119"><dt>**SIGNER\_CERT\_POLICY\_CHAIN**</dt> <dt>2 (0x2)</dt></span></span> </dl>                           | <span data-ttu-id="886f8-120">只新增憑證鏈中的憑證。</span><span class="sxs-lookup"><span data-stu-id="886f8-120">Add only certificates in the certificate chain.</span></span><br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <span data-ttu-id="886f8-121"><dt>**簽署者 \_CERT \_ POLICY \_ CHAIN \_ NO \_ ROOT**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="886f8-121"><dt>**SIGNER\_CERT\_POLICY\_CHAIN\_NO\_ROOT**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="886f8-122">只新增憑證鏈中的憑證，但不包含根憑證。</span><span class="sxs-lookup"><span data-stu-id="886f8-122">Add only certificates in the certificate chain, excluding the root certificate.</span></span><br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <span data-ttu-id="886f8-123"><dt>**簽署者 \_CERT \_ POLICY \_ STORE**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="886f8-123"><dt>**SIGNER\_CERT\_POLICY\_STORE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                           | <span data-ttu-id="886f8-124">新增 **hCertStore** 成員所指定之存放區中的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="886f8-124">Add all certificates in the store specified by the **hCertStore** member.</span></span> <span data-ttu-id="886f8-125">此旗標可以是與此成員的任何其他可能值的位 **or** 組合。</span><span class="sxs-lookup"><span data-stu-id="886f8-125">This flag can be a bitwise-**OR** combination with any of the other possible values for this member.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="886f8-126">**hCertStore**</span><span class="sxs-lookup"><span data-stu-id="886f8-126">**hCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="886f8-127">選擇性。</span><span class="sxs-lookup"><span data-stu-id="886f8-127">Optional.</span></span> <span data-ttu-id="886f8-128">其他憑證存放區的控制碼。</span><span class="sxs-lookup"><span data-stu-id="886f8-128">A handle to an additional certificate store.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="886f8-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="886f8-129">Requirements</span></span>



| <span data-ttu-id="886f8-130">需求</span><span class="sxs-lookup"><span data-stu-id="886f8-130">Requirement</span></span> | <span data-ttu-id="886f8-131">值</span><span class="sxs-lookup"><span data-stu-id="886f8-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="886f8-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="886f8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="886f8-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="886f8-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="886f8-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="886f8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="886f8-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="886f8-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="886f8-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="886f8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="886f8-137">**簽署 \_ 者憑證**</span><span class="sxs-lookup"><span data-stu-id="886f8-137">**SIGNER\_CERT**</span></span>](signer-cert.md)
</dt> </dl>

 

 
