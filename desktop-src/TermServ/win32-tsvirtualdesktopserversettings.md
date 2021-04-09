---
title: Win32_TSVirtualDesktopServerSettings 類別
description: 包含 (RD 虛擬主機) server 的遠端桌面虛擬化主機的設定資訊。
ms.assetid: 749018aa-a8aa-433e-985b-40b44ef8aa7f
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualDesktopServerSettings 類別遠端桌面服務
- Win32_TSVirtualDesktopServerSettings 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSVirtualDesktopServerSettings
- Win32_TSVirtualDesktopServerSettings.SessionBrokerName
- Win32_TSVirtualDesktopServerSettings.PolicySourceSessionBrokerName
- Win32_TSVirtualDesktopServerSettings.Concurrency
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39635aee7b32430ace0ead0e3b007051a3c049d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686349"
---
# <a name="win32_tsvirtualdesktopserversettings-class"></a><span data-ttu-id="ea4db-105">Win32 \_ TSVirtualDesktopServerSettings 類別</span><span class="sxs-lookup"><span data-stu-id="ea4db-105">Win32\_TSVirtualDesktopServerSettings class</span></span>

<span data-ttu-id="ea4db-106">包含 (RD 虛擬主機) server 的遠端桌面虛擬化主機的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="ea4db-106">Contains configuration information for a Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

<span data-ttu-id="ea4db-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ea4db-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea4db-108">語法</span><span class="sxs-lookup"><span data-stu-id="ea4db-108">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVirtualDesktopServerSettings
{
  string SessionBrokerName;
  sint32 PolicySourceSessionBrokerName;
  uint32 Concurrency;
};
```

## <a name="members"></a><span data-ttu-id="ea4db-109">成員</span><span class="sxs-lookup"><span data-stu-id="ea4db-109">Members</span></span>

<span data-ttu-id="ea4db-110">**Win32 \_ TSVirtualDesktopServerSettings** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ea4db-110">The **Win32\_TSVirtualDesktopServerSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="ea4db-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ea4db-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ea4db-112">屬性</span><span class="sxs-lookup"><span data-stu-id="ea4db-112">Properties</span></span>

<span data-ttu-id="ea4db-113">**Win32 \_ TSVirtualDesktopServerSettings** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ea4db-113">The **Win32\_TSVirtualDesktopServerSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea4db-114">**並行**</span><span class="sxs-lookup"><span data-stu-id="ea4db-114">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4db-115">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ea4db-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4db-116">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ea4db-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ea4db-117">此虛擬桌面伺服器允許的並行布建要求數上限。</span><span class="sxs-lookup"><span data-stu-id="ea4db-117">The maximum allowed concurrent provisioning requests for this Virtual Desktop Server.</span></span>

</dd> <dt>

<span data-ttu-id="ea4db-118">**PolicySourceSessionBrokerName**</span><span class="sxs-lookup"><span data-stu-id="ea4db-118">**PolicySourceSessionBrokerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4db-119">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ea4db-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea4db-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ea4db-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea4db-121">如果設定為0，表示 **SessionBrokerName** 屬性是由伺服器設定;如果設定為1，表示 **SessionBrokerName** 屬性是由群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="ea4db-121">If set to 0, indicates that the **SessionBrokerName** property is configured by the server; if set to 1, indicates the **SessionBrokerName** property is configured by a group policy.</span></span>

</dd> <dt>

<span data-ttu-id="ea4db-122">**SessionBrokerName**</span><span class="sxs-lookup"><span data-stu-id="ea4db-122">**SessionBrokerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea4db-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ea4db-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea4db-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ea4db-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ea4db-125">RD 虛擬主機伺服器之會話代理人的完整分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="ea4db-125">The fully qualified distinguished name of the session broker for the RD Virtualization Host server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea4db-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea4db-126">Requirements</span></span>



| <span data-ttu-id="ea4db-127">需求</span><span class="sxs-lookup"><span data-stu-id="ea4db-127">Requirement</span></span> | <span data-ttu-id="ea4db-128">值</span><span class="sxs-lookup"><span data-stu-id="ea4db-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4db-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea4db-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ea4db-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="ea4db-130">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="ea4db-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea4db-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ea4db-132">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ea4db-132">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="ea4db-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="ea4db-133">Namespace</span></span><br/>                | <span data-ttu-id="ea4db-134">根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="ea4db-134">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="ea4db-135">MOF</span><span class="sxs-lookup"><span data-stu-id="ea4db-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea4db-136"><dt>TSVmHost mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea4db-136"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="ea4db-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ea4db-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea4db-138"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea4db-138"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

 





