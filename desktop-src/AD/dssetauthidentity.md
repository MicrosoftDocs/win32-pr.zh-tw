---
title: 'DsSetAuthIdentity 函式 (Ntdsbcli) '
description: 設定用來呼叫目錄備份 Api 的安全性內容。
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- DsSetAuthIdentity 函式 Active Directory
topic_type:
- apiref
api_name:
- DsSetAuthIdentity
- DsSetAuthIdentityA
- DsSetAuthIdentityW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d973d5f818b4bd81278a1466487ae89ebf888f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465725"
---
# <a name="dssetauthidentity-function"></a><span data-ttu-id="93a1b-104">DsSetAuthIdentity 函式</span><span class="sxs-lookup"><span data-stu-id="93a1b-104">DsSetAuthIdentity function</span></span>

<span data-ttu-id="93a1b-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="93a1b-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="93a1b-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="93a1b-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="93a1b-107">從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="93a1b-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="93a1b-108">**DsSetAuthIdentity** 函式會設定用來呼叫目錄備份 api 的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="93a1b-108">The **DsSetAuthIdentity** function sets the security context under which the directory backup APIs are called.</span></span>

## <a name="syntax"></a><span data-ttu-id="93a1b-109">語法</span><span class="sxs-lookup"><span data-stu-id="93a1b-109">Syntax</span></span>


```C++
HRESULT DsSetAuthIdentity(
  _In_ LPCTSTR szUserName,
  _In_ LPCTSTR szDomainName,
  _In_ LPCTSTR szPassword
);
```



## <a name="parameters"></a><span data-ttu-id="93a1b-110">參數</span><span class="sxs-lookup"><span data-stu-id="93a1b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93a1b-111">*szUserName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93a1b-111">*szUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93a1b-112">指定使用者名稱的以 null 結束的字串。</span><span class="sxs-lookup"><span data-stu-id="93a1b-112">The null-terminated string that specifies the user name.</span></span>

</dd> <dt>

<span data-ttu-id="93a1b-113">*szDomainName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93a1b-113">*szDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93a1b-114">以 null 終止的字串，指定使用者所屬之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="93a1b-114">The null-terminated string that specifies the name of the domain that the user belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="93a1b-115">*szPassword* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93a1b-115">*szPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93a1b-116">以 null 終止的字串，指定指定網域中使用者的密碼。</span><span class="sxs-lookup"><span data-stu-id="93a1b-116">The null-terminated string that specifies the password of the user in the specified domain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93a1b-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="93a1b-117">Return value</span></span>

<span data-ttu-id="93a1b-118">如果成功，則傳回標準的 **HRESULT** 成功碼;否則，會傳回失敗碼。</span><span class="sxs-lookup"><span data-stu-id="93a1b-118">If successful, returns a standard **HRESULT** success codes; otherwise, a failure code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="93a1b-119">備註</span><span class="sxs-lookup"><span data-stu-id="93a1b-119">Remarks</span></span>

<span data-ttu-id="93a1b-120">如果未呼叫 **DsSetAuthIdentity** ，則會假設為目前進程的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="93a1b-120">If **DsSetAuthIdentity** is not called, security context of the current process is assumed.</span></span>

## <a name="requirements"></a><span data-ttu-id="93a1b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="93a1b-121">Requirements</span></span>



| <span data-ttu-id="93a1b-122">需求</span><span class="sxs-lookup"><span data-stu-id="93a1b-122">Requirement</span></span> | <span data-ttu-id="93a1b-123">值</span><span class="sxs-lookup"><span data-stu-id="93a1b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93a1b-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93a1b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="93a1b-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93a1b-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93a1b-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93a1b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="93a1b-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93a1b-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93a1b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="93a1b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="93a1b-129"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="93a1b-129"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="93a1b-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="93a1b-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="93a1b-131"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="93a1b-131"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="93a1b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="93a1b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93a1b-133"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93a1b-133"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="93a1b-134">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="93a1b-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="93a1b-135">**DsSetAuthIdentityW** (Unicode) 和 **DsSetAuthIdentityA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="93a1b-135">**DsSetAuthIdentityW** (Unicode) and **DsSetAuthIdentityA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="93a1b-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93a1b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93a1b-137">備份與還原 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="93a1b-137">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="93a1b-138">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="93a1b-138">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

