---
description: 指定要在其上註冊憑證的使用者名稱。
ms.assetid: e088af63-5064-4b1b-976f-047f52e56af8
title: ISCrdEnr：： setUserName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setUserName
- SCrdEnr.setUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: cc2d3157e41fc7ffd9fc0bf7f607de137559e751
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990485"
---
# <a name="iscrdenrsetusername-method"></a><span data-ttu-id="eb42c-103">ISCrdEnr：： setUserName 方法</span><span class="sxs-lookup"><span data-stu-id="eb42c-103">ISCrdEnr::setUserName method</span></span>

<span data-ttu-id="eb42c-104">**SetUserName** 方法會指定要在其上註冊憑證的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="eb42c-104">The **setUserName** method specifies the name of the user on whose behalf the certificate enrollment is intended.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb42c-105">語法</span><span class="sxs-lookup"><span data-stu-id="eb42c-105">Syntax</span></span>


```C++
HRESULT setUserName(
  [in] DWORD dwFlags,
  [in] BSTR bstrUserName
);
```


```VB

SCrdEnr.setUserName( _
  ByVal dwFlags, _
  ByVal bstrUserName _
)
```





## <a name="parameters"></a><span data-ttu-id="eb42c-106">參數</span><span class="sxs-lookup"><span data-stu-id="eb42c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb42c-107">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb42c-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb42c-108">此值必須是捨棄 \_ 註冊 \_ UPN \_ 名稱 (定義為 1) 或捨棄 \_ 註冊 \_ SAM \_ 相容 \_ 名稱 (定義為 2) 。</span><span class="sxs-lookup"><span data-stu-id="eb42c-108">This value must be either SCARD\_ENROLL\_UPN\_NAME (defined as 1) or SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME (defined as 2).</span></span>

<span data-ttu-id="eb42c-109">\_ \_ \_ 如果在 *bstrUserName* 中指定的名稱是使用者的通用主體名稱（例如 ""），請將此值設定為捨棄註冊 UPN 名稱 someone@example.com 。</span><span class="sxs-lookup"><span data-stu-id="eb42c-109">Set this value to SCARD\_ENROLL\_UPN\_NAME, if the name specified in *bstrUserName* is the user's Universal Principal Name, such as "someone@example.com".</span></span> <span data-ttu-id="eb42c-110">使用者的 UPN 名稱必須對應到現有的安全性存取管理員 (SAM) 名稱。</span><span class="sxs-lookup"><span data-stu-id="eb42c-110">The user's UPN name must correspond to an existing security access manager (SAM) name.</span></span>

<span data-ttu-id="eb42c-111">\_ \_ \_ \_ 如果在 *bstrUserName* 中指定的名稱是使用者的 SAM 名稱（格式為 "DOMAIN user"），請 \\ 將此值設定為捨棄註冊 SAM 相容名稱。</span><span class="sxs-lookup"><span data-stu-id="eb42c-111">Set this value to SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME, if the name specified in *bstrUserName* is the user's SAM name in the format of "DOMAIN\\USER".</span></span>

</dd> <dt>

<span data-ttu-id="eb42c-112">*bstrUserName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb42c-112">*bstrUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb42c-113">使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="eb42c-113">Name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb42c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb42c-114">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="eb42c-115">VB</span><span class="sxs-lookup"><span data-stu-id="eb42c-115">VB</span></span>

<span data-ttu-id="eb42c-116">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="eb42c-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="eb42c-117">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="eb42c-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="eb42c-118">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="eb42c-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eb42c-119">備註</span><span class="sxs-lookup"><span data-stu-id="eb42c-119">Remarks</span></span>

<span data-ttu-id="eb42c-120">呼叫這個方法來指定要發出 [*智慧卡*](../secgloss/s-gly.md)的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="eb42c-120">Call this method to specify the user name to be issued the [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="eb42c-121">**SetUserName** 的替代方案是 [**ISCrdEnr：： selectUserName**](iscrdenr-selectusername.md)。</span><span class="sxs-lookup"><span data-stu-id="eb42c-121">An alternative to **setUserName** is [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md).</span></span>

<span data-ttu-id="eb42c-122">指定使用者名稱之後，您可以藉由呼叫 [**getUserName**](iscrdenr-getusername.md)來取出其值。</span><span class="sxs-lookup"><span data-stu-id="eb42c-122">After a user name has been specified, its value can be retrieved by calling [**getUserName**](iscrdenr-getusername.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb42c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb42c-123">Requirements</span></span>



| <span data-ttu-id="eb42c-124">需求</span><span class="sxs-lookup"><span data-stu-id="eb42c-124">Requirement</span></span> | <span data-ttu-id="eb42c-125">值</span><span class="sxs-lookup"><span data-stu-id="eb42c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb42c-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb42c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="eb42c-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="eb42c-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="eb42c-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb42c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="eb42c-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb42c-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eb42c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="eb42c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb42c-131"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb42c-131"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="eb42c-132">IID</span><span class="sxs-lookup"><span data-stu-id="eb42c-132">IID</span></span><br/>                      | <span data-ttu-id="eb42c-133">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="eb42c-133">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="eb42c-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb42c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb42c-135">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="eb42c-135">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="eb42c-136">**ISCrdEnr：： getUserName**</span><span class="sxs-lookup"><span data-stu-id="eb42c-136">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="eb42c-137">**ISCrdEnr::resetUser**</span><span class="sxs-lookup"><span data-stu-id="eb42c-137">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="eb42c-138">**ISCrdEnr::selectUserName**</span><span class="sxs-lookup"><span data-stu-id="eb42c-138">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> </dl>

 

 
