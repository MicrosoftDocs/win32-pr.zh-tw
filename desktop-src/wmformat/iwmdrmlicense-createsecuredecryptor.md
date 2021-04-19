---
title: 'IWMDRMLicense CreateSecureDecryptor 方法 (Wmdrmsdk .h) '
description: CreateSecureDecryptor 方法會建立安全的解密子物件。 安全解密程式與一般解密程式不同，因為它會解密內容，然後根據此方法的參數中指定的設定重新加密。
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- CreateSecureDecryptor 方法 windows Media 格式
- CreateSecureDecryptor 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，CreateSecureDecryptor 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateSecureDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ededb4c985e345c1e40563d02c87bfe447b8960f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988248"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a><span data-ttu-id="d9b2d-107">IWMDRMLicense：： CreateSecureDecryptor 方法</span><span class="sxs-lookup"><span data-stu-id="d9b2d-107">IWMDRMLicense::CreateSecureDecryptor method</span></span>

<span data-ttu-id="d9b2d-108">**CreateSecureDecryptor** 方法會建立安全的解密子物件。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-108">The **CreateSecureDecryptor** method creates a secure decryptor object.</span></span> <span data-ttu-id="d9b2d-109">安全解密程式與一般解密程式不同，因為它會解密內容，然後根據此方法的參數中指定的設定重新加密。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-109">The secure decryptor differs from the normal decryptor in that it decrypts the content and then re-encrypts it according to the settings specified in the parameters of this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9b2d-110">語法</span><span class="sxs-lookup"><span data-stu-id="d9b2d-110">Syntax</span></span>


```C++
HRESULT CreateSecureDecryptor(
  [in]      BYTE          *pbCertificate,
  [in]      DWORD         cbCertificate,
  [in]      DWORD         dwCertificateType,
  [in]      DWORD         dwFlags,
  [out]     BYTE          *pbInitializationVector,
  [in, out] DWORD         *pcbInitializationVector,
  [out]     IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a><span data-ttu-id="d9b2d-111">參數</span><span class="sxs-lookup"><span data-stu-id="d9b2d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9b2d-112">*pbCertificate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d9b2d-112">*pbCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b2d-113">呼叫應用程式的憑證。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-113">Certificate of the calling application.</span></span>

</dd> <dt>

<span data-ttu-id="d9b2d-114">*cbCertificate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d9b2d-114">*cbCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b2d-115">憑證的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-115">Size of the certificate in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d9b2d-116">*dwCertificateType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d9b2d-116">*dwCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b2d-117">憑證的類型。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-117">The type of the certificate.</span></span> <span data-ttu-id="d9b2d-118">設定為 WMDRM \_ 憑證 \_ 類型 \_ XML。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-118">Set to WMDRM\_CERTIFICATE\_TYPE\_XML.</span></span>

</dd> <dt>

<span data-ttu-id="d9b2d-119">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d9b2d-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b2d-120">要用於重新編碼的會話保護類型。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-120">The type of session protection to use for re-encoding.</span></span> <span data-ttu-id="d9b2d-121">必須設定為下表中的其中一個常數：</span><span class="sxs-lookup"><span data-stu-id="d9b2d-121">Must be set to one of the constants in the following table:</span></span>



| <span data-ttu-id="d9b2d-122">常數</span><span class="sxs-lookup"><span data-stu-id="d9b2d-122">Constant</span></span>                     | <span data-ttu-id="d9b2d-123">描述</span><span class="sxs-lookup"><span data-stu-id="d9b2d-123">Description</span></span>                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b2d-124">WMDRM \_ 保護 \_ 類型 \_ RC4</span><span class="sxs-lookup"><span data-stu-id="d9b2d-124">WMDRM\_PROTECTION\_TYPE\_RC4</span></span> | <span data-ttu-id="d9b2d-125">使用 RC4 加密進行會話加密。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-125">Uses RC4 encryption for session encryption.</span></span> <span data-ttu-id="d9b2d-126">這是此版本唯一支援的會話保護。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-126">This is the only supported session protection for this version.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d9b2d-127">*pbInitializationVector* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d9b2d-127">*pbInitializationVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b2d-128">接收初始化向量。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-128">Receives the initialization vector.</span></span> <span data-ttu-id="d9b2d-129">初始化向量是使用 OAEP 填補配置與憑證中找到的 RSA 公開金鑰進行加密的 RSA。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-129">The initialization vector is RSA encrypted using the OAEP padding scheme with the RSA public key found in the certificate.</span></span> <span data-ttu-id="d9b2d-130">設定為 **Null** ，以接收 *pcbInitializationVector* 中所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-130">Set to **NULL** to receive the required buffer size in *pcbInitializationVector*.</span></span>

</dd> <dt>

<span data-ttu-id="d9b2d-131">*pcbInitializationVector* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d9b2d-131">*pcbInitializationVector* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b2d-132">在輸入時，緩衝區的大小會以 *pbInitializationVector* 的形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-132">On input, the size of the buffer passed as *pbInitializationVector*.</span></span> <span data-ttu-id="d9b2d-133">在輸出時，緩衝區所使用部分的大小。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-133">On output, the size of the used portion of the buffer.</span></span> <span data-ttu-id="d9b2d-134">如果您傳遞 **Null** 給 *pbInitializationVector*，此值會在輸出時設定為所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-134">If you pass **NULL** for *pbInitializationVector*, this value is set to the required buffer size on output.</span></span>

</dd> <dt>

<span data-ttu-id="d9b2d-135">*ppDecryptor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d9b2d-135">*ppDecryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b2d-136">接收新建立物件之 [**IWMDRMDecrypt**](iwmdrmdecrypt.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-136">Receives a pointer to the [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9b2d-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9b2d-137">Return value</span></span>

<span data-ttu-id="d9b2d-138">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-138">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d9b2d-139">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-139">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d9b2d-140">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d9b2d-140">Return code</span></span>                                                                          | <span data-ttu-id="d9b2d-141">Description</span><span class="sxs-lookup"><span data-stu-id="d9b2d-141">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d9b2d-142"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d9b2d-142"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d9b2d-143">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-143">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d9b2d-144">備註</span><span class="sxs-lookup"><span data-stu-id="d9b2d-144">Remarks</span></span>

<span data-ttu-id="d9b2d-145">無。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-145">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9b2d-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9b2d-146">Requirements</span></span>



| <span data-ttu-id="d9b2d-147">需求</span><span class="sxs-lookup"><span data-stu-id="d9b2d-147">Requirement</span></span> | <span data-ttu-id="d9b2d-148">值</span><span class="sxs-lookup"><span data-stu-id="d9b2d-148">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b2d-149">標頭</span><span class="sxs-lookup"><span data-stu-id="d9b2d-149">Header</span></span><br/> | <dl> <span data-ttu-id="d9b2d-150"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="d9b2d-150"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9b2d-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9b2d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9b2d-152">**IWMDRMLicense 介面**</span><span class="sxs-lookup"><span data-stu-id="d9b2d-152">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





