---
title: Enable SystemRestore 類別的方法
description: 在特定磁片磁碟機上啟用監視。
ms.assetid: f3140f6d-d190-46a4-8587-c2e928ac8ecf
keywords:
- 啟用方法系統還原
- Enable 方法系統還原，SystemRestore 類別
- SystemRestore 類別系統還原，Enable 方法
topic_type:
- apiref
api_name:
- SystemRestore.Enable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090aa01b4028a7146ea1d7f271ba4390f43ca260
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969979"
---
# <a name="enable-method-of-the-systemrestore-class"></a><span data-ttu-id="807c1-106">Enable SystemRestore 類別的方法</span><span class="sxs-lookup"><span data-stu-id="807c1-106">Enable method of the SystemRestore class</span></span>

<span data-ttu-id="807c1-107">在特定磁片磁碟機上啟用監視。</span><span class="sxs-lookup"><span data-stu-id="807c1-107">Enables monitoring on a particular drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="807c1-108">語法</span><span class="sxs-lookup"><span data-stu-id="807c1-108">Syntax</span></span>


```mof
uint32 Enable(
  [in] String Drive
);
```



## <a name="parameters"></a><span data-ttu-id="807c1-109">參數</span><span class="sxs-lookup"><span data-stu-id="807c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="807c1-110">*磁片磁碟機* \[在\]</span><span class="sxs-lookup"><span data-stu-id="807c1-110">*Drive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="807c1-111">要啟用的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="807c1-111">The drive to be enabled.</span></span> <span data-ttu-id="807c1-112">磁片磁碟機字串的格式應為 "C： \\ "。</span><span class="sxs-lookup"><span data-stu-id="807c1-112">The drive string should be of the form "C:\\".</span></span> <span data-ttu-id="807c1-113">如果此參數為系統磁片磁碟機，或 ( "" ) 的空字串，則會監視所有磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="807c1-113">If this parameter is the system drive or an empty string (""), all drives are monitored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="807c1-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="807c1-114">Return value</span></span>

<span data-ttu-id="807c1-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="807c1-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="807c1-116">否則，方法會傳回 Winerror.h 中定義的其中一個 COM 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="807c1-116">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="807c1-117">備註</span><span class="sxs-lookup"><span data-stu-id="807c1-117">Remarks</span></span>

<span data-ttu-id="807c1-118">**Enable** 方法在傳回之前，不會等待監視完全啟用，因為這可能需要一些時間。</span><span class="sxs-lookup"><span data-stu-id="807c1-118">The **Enable** method does not wait for monitoring to be enabled completely before it returns, because this could take a while.</span></span> <span data-ttu-id="807c1-119">相反地，它會在啟動系統還原服務和篩選器驅動程式之後立即返回。</span><span class="sxs-lookup"><span data-stu-id="807c1-119">Instead, it returns immediately after starting the System Restore service and filter driver.</span></span>

<span data-ttu-id="807c1-120">若要在非系統磁片磁碟機上啟用系統還原，您必須先在系統磁片磁碟機上啟用系統還原。</span><span class="sxs-lookup"><span data-stu-id="807c1-120">To enable System Restore on a non-system drive, you must first enable System Restore on the system drive.</span></span>

<span data-ttu-id="807c1-121">在安全模式中，這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="807c1-121">This method fails in safe mode.</span></span>

## <a name="examples"></a><span data-ttu-id="807c1-122">範例</span><span class="sxs-lookup"><span data-stu-id="807c1-122">Examples</span></span>


```VB
'Enable Method of the SystemRestore Class
'Enables monitoring on a particular drive.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else 
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
If (obj.Enable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="807c1-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="807c1-123">Requirements</span></span>



| <span data-ttu-id="807c1-124">需求</span><span class="sxs-lookup"><span data-stu-id="807c1-124">Requirement</span></span> | <span data-ttu-id="807c1-125">值</span><span class="sxs-lookup"><span data-stu-id="807c1-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="807c1-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="807c1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="807c1-127">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="807c1-127">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="807c1-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="807c1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="807c1-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="807c1-129">None supported</span></span><br/>                                                         |
| <span data-ttu-id="807c1-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="807c1-130">Namespace</span></span><br/>                | <span data-ttu-id="807c1-131">根 \\ 預設值</span><span class="sxs-lookup"><span data-stu-id="807c1-131">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="807c1-132">MOF</span><span class="sxs-lookup"><span data-stu-id="807c1-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="807c1-133"><dt>Sr-iov</dt></span><span class="sxs-lookup"><span data-stu-id="807c1-133"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="807c1-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="807c1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="807c1-135">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="807c1-135">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





