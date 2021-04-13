---
title: Win32_SessionDirectoryCluster 類別
description: 提供屬性，以在遠端桌面連線代理人 (RD 連線代理人) 中查看伺服器陣列的屬性。
ms.assetid: a4a924fd-88ea-46db-968e-378c3dc46cfc
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryCluster 類別遠端桌面服務
- Win32_SessionDirectoryCluster 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryCluster
- Win32_SessionDirectoryCluster.ClusterName
- Win32_SessionDirectoryCluster.NumberOfServers
- Win32_SessionDirectoryCluster.SingleSessionMode
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3979dbe5403ca8f18e941b01e95774dabefe3211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464965"
---
# <a name="win32_sessiondirectorycluster-class"></a><span data-ttu-id="97bcc-105">Win32 \_ SessionDirectoryCluster 類別</span><span class="sxs-lookup"><span data-stu-id="97bcc-105">Win32\_SessionDirectoryCluster class</span></span>

<span data-ttu-id="97bcc-106">提供屬性，以在遠端桌面連線代理人 (RD 連線代理人) 中查看伺服器陣列的屬性。</span><span class="sxs-lookup"><span data-stu-id="97bcc-106">Provides properties for viewing the properties of a farm in Remote Desktop Connection Broker (RD Connection Broker).</span></span>

> [!Note]  
> <span data-ttu-id="97bcc-107">在 Windows Server 2008 R2 中，終端機服務會話代理人 (TS 會話代理人) 的名稱已變更為 RD 連線代理人。</span><span class="sxs-lookup"><span data-stu-id="97bcc-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="97bcc-108">除非另有說明，否則這些屬性適用于所有支援的作業系統。</span><span class="sxs-lookup"><span data-stu-id="97bcc-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="97bcc-109">語法</span><span class="sxs-lookup"><span data-stu-id="97bcc-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYCLUSTER_Prov"), AMENDMENT]
class Win32_SessionDirectoryCluster
{
  string ClusterName;
  uint32 NumberOfServers;
  uint32 SingleSessionMode;
};
```

## <a name="members"></a><span data-ttu-id="97bcc-110">成員</span><span class="sxs-lookup"><span data-stu-id="97bcc-110">Members</span></span>

<span data-ttu-id="97bcc-111">**Win32 \_ SessionDirectoryCluster** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="97bcc-111">The **Win32\_SessionDirectoryCluster** class has these types of members:</span></span>

-   [<span data-ttu-id="97bcc-112">屬性</span><span class="sxs-lookup"><span data-stu-id="97bcc-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97bcc-113">屬性</span><span class="sxs-lookup"><span data-stu-id="97bcc-113">Properties</span></span>

<span data-ttu-id="97bcc-114">**Win32 \_ SessionDirectoryCluster** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="97bcc-114">The **Win32\_SessionDirectoryCluster** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97bcc-115">**ClusterName**</span><span class="sxs-lookup"><span data-stu-id="97bcc-115">**ClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bcc-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="97bcc-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97bcc-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="97bcc-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bcc-118">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="97bcc-118">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="97bcc-119">RD 連線代理人中伺服器陣列的名稱。</span><span class="sxs-lookup"><span data-stu-id="97bcc-119">Name of the farm in RD Connection Broker.</span></span>

</dd> <dt>

<span data-ttu-id="97bcc-120">**NumberOfServers**</span><span class="sxs-lookup"><span data-stu-id="97bcc-120">**NumberOfServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bcc-121">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="97bcc-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97bcc-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="97bcc-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97bcc-123">RD 連線代理人中伺服器陣列中的伺服器數目。</span><span class="sxs-lookup"><span data-stu-id="97bcc-123">Number of servers in the farm in RD Connection Broker.</span></span>

</dd> <dt>

<span data-ttu-id="97bcc-124">**SingleSessionMode**</span><span class="sxs-lookup"><span data-stu-id="97bcc-124">**SingleSessionMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bcc-125">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="97bcc-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97bcc-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="97bcc-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97bcc-127">RD 連線代理人中伺服器陣列的單一會話模式。</span><span class="sxs-lookup"><span data-stu-id="97bcc-127">Single session mode of the farm in RD Connection Broker.</span></span>

<dt>

<span data-ttu-id="97bcc-128">0</span><span class="sxs-lookup"><span data-stu-id="97bcc-128">0</span></span>
</dt> <dd>

<span data-ttu-id="97bcc-129">RD 連線代理人中的伺服器陣列不在單一會話模式中。</span><span class="sxs-lookup"><span data-stu-id="97bcc-129">The farm in RD Connection Broker is not in single session mode.</span></span>

</dd> <dt>

<span data-ttu-id="97bcc-130">1</span><span class="sxs-lookup"><span data-stu-id="97bcc-130">1</span></span>
</dt> <dd>

<span data-ttu-id="97bcc-131">RD 連線代理人中的伺服器陣列處於單一會話模式。</span><span class="sxs-lookup"><span data-stu-id="97bcc-131">The farm in RD Connection Broker is in single session mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97bcc-132">備註</span><span class="sxs-lookup"><span data-stu-id="97bcc-132">Remarks</span></span>

<span data-ttu-id="97bcc-133">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="97bcc-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="97bcc-134">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="97bcc-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="97bcc-135">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="97bcc-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="97bcc-136">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="97bcc-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="97bcc-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="97bcc-137">Requirements</span></span>



| <span data-ttu-id="97bcc-138">需求</span><span class="sxs-lookup"><span data-stu-id="97bcc-138">Requirement</span></span> | <span data-ttu-id="97bcc-139">值</span><span class="sxs-lookup"><span data-stu-id="97bcc-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97bcc-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97bcc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="97bcc-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="97bcc-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="97bcc-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97bcc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="97bcc-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97bcc-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="97bcc-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="97bcc-144">Namespace</span></span><br/>                | <span data-ttu-id="97bcc-145">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="97bcc-145">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="97bcc-146">MOF</span><span class="sxs-lookup"><span data-stu-id="97bcc-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97bcc-147"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="97bcc-147"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="97bcc-148">DLL</span><span class="sxs-lookup"><span data-stu-id="97bcc-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97bcc-149"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97bcc-149"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97bcc-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97bcc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97bcc-151">**Win32 \_ SessionDirectoryServer**</span><span class="sxs-lookup"><span data-stu-id="97bcc-151">**Win32\_SessionDirectoryServer**</span></span>](win32-sessiondirectoryserver.md)
</dt> <dt>

[<span data-ttu-id="97bcc-152">**Win32 \_ SessionDirectorySession**</span><span class="sxs-lookup"><span data-stu-id="97bcc-152">**Win32\_SessionDirectorySession**</span></span>](win32-sessiondirectorysession.md)
</dt> </dl>

 

