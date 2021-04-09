---
title: 'DsRestoreEnd 函式 (Ntdsbcli) '
description: 呼叫以終止還原作業。
ms.assetid: 2c3b9aba-3e92-4e5b-afff-3ed9bf64832b
ms.tgt_platform: multiple
keywords:
- DsRestoreEnd 函式 Active Directory
topic_type:
- apiref
api_name:
- DsRestoreEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabbe216875c2fe934f3c87e32688cd17bc8992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025003"
---
# <a name="dsrestoreend-function"></a><span data-ttu-id="c7fcc-104">DsRestoreEnd 函式</span><span class="sxs-lookup"><span data-stu-id="c7fcc-104">DsRestoreEnd function</span></span>

<span data-ttu-id="c7fcc-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c7fcc-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c7fcc-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="c7fcc-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c7fcc-107">改為使用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="c7fcc-107">Use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="c7fcc-108">呼叫 **DsRestoreEnd** 函數，以終止還原作業。</span><span class="sxs-lookup"><span data-stu-id="c7fcc-108">The **DsRestoreEnd** function is called to terminate a restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7fcc-109">語法</span><span class="sxs-lookup"><span data-stu-id="c7fcc-109">Syntax</span></span>


```C++
HRESULT DsRestoreEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="c7fcc-110">參數</span><span class="sxs-lookup"><span data-stu-id="c7fcc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7fcc-111">*hbc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7fcc-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7fcc-112">包含使用 [**DsRestorePrepare**](dsrestoreprepare.md) 函數取得的還原內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="c7fcc-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7fcc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7fcc-113">Return value</span></span>

<span data-ttu-id="c7fcc-114">如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c7fcc-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="c7fcc-115">下列清單列出可能的錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="c7fcc-115">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="c7fcc-116">**錯誤 \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="c7fcc-116">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="c7fcc-117">*hbc* 無效。</span><span class="sxs-lookup"><span data-stu-id="c7fcc-117">*hbc* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7fcc-118">備註</span><span class="sxs-lookup"><span data-stu-id="c7fcc-118">Remarks</span></span>

<span data-ttu-id="c7fcc-119">**DsRestoreEnd** 函式會關閉未完成的系結控制碼，並在嘗試還原之後執行清除作業。</span><span class="sxs-lookup"><span data-stu-id="c7fcc-119">The **DsRestoreEnd** function closes outstanding binding handles and performs a cleanup operation after a restore attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7fcc-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7fcc-120">Requirements</span></span>



| <span data-ttu-id="c7fcc-121">需求</span><span class="sxs-lookup"><span data-stu-id="c7fcc-121">Requirement</span></span> | <span data-ttu-id="c7fcc-122">值</span><span class="sxs-lookup"><span data-stu-id="c7fcc-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7fcc-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7fcc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c7fcc-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="c7fcc-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c7fcc-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7fcc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c7fcc-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="c7fcc-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c7fcc-127">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c7fcc-127">End of client support</span></span><br/>    | <span data-ttu-id="c7fcc-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="c7fcc-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c7fcc-129">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c7fcc-129">End of server support</span></span><br/>    | <span data-ttu-id="c7fcc-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="c7fcc-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c7fcc-131">標頭</span><span class="sxs-lookup"><span data-stu-id="c7fcc-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7fcc-132"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7fcc-132"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7fcc-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="c7fcc-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7fcc-134"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7fcc-134"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="c7fcc-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c7fcc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7fcc-136"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7fcc-136"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7fcc-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7fcc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7fcc-138">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="c7fcc-138">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="c7fcc-139">還原 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="c7fcc-139">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="c7fcc-140">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="c7fcc-140">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

