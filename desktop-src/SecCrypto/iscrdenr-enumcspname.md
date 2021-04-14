---
description: 列舉 (Csp) 的可用密碼編譯服務提供者的名稱。
ms.assetid: d0dc8a8a-afff-4ccc-96e0-2c52913c3322
title: ISCrdEnr：： enumCSPName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCSPName
- SCrdEnr.enumCSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e7bba587b56300cd02efd81758288d3b77c65a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513989"
---
# <a name="iscrdenrenumcspname-method"></a><span data-ttu-id="b01b0-103">ISCrdEnr：： enumCSPName 方法</span><span class="sxs-lookup"><span data-stu-id="b01b0-103">ISCrdEnr::enumCSPName method</span></span>

<span data-ttu-id="b01b0-104">**EnumCSPName** 方法會列舉 (csp) 的可用 [*密碼編譯服務提供者*](../secgloss/c-gly.md)的名稱。</span><span class="sxs-lookup"><span data-stu-id="b01b0-104">The **enumCSPName** method enumerates the name of the available [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs).</span></span>

## <a name="syntax"></a><span data-ttu-id="b01b0-105">語法</span><span class="sxs-lookup"><span data-stu-id="b01b0-105">Syntax</span></span>


```C++
HRESULT enumCSPName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCSPName
);
```


```VB

SCrdEnr.enumCSPName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCSPName _
)
```





## <a name="parameters"></a><span data-ttu-id="b01b0-106">參數</span><span class="sxs-lookup"><span data-stu-id="b01b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b01b0-107">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b01b0-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b01b0-108">列舉序列的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="b01b0-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="b01b0-109">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b01b0-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b01b0-110">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="b01b0-110">Reserved for future use.</span></span> <span data-ttu-id="b01b0-111">將此值設定為零。</span><span class="sxs-lookup"><span data-stu-id="b01b0-111">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b01b0-112">*pbstrCSPName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b01b0-112">*pbstrCSPName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b01b0-113">傳回列舉 CSP 名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="b01b0-113">A pointer to a string that returns the name of the enumerated CSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b01b0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b01b0-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="b01b0-115">C++</span><span class="sxs-lookup"><span data-stu-id="b01b0-115">C++</span></span>

<span data-ttu-id="b01b0-116">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b01b0-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="b01b0-117">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b01b0-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="b01b0-118">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="b01b0-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="b01b0-119">VB</span><span class="sxs-lookup"><span data-stu-id="b01b0-119">VB</span></span>

<span data-ttu-id="b01b0-120">表示列舉之 CSP 名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="b01b0-120">A string that represents the name of the enumerated CSP.</span></span>

## <a name="requirements"></a><span data-ttu-id="b01b0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b01b0-121">Requirements</span></span>



| <span data-ttu-id="b01b0-122">需求</span><span class="sxs-lookup"><span data-stu-id="b01b0-122">Requirement</span></span> | <span data-ttu-id="b01b0-123">值</span><span class="sxs-lookup"><span data-stu-id="b01b0-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b01b0-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b01b0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b01b0-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="b01b0-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b01b0-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b01b0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b01b0-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b01b0-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b01b0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b01b0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b01b0-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b01b0-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="b01b0-130">IID</span><span class="sxs-lookup"><span data-stu-id="b01b0-130">IID</span></span><br/>                      | <span data-ttu-id="b01b0-131">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="b01b0-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="b01b0-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b01b0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b01b0-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="b01b0-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="b01b0-134">**ISCrdEnr::CSPCount**</span><span class="sxs-lookup"><span data-stu-id="b01b0-134">**ISCrdEnr::CSPCount**</span></span>](iscrdenr-cspcount.md)
</dt> <dt>

[<span data-ttu-id="b01b0-135">**ISCrdEnr::CSPName**</span><span class="sxs-lookup"><span data-stu-id="b01b0-135">**ISCrdEnr::CSPName**</span></span>](iscrdenr-cspname.md)
</dt> </dl>

 

 
