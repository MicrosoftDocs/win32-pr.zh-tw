---
description: 取得指定憑證範本 (CA) 的指定憑證授權單位單位名稱。
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: ISCrdEnr：： getCAName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCAName
- SCrdEnr.getCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b62b0a7e871a29ff0a8edd28eb8cd5e18e97c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194741"
---
# <a name="iscrdenrgetcaname-method"></a><span data-ttu-id="b2cbd-103">ISCrdEnr：： getCAName 方法</span><span class="sxs-lookup"><span data-stu-id="b2cbd-103">ISCrdEnr::getCAName method</span></span>

<span data-ttu-id="b2cbd-104">**GetCAName** 方法會針對指定的憑證範本，抓取指定的 [*憑證授權單位*](../secgloss/c-gly.md)單位 (CA) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2cbd-104">The **getCAName** method retrieves the name of the specified [*certification authority*](../secgloss/c-gly.md) (CA) for a given certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2cbd-105">語法</span><span class="sxs-lookup"><span data-stu-id="b2cbd-105">Syntax</span></span>


```C++
HRESULT getCAName(
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.getCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="b2cbd-106">參數</span><span class="sxs-lookup"><span data-stu-id="b2cbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2cbd-107">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b2cbd-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2cbd-108">值，這個值會判斷名稱是指 CA 名稱或 CA 的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="b2cbd-108">A value that determines whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="b2cbd-109">如果此值為捨棄 \_ 註冊 \_ CA \_ 電腦 \_ 名稱 (定義為 0x01) 則名稱會參考 ca 的電腦名稱稱，否則名稱會參考 ca 名稱。</span><span class="sxs-lookup"><span data-stu-id="b2cbd-109">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01) then the name refers to the CA's machine name; otherwise the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="b2cbd-110">*bstrCertTemplateName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b2cbd-110">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2cbd-111">憑證範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2cbd-111">The name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="b2cbd-112">*pbstrCAName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b2cbd-112">*pbstrCAName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2cbd-113">傳回 CA 名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="b2cbd-113">A pointer to a string that returns the name of the CA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2cbd-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2cbd-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="b2cbd-115">C++</span><span class="sxs-lookup"><span data-stu-id="b2cbd-115">C++</span></span>

<span data-ttu-id="b2cbd-116">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b2cbd-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="b2cbd-117">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b2cbd-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="b2cbd-118">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="b2cbd-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="b2cbd-119">VB</span><span class="sxs-lookup"><span data-stu-id="b2cbd-119">VB</span></span>

<span data-ttu-id="b2cbd-120">表示 CA 名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="b2cbd-120">A string that represents the name of the CA.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2cbd-121">備註</span><span class="sxs-lookup"><span data-stu-id="b2cbd-121">Remarks</span></span>

<span data-ttu-id="b2cbd-122">預設 CA 名稱是可用 Ca 清單中的名字。</span><span class="sxs-lookup"><span data-stu-id="b2cbd-122">The default CA name is the first name in the available list of CAs.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2cbd-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2cbd-123">Requirements</span></span>



| <span data-ttu-id="b2cbd-124">需求</span><span class="sxs-lookup"><span data-stu-id="b2cbd-124">Requirement</span></span> | <span data-ttu-id="b2cbd-125">值</span><span class="sxs-lookup"><span data-stu-id="b2cbd-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2cbd-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2cbd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b2cbd-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="b2cbd-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b2cbd-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2cbd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b2cbd-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2cbd-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2cbd-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b2cbd-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2cbd-131"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2cbd-131"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2cbd-132">IID</span><span class="sxs-lookup"><span data-stu-id="b2cbd-132">IID</span></span><br/>                      | <span data-ttu-id="b2cbd-133">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="b2cbd-133">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="b2cbd-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2cbd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2cbd-135">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="b2cbd-135">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="b2cbd-136">**ISCrdEnr::enumCAName**</span><span class="sxs-lookup"><span data-stu-id="b2cbd-136">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="b2cbd-137">**ISCrdEnr::getCACount**</span><span class="sxs-lookup"><span data-stu-id="b2cbd-137">**ISCrdEnr::getCACount**</span></span>](iscrdenr-getcacount.md)
</dt> <dt>

[<span data-ttu-id="b2cbd-138">**ISCrdEnr::setCAName**</span><span class="sxs-lookup"><span data-stu-id="b2cbd-138">**ISCrdEnr::setCAName**</span></span>](iscrdenr-setcaname.md)
</dt> </dl>

 

 
