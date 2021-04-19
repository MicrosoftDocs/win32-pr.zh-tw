---
title: 'IWMDRMSecurity GetMachineCertificate 方法 (Wmdrmsdk .h) '
description: GetMachineCertificate 方法會抓取用戶端電腦上 DRM 子系統的電腦憑證。
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- GetMachineCertificate 方法 windows Media 格式
- GetMachineCertificate 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，GetMachineCertificate 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetMachineCertificate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6c66c54ab9528a458910def5978ec83b191654
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977693"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a><span data-ttu-id="f88ee-106">IWMDRMSecurity：： GetMachineCertificate 方法</span><span class="sxs-lookup"><span data-stu-id="f88ee-106">IWMDRMSecurity::GetMachineCertificate method</span></span>

<span data-ttu-id="f88ee-107">**GetMachineCertificate** 方法會抓取用戶端電腦上 DRM 子系統的電腦憑證。</span><span class="sxs-lookup"><span data-stu-id="f88ee-107">The **GetMachineCertificate** method retrieves the machine certificate of the DRM subsystem on the client computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f88ee-108">語法</span><span class="sxs-lookup"><span data-stu-id="f88ee-108">Syntax</span></span>


```C++
HRESULT GetMachineCertificate(
  [in]      DWORD dwCertificateType,
  [out]     BYTE  rgbVersion[4],
  [out]     BYTE  **ppbCertificate,
  [in, out] DWORD *pcbCertificate
);
```



## <a name="parameters"></a><span data-ttu-id="f88ee-109">參數</span><span class="sxs-lookup"><span data-stu-id="f88ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f88ee-110">*dwCertificateType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f88ee-110">*dwCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f88ee-111">要取出的憑證類型。</span><span class="sxs-lookup"><span data-stu-id="f88ee-111">Type of certificate to retrieve.</span></span> <span data-ttu-id="f88ee-112">設定為下表中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f88ee-112">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="f88ee-113">值</span><span class="sxs-lookup"><span data-stu-id="f88ee-113">Value</span></span>                        | <span data-ttu-id="f88ee-114">描述</span><span class="sxs-lookup"><span data-stu-id="f88ee-114">Description</span></span>                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f88ee-115">WMDRM \_ 憑證 \_ 類型 \_ V1</span><span class="sxs-lookup"><span data-stu-id="f88ee-115">WMDRM\_CERTIFICATE\_TYPE\_V1</span></span> | <span data-ttu-id="f88ee-116">憑證將以舊版元件使用的格式抓取。</span><span class="sxs-lookup"><span data-stu-id="f88ee-116">The certificate will be retrieved in the format used by legacy components.</span></span>            |
| <span data-ttu-id="f88ee-117">WMDRM \_ 憑證 \_ 類型 \_ V2</span><span class="sxs-lookup"><span data-stu-id="f88ee-117">WMDRM\_CERTIFICATE\_TYPE\_V2</span></span> | <span data-ttu-id="f88ee-118">憑證將以 Windows Vista 元件使用的格式抓取。</span><span class="sxs-lookup"><span data-stu-id="f88ee-118">The certificate will be retrieved in the format used by the Windows Vista components.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f88ee-119">*rgbVersion \[ 4 \]* \[ 輸出\]</span><span class="sxs-lookup"><span data-stu-id="f88ee-119">*rgbVersion\[4\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f88ee-120">四個位元組的陣列，指定用戶端電腦上的 DRM 子系統版本。</span><span class="sxs-lookup"><span data-stu-id="f88ee-120">Array of four bytes specifying the version of the DRM subsystem on the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="f88ee-121">*ppbCertificate* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f88ee-121">*ppbCertificate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f88ee-122">接收憑證資料指標之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="f88ee-122">Address of a variable that receives a pointer to the certificate data.</span></span> <span data-ttu-id="f88ee-123">設定為 **Null** ，讓方法提供在 *pcbCertificate* 中保存憑證所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="f88ee-123">Set to **NULL** to have the method provide the buffer size required to hold the certificate in *pcbCertificate*.</span></span>

</dd> <dt>

<span data-ttu-id="f88ee-124">*pcbCertificate* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f88ee-124">*pcbCertificate* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f88ee-125">憑證的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f88ee-125">Size of the certificate in bytes.</span></span> <span data-ttu-id="f88ee-126">如果 *ppbCertificate* 為 **Null**，則此值會設定為憑證的大小。</span><span class="sxs-lookup"><span data-stu-id="f88ee-126">If *ppbCertificate* is **NULL**, this value will be set to the size of the certificate.</span></span> <span data-ttu-id="f88ee-127">如果 *ppbCertificate* 不是 **Null**，這個值就必須設定為緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="f88ee-127">If *ppbCertificate* is not **NULL**, this value must be set to the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f88ee-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="f88ee-128">Return value</span></span>

<span data-ttu-id="f88ee-129">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="f88ee-129">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f88ee-130">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="f88ee-130">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f88ee-131">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f88ee-131">Return code</span></span>                                                                          | <span data-ttu-id="f88ee-132">Description</span><span class="sxs-lookup"><span data-stu-id="f88ee-132">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f88ee-133"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f88ee-133"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f88ee-134">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="f88ee-134">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f88ee-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="f88ee-135">Requirements</span></span>



| <span data-ttu-id="f88ee-136">需求</span><span class="sxs-lookup"><span data-stu-id="f88ee-136">Requirement</span></span> | <span data-ttu-id="f88ee-137">值</span><span class="sxs-lookup"><span data-stu-id="f88ee-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f88ee-138">標頭</span><span class="sxs-lookup"><span data-stu-id="f88ee-138">Header</span></span><br/>  | <dl> <span data-ttu-id="f88ee-139"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="f88ee-139"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="f88ee-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="f88ee-140">Library</span></span><br/> | <dl> <span data-ttu-id="f88ee-141"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f88ee-141"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f88ee-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f88ee-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f88ee-143">**IWMDRMSecurity 介面**</span><span class="sxs-lookup"><span data-stu-id="f88ee-143">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





