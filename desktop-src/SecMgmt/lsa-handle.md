---
description: 本機原則物件的控制碼。
ms.assetid: f5878d27-558b-4ef1-9401-1277e740c61d
title: 'LSA_HANDLE (Ntsecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07bd71a14666dde7bb92e439159a55dd71706612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026803"
---
# <a name="lsa_handle"></a><span data-ttu-id="33136-103">LSA \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="33136-103">LSA\_HANDLE</span></span>

<span data-ttu-id="33136-104">**LSA \_ 控制碼** 資料類型是本機 [**原則**](policy-object.md)物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="33136-104">The **LSA\_HANDLE** data type is a handle to the local [**Policy**](policy-object.md) object.</span></span>


```C++
typedef PVOID LSA_HANDLE, *PLSA_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="33136-105">備註</span><span class="sxs-lookup"><span data-stu-id="33136-105">Remarks</span></span>

<span data-ttu-id="33136-106">您的應用程式必須先開啟 [**原則**](policy-object.md) 物件的控制碼，您才能使用本機原則 API。</span><span class="sxs-lookup"><span data-stu-id="33136-106">Before you can use the local policy API your application must open a handle to a [**Policy**](policy-object.md) object.</span></span> <span data-ttu-id="33136-107">若要這樣做，請呼叫 [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)。</span><span class="sxs-lookup"><span data-stu-id="33136-107">To do this, call [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy).</span></span> <span data-ttu-id="33136-108">此函式會傳回一個控制碼，讓您的應用程式可以在後續的 LSA 原則函式呼叫中指定。</span><span class="sxs-lookup"><span data-stu-id="33136-108">This function returns a handle that your application can then specify in subsequent LSA policy function calls.</span></span>

<span data-ttu-id="33136-109">每個控制碼都有一組相關聯的許可權，可決定您的應用程式可以使用控制碼在 [**原則**](policy-object.md) 物件上執行的作業。</span><span class="sxs-lookup"><span data-stu-id="33136-109">Each handle has an associated set of permissions that determine the operations your application can perform on the [**Policy**](policy-object.md) object by using the handle.</span></span> <span data-ttu-id="33136-110">您的應用程式一次可以開啟一個以上的 **原則** 物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="33136-110">Your application can open more than one handle to the **Policy** object at a time.</span></span> <span data-ttu-id="33136-111">當不再需要控制碼時，您的應用程式應該透過呼叫 [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)來關閉它。</span><span class="sxs-lookup"><span data-stu-id="33136-111">When a handle is no longer required, your application should close it by calling [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).</span></span>

## <a name="requirements"></a><span data-ttu-id="33136-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="33136-112">Requirements</span></span>



| <span data-ttu-id="33136-113">需求</span><span class="sxs-lookup"><span data-stu-id="33136-113">Requirement</span></span> | <span data-ttu-id="33136-114">值</span><span class="sxs-lookup"><span data-stu-id="33136-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33136-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33136-115">Minimum supported client</span></span><br/> | <span data-ttu-id="33136-116">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33136-116">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="33136-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33136-117">Minimum supported server</span></span><br/> | <span data-ttu-id="33136-118">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33136-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33136-119">標頭</span><span class="sxs-lookup"><span data-stu-id="33136-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="33136-120"><dt>Ntsecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="33136-120"><dt>Ntsecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33136-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33136-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33136-122">**LsaClose**</span><span class="sxs-lookup"><span data-stu-id="33136-122">**LsaClose**</span></span>](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)
</dt> <dt>

[<span data-ttu-id="33136-123">**LsaOpenPolicy**</span><span class="sxs-lookup"><span data-stu-id="33136-123">**LsaOpenPolicy**</span></span>](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)
</dt> </dl>

 

