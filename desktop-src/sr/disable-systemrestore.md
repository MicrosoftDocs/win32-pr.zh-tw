---
title: Disable SystemRestore 類別的方法
description: 停用特定磁片磁碟機上的監視。
ms.assetid: 2ad37dd4-7d80-4697-9dbb-abb329a34ff7
keywords:
- 停用方法系統還原
- Disable 方法系統還原，SystemRestore 類別
- SystemRestore 類別系統還原，Disable 方法
topic_type:
- apiref
api_name:
- SystemRestore.Disable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19556833684aeab0cc126eff7aff0a258335c8e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104063"
---
# <a name="disable-method-of-the-systemrestore-class"></a><span data-ttu-id="7288f-106">Disable SystemRestore 類別的方法</span><span class="sxs-lookup"><span data-stu-id="7288f-106">Disable method of the SystemRestore class</span></span>

<span data-ttu-id="7288f-107">停用特定磁片磁碟機上的監視。</span><span class="sxs-lookup"><span data-stu-id="7288f-107">Disables monitoring on a particular drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="7288f-108">語法</span><span class="sxs-lookup"><span data-stu-id="7288f-108">Syntax</span></span>


```mof
uint32 Disable(
  [in] String Drive
);
```



## <a name="parameters"></a><span data-ttu-id="7288f-109">參數</span><span class="sxs-lookup"><span data-stu-id="7288f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7288f-110">*磁片磁碟機* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7288f-110">*Drive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7288f-111">要停用的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="7288f-111">The drive to be disabled.</span></span> <span data-ttu-id="7288f-112">磁片磁碟機字串的格式應為 "C： \\ "。</span><span class="sxs-lookup"><span data-stu-id="7288f-112">The drive string should be of the form "C:\\".</span></span> <span data-ttu-id="7288f-113">如果此參數為系統磁片磁碟機或空字串 ( "" ) ，則不會監視任何磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="7288f-113">If this parameter is the system drive or an empty string (""), no drives are monitored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7288f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="7288f-114">Return value</span></span>

<span data-ttu-id="7288f-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="7288f-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7288f-116">否則，方法會傳回 Winerror.h 中定義的其中一個 COM 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7288f-116">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="examples"></a><span data-ttu-id="7288f-117">範例</span><span class="sxs-lookup"><span data-stu-id="7288f-117">Examples</span></span>


```VB
'Disable Method of the SystemRestore Class
'Disables monitoring on a particular drive.
Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.Disable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="7288f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7288f-118">Requirements</span></span>



| <span data-ttu-id="7288f-119">需求</span><span class="sxs-lookup"><span data-stu-id="7288f-119">Requirement</span></span> | <span data-ttu-id="7288f-120">值</span><span class="sxs-lookup"><span data-stu-id="7288f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7288f-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7288f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7288f-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7288f-122">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7288f-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7288f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7288f-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="7288f-124">None supported</span></span><br/>                                                         |
| <span data-ttu-id="7288f-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="7288f-125">Namespace</span></span><br/>                | <span data-ttu-id="7288f-126">根 \\ 預設值</span><span class="sxs-lookup"><span data-stu-id="7288f-126">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="7288f-127">MOF</span><span class="sxs-lookup"><span data-stu-id="7288f-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7288f-128"><dt>Sr-iov</dt></span><span class="sxs-lookup"><span data-stu-id="7288f-128"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7288f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7288f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7288f-130">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="7288f-130">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





