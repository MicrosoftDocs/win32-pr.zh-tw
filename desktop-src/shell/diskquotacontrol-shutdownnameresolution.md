---
description: 關閉使用者名稱解析執行緒。
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: 'DiskQuotaControl. ShutdownNameResolution 方法 (Dskquota .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.ShutdownNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0db952a502210e509abeb527b2006eab087434e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026170"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a><span data-ttu-id="3545a-103">DiskQuotaControl. ShutdownNameResolution 方法</span><span class="sxs-lookup"><span data-stu-id="3545a-103">DiskQuotaControl.ShutdownNameResolution method</span></span>

<span data-ttu-id="3545a-104">關閉使用者名稱解析執行緒。</span><span class="sxs-lookup"><span data-stu-id="3545a-104">Shuts down the user name resolution thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="3545a-105">語法</span><span class="sxs-lookup"><span data-stu-id="3545a-105">Syntax</span></span>


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a><span data-ttu-id="3545a-106">參數</span><span class="sxs-lookup"><span data-stu-id="3545a-106">Parameters</span></span>

<span data-ttu-id="3545a-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3545a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3545a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3545a-108">Return value</span></span>

<span data-ttu-id="3545a-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3545a-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3545a-110">備註</span><span class="sxs-lookup"><span data-stu-id="3545a-110">Remarks</span></span>

<span data-ttu-id="3545a-111">安全識別碼 (SID) 名稱解析程式會將 SID 轉譯為背景執行緒上的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="3545a-111">The security identifier (SID) name resolver translates SID to user names on a background thread.</span></span> <span data-ttu-id="3545a-112">當相關聯的配額控制物件終結時，就會自動關閉這個執行緒。</span><span class="sxs-lookup"><span data-stu-id="3545a-112">This thread is shut down automatically when the associated quota control object is destroyed.</span></span> <span data-ttu-id="3545a-113">不過，在某些情況下，已不再需要執行緒，但物件尚未準備好終結。</span><span class="sxs-lookup"><span data-stu-id="3545a-113">However, there are some cases when the thread is no longer needed, but the object is not yet ready to be destroyed.</span></span> <span data-ttu-id="3545a-114">典型的範例是，當沒有進一步的處理時，用戶端仍會保留物件的參考。</span><span class="sxs-lookup"><span data-stu-id="3545a-114">A typical example is when no further processing is taking place, but clients are still holding references to the object.</span></span> <span data-ttu-id="3545a-115">**ShutdownNameResolution** 方法可讓您終止解析程式執行緒，並釋放相關聯的資源，而不會終結配額控制物件。</span><span class="sxs-lookup"><span data-stu-id="3545a-115">The **ShutdownNameResolution** method allows you to terminate the resolver thread and free the associated resources without destroying the quota control object.</span></span>

> [!Note]  
> <span data-ttu-id="3545a-116">當您關閉解析程式執行緒時，非同步名稱解析會立即停止。</span><span class="sxs-lookup"><span data-stu-id="3545a-116">When you shut down the resolver thread, asynchronous name resolution immediately stops.</span></span> <span data-ttu-id="3545a-117">如果後續對 [**AddUser**](diskquotacontrol-adduser.md) 或 [**FindUser**](diskquotacontrol-finduser.md)等方法進行呼叫，配額物件可能會重新建立解析程式執行緒。</span><span class="sxs-lookup"><span data-stu-id="3545a-117">If calls are subsequently made to methods such as [**AddUser**](diskquotacontrol-adduser.md) or [**FindUser**](diskquotacontrol-finduser.md), the quota object might re-create the resolver thread.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3545a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3545a-118">Requirements</span></span>



| <span data-ttu-id="3545a-119">需求</span><span class="sxs-lookup"><span data-stu-id="3545a-119">Requirement</span></span> | <span data-ttu-id="3545a-120">值</span><span class="sxs-lookup"><span data-stu-id="3545a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3545a-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3545a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3545a-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3545a-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3545a-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3545a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3545a-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3545a-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3545a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3545a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3545a-126"><dt>Dskquota。h</dt></span><span class="sxs-lookup"><span data-stu-id="3545a-126"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="3545a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3545a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3545a-128"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="3545a-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3545a-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3545a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3545a-130">**DiskQuotaControl 物件**</span><span class="sxs-lookup"><span data-stu-id="3545a-130">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




