---
title: ITSRemoteProgram RemoteProgramMode 屬性
description: Windows Server 2008 R2 RemoteApp 模式。
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- RemoteProgramMode 屬性遠端桌面服務
- RemoteProgramMode 屬性遠端桌面服務，ITSRemoteProgram 介面
- ITSRemoteProgram 介面遠端桌面服務，RemoteProgramMode 屬性
- RemoteProgramMode 屬性遠端桌面服務，ITSRemoteProgram2 介面
- ITSRemoteProgram2 介面遠端桌面服務，RemoteProgramMode 屬性
- RemoteProgramMode 屬性遠端桌面服務，ITSRemoteProgram3 介面
- ITSRemoteProgram3 介面遠端桌面服務，RemoteProgramMode 屬性
topic_type:
- apiref
api_name:
- ITSRemoteProgram.RemoteProgramMode
- ITSRemoteProgram.get_RemoteProgramMode
- ITSRemoteProgram.put_RemoteProgramMode
- ITSRemoteProgram2.RemoteProgramMode
- ITSRemoteProgram2.get_RemoteProgramMode
- ITSRemoteProgram2.put_RemoteProgramMode
- ITSRemoteProgram3.RemoteProgramMode
- ITSRemoteProgram3.get_RemoteProgramMode
- ITSRemoteProgram3.put_RemoteProgramMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8582824e2f6349e37b125ffd974847b602ad6fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106983314"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a><span data-ttu-id="78f93-110">ITSRemoteProgram：： RemoteProgramMode 屬性</span><span class="sxs-lookup"><span data-stu-id="78f93-110">ITSRemoteProgram::RemoteProgramMode property</span></span>

<span data-ttu-id="78f93-111">Windows Server 2008 R2 RemoteApp 模式。</span><span class="sxs-lookup"><span data-stu-id="78f93-111">The Windows Server 2008 R2 RemoteApp mode.</span></span>

<span data-ttu-id="78f93-112">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="78f93-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="78f93-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="78f93-113">Syntax</span></span>


```C++
HRESULT put_RemoteProgramMode(
  [in]  VARIANT_BOOL vboolRemoteProgramMode
);

HRESULT get_RemoteProgramMode(
  [out] VARIANT_BOOL *pvboolRemoteProgramMode
);
```



## <a name="property-value"></a><span data-ttu-id="78f93-114">屬性值</span><span class="sxs-lookup"><span data-stu-id="78f93-114">Property value</span></span>

<span data-ttu-id="78f93-115">RemoteApp 模式。</span><span class="sxs-lookup"><span data-stu-id="78f93-115">The RemoteApp mode.</span></span> <span data-ttu-id="78f93-116">如果設定為 **VARIANT \_ TRUE**，則會啟用 remoteapp 模式，而遠端會話將會裝載 remoteapp 程式。</span><span class="sxs-lookup"><span data-stu-id="78f93-116">If set to **VARIANT\_TRUE**, RemoteApp mode is enabled, and the remote session will host RemoteApp programs.</span></span> <span data-ttu-id="78f93-117">如果設定為 **VARIANT \_ FALSE** (預設) ，則不會啟用 RemoteApp 模式。</span><span class="sxs-lookup"><span data-stu-id="78f93-117">If set to **VARIANT\_FALSE** (the default), RemoteApp mode is not enabled.</span></span> <span data-ttu-id="78f93-118">遠端會話將裝載遠端桌面。</span><span class="sxs-lookup"><span data-stu-id="78f93-118">The remote session will host a remote desktop.</span></span>

## <a name="error-codes"></a><span data-ttu-id="78f93-119">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="78f93-119">Error codes</span></span>

<span data-ttu-id="78f93-120">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="78f93-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="78f93-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="78f93-121">Requirements</span></span>



| <span data-ttu-id="78f93-122">需求</span><span class="sxs-lookup"><span data-stu-id="78f93-122">Requirement</span></span> | <span data-ttu-id="78f93-123">值</span><span class="sxs-lookup"><span data-stu-id="78f93-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78f93-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78f93-124">Minimum supported client</span></span><br/> | <span data-ttu-id="78f93-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78f93-125">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="78f93-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78f93-126">Minimum supported server</span></span><br/> | <span data-ttu-id="78f93-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78f93-127">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="78f93-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="78f93-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="78f93-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78f93-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="78f93-130">DLL</span><span class="sxs-lookup"><span data-stu-id="78f93-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78f93-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78f93-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="78f93-132">IID</span><span class="sxs-lookup"><span data-stu-id="78f93-132">IID</span></span><br/>                      | <span data-ttu-id="78f93-133">IID \_ ITSRemoteProgram 定義為 FDD029F9-467A-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="78f93-133">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="78f93-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78f93-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78f93-135">**ITSRemoteProgram2**</span><span class="sxs-lookup"><span data-stu-id="78f93-135">**ITSRemoteProgram2**</span></span>](itsremoteprogram2.md)
</dt> <dt>

[<span data-ttu-id="78f93-136">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="78f93-136">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> <dt>

[<span data-ttu-id="78f93-137">**ITSRemoteProgram**</span><span class="sxs-lookup"><span data-stu-id="78f93-137">**ITSRemoteProgram**</span></span>](itsremoteprogram.md)
</dt> </dl>

 

 





