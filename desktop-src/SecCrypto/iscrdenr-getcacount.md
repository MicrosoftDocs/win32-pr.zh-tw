---
description: 傳回 (Ca 的憑證授權單位單位數目) 願意根據指定的憑證範本頒發證書。
ms.assetid: 377121a8-3895-4308-a803-4a62580c6de0
title: ISCrdEnr：： getCACount 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCACount
- SCrdEnr.getCACount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: eb33f6c7345862dedf6c909054d811ff4da470ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998537"
---
# <a name="iscrdenrgetcacount-method"></a><span data-ttu-id="19752-103">ISCrdEnr：： getCACount 方法</span><span class="sxs-lookup"><span data-stu-id="19752-103">ISCrdEnr::getCACount method</span></span>

<span data-ttu-id="19752-104">**GetCACount** 方法會傳回 (ca 的 [*憑證授權單位*](../secgloss/c-gly.md)單位數目) 願意根據指定的憑證範本頒發證書。</span><span class="sxs-lookup"><span data-stu-id="19752-104">The **getCACount** method returns the number of [*certification authorities*](../secgloss/c-gly.md) (CAs) willing to issue a certificate based on the specified certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="19752-105">語法</span><span class="sxs-lookup"><span data-stu-id="19752-105">Syntax</span></span>


```C++
HRESULT getCACount(
  [in]  BSTR     bstrCertTemplateName,
  [out] LONG *pdwCACount
);
```


```VB

SCrdEnr.getCACount( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCACount _
)
```





## <a name="parameters"></a><span data-ttu-id="19752-106">參數</span><span class="sxs-lookup"><span data-stu-id="19752-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19752-107">*bstrCertTemplateName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19752-107">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19752-108">表示憑證範本名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="19752-108">A string that represents the name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="19752-109">*pdwCACount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="19752-109">*pdwCACount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19752-110">**LONG** 的指標，傳回將為 *bstrCertTemplateName* 中指定的憑證範本發出憑證的可用 ca 數目。</span><span class="sxs-lookup"><span data-stu-id="19752-110">A pointer to a **LONG** that returns the number of available CAs that will issue a certificate for the certificate template specified in *bstrCertTemplateName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19752-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="19752-111">Return value</span></span>

### <a name="c"></a><span data-ttu-id="19752-112">C++</span><span class="sxs-lookup"><span data-stu-id="19752-112">C++</span></span>

<span data-ttu-id="19752-113">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="19752-113">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="19752-114">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="19752-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="19752-115">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="19752-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="19752-116">VB</span><span class="sxs-lookup"><span data-stu-id="19752-116">VB</span></span>

<span data-ttu-id="19752-117">**Long** 值，代表將為 *bstrCertTemplateName* 中指定的憑證範本發出憑證的可用 ca 數目。</span><span class="sxs-lookup"><span data-stu-id="19752-117">A **Long** value that represents the number of available CAs that will issue a certificate for the certificate template specified in *bstrCertTemplateName*.</span></span>

## <a name="requirements"></a><span data-ttu-id="19752-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="19752-118">Requirements</span></span>



| <span data-ttu-id="19752-119">需求</span><span class="sxs-lookup"><span data-stu-id="19752-119">Requirement</span></span> | <span data-ttu-id="19752-120">值</span><span class="sxs-lookup"><span data-stu-id="19752-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19752-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19752-121">Minimum supported client</span></span><br/> | <span data-ttu-id="19752-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="19752-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="19752-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19752-123">Minimum supported server</span></span><br/> | <span data-ttu-id="19752-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19752-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="19752-125">DLL</span><span class="sxs-lookup"><span data-stu-id="19752-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19752-126"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19752-126"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="19752-127">IID</span><span class="sxs-lookup"><span data-stu-id="19752-127">IID</span></span><br/>                      | <span data-ttu-id="19752-128">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="19752-128">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="19752-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19752-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19752-130">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="19752-130">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="19752-131">**ISCrdEnr::enumCAName**</span><span class="sxs-lookup"><span data-stu-id="19752-131">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="19752-132">**ISCrdEnr::getCAName**</span><span class="sxs-lookup"><span data-stu-id="19752-132">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> </dl>

 

 
