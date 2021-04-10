---
title: 'DsIsNTDSOnline 函式 (Ntdsbcli) '
description: 判斷指定的伺服器上 Active Directory Domain Services 是否在線上。
ms.assetid: 8f46e4d8-6d05-402c-a5b4-291fd2d6609b
ms.tgt_platform: multiple
keywords:
- DsIsNTDSOnline 函式 Active Directory
topic_type:
- apiref
api_name:
- DsIsNTDSOnline
- DsIsNTDSOnlineA
- DsIsNTDSOnlineW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f6728f4481eb8820055b48f10cfa0f94c7aaa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103799"
---
# <a name="dsisntdsonline-function"></a><span data-ttu-id="58ce7-104">DsIsNTDSOnline 函式</span><span class="sxs-lookup"><span data-stu-id="58ce7-104">DsIsNTDSOnline function</span></span>

<span data-ttu-id="58ce7-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="58ce7-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="58ce7-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="58ce7-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="58ce7-107">從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="58ce7-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="58ce7-108">**DsIsNTDSOnline** 函式會判斷指定的伺服器上 Active Directory Domain Services 是否在線上。</span><span class="sxs-lookup"><span data-stu-id="58ce7-108">The **DsIsNTDSOnline** function determines if Active Directory Domain Services are online on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="58ce7-109">語法</span><span class="sxs-lookup"><span data-stu-id="58ce7-109">Syntax</span></span>


```C++
HRESULT DsIsNTDSOnline(
  _In_  LPCTSTR szServerName,
  _Out_ BOOL    *pfNTDSOnline
);
```



## <a name="parameters"></a><span data-ttu-id="58ce7-110">參數</span><span class="sxs-lookup"><span data-stu-id="58ce7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58ce7-111">*szServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="58ce7-111">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ce7-112">以 null 終止的字串指標，其中包含要測試之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="58ce7-112">Pointer to a null-terminated string that contains the name of the server to test.</span></span> <span data-ttu-id="58ce7-113">前面的反斜線是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="58ce7-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="58ce7-114">伺服器必須是呼叫此函式的同一部電腦。</span><span class="sxs-lookup"><span data-stu-id="58ce7-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="58ce7-115">伺服器名稱不能包含任何底線 (\_) 字元。</span><span class="sxs-lookup"><span data-stu-id="58ce7-115">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="58ce7-116">伺服器名稱的範例是「server1」 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="58ce7-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="58ce7-117">*pfNTDSOnline* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="58ce7-117">*pfNTDSOnline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58ce7-118">接收結果之 **BOOL** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="58ce7-118">Pointer to **BOOL** value that receives the result.</span></span> <span data-ttu-id="58ce7-119">如果目錄服務已上線，則會收到 **TRUE** ，如果目錄服務離線，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="58ce7-119">Receives **TRUE** if the directory service is online or **FALSE** if the directory service is offline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58ce7-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="58ce7-120">Return value</span></span>

<span data-ttu-id="58ce7-121">如果函式成功，則傳回 **S \_ OK** ，否則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="58ce7-121">Returns **S\_OK** if the function is successful or an error code otherwise.</span></span> <span data-ttu-id="58ce7-122">下列清單列出可能的錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="58ce7-122">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="58ce7-123">**\_拒絕存取 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="58ce7-123">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="58ce7-124">呼叫端沒有適當的存取權限可呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="58ce7-124">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="58ce7-125">[**DsSetAuthIdentity**](dssetauthidentity.md)函式可用來設定用於備份和還原功能的認證。</span><span class="sxs-lookup"><span data-stu-id="58ce7-125">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="58ce7-126">**hrCouldNotConnect**</span><span class="sxs-lookup"><span data-stu-id="58ce7-126">**hrCouldNotConnect**</span></span>
</dt> <dd>

<span data-ttu-id="58ce7-127">找不到 *szServerName* 中的伺服器、不是網域控制站，或 *szServerName* 的格式不正確。</span><span class="sxs-lookup"><span data-stu-id="58ce7-127">The server in *szServerName* cannot be found, is not a domain controller, or *szServerName* is not formatted correctly.</span></span> <span data-ttu-id="58ce7-128">此值定義于 Ntdsbmsg 中。</span><span class="sxs-lookup"><span data-stu-id="58ce7-128">This value is defined in Ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="58ce7-129">**RPC \_ S \_ 不正確系結 \_**</span><span class="sxs-lookup"><span data-stu-id="58ce7-129">**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd>

<span data-ttu-id="58ce7-130">正在遠端呼叫 [**DsIsNTDSOnline**](dsisntdsonline.md) 函數，或 *szServerName* 中的伺服器不是網域控制站。</span><span class="sxs-lookup"><span data-stu-id="58ce7-130">The [**DsIsNTDSOnline**](dsisntdsonline.md) function is being called remotely or the server in *szServerName* is not a domain controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58ce7-131">備註</span><span class="sxs-lookup"><span data-stu-id="58ce7-131">Remarks</span></span>

<span data-ttu-id="58ce7-132">呼叫此函式之前，請先呼叫此函式，再呼叫任何目錄備份或還原功能。</span><span class="sxs-lookup"><span data-stu-id="58ce7-132">Call this function before calling any of the directory backup or restore functions.</span></span> <span data-ttu-id="58ce7-133">目錄必須在線上，才能執行備份。</span><span class="sxs-lookup"><span data-stu-id="58ce7-133">The directory must be online in order to perform a backup.</span></span> <span data-ttu-id="58ce7-134">目錄必須離線才能執行還原。</span><span class="sxs-lookup"><span data-stu-id="58ce7-134">The directory must by offline to perform a restore.</span></span>

<span data-ttu-id="58ce7-135">這個函式只能從同時也是 *szServerName* 中所指定之目標伺服器的網域控制站呼叫。</span><span class="sxs-lookup"><span data-stu-id="58ce7-135">This function can only be called from a domain controller that is also the target server specified in *szServerName*.</span></span> <span data-ttu-id="58ce7-136">無法從遠端呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="58ce7-136">This function cannot be called remotely.</span></span>

## <a name="requirements"></a><span data-ttu-id="58ce7-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="58ce7-137">Requirements</span></span>



| <span data-ttu-id="58ce7-138">需求</span><span class="sxs-lookup"><span data-stu-id="58ce7-138">Requirement</span></span> | <span data-ttu-id="58ce7-139">值</span><span class="sxs-lookup"><span data-stu-id="58ce7-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58ce7-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58ce7-140">Minimum supported client</span></span><br/> | <span data-ttu-id="58ce7-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58ce7-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58ce7-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58ce7-142">Minimum supported server</span></span><br/> | <span data-ttu-id="58ce7-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58ce7-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58ce7-144">標頭</span><span class="sxs-lookup"><span data-stu-id="58ce7-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="58ce7-145"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="58ce7-145"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="58ce7-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="58ce7-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="58ce7-147"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="58ce7-147"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="58ce7-148">DLL</span><span class="sxs-lookup"><span data-stu-id="58ce7-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58ce7-149"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58ce7-149"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="58ce7-150">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="58ce7-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="58ce7-151">**DsIsNTDSOnlineW** (Unicode) 和 **DsIsNTDSOnlineA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="58ce7-151">**DsIsNTDSOnlineW** (Unicode) and **DsIsNTDSOnlineA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="58ce7-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58ce7-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ce7-153">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="58ce7-153">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="58ce7-154">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="58ce7-154">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="58ce7-155">備份與還原 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="58ce7-155">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> </dl>

 

