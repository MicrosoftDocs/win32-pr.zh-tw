---
description: 顯示選取的使用者介面，允許選取使用者名稱。
ms.assetid: 0a02d9e5-b2cf-4818-a2e1-89e6019e53d4
title: ISCrdEnr：： selectUserName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectUserName
- SCrdEnr.selectUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 13059775abc8520c39a0ad3dea2d604fc8d65455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971549"
---
# <a name="iscrdenrselectusername-method"></a><span data-ttu-id="750c0-103">ISCrdEnr：： selectUserName 方法</span><span class="sxs-lookup"><span data-stu-id="750c0-103">ISCrdEnr::selectUserName method</span></span>

<span data-ttu-id="750c0-104">**SelectUserName** 方法會顯示 **選取的使用者** 介面，允許選取使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="750c0-104">The **selectUserName** method displays a **Select User** interface, allowing a user name to be selected.</span></span>

<span data-ttu-id="750c0-105">使用者名稱會套用至代表憑證註冊的使用者。</span><span class="sxs-lookup"><span data-stu-id="750c0-105">The user name applies to the user on whose behalf the certificate enrollment is intended.</span></span>

## <a name="syntax"></a><span data-ttu-id="750c0-106">語法</span><span class="sxs-lookup"><span data-stu-id="750c0-106">Syntax</span></span>


```C++
HRESULT selectUserName(
  [in] DWORD dwFlags
);
```


```VB

SCrdEnr.selectUserName( _
  ByVal dwFlags _
)
```





## <a name="parameters"></a><span data-ttu-id="750c0-107">參數</span><span class="sxs-lookup"><span data-stu-id="750c0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="750c0-108">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="750c0-108">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="750c0-109">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="750c0-109">Reserved for future use.</span></span> <span data-ttu-id="750c0-110">將此值設定為零。</span><span class="sxs-lookup"><span data-stu-id="750c0-110">Set this value to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="750c0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="750c0-111">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="750c0-112">VB</span><span class="sxs-lookup"><span data-stu-id="750c0-112">VB</span></span>

<span data-ttu-id="750c0-113">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="750c0-113">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="750c0-114">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="750c0-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="750c0-115">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="750c0-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="750c0-116">備註</span><span class="sxs-lookup"><span data-stu-id="750c0-116">Remarks</span></span>

<span data-ttu-id="750c0-117">使用這個方法來選取使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="750c0-117">Use this method to select the name of the user.</span></span> <span data-ttu-id="750c0-118">選取使用者名稱之後，您可以藉由呼叫 [**ISCrdEnr：： getUserName**](iscrdenr-getusername.md) 方法來取出其值。</span><span class="sxs-lookup"><span data-stu-id="750c0-118">After a user name has been selected, its value can be retrieved by calling the [**ISCrdEnr::getUserName**](iscrdenr-getusername.md) method.</span></span>

<span data-ttu-id="750c0-119">使用「選取使用者」介面的另一種方式，是藉由呼叫 [**ISCrdEnr：： setUserName**](iscrdenr-setusername.md) 方法來指定使用者。</span><span class="sxs-lookup"><span data-stu-id="750c0-119">An alternative to using the 'Select User' interface is to specify a user by calling the [**ISCrdEnr::setUserName**](iscrdenr-setusername.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="750c0-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="750c0-120">Requirements</span></span>



| <span data-ttu-id="750c0-121">需求</span><span class="sxs-lookup"><span data-stu-id="750c0-121">Requirement</span></span> | <span data-ttu-id="750c0-122">值</span><span class="sxs-lookup"><span data-stu-id="750c0-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="750c0-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="750c0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="750c0-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="750c0-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="750c0-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="750c0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="750c0-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="750c0-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="750c0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="750c0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="750c0-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="750c0-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="750c0-129">IID</span><span class="sxs-lookup"><span data-stu-id="750c0-129">IID</span></span><br/>                      | <span data-ttu-id="750c0-130">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="750c0-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="750c0-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="750c0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="750c0-132">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="750c0-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="750c0-133">**ISCrdEnr：： getUserName**</span><span class="sxs-lookup"><span data-stu-id="750c0-133">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="750c0-134">**ISCrdEnr::resetUser**</span><span class="sxs-lookup"><span data-stu-id="750c0-134">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="750c0-135">**ISCrdEnr::setUserName**</span><span class="sxs-lookup"><span data-stu-id="750c0-135">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 




