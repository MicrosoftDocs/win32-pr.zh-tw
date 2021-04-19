---
description: Lsa \_ \_ 函數會使用 lsa 列舉控制碼資料類型來列舉 TrustedDomain 物件： LsaEnumerateTrustedDomainsEx。
ms.assetid: 99dad3aa-cb92-4b7e-8a18-2c977cb2737c
title: 'LSA_ENUMERATION_HANDLE (Ntsecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db71e9522a188956a7aa838b11ba74f08bde39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974470"
---
# <a name="lsa_enumeration_handle"></a><span data-ttu-id="9be0c-103">LSA \_ 列舉 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="9be0c-103">LSA\_ENUMERATION\_HANDLE</span></span>

<span data-ttu-id="9be0c-104">Lsa 函數會使用 **lsa \_ 列舉 \_ 控制碼** 資料類型來列舉 [**TrustedDomain**](trusteddomain-object.md) 物件： [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)。</span><span class="sxs-lookup"><span data-stu-id="9be0c-104">The **LSA\_ENUMERATION\_HANDLE** data type is used by the LSA function that enumerates [**TrustedDomain**](trusteddomain-object.md) objects: [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span></span> <span data-ttu-id="9be0c-105">這個函式的設計目的，是為了讓您可以進行多個呼叫，以列舉資料庫中特定類型的所有物件。</span><span class="sxs-lookup"><span data-stu-id="9be0c-105">This function is designed so that you can make multiple calls to enumerate all the objects of a given type in the database.</span></span>

<span data-ttu-id="9be0c-106">在初始列舉函式呼叫中，您會將指標傳遞至已初始化為零的 **LSA \_ 列舉 \_ 控制碼** 變數。</span><span class="sxs-lookup"><span data-stu-id="9be0c-106">On the initial enumeration function call, you pass in a pointer to an **LSA\_ENUMERATION\_HANDLE** variable that is initialized to zero.</span></span> <span data-ttu-id="9be0c-107">函數會更新此值。</span><span class="sxs-lookup"><span data-stu-id="9be0c-107">The function updates this value.</span></span> <span data-ttu-id="9be0c-108">如果函式傳回的值指出有更多要列舉的物件，請再次呼叫函式，並傳入更新的 **LSA \_ 列舉 \_ 控制碼** 值，以取得從先前列舉中斷的點繼續的列舉。</span><span class="sxs-lookup"><span data-stu-id="9be0c-108">If the function returns a value that indicates there are more objects to enumerate, call the function again and pass in the updated **LSA\_ENUMERATION\_HANDLE** value to obtain an enumeration continuing from the point where the previous enumeration left off.</span></span>


```C++
typedef ULONG LSA_ENUMERATION_HANDLE, *PLSA_ENUMERATION_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="9be0c-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="9be0c-109">Requirements</span></span>



| <span data-ttu-id="9be0c-110">需求</span><span class="sxs-lookup"><span data-stu-id="9be0c-110">Requirement</span></span> | <span data-ttu-id="9be0c-111">值</span><span class="sxs-lookup"><span data-stu-id="9be0c-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9be0c-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9be0c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="9be0c-113">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9be0c-113">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9be0c-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9be0c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="9be0c-115">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9be0c-115">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9be0c-116">標頭</span><span class="sxs-lookup"><span data-stu-id="9be0c-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="9be0c-117"><dt>Ntsecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9be0c-117"><dt>Ntsecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9be0c-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9be0c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9be0c-119">**LsaEnumerateTrustedDomainsEx**</span><span class="sxs-lookup"><span data-stu-id="9be0c-119">**LsaEnumerateTrustedDomainsEx**</span></span>](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)
</dt> </dl>

 

 




