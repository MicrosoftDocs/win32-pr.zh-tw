---
description: 從智慧卡控制項清除使用者名稱。
ms.assetid: fff50db5-0610-4985-94c6-96d7ce990219
title: ISCrdEnr：： resetUser 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.resetUser
- SCrdEnr.resetUser
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3b00721229890f82b00e7e7a41ccb8796a81b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991918"
---
# <a name="iscrdenrresetuser-method"></a><span data-ttu-id="69317-103">ISCrdEnr：： resetUser 方法</span><span class="sxs-lookup"><span data-stu-id="69317-103">ISCrdEnr::resetUser method</span></span>

<span data-ttu-id="69317-104">**ResetUser** 方法會從智慧卡控制項中清除使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="69317-104">The **resetUser** method clears the user name from the smart card control.</span></span>

## <a name="syntax"></a><span data-ttu-id="69317-105">語法</span><span class="sxs-lookup"><span data-stu-id="69317-105">Syntax</span></span>


```C++
HRESULT resetUser();
```



## <a name="parameters"></a><span data-ttu-id="69317-106">參數</span><span class="sxs-lookup"><span data-stu-id="69317-106">Parameters</span></span>

<span data-ttu-id="69317-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="69317-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="69317-108">備註</span><span class="sxs-lookup"><span data-stu-id="69317-108">Remarks</span></span>

<span data-ttu-id="69317-109">這個方法會從記憶體中清除任何現有的使用者名稱和先前註冊的憑證。</span><span class="sxs-lookup"><span data-stu-id="69317-109">This method clears any existing user name and previously enrolled certificate from memory.</span></span> <span data-ttu-id="69317-110">但先前註冊的憑證並不會從智慧卡移除。</span><span class="sxs-lookup"><span data-stu-id="69317-110">The previously enrolled certificate is not removed from the smart card, however.</span></span>

## <a name="requirements"></a><span data-ttu-id="69317-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="69317-111">Requirements</span></span>



| <span data-ttu-id="69317-112">需求</span><span class="sxs-lookup"><span data-stu-id="69317-112">Requirement</span></span> | <span data-ttu-id="69317-113">值</span><span class="sxs-lookup"><span data-stu-id="69317-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69317-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69317-114">Minimum supported client</span></span><br/> | <span data-ttu-id="69317-115">都不支援</span><span class="sxs-lookup"><span data-stu-id="69317-115">None supported</span></span><br/>                                                               |
| <span data-ttu-id="69317-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69317-116">Minimum supported server</span></span><br/> | <span data-ttu-id="69317-117">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69317-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="69317-118">DLL</span><span class="sxs-lookup"><span data-stu-id="69317-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69317-119"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69317-119"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="69317-120">IID</span><span class="sxs-lookup"><span data-stu-id="69317-120">IID</span></span><br/>                      | <span data-ttu-id="69317-121">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="69317-121">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="69317-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69317-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69317-123">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="69317-123">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="69317-124">**ISCrdEnr：： getUserName**</span><span class="sxs-lookup"><span data-stu-id="69317-124">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="69317-125">**ISCrdEnr::selectUserName**</span><span class="sxs-lookup"><span data-stu-id="69317-125">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> <dt>

[<span data-ttu-id="69317-126">**ISCrdEnr::setUserName**</span><span class="sxs-lookup"><span data-stu-id="69317-126">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 




