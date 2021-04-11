---
description: 抓取憑證範本的名稱。
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: ISCrdEnr：： getCertTemplateName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateName
- SCrdEnr.getCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4eee84140e0a23b8a0dd5d26099ca61b868a90fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194739"
---
# <a name="iscrdenrgetcerttemplatename-method"></a><span data-ttu-id="8074a-103">ISCrdEnr：： getCertTemplateName 方法</span><span class="sxs-lookup"><span data-stu-id="8074a-103">ISCrdEnr::getCertTemplateName method</span></span>

<span data-ttu-id="8074a-104">**GetCertTemplateName** 方法會抓取憑證範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="8074a-104">The **getCertTemplateName** method retrieves the name of the certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="8074a-105">語法</span><span class="sxs-lookup"><span data-stu-id="8074a-105">Syntax</span></span>


```C++
HRESULT getCertTemplateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.getCertTemplateName( _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="8074a-106">參數</span><span class="sxs-lookup"><span data-stu-id="8074a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8074a-107">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8074a-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8074a-108">值，決定是否傳回憑證範本的真實名稱或顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8074a-108">A value that determines whether the certificate template's real name or display name is returned.</span></span> <span data-ttu-id="8074a-109">如果 *dwFlags* 具有 [ \_ 註冊 \_ \_ 憑證範本] \_ 顯示名稱的值，則 \_ 會抓取憑證範本的顯示名稱; 否則，會顯示憑證範本的真實名稱。</span><span class="sxs-lookup"><span data-stu-id="8074a-109">If *dwFlags* has the value SCARD\_ENROLL\_CERT\_TEMPLATE\_DISPLAY\_NAME, the certificate template's display name is retrieved; otherwise, the real name of the certificate template is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="8074a-110">*pbstrCertTemplateName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8074a-110">*pbstrCertTemplateName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8074a-111">字串的指標，該字串會傳回將在 [*憑證要求*](../secgloss/c-gly.md)中使用的憑證範本名稱。</span><span class="sxs-lookup"><span data-stu-id="8074a-111">A pointer to a string that returns the name of the certificate template which will be used in the [*certificate request*](../secgloss/c-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8074a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8074a-112">Return value</span></span>

### <a name="c"></a><span data-ttu-id="8074a-113">C++</span><span class="sxs-lookup"><span data-stu-id="8074a-113">C++</span></span>

<span data-ttu-id="8074a-114">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="8074a-114">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="8074a-115">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="8074a-115">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="8074a-116">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="8074a-116">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="8074a-117">VB</span><span class="sxs-lookup"><span data-stu-id="8074a-117">VB</span></span>

<span data-ttu-id="8074a-118">字串，代表將在 [*憑證要求*](../secgloss/c-gly.md)中使用的憑證範本名稱。</span><span class="sxs-lookup"><span data-stu-id="8074a-118">A string that represents the name of the certificate template which will be used in the [*certificate request*](../secgloss/c-gly.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8074a-119">備註</span><span class="sxs-lookup"><span data-stu-id="8074a-119">Remarks</span></span>

<span data-ttu-id="8074a-120">如果您未藉由呼叫 [**ISCrdEnr：： setCertTemplateName**](iscrdenr-setcerttemplatename.md)來設定憑證範本名稱，則名稱會預設為可用憑證範本清單中的第一個名稱。</span><span class="sxs-lookup"><span data-stu-id="8074a-120">If you do not set the certificate template name by calling [**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md), the name defaults to the first name in the list of available certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="8074a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8074a-121">Requirements</span></span>



| <span data-ttu-id="8074a-122">需求</span><span class="sxs-lookup"><span data-stu-id="8074a-122">Requirement</span></span> | <span data-ttu-id="8074a-123">值</span><span class="sxs-lookup"><span data-stu-id="8074a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8074a-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8074a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8074a-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="8074a-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8074a-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8074a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8074a-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8074a-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8074a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8074a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8074a-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8074a-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="8074a-130">IID</span><span class="sxs-lookup"><span data-stu-id="8074a-130">IID</span></span><br/>                      | <span data-ttu-id="8074a-131">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="8074a-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="8074a-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8074a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8074a-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="8074a-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="8074a-134">**ISCrdEnr::setCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="8074a-134">**ISCrdEnr::setCertTemplateName**</span></span>](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
