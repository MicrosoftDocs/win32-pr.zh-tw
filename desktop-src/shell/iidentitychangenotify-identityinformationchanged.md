---
description: IdentityInformationChanged 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 3aca8a98-3d12-482d-9991-d6b53adde522
title: 'IIdentityChangeNotify：： IdentityInformationChanged 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.IdentityInformationChanged
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: c33f67a4def3312564ed943e2a3a917fe2843980
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849183"
---
# <a name="iidentitychangenotifyidentityinformationchanged-method"></a><span data-ttu-id="a0112-104">IIdentityChangeNotify：： IdentityInformationChanged 方法</span><span class="sxs-lookup"><span data-stu-id="a0112-104">IIdentityChangeNotify::IdentityInformationChanged method</span></span>

<span data-ttu-id="a0112-105">\[**IdentityInformationChanged** 不受支援，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="a0112-105">\[**IdentityInformationChanged** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="a0112-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="a0112-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="a0112-107">當使用者身分識別的相關資訊變更，或新增或刪除使用者身分識別時呼叫。</span><span class="sxs-lookup"><span data-stu-id="a0112-107">Called when information about a user identity has changed, or when a user identity has been added or deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0112-108">語法</span><span class="sxs-lookup"><span data-stu-id="a0112-108">Syntax</span></span>


```C++
HRESULT IdentityInformationChanged(
   DWORD dwType
);
```



## <a name="parameters"></a><span data-ttu-id="a0112-109">參數</span><span class="sxs-lookup"><span data-stu-id="a0112-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0112-110">*dwType*</span><span class="sxs-lookup"><span data-stu-id="a0112-110">*dwType*</span></span> 
</dt> <dd>

<span data-ttu-id="a0112-111">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a0112-111">Type: **DWORD**</span></span>

<span data-ttu-id="a0112-112">值，指定變更的資訊類型，或針對身分識別所執行的作業。</span><span class="sxs-lookup"><span data-stu-id="a0112-112">A value that specifies the type of information changed, or the operation performed on an identity.</span></span> <span data-ttu-id="a0112-113">可以是下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="a0112-113">Can be a combination of the following values.</span></span>

<dt>



 <span data-ttu-id="a0112-114"> (IIC \_ 目前的身分 \_ 識別 \_ 已變更) </span><span class="sxs-lookup"><span data-stu-id="a0112-114">(IIC\_CURRENT\_IDENTITY\_CHANGED)</span></span>


</dt> <dd>

<span data-ttu-id="a0112-115">目前的身分識別已修改。</span><span class="sxs-lookup"><span data-stu-id="a0112-115">The current identity has been modified.</span></span>

</dd> <dt>



 <span data-ttu-id="a0112-116"> (IIC 身分 \_ 識別 \_ 已變更) </span><span class="sxs-lookup"><span data-stu-id="a0112-116">(IIC\_IDENTITY\_CHANGED)</span></span>


</dt> <dd>

<span data-ttu-id="a0112-117">已修改身分識別。</span><span class="sxs-lookup"><span data-stu-id="a0112-117">An identity has been modified.</span></span>

</dd> <dt>



 <span data-ttu-id="a0112-118"> (已刪除的 IIC 身分 \_ 識別 \_) </span><span class="sxs-lookup"><span data-stu-id="a0112-118">(IIC\_IDENTITY\_DELETED)</span></span>


</dt> <dd>

<span data-ttu-id="a0112-119">已刪除身分識別。</span><span class="sxs-lookup"><span data-stu-id="a0112-119">An identity has been deleted.</span></span>

</dd> <dt>



 <span data-ttu-id="a0112-120"> (新增的 IIC 身分 \_ 識別 \_) </span><span class="sxs-lookup"><span data-stu-id="a0112-120">(IIC\_IDENTITY\_ADDED)</span></span>


</dt> <dd>

<span data-ttu-id="a0112-121">已新增身分識別。</span><span class="sxs-lookup"><span data-stu-id="a0112-121">A new identity has been added.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0112-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="a0112-122">Return value</span></span>

<span data-ttu-id="a0112-123">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a0112-123">Type: **HRESULT**</span></span>

<span data-ttu-id="a0112-124">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a0112-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a0112-125">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a0112-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0112-126">備註</span><span class="sxs-lookup"><span data-stu-id="a0112-126">Remarks</span></span>

<span data-ttu-id="a0112-127">當系統上的使用者身分識別清單已修改時，您可以執行此方法，以提供應用程式的自訂行為。</span><span class="sxs-lookup"><span data-stu-id="a0112-127">You may implement this method to provide custom behavior for your application when the list of user identities on the system has been modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0112-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0112-128">Requirements</span></span>



| <span data-ttu-id="a0112-129">需求</span><span class="sxs-lookup"><span data-stu-id="a0112-129">Requirement</span></span> | <span data-ttu-id="a0112-130">值</span><span class="sxs-lookup"><span data-stu-id="a0112-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0112-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0112-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a0112-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0112-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a0112-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0112-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a0112-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0112-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a0112-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a0112-135">End of client support</span></span><br/>    | <span data-ttu-id="a0112-136">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a0112-136">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="a0112-137">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="a0112-137">End of server support</span></span><br/>    | <span data-ttu-id="a0112-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a0112-138">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="a0112-139">標頭</span><span class="sxs-lookup"><span data-stu-id="a0112-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0112-140"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="a0112-140"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0112-141">Idl</span><span class="sxs-lookup"><span data-stu-id="a0112-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a0112-142"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a0112-142"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="a0112-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a0112-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0112-144"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0112-144"><dt>Msoe.dll</dt></span></span> </dl>    |



 

 




