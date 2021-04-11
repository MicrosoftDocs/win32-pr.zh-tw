---
title: RegisteredTask. GetSecurityDescriptor 方法
description: 針對腳本，取得用來作為已註冊工作之認證的安全描述項。
ms.assetid: 9b5985c5-c01a-4104-940f-1e0e79f18bb7
keywords:
- GetSecurityDescriptor 方法工作排程器
- GetSecurityDescriptor 方法工作排程器，RegisteredTask 物件
- RegisteredTask 物件工作排程器，GetSecurityDescriptor 方法
topic_type:
- apiref
api_name:
- RegisteredTask.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c7c0e6125bc848b361e4cc2d4515c32d797c57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934836"
---
# <a name="registeredtaskgetsecuritydescriptor-method"></a><span data-ttu-id="6bb48-106">RegisteredTask. GetSecurityDescriptor 方法</span><span class="sxs-lookup"><span data-stu-id="6bb48-106">RegisteredTask.GetSecurityDescriptor method</span></span>

<span data-ttu-id="6bb48-107">針對腳本，取得用來作為已註冊工作之認證的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="6bb48-107">For scripting, gets the security descriptor that is used as credentials for the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb48-108">語法</span><span class="sxs-lookup"><span data-stu-id="6bb48-108">Syntax</span></span>


```VB
sddl = .GetSecurityDescriptor( _
  ByVal securityInformation _
)
```



## <a name="parameters"></a><span data-ttu-id="6bb48-109">參數</span><span class="sxs-lookup"><span data-stu-id="6bb48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bb48-110">*securityInformation*</span><span class="sxs-lookup"><span data-stu-id="6bb48-110">*securityInformation*</span></span> 
</dt> <dd>

<span data-ttu-id="6bb48-111">[**安全性 \_**](/windows/desktop/SecAuthZ/security-information)資訊的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="6bb48-111">The security information from [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bb48-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6bb48-112">Return value</span></span>

<span data-ttu-id="6bb48-113">已註冊工作的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="6bb48-113">The security descriptor for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb48-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bb48-114">Requirements</span></span>



| <span data-ttu-id="6bb48-115">需求</span><span class="sxs-lookup"><span data-stu-id="6bb48-115">Requirement</span></span> | <span data-ttu-id="6bb48-116">值</span><span class="sxs-lookup"><span data-stu-id="6bb48-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb48-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6bb48-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb48-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bb48-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6bb48-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6bb48-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb48-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bb48-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6bb48-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6bb48-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="6bb48-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6bb48-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6bb48-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6bb48-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bb48-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bb48-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb48-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bb48-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb48-126">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="6bb48-126">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="6bb48-127">**TaskFolder. GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="6bb48-127">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="6bb48-128">**RegisteredTask.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="6bb48-128">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

