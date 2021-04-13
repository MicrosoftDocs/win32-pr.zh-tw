---
title: 'VMUndoAction 列舉 (VPCCOMInterfaces) '
description: 指定當虛擬機器關閉或關閉時，復原磁片磁碟機會發生什麼事。
ms.assetid: f8f96fd3-0b2a-40ae-8b2e-b6bcc995dedd
keywords:
- VMUndoAction 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMUndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10917a5fb8d00e16a28f4b175237484b977cf914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509327"
---
# <a name="vmundoaction-enumeration"></a><span data-ttu-id="aee5f-104">VMUndoAction 列舉</span><span class="sxs-lookup"><span data-stu-id="aee5f-104">VMUndoAction enumeration</span></span>

<span data-ttu-id="aee5f-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="aee5f-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="aee5f-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="aee5f-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="aee5f-107">指定當虛擬機器關閉或關閉時，復原磁片磁碟機會發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="aee5f-107">Specifies what happens to undo drives when a virtual machine is shut down or turned off.</span></span>

## <a name="syntax"></a><span data-ttu-id="aee5f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aee5f-108">Syntax</span></span>


```C++
typedef enum  { 
  vmUndoAction_Discard  = 0,
  vmUndoAction_Keep     = 1,
  vmUndoAction_Commit   = 2
} VMUndoAction;
```



## <a name="constants"></a><span data-ttu-id="aee5f-109">常數</span><span class="sxs-lookup"><span data-stu-id="aee5f-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="aee5f-110"><span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**vmUndoAction \_ 捨棄**</span><span class="sxs-lookup"><span data-stu-id="aee5f-110"><span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**vmUndoAction\_Discard**</span></span>
</dt> <dd>

<span data-ttu-id="aee5f-111">捨棄復原磁片磁碟機;父磁片磁碟機保持不變。</span><span class="sxs-lookup"><span data-stu-id="aee5f-111">Discard the undo drives; the parent drives remain unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="aee5f-112"><span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmUndoAction \_ 保留**</span><span class="sxs-lookup"><span data-stu-id="aee5f-112"><span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmUndoAction\_Keep**</span></span>
</dt> <dd>

<span data-ttu-id="aee5f-113">保留復原磁片磁碟機;父磁片磁碟機保持不變，但下次虛擬機器啟動時，將會保留變更。</span><span class="sxs-lookup"><span data-stu-id="aee5f-113">Keep the undo drives; the parent drives remain unchanged, but changes will be maintained the next time the virtual machine starts.</span></span>

</dd> <dt>

<span data-ttu-id="aee5f-114"><span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**vmUndoAction \_ 認可**</span><span class="sxs-lookup"><span data-stu-id="aee5f-114"><span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**vmUndoAction\_Commit**</span></span>
</dt> <dd>

<span data-ttu-id="aee5f-115">認可父磁片磁碟機的變更。</span><span class="sxs-lookup"><span data-stu-id="aee5f-115">Commit changes to the parent drives.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aee5f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="aee5f-116">Requirements</span></span>



| <span data-ttu-id="aee5f-117">需求</span><span class="sxs-lookup"><span data-stu-id="aee5f-117">Requirement</span></span> | <span data-ttu-id="aee5f-118">值</span><span class="sxs-lookup"><span data-stu-id="aee5f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aee5f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aee5f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aee5f-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aee5f-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aee5f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aee5f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aee5f-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="aee5f-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="aee5f-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="aee5f-123">End of client support</span></span><br/>    | <span data-ttu-id="aee5f-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aee5f-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="aee5f-125">產品</span><span class="sxs-lookup"><span data-stu-id="aee5f-125">Product</span></span><br/>                  | <span data-ttu-id="aee5f-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="aee5f-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="aee5f-127">標頭</span><span class="sxs-lookup"><span data-stu-id="aee5f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="aee5f-128"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="aee5f-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aee5f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aee5f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee5f-130">**IVMVirtualMachine::UndoAction**</span><span class="sxs-lookup"><span data-stu-id="aee5f-130">**IVMVirtualMachine::UndoAction**</span></span>](ivmvirtualmachine-undoaction.md)
</dt> </dl>

 

