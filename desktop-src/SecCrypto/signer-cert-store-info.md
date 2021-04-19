---
description: 指定用來簽署檔的憑證存放區。
ms.assetid: aabad010-6fa3-4677-bd73-b8c52d68dbc8
title: SIGNER_CERT_STORE_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT_STORE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 197bd4855a7d2afec4c0b23662365e5f9197e302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998464"
---
# <a name="signer_cert_store_info-structure"></a><span data-ttu-id="7c993-103">簽署者 \_ 證書 \_ 存儲 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="7c993-103">SIGNER\_CERT\_STORE\_INFO structure</span></span>

<span data-ttu-id="7c993-104">**簽署者 \_ 證書 \_ 存儲 \_ 資訊** 結構會指定用來簽署檔的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="7c993-104">The **SIGNER\_CERT\_STORE\_INFO** structure specifies the certificate store used to sign a document.</span></span>

> [!Note]  
> <span data-ttu-id="7c993-105">此結構未定義于任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="7c993-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="7c993-106">若要使用這個結構，您必須自行定義，如本主題所示。</span><span class="sxs-lookup"><span data-stu-id="7c993-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7c993-107">語法</span><span class="sxs-lookup"><span data-stu-id="7c993-107">Syntax</span></span>


```C++
typedef struct _SIGNER_CERT_STORE_INFO {
  DWORD          cbSize;
  PCCERT_CONTEXT pSigningCert;
  DWORD          dwCertPolicy;
  HCERTSTORE     hCertStore;
} SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
```



## <a name="members"></a><span data-ttu-id="7c993-108">成員</span><span class="sxs-lookup"><span data-stu-id="7c993-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7c993-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="7c993-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="7c993-110">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7c993-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="7c993-111">**pSigningCert**</span><span class="sxs-lookup"><span data-stu-id="7c993-111">**pSigningCert**</span></span>
</dt> <dd>

<span data-ttu-id="7c993-112">簽署憑證之憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7c993-112">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure for the signing certificate.</span></span>

</dd> <dt>

<span data-ttu-id="7c993-113">**dwCertPolicy**</span><span class="sxs-lookup"><span data-stu-id="7c993-113">**dwCertPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="7c993-114">指定如何將憑證加入至簽章。</span><span class="sxs-lookup"><span data-stu-id="7c993-114">Specifies how certificates are added to the signature.</span></span> <span data-ttu-id="7c993-115">若要尋找憑證鏈，除了 **hCertStore** 成員所指定的存放區之外，還會檢查「我的」、「CA」、「根」和「SPC」存放區。</span><span class="sxs-lookup"><span data-stu-id="7c993-115">To find the certificate chain, the MY, CA, ROOT, and SPC stores, in addition to the store specified by the **hCertStore** member, are checked.</span></span> <span data-ttu-id="7c993-116">這個成員可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="7c993-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="7c993-117">值</span><span class="sxs-lookup"><span data-stu-id="7c993-117">Value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="7c993-118">意義</span><span class="sxs-lookup"><span data-stu-id="7c993-118">Meaning</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <span data-ttu-id="7c993-119"><dt>**簽署者 \_CERT \_ POLICY \_ CHAIN**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="7c993-119"><dt>**SIGNER\_CERT\_POLICY\_CHAIN**</dt> <dt>2 (0x2)</dt></span></span> </dl>                           | <span data-ttu-id="7c993-120">只新增憑證鏈中的憑證。</span><span class="sxs-lookup"><span data-stu-id="7c993-120">Add only certificates in the certificate chain.</span></span><br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <span data-ttu-id="7c993-121"><dt>**簽署者 \_CERT \_ POLICY \_ CHAIN \_ NO \_ ROOT**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="7c993-121"><dt>**SIGNER\_CERT\_POLICY\_CHAIN\_NO\_ROOT**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="7c993-122">只新增憑證鏈中的憑證，但不包含根憑證。</span><span class="sxs-lookup"><span data-stu-id="7c993-122">Add only certificates in the certificate chain, excluding the root certificate.</span></span><br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <span data-ttu-id="7c993-123"><dt>**簽署者 \_CERT \_ POLICY \_ STORE**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="7c993-123"><dt>**SIGNER\_CERT\_POLICY\_STORE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                           | <span data-ttu-id="7c993-124">新增 **hCertStore** 成員所指定之存放區中的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="7c993-124">Add all certificates in the store specified by the **hCertStore** member.</span></span> <span data-ttu-id="7c993-125">此旗標可以是與此成員的任何其他可能值的位 **or** 組合。</span><span class="sxs-lookup"><span data-stu-id="7c993-125">This flag can be a bitwise-**OR** combination with any of the other possible values for this member.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7c993-126">**hCertStore**</span><span class="sxs-lookup"><span data-stu-id="7c993-126">**hCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="7c993-127">選擇性。</span><span class="sxs-lookup"><span data-stu-id="7c993-127">Optional.</span></span> <span data-ttu-id="7c993-128">其他憑證存放區的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7c993-128">A handle to an additional certificate store.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c993-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c993-129">Requirements</span></span>



| <span data-ttu-id="7c993-130">需求</span><span class="sxs-lookup"><span data-stu-id="7c993-130">Requirement</span></span> | <span data-ttu-id="7c993-131">值</span><span class="sxs-lookup"><span data-stu-id="7c993-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7c993-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c993-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7c993-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c993-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7c993-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c993-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7c993-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c993-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c993-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c993-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c993-137">**簽署 \_ 者憑證**</span><span class="sxs-lookup"><span data-stu-id="7c993-137">**SIGNER\_CERT**</span></span>](signer-cert.md)
</dt> </dl>

 

 




