---
description: 抓取 (Csp) 的密碼編譯服務提供者數目。
ms.assetid: 7e0c1613-85ad-4f25-837e-d7b0f11e654a
title: ISCrdEnr：： CSPCount 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPCount
- ISCrdEnr.get_CSPCount
- SCrdEnr.CSPCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b2aea22db3c804ae4808996002b68efdcb6cf9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320383"
---
# <a name="iscrdenrcspcount-property"></a><span data-ttu-id="e104c-103">ISCrdEnr：： CSPCount 屬性</span><span class="sxs-lookup"><span data-stu-id="e104c-103">ISCrdEnr::CSPCount property</span></span>

<span data-ttu-id="e104c-104">**CSPCount** 屬性會抓取 (csp) 的 [*密碼編譯服務提供者*](../secgloss/c-gly.md)數目。</span><span class="sxs-lookup"><span data-stu-id="e104c-104">The **CSPCount** property retrieves the number of [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs).</span></span>

<span data-ttu-id="e104c-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e104c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e104c-106">語法</span><span class="sxs-lookup"><span data-stu-id="e104c-106">Syntax</span></span>


```C++
HRESULT get_CSPCount(
   LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="e104c-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="e104c-107">Property value</span></span>

<span data-ttu-id="e104c-108">Csp 的數目。</span><span class="sxs-lookup"><span data-stu-id="e104c-108">The number of CSPs.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e104c-109">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e104c-109">Error codes</span></span>

<span data-ttu-id="e104c-110">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e104c-110">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="e104c-111">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="e104c-111">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="e104c-112">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="e104c-112">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e104c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e104c-113">Requirements</span></span>



| <span data-ttu-id="e104c-114">需求</span><span class="sxs-lookup"><span data-stu-id="e104c-114">Requirement</span></span> | <span data-ttu-id="e104c-115">值</span><span class="sxs-lookup"><span data-stu-id="e104c-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e104c-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e104c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e104c-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="e104c-117">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e104c-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e104c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e104c-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e104c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e104c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e104c-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e104c-121"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e104c-121"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="e104c-122">IID</span><span class="sxs-lookup"><span data-stu-id="e104c-122">IID</span></span><br/>                      | <span data-ttu-id="e104c-123">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="e104c-123">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="e104c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e104c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e104c-125">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="e104c-125">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="e104c-126">**ISCrdEnr::CSPName**</span><span class="sxs-lookup"><span data-stu-id="e104c-126">**ISCrdEnr::CSPName**</span></span>](iscrdenr-cspname.md)
</dt> <dt>

[<span data-ttu-id="e104c-127">**ISCrdEnr::enumCSPName**</span><span class="sxs-lookup"><span data-stu-id="e104c-127">**ISCrdEnr::enumCSPName**</span></span>](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
