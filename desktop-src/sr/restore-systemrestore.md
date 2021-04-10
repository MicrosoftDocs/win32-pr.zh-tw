---
title: SystemRestore 類別的 Restore 方法
description: 起始系統還原。
ms.assetid: ca4aa97b-fa59-407d-b127-951d46932c33
keywords:
- Restore 方法系統還原
- Restore 方法系統還原，SystemRestore 類別
- SystemRestore 類別系統還原，Restore 方法
topic_type:
- apiref
api_name:
- SystemRestore.Restore
api_location:
- Root\\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b7747b710801718d9b169c8999c51dd30cefde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685610"
---
# <a name="restore-method-of-the-systemrestore-class"></a><span data-ttu-id="c1c63-106">SystemRestore 類別的 Restore 方法</span><span class="sxs-lookup"><span data-stu-id="c1c63-106">Restore method of the SystemRestore class</span></span>

<span data-ttu-id="c1c63-107">起始系統還原。</span><span class="sxs-lookup"><span data-stu-id="c1c63-107">Initiates a system restore.</span></span> <span data-ttu-id="c1c63-108">呼叫端必須強制系統重新開機。</span><span class="sxs-lookup"><span data-stu-id="c1c63-108">The caller must force a system reboot.</span></span> <span data-ttu-id="c1c63-109">在重新開機期間進行實際的還原。</span><span class="sxs-lookup"><span data-stu-id="c1c63-109">The actual restoration occurs during the reboot.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c63-110">語法</span><span class="sxs-lookup"><span data-stu-id="c1c63-110">Syntax</span></span>


```mof
uint32 Restore(
  [in] uint32 SequenceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="c1c63-111">參數</span><span class="sxs-lookup"><span data-stu-id="c1c63-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1c63-112">*SequenceNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1c63-112">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c63-113">還原點的序號。</span><span class="sxs-lookup"><span data-stu-id="c1c63-113">The sequence number of the restore point.</span></span> <span data-ttu-id="c1c63-114">若要判斷特定還原點的序號，請列舉系統上的所有還原點。</span><span class="sxs-lookup"><span data-stu-id="c1c63-114">To determine the sequence number for a specific restore point, enumerate all restore points on the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1c63-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1c63-115">Return value</span></span>

<span data-ttu-id="c1c63-116">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c1c63-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c1c63-117">否則，方法會傳回 Winerror.h 中定義的其中一個 COM 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c1c63-117">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="examples"></a><span data-ttu-id="c1c63-118">範例</span><span class="sxs-lookup"><span data-stu-id="c1c63-118">Examples</span></span>


```VB
'Restore Method of the SystemRestore Class
'Initiates a system restore. The caller must 
'force a system reboot. The actual restoration 
'occurs during the reboot.
Set Args = wscript.Arguments
RpNum = Args.item(0)
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
if obj.Restore(RpNum) <> 0 Then
    wscript.Echo "Restore failed"
End If
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
for each OpSys in OpSysSet
    OpSys.Reboot()
next
```



## <a name="requirements"></a><span data-ttu-id="c1c63-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1c63-119">Requirements</span></span>



| <span data-ttu-id="c1c63-120">需求</span><span class="sxs-lookup"><span data-stu-id="c1c63-120">Requirement</span></span> | <span data-ttu-id="c1c63-121">值</span><span class="sxs-lookup"><span data-stu-id="c1c63-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c1c63-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1c63-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c1c63-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1c63-123">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c1c63-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1c63-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c1c63-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="c1c63-125">None supported</span></span><br/>                                                         |
| <span data-ttu-id="c1c63-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="c1c63-126">Namespace</span></span><br/>                | <span data-ttu-id="c1c63-127">根 \\ \\ 預設值</span><span class="sxs-lookup"><span data-stu-id="c1c63-127">Root\\\\Default</span></span><br/>                                                        |
| <span data-ttu-id="c1c63-128">MOF</span><span class="sxs-lookup"><span data-stu-id="c1c63-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1c63-129"><dt>Sr-iov</dt></span><span class="sxs-lookup"><span data-stu-id="c1c63-129"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1c63-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1c63-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c63-131">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="c1c63-131">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





