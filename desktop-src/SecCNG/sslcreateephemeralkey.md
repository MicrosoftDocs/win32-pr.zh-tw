---
description: 建立在安全通訊端層通訊協定 (SSL) 交握期間所發生驗證期間所使用的暫時金鑰。
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: 'SslCreateEphemeralKey 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateEphemeralKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452b0166da367bb6b1530f5669e55b7ca909e13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000106"
---
# <a name="sslcreateephemeralkey-function"></a><span data-ttu-id="cd8c8-103">SslCreateEphemeralKey 函式</span><span class="sxs-lookup"><span data-stu-id="cd8c8-103">SslCreateEphemeralKey function</span></span>

<span data-ttu-id="cd8c8-104">**SslCreateEphemeralKey** 函式會建立暫時金鑰，以供在 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 交握期間進行驗證時使用。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-104">The **SslCreateEphemeralKey** function creates an ephemeral key for use during the authentication that occurs during the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) handshake.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd8c8-105">語法</span><span class="sxs-lookup"><span data-stu-id="cd8c8-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateEphemeralKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phEphemeralKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _In_  DWORD              dwKeyBitLen,
  _In_  PBYTE              pbParams,
  _In_  DWORD              cbParams,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="cd8c8-106">參數</span><span class="sxs-lookup"><span data-stu-id="cd8c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd8c8-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd8c8-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd8c8-108">SSL 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="cd8c8-109">*phEphemeralKey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cd8c8-109">*phEphemeralKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd8c8-110">暫時金鑰的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-110">The handle of the ephemeral key.</span></span>

</dd> <dt>

<span data-ttu-id="cd8c8-111">*dwProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd8c8-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd8c8-112">其中一個 [**CNG SSL 提供者通訊協定識別碼**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="cd8c8-113">*dwCipherSuite* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd8c8-113">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd8c8-114">其中一個 [**CNG SSL 提供者加密套件識別碼**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-114">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="cd8c8-115">*dwKeyType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd8c8-115">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd8c8-116">其中一個 [**CNG SSL 提供者金鑰類型識別碼**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) 值。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-116">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="cd8c8-117">針對非 [*橢圓曲線密碼*](/windows/desktop/SecGloss/e-gly) 編譯 (ECC) 的索引鍵類型，將此參數設定為零。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-117">Set this parameter to zero for key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC).</span></span>

</dd> <dt>

<span data-ttu-id="cd8c8-118">*dwKeyBitLen* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd8c8-118">*dwKeyBitLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd8c8-119">金鑰的長度 (位元數)。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-119">The length, in bits, of the key.</span></span>

</dd> <dt>

<span data-ttu-id="cd8c8-120">*pbParams* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd8c8-120">*pbParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd8c8-121">緩衝區的指標，其中包含要建立之索引鍵的參數。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-121">A pointer to a buffer to contain parameters for the key that is to be created.</span></span> <span data-ttu-id="cd8c8-122">如果未使用 [*diffie-hellman (暫時) 金鑰交換演算法*](/windows/desktop/SecGloss/d-gly) (DHE) 加密套件，請將 *pbParams* 參數設定為 **Null** ，並將 *cbParams* 參數設定為零。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-122">If a [*Diffie-Hellman (ephemeral) key-exchange algorithm*](/windows/desktop/SecGloss/d-gly) (DHE) cipher suite is not used, set the *pbParams* parameter to **NULL** and the *cbParams* parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="cd8c8-123">*cbParams* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd8c8-123">*cbParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd8c8-124">*PbParams* 緩衝區中資料的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-124">The length, in bytes, of the data in the *pbParams* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cd8c8-125">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd8c8-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd8c8-126">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-126">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd8c8-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd8c8-127">Return value</span></span>

<span data-ttu-id="cd8c8-128">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="cd8c8-129">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-129">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="cd8c8-130">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="cd8c8-130">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="cd8c8-131">Description</span><span class="sxs-lookup"><span data-stu-id="cd8c8-131">Description</span></span>                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="cd8c8-132">不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="cd8c8-132"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="cd8c8-133">記憶體不足，無法配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-133">There is insufficient memory to allocate the buffer.</span></span><br/> |
| <dl> <span data-ttu-id="cd8c8-134">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="cd8c8-134"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="cd8c8-135">*HSslProvider* 控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-135">The *hSslProvider* handle is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="cd8c8-136">不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="cd8c8-136"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="cd8c8-137">其中一個提供的參數無效。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-137">One of the supplied parameters is not valid.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="cd8c8-138">備註</span><span class="sxs-lookup"><span data-stu-id="cd8c8-138">Remarks</span></span>

<span data-ttu-id="cd8c8-139">使用 DHE 加密套件時，內部 SSL 執行會將伺服器 *p* 和 *g* 參數傳遞至 *pbParams* 和 *cbParams* 參數中的 **SslCreateEphemeralKey** 函式。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-139">When using a DHE cipher suite, the internal SSL implementation passes server *p* and *g* parameters to the **SslCreateEphemeralKey** function in the *pbParams* and *cbParams* parameters.</span></span>

<span data-ttu-id="cd8c8-140">*PbParams* 緩衝區中的資料格式與設定 [**BCRYPT \_ DH \_ PARAMETERS**](cng-property-identifiers.md)屬性時所使用的格式相同，且開頭為 [**BCRYPT \_ DH \_ 參數 \_ 標頭**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header)結構。</span><span class="sxs-lookup"><span data-stu-id="cd8c8-140">The format of the data in the *pbParams* buffer is the same as that used when setting the [**BCRYPT\_DH\_PARAMETERS**](cng-property-identifiers.md) property, and it starts with a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd8c8-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd8c8-141">Requirements</span></span>



| <span data-ttu-id="cd8c8-142">需求</span><span class="sxs-lookup"><span data-stu-id="cd8c8-142">Requirement</span></span> | <span data-ttu-id="cd8c8-143">值</span><span class="sxs-lookup"><span data-stu-id="cd8c8-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd8c8-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd8c8-144">Minimum supported client</span></span><br/> | <span data-ttu-id="cd8c8-145">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd8c8-145">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cd8c8-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd8c8-146">Minimum supported server</span></span><br/> | <span data-ttu-id="cd8c8-147">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd8c8-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cd8c8-148">標頭</span><span class="sxs-lookup"><span data-stu-id="cd8c8-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd8c8-149"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="cd8c8-149"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="cd8c8-150">DLL</span><span class="sxs-lookup"><span data-stu-id="cd8c8-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd8c8-151"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd8c8-151"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

