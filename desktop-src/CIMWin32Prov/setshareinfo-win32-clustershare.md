---
description: 設定共用資源的參數。
ms.assetid: 592d0fa6-c865-4f70-89c3-b58204a8c5a6
ms.tgt_platform: multiple
title: Win32_ClusterShare 類別的 SetShareInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bda6fe36d1168045ea9f8d331ff334920ed1dd19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972150"
---
# <a name="setshareinfo-method-of-the-win32_clustershare-class"></a><span data-ttu-id="9163e-103">Win32 ClusterShare 類別的 SetShareInfo 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9163e-103">SetShareInfo method of the Win32\_ClusterShare class</span></span>

<span data-ttu-id="9163e-104">設定共用資源的參數。</span><span class="sxs-lookup"><span data-stu-id="9163e-104">Sets the parameters of the shared resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="9163e-105">語法</span><span class="sxs-lookup"><span data-stu-id="9163e-105">Syntax</span></span>


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="9163e-106">參數</span><span class="sxs-lookup"><span data-stu-id="9163e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9163e-107">*MaximumAllowed* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9163e-107">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9163e-108">允許同時使用此資源的使用者數目上限。</span><span class="sxs-lookup"><span data-stu-id="9163e-108">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="9163e-109">*描述* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9163e-109">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9163e-110">描述正在共用的資源。</span><span class="sxs-lookup"><span data-stu-id="9163e-110">Describes the resource being shared.</span></span>

</dd> <dt>

<span data-ttu-id="9163e-111">*存取* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9163e-111">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9163e-112">使用者層級許可權的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="9163e-112">Security descriptor for user-level permissions.</span></span> <span data-ttu-id="9163e-113">安全描述項包含資源的許可權、擁有者和存取功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9163e-113">A security descriptor contains information about the permission, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="9163e-114">如需詳細資訊，請參閱 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)。</span><span class="sxs-lookup"><span data-stu-id="9163e-114">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9163e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="9163e-115">Requirements</span></span>



| <span data-ttu-id="9163e-116">需求</span><span class="sxs-lookup"><span data-stu-id="9163e-116">Requirement</span></span> | <span data-ttu-id="9163e-117">值</span><span class="sxs-lookup"><span data-stu-id="9163e-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9163e-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9163e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9163e-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9163e-119">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="9163e-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9163e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9163e-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9163e-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="9163e-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="9163e-122">Namespace</span></span><br/>                | <span data-ttu-id="9163e-123">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9163e-123">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9163e-124">MOF</span><span class="sxs-lookup"><span data-stu-id="9163e-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9163e-125"><dt>Cimwin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9163e-125"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9163e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9163e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9163e-127"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9163e-127"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9163e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9163e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9163e-129">**Win32 \_ ClusterShare**</span><span class="sxs-lookup"><span data-stu-id="9163e-129">**Win32\_ClusterShare**</span></span>](win32-clustershare.md)
</dt> </dl>

 

