---
description: 建立新的 Win32 \_ ClusterShare 實例。
ms.assetid: a6fde28d-f19e-4a31-8f0d-35927c75a030
ms.tgt_platform: multiple
title: Win32_ClusterShare 類別的 Create 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cbf7c42b8523bcd12b19e9b474ecc50bd031939
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111533"
---
# <a name="create-method-of-the-win32_clustershare-class"></a><span data-ttu-id="c882a-103">Win32 ClusterShare 類別的 Create 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c882a-103">Create method of the Win32\_ClusterShare class</span></span>

<span data-ttu-id="c882a-104">建立新的 [**Win32 \_ ClusterShare**](win32-clustershare.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="c882a-104">Creates a new [**Win32\_ClusterShare**](win32-clustershare.md) instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="c882a-105">語法</span><span class="sxs-lookup"><span data-stu-id="c882a-105">Syntax</span></span>


```mof
static uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="c882a-106">參數</span><span class="sxs-lookup"><span data-stu-id="c882a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c882a-107">*路徑* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c882a-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c882a-108">Windows 共用的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="c882a-108">Local path of the Windows share.</span></span>

<span data-ttu-id="c882a-109">範例： "C： \\ Program Files"。</span><span class="sxs-lookup"><span data-stu-id="c882a-109">Example, "C:\\Program Files".</span></span>

</dd> <dt>

<span data-ttu-id="c882a-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c882a-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c882a-111">在執行 Windows 的電腦系統上，設定為共用的路徑別名。</span><span class="sxs-lookup"><span data-stu-id="c882a-111">The alias to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="c882a-112">範例： "public"。</span><span class="sxs-lookup"><span data-stu-id="c882a-112">Example, "public".</span></span>

</dd> <dt>

<span data-ttu-id="c882a-113">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c882a-113">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c882a-114">共用的資源類型。</span><span class="sxs-lookup"><span data-stu-id="c882a-114">Type of resource being shared.</span></span> <span data-ttu-id="c882a-115">類型包括：磁片磁碟機、列印佇列、處理序間通訊 (IPC) 和一般裝置。</span><span class="sxs-lookup"><span data-stu-id="c882a-115">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<dt>

<span data-ttu-id="c882a-116">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="c882a-116">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c882a-117">磁碟機</span><span class="sxs-lookup"><span data-stu-id="c882a-117">Disk Drive</span></span>

</dd> <dt>

<span data-ttu-id="c882a-118">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="c882a-118">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c882a-119">列印佇列</span><span class="sxs-lookup"><span data-stu-id="c882a-119">Print Queue</span></span>

</dd> <dt>

<span data-ttu-id="c882a-120">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="c882a-120">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="c882a-121">裝置</span><span class="sxs-lookup"><span data-stu-id="c882a-121">Device</span></span>

</dd> <dt>

<span data-ttu-id="c882a-122">3 (0x3) </span><span class="sxs-lookup"><span data-stu-id="c882a-122">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="c882a-123">IPC</span><span class="sxs-lookup"><span data-stu-id="c882a-123">IPC</span></span>

</dd> <dt>

<span data-ttu-id="c882a-124">2147483648 (0x80000000) </span><span class="sxs-lookup"><span data-stu-id="c882a-124">2147483648 (0x80000000)</span></span>
</dt> <dd>

<span data-ttu-id="c882a-125">磁片磁碟機系統管理員</span><span class="sxs-lookup"><span data-stu-id="c882a-125">Disk Drive Admin</span></span>

</dd> <dt>

<span data-ttu-id="c882a-126">2147483649 (0x80000001) </span><span class="sxs-lookup"><span data-stu-id="c882a-126">2147483649 (0x80000001)</span></span>
</dt> <dd>

<span data-ttu-id="c882a-127">列印佇列管理員</span><span class="sxs-lookup"><span data-stu-id="c882a-127">Print Queue Admin</span></span>

</dd> <dt>

<span data-ttu-id="c882a-128">2147483650 (0x80000002) </span><span class="sxs-lookup"><span data-stu-id="c882a-128">2147483650 (0x80000002)</span></span>
</dt> <dd>

<span data-ttu-id="c882a-129">裝置系統管理員</span><span class="sxs-lookup"><span data-stu-id="c882a-129">Device Admin</span></span>

</dd> <dt>

<span data-ttu-id="c882a-130">2147483651 (0x80000003) </span><span class="sxs-lookup"><span data-stu-id="c882a-130">2147483651 (0x80000003)</span></span>
</dt> <dd>

<span data-ttu-id="c882a-131">IPC 系統管理員</span><span class="sxs-lookup"><span data-stu-id="c882a-131">IPC Admin</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c882a-132">*MaximumAllowed* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c882a-132">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c882a-133">允許同時使用此資源的使用者數目上限。</span><span class="sxs-lookup"><span data-stu-id="c882a-133">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="c882a-134">*描述* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c882a-134">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c882a-135">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="c882a-135">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="c882a-136">*密碼* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c882a-136">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c882a-137">TBD</span><span class="sxs-lookup"><span data-stu-id="c882a-137">TBD</span></span>

</dd> <dt>

<span data-ttu-id="c882a-138">*存取* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c882a-138">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c882a-139">[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)類別的選擇性內嵌實例，其中包含新共用的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="c882a-139">Optional embedded instance of a [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class that contains the security descriptor for the new share.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c882a-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="c882a-140">Requirements</span></span>



| <span data-ttu-id="c882a-141">需求</span><span class="sxs-lookup"><span data-stu-id="c882a-141">Requirement</span></span> | <span data-ttu-id="c882a-142">值</span><span class="sxs-lookup"><span data-stu-id="c882a-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c882a-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c882a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c882a-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c882a-144">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="c882a-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c882a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c882a-146">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c882a-146">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="c882a-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="c882a-147">Namespace</span></span><br/>                | <span data-ttu-id="c882a-148">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c882a-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c882a-149">MOF</span><span class="sxs-lookup"><span data-stu-id="c882a-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c882a-150"><dt>Cimwin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c882a-150"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c882a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="c882a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c882a-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c882a-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c882a-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c882a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c882a-154">**Win32 \_ ClusterShare**</span><span class="sxs-lookup"><span data-stu-id="c882a-154">**Win32\_ClusterShare**</span></span>](win32-clustershare.md)
</dt> </dl>

 

