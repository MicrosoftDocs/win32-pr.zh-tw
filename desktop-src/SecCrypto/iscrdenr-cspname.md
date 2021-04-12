---
description: 設定或抓取 (CSP) 的密碼編譯服務提供者的名稱。
ms.assetid: 34fde7b0-747d-4592-a89a-207f82369f52
title: ISCrdEnr：： CSPName 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPName
- ISCrdEnr.get_CSPName
- ISCrdEnr.put_CSPName
- SCrdEnr.CSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 363f2f9120d3b0a202335d0e8e450464cbc1f118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027398"
---
# <a name="iscrdenrcspname-property"></a><span data-ttu-id="1713e-103">ISCrdEnr：： CSPName 屬性</span><span class="sxs-lookup"><span data-stu-id="1713e-103">ISCrdEnr::CSPName property</span></span>

<span data-ttu-id="1713e-104">**CSPName** 屬性會設定或抓取 (CSP) 的 [*密碼編譯服務提供者*](../secgloss/c-gly.md)的名稱。</span><span class="sxs-lookup"><span data-stu-id="1713e-104">The **CSPName** property sets or retrieves the name of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

<span data-ttu-id="1713e-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="1713e-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1713e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1713e-106">Syntax</span></span>


```C++
HRESULT put_CSPName(
   BSTR newVal
);

HRESULT get_CSPName(
   BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="1713e-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="1713e-107">Property value</span></span>

<span data-ttu-id="1713e-108">CSP 的名稱。</span><span class="sxs-lookup"><span data-stu-id="1713e-108">The name of the CSP.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1713e-109">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="1713e-109">Error codes</span></span>

<span data-ttu-id="1713e-110">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="1713e-110">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="1713e-111">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="1713e-111">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="1713e-112">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="1713e-112">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1713e-113">備註</span><span class="sxs-lookup"><span data-stu-id="1713e-113">Remarks</span></span>

<span data-ttu-id="1713e-114">設定此屬性可指定要與智慧卡註冊控制項搭配使用的 CSP 名稱。</span><span class="sxs-lookup"><span data-stu-id="1713e-114">Set this property to specify the name of the CSP to use with the Smart Card Enrollment Control.</span></span> <span data-ttu-id="1713e-115">取得此屬性以取得指定之 CSP 的名稱。</span><span class="sxs-lookup"><span data-stu-id="1713e-115">Get this property to retrieve the name of the specified CSP.</span></span> <span data-ttu-id="1713e-116">如果您未指定此屬性的值， **CSPName** 屬性會預設為可用 csp 清單中的名字。</span><span class="sxs-lookup"><span data-stu-id="1713e-116">If you do not specify a value for this property, the **CSPName** property defaults to the first name in the available list of CSPs.</span></span>

## <a name="requirements"></a><span data-ttu-id="1713e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1713e-117">Requirements</span></span>



| <span data-ttu-id="1713e-118">需求</span><span class="sxs-lookup"><span data-stu-id="1713e-118">Requirement</span></span> | <span data-ttu-id="1713e-119">值</span><span class="sxs-lookup"><span data-stu-id="1713e-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1713e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1713e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1713e-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="1713e-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1713e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1713e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1713e-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1713e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1713e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1713e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1713e-125"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1713e-125"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="1713e-126">IID</span><span class="sxs-lookup"><span data-stu-id="1713e-126">IID</span></span><br/>                      | <span data-ttu-id="1713e-127">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="1713e-127">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="1713e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1713e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1713e-129">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="1713e-129">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="1713e-130">**ISCrdEnr::CSPCount**</span><span class="sxs-lookup"><span data-stu-id="1713e-130">**ISCrdEnr::CSPCount**</span></span>](iscrdenr-cspcount.md)
</dt> <dt>

[<span data-ttu-id="1713e-131">**ISCrdEnr::enumCSPName**</span><span class="sxs-lookup"><span data-stu-id="1713e-131">**ISCrdEnr::enumCSPName**</span></span>](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
