---
description: 針對指定的憑證範本名稱，列舉 (Ca) 的憑證授權單位單位名稱。
ms.assetid: 82cc3346-a8b9-4abd-933a-c212a37a373e
title: ISCrdEnr：： enumCAName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCAName
- SCrdEnr.enumCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: c23df2f74cdf3791f1280e38cbff8ddd48f924b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984707"
---
# <a name="iscrdenrenumcaname-method"></a><span data-ttu-id="cc0e9-103">ISCrdEnr：： enumCAName 方法</span><span class="sxs-lookup"><span data-stu-id="cc0e9-103">ISCrdEnr::enumCAName method</span></span>

<span data-ttu-id="cc0e9-104">**EnumCAName** 方法會為指定的憑證範本名稱，列舉 (ca) 的 [*憑證授權單位*](../secgloss/c-gly.md)單位名稱。</span><span class="sxs-lookup"><span data-stu-id="cc0e9-104">The **enumCAName** method enumerates the name of the [*certification authorities*](../secgloss/c-gly.md) (CAs) for a given certificate template name.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc0e9-105">語法</span><span class="sxs-lookup"><span data-stu-id="cc0e9-105">Syntax</span></span>


```C++
HRESULT enumCAName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.enumCAName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="cc0e9-106">參數</span><span class="sxs-lookup"><span data-stu-id="cc0e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc0e9-107">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cc0e9-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc0e9-108">列舉序列的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="cc0e9-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="cc0e9-109">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cc0e9-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc0e9-110">值，這個值會判斷名稱是指 CA 名稱或 CA 的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="cc0e9-110">A value that determines whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="cc0e9-111">如果此值為捨棄 \_ 註冊 \_ CA \_ 電腦 \_ 名稱 (定義為 0x01) ，則名稱會參考 CA 的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="cc0e9-111">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01), the name refers to the CA's machine name.</span></span> <span data-ttu-id="cc0e9-112">否則，名稱會參考 CA 名稱。</span><span class="sxs-lookup"><span data-stu-id="cc0e9-112">Otherwise the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="cc0e9-113">*bstrCertTemplateName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cc0e9-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc0e9-114">憑證範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc0e9-114">The name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="cc0e9-115">*pbstrCAName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cc0e9-115">*pbstrCAName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc0e9-116">傳回 CA 名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="cc0e9-116">A pointer to a string that returns the name of the CA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc0e9-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="cc0e9-117">Return value</span></span>

### <a name="c"></a><span data-ttu-id="cc0e9-118">C++</span><span class="sxs-lookup"><span data-stu-id="cc0e9-118">C++</span></span>

<span data-ttu-id="cc0e9-119">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="cc0e9-119">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="cc0e9-120">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="cc0e9-120">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="cc0e9-121">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="cc0e9-121">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="cc0e9-122">VB</span><span class="sxs-lookup"><span data-stu-id="cc0e9-122">VB</span></span>

<span data-ttu-id="cc0e9-123">表示 CA 名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="cc0e9-123">A string that represents the name of the CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc0e9-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc0e9-124">Requirements</span></span>



| <span data-ttu-id="cc0e9-125">需求</span><span class="sxs-lookup"><span data-stu-id="cc0e9-125">Requirement</span></span> | <span data-ttu-id="cc0e9-126">值</span><span class="sxs-lookup"><span data-stu-id="cc0e9-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc0e9-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc0e9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cc0e9-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="cc0e9-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="cc0e9-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc0e9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cc0e9-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc0e9-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cc0e9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="cc0e9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc0e9-132"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc0e9-132"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="cc0e9-133">IID</span><span class="sxs-lookup"><span data-stu-id="cc0e9-133">IID</span></span><br/>                      | <span data-ttu-id="cc0e9-134">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="cc0e9-134">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="cc0e9-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc0e9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc0e9-136">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="cc0e9-136">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="cc0e9-137">**ISCrdEnr::getCACount**</span><span class="sxs-lookup"><span data-stu-id="cc0e9-137">**ISCrdEnr::getCACount**</span></span>](iscrdenr-getcacount.md)
</dt> <dt>

[<span data-ttu-id="cc0e9-138">**ISCrdEnr::getCAName**</span><span class="sxs-lookup"><span data-stu-id="cc0e9-138">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> <dt>

[<span data-ttu-id="cc0e9-139">**ISCrdEnr::setCAName**</span><span class="sxs-lookup"><span data-stu-id="cc0e9-139">**ISCrdEnr::setCAName**</span></span>](iscrdenr-setcaname.md)
</dt> </dl>

 

 
