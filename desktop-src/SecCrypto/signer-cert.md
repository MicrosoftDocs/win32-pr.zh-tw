---
description: 指定用來簽署檔的憑證。 憑證可以儲存在軟體發行者憑證 (SPC) 檔或憑證存放區中。
ms.assetid: 9a99ce98-237d-4223-ab3d-0576041038e3
title: SIGNER_CERT 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT
api_type:
- NA
api_location: ''
ms.openlocfilehash: a14f955749e98ca34cda0be2c57a3d5c546afc41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194363"
---
# <a name="signer_cert-structure"></a><span data-ttu-id="e9d37-104">簽署者 \_ CERT 結構</span><span class="sxs-lookup"><span data-stu-id="e9d37-104">SIGNER\_CERT structure</span></span>

<span data-ttu-id="e9d37-105">**簽署者 \_ CERT** 結構會指定 [*用來*](../secgloss/c-gly.md)簽署檔的憑證。</span><span class="sxs-lookup"><span data-stu-id="e9d37-105">The **SIGNER\_CERT** structure specifies a [*certificate*](../secgloss/c-gly.md) used to sign a document.</span></span> <span data-ttu-id="e9d37-106">憑證可以儲存在 [*軟體發行者憑證*](../secgloss/s-gly.md) (SPC) 檔或 [*憑證存放區*](../secgloss/c-gly.md)中。</span><span class="sxs-lookup"><span data-stu-id="e9d37-106">The certificate can be stored in a [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) file or in a [*certificate store*](../secgloss/c-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="e9d37-107">此結構未定義于任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="e9d37-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="e9d37-108">若要使用這個結構，您必須自行定義，如本主題所示。</span><span class="sxs-lookup"><span data-stu-id="e9d37-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e9d37-109">語法</span><span class="sxs-lookup"><span data-stu-id="e9d37-109">Syntax</span></span>


```C++
typedef struct _SIGNER_CERT {
  DWORD cbSize;
  DWORD dwCertChoice;
  union {
    LPCWSTR                pwszSpcFile;
    SIGNER_CERT_STORE_INFO *pCertStoreInfo;
    SIGNER_SPC_CHAIN_INFO  *pSpcChainInfo;
  };
  HWND  hwnd;
} SIGNER_CERT, *PSIGNER_CERT;
```



## <a name="members"></a><span data-ttu-id="e9d37-110">成員</span><span class="sxs-lookup"><span data-stu-id="e9d37-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9d37-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="e9d37-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="e9d37-112">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e9d37-112">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="e9d37-113">**dwCertChoice**</span><span class="sxs-lookup"><span data-stu-id="e9d37-113">**dwCertChoice**</span></span>
</dt> <dd>

<span data-ttu-id="e9d37-114">指定憑證的儲存方式。</span><span class="sxs-lookup"><span data-stu-id="e9d37-114">Specifies how the certificate is stored.</span></span> <span data-ttu-id="e9d37-115">這個成員可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="e9d37-115">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="e9d37-116">值</span><span class="sxs-lookup"><span data-stu-id="e9d37-116">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="e9d37-117">意義</span><span class="sxs-lookup"><span data-stu-id="e9d37-117">Meaning</span></span>                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_SPC_FILE"></span><span id="signer_cert_spc_file"></span><dl> <span data-ttu-id="e9d37-118"><dt>**簽署者 \_CERT \_ SPC \_ FILE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e9d37-118"><dt>**SIGNER\_CERT\_SPC\_FILE**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="e9d37-119">憑證會儲存在 SPC 檔案中。</span><span class="sxs-lookup"><span data-stu-id="e9d37-119">The certificate is stored in an SPC file.</span></span> <span data-ttu-id="e9d37-120">**PwszSpcFile** 成員包含 SPC 檔案的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="e9d37-120">The **pwszSpcFile** member contains the path and file name of the SPC file.</span></span><br/>                                                                                                                                                  |
| <span id="SIGNER_CERT_STORE"></span><span id="signer_cert_store"></span><dl> <span data-ttu-id="e9d37-121"><dt>**簽署者 \_證書 \_ 存儲**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e9d37-121"><dt>**SIGNER\_CERT\_STORE**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="e9d37-122">憑證會儲存在憑證存放區中。</span><span class="sxs-lookup"><span data-stu-id="e9d37-122">The certificate is stored in a certificate store.</span></span> <span data-ttu-id="e9d37-123">**PCertStoreInfo** 成員包含 [**簽署者 \_ 證書 \_ 存儲 \_ 資訊**](signer-cert-store-info.md)結構的指標，此結構會指定儲存憑證的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="e9d37-123">The **pCertStoreInfo** member contains a pointer to a [**SIGNER\_CERT\_STORE\_INFO**](signer-cert-store-info.md) structure that specifies the certificate store in which the certificate is stored.</span></span><br/>                 |
| <span id="SIGNER_CERT_SPC_CHAIN"></span><span id="signer_cert_spc_chain"></span><dl> <span data-ttu-id="e9d37-124"><dt>**簽署者 \_CERT \_ SPC \_ CHAIN**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e9d37-124"><dt>**SIGNER\_CERT\_SPC\_CHAIN**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="e9d37-125">憑證會儲存在 SPC 檔案中，並與憑證鏈相關聯。</span><span class="sxs-lookup"><span data-stu-id="e9d37-125">The certificate is stored in an SPC file and is associated with a certificate chain.</span></span> <span data-ttu-id="e9d37-126">**PSpcChainInfo** 成員包含 [**簽署者 \_ SPC \_ 連鎖 \_ 資訊**](signer-spc-chain-info.md)結構的指標，其中包含憑證的連鎖資訊。</span><span class="sxs-lookup"><span data-stu-id="e9d37-126">The **pSpcChainInfo** member contains a pointer to a [**SIGNER\_SPC\_CHAIN\_INFO**](signer-spc-chain-info.md) structure that contains the chain information for the certificate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e9d37-127">**pwszSpcFile**</span><span class="sxs-lookup"><span data-stu-id="e9d37-127">**pwszSpcFile**</span></span>
</dt> <dd>

<span data-ttu-id="e9d37-128">以 null 終止的 Unicode 字串指標，其中包含儲存憑證之 SPC 檔案的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="e9d37-128">A pointer to a null-terminated Unicode string that contains the path and file name of the SPC file in which the certificate is stored.</span></span> <span data-ttu-id="e9d37-129">只有當 **dwCertChoice** 成員包含 **簽署者憑證 \_ \_ SPC \_** 檔案時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="e9d37-129">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_SPC\_FILE**.</span></span>

</dd> <dt>

<span data-ttu-id="e9d37-130">**pCertStoreInfo**</span><span class="sxs-lookup"><span data-stu-id="e9d37-130">**pCertStoreInfo**</span></span>
</dt> <dd>

<span data-ttu-id="e9d37-131">[**簽署者 \_ 證書 \_ 存儲 \_ 資訊**](signer-cert-store-info.md)結構的指標，指定儲存憑證的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="e9d37-131">A pointer to a [**SIGNER\_CERT\_STORE\_INFO**](signer-cert-store-info.md) structure that specifies the certificate store in which the certificate is stored.</span></span> <span data-ttu-id="e9d37-132">只有當 **dwCertChoice** 成員包含「 **簽署人」 \_ 證書 \_ 存儲** 時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="e9d37-132">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_STORE**.</span></span>

</dd> <dt>

<span data-ttu-id="e9d37-133">**pSpcChainInfo**</span><span class="sxs-lookup"><span data-stu-id="e9d37-133">**pSpcChainInfo**</span></span>
</dt> <dd>

<span data-ttu-id="e9d37-134">[**簽署者的 \_ SPC \_ 連鎖 \_ 資訊**](signer-spc-chain-info.md)結構的指標，其中包含憑證的鏈資訊。</span><span class="sxs-lookup"><span data-stu-id="e9d37-134">A pointer to a [**SIGNER\_SPC\_CHAIN\_INFO**](signer-spc-chain-info.md) structure that contains the chain information for the certificate.</span></span> <span data-ttu-id="e9d37-135">只有在 **dwCertChoice** 成員包含 **簽署者憑證 \_ \_ SPC \_ 鏈** 時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="e9d37-135">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_SPC\_CHAIN**.</span></span>

</dd> <dt>

<span data-ttu-id="e9d37-136">**hwnd**</span><span class="sxs-lookup"><span data-stu-id="e9d37-136">**hwnd**</span></span>
</dt> <dd>

<span data-ttu-id="e9d37-137">要做為顯示之任何對話方塊擁有者使用的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="e9d37-137">The handle of the window to use as the owner of any dialog boxes that are displayed.</span></span> <span data-ttu-id="e9d37-138">目前未使用這個成員，所以會忽略。</span><span class="sxs-lookup"><span data-stu-id="e9d37-138">This member is not currently used and is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9d37-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9d37-139">Requirements</span></span>



| <span data-ttu-id="e9d37-140">需求</span><span class="sxs-lookup"><span data-stu-id="e9d37-140">Requirement</span></span> | <span data-ttu-id="e9d37-141">值</span><span class="sxs-lookup"><span data-stu-id="e9d37-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e9d37-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9d37-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e9d37-143">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9d37-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e9d37-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9d37-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e9d37-145">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9d37-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9d37-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9d37-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9d37-147">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="e9d37-147">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="e9d37-148">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="e9d37-148">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
