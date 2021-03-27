---
description: 使安全性識別碼的使用者名稱快取失效。
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: 'DiskQuotaControl. InvalidateSidNameCache 方法 (Dskquota .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.InvalidateSidNameCache
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4e7202c1293d32d55e12e88671ed9960d376f63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943265"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a><span data-ttu-id="7d16e-103">DiskQuotaControl. InvalidateSidNameCache 方法</span><span class="sxs-lookup"><span data-stu-id="7d16e-103">DiskQuotaControl.InvalidateSidNameCache method</span></span>

<span data-ttu-id="7d16e-104">使安全性識別碼的使用者名稱快取失效。</span><span class="sxs-lookup"><span data-stu-id="7d16e-104">Invalidates the security ID user name cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d16e-105">語法</span><span class="sxs-lookup"><span data-stu-id="7d16e-105">Syntax</span></span>


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a><span data-ttu-id="7d16e-106">參數</span><span class="sxs-lookup"><span data-stu-id="7d16e-106">Parameters</span></span>

<span data-ttu-id="7d16e-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7d16e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d16e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d16e-108">Return value</span></span>

<span data-ttu-id="7d16e-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7d16e-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d16e-110">備註</span><span class="sxs-lookup"><span data-stu-id="7d16e-110">Remarks</span></span>

<span data-ttu-id="7d16e-111">使用者名稱和相關聯的安全識別碼會儲存在快取中。</span><span class="sxs-lookup"><span data-stu-id="7d16e-111">User names and associated security IDs are stored in a cache.</span></span> <span data-ttu-id="7d16e-112">您可以藉由呼叫 **InvalidateSidNameCache** 來清除此快取。</span><span class="sxs-lookup"><span data-stu-id="7d16e-112">You can clear this cache by calling **InvalidateSidNameCache**.</span></span> <span data-ttu-id="7d16e-113">如果您之後建立新的使用者物件，就必須從網域控制站取得資訊，而且必須重新建立快取。</span><span class="sxs-lookup"><span data-stu-id="7d16e-113">If you subsequently create a new user object, the information will have to be obtained from the domain controller, and the cache will have to be reestablished.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d16e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d16e-114">Requirements</span></span>



| <span data-ttu-id="7d16e-115">需求</span><span class="sxs-lookup"><span data-stu-id="7d16e-115">Requirement</span></span> | <span data-ttu-id="7d16e-116">值</span><span class="sxs-lookup"><span data-stu-id="7d16e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d16e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d16e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7d16e-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d16e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d16e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d16e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7d16e-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d16e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7d16e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7d16e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d16e-122"><dt>Dskquota。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d16e-122"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="7d16e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7d16e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d16e-124"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="7d16e-124"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d16e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d16e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d16e-126">**DiskQuotaControl 物件**</span><span class="sxs-lookup"><span data-stu-id="7d16e-126">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




