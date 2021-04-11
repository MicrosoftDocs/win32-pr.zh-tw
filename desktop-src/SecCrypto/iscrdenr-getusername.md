---
description: 抓取要作為憑證註冊目標之使用者的名稱。
ms.assetid: 7bd71944-f7dd-4c92-a71c-ecc5c0afd5b2
title: ISCrdEnr：： getUserName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getUserName
- SCrdEnr.getUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 51f551a704f3a98b932e646c95810f928e73bac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320379"
---
# <a name="iscrdenrgetusername-method"></a><span data-ttu-id="2e2ee-103">ISCrdEnr：： getUserName 方法</span><span class="sxs-lookup"><span data-stu-id="2e2ee-103">ISCrdEnr::getUserName method</span></span>

<span data-ttu-id="2e2ee-104">**GetUserName** 方法會抓取代表憑證註冊之使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e2ee-104">The **getUserName** method retrieves the name of the user on whose behalf the certificate enrollment is intended.</span></span>

<span data-ttu-id="2e2ee-105">在呼叫這個方法之前，您必須在 [**ISCrdEnr：： selectUserName**](iscrdenr-selectusername.md) 或 [**ISCrdEnr：： setUserName**](iscrdenr-setusername.md)的呼叫中指定使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="2e2ee-105">Before calling this method, you must specify the user name in a call to [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md) or [**ISCrdEnr::setUserName**](iscrdenr-setusername.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e2ee-106">語法</span><span class="sxs-lookup"><span data-stu-id="2e2ee-106">Syntax</span></span>


```C++
HRESULT getUserName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrUserName
);
```


```VB

SCrdEnr.getUserName( _
  ByVal dwFlags, _
  ByRef pbstrUserName _
)
```





## <a name="parameters"></a><span data-ttu-id="2e2ee-107">參數</span><span class="sxs-lookup"><span data-stu-id="2e2ee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e2ee-108">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e2ee-108">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e2ee-109">此值必須是零 (0) 、捨棄 \_ 註冊 \_ UPN \_ 名稱或捨棄 \_ 註冊 \_ SAM \_ 相容 \_ 名稱。</span><span class="sxs-lookup"><span data-stu-id="2e2ee-109">This value must be either zero (0), SCARD\_ENROLL\_UPN\_NAME, or SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME.</span></span>

<span data-ttu-id="2e2ee-110">如果此值為捨棄 \_ 註冊 \_ UPN \_ 名稱， **getUserName** 會傳回使用者的通用主體名稱 (UPN) ，例如 " someone@example.com "。</span><span class="sxs-lookup"><span data-stu-id="2e2ee-110">If this value is SCARD\_ENROLL\_UPN\_NAME, **getUserName** returns the user's Universal Principal Name (UPN), such as "someone@example.com".</span></span>

<span data-ttu-id="2e2ee-111">如果這個值是捨棄 \_ 註冊 \_ SAM \_ 相容 \_ 名稱，方法會以 "DOMAIN user" 格式傳回使用者的安全性存取管理員 (SAM) 名稱 \\ 。</span><span class="sxs-lookup"><span data-stu-id="2e2ee-111">If this value is SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME, the method returns the user's security access manager (SAM) name in the format "DOMAIN\\USER".</span></span>

<span data-ttu-id="2e2ee-112">如果此值為零，則方法會傳回使用者的 UPN 名稱（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="2e2ee-112">If this value is zero, the method returns the user's UPN name if it exists.</span></span> <span data-ttu-id="2e2ee-113">如果使用者沒有 UPN 名稱，方法會傳回使用者的 SAM 名稱。</span><span class="sxs-lookup"><span data-stu-id="2e2ee-113">If the user does not have a UPN name, the method returns the user's SAM name.</span></span>

</dd> <dt>

<span data-ttu-id="2e2ee-114">*pbstrUserName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2e2ee-114">*pbstrUserName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e2ee-115">傳回使用者名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="2e2ee-115">A pointer to a string that returns the name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e2ee-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e2ee-116">Return value</span></span>

### <a name="c"></a><span data-ttu-id="2e2ee-117">C++</span><span class="sxs-lookup"><span data-stu-id="2e2ee-117">C++</span></span>

<span data-ttu-id="2e2ee-118">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="2e2ee-118">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="2e2ee-119">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="2e2ee-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="2e2ee-120">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="2e2ee-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="2e2ee-121">VB</span><span class="sxs-lookup"><span data-stu-id="2e2ee-121">VB</span></span>

<span data-ttu-id="2e2ee-122">表示使用者名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="2e2ee-122">String that represents the name of the user.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e2ee-123">備註</span><span class="sxs-lookup"><span data-stu-id="2e2ee-123">Remarks</span></span>

<span data-ttu-id="2e2ee-124">您可以藉由呼叫 [**ISCrdEnr：： setUserName**](iscrdenr-setusername.md)或 [**ISCrdEnr：： selectUserName**](iscrdenr-selectusername.md)，指定 [*智慧卡*](../secgloss/s-gly.md)發出的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="2e2ee-124">You can specify the name of the user to whom the [*smart card*](../secgloss/s-gly.md) is issued by calling either [**ISCrdEnr::setUserName**](iscrdenr-setusername.md) or [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md).</span></span> <span data-ttu-id="2e2ee-125">指定使用者名稱之後，您可以藉由呼叫 **getUserName** 來取出其值。</span><span class="sxs-lookup"><span data-stu-id="2e2ee-125">After a user name has been specified, its value can be retrieved by calling **getUserName**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e2ee-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e2ee-126">Requirements</span></span>



| <span data-ttu-id="2e2ee-127">需求</span><span class="sxs-lookup"><span data-stu-id="2e2ee-127">Requirement</span></span> | <span data-ttu-id="2e2ee-128">值</span><span class="sxs-lookup"><span data-stu-id="2e2ee-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e2ee-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e2ee-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2e2ee-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="2e2ee-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2e2ee-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e2ee-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2e2ee-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e2ee-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2e2ee-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2e2ee-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e2ee-134"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e2ee-134"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="2e2ee-135">IID</span><span class="sxs-lookup"><span data-stu-id="2e2ee-135">IID</span></span><br/>                      | <span data-ttu-id="2e2ee-136">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="2e2ee-136">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="2e2ee-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e2ee-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e2ee-138">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="2e2ee-138">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="2e2ee-139">**ISCrdEnr::resetUser**</span><span class="sxs-lookup"><span data-stu-id="2e2ee-139">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="2e2ee-140">**ISCrdEnr::selectUserName**</span><span class="sxs-lookup"><span data-stu-id="2e2ee-140">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> <dt>

[<span data-ttu-id="2e2ee-141">**ISCrdEnr::setUserName**</span><span class="sxs-lookup"><span data-stu-id="2e2ee-141">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 
