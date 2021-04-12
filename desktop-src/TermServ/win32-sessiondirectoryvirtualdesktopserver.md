---
title: Win32_SessionDirectoryVirtualDesktopServer 類別
description: 代表加入會話代理人的遠端桌面虛擬化主機 (RD 虛擬化主機) 伺服器。
ms.assetid: a09221bd-d1b1-465b-91bb-9ca400a796b1
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVirtualDesktopServer 類別遠端桌面服務
- Win32_SessionDirectoryVirtualDesktopServer 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVirtualDesktopServer
- Win32_SessionDirectoryVirtualDesktopServer.Name
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2940679c13c5bd86f7d6b02340698f529e8149e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024814"
---
# <a name="win32_sessiondirectoryvirtualdesktopserver-class"></a><span data-ttu-id="9f9e6-105">Win32 \_ SessionDirectoryVirtualDesktopServer 類別</span><span class="sxs-lookup"><span data-stu-id="9f9e6-105">Win32\_SessionDirectoryVirtualDesktopServer class</span></span>

<span data-ttu-id="9f9e6-106">代表加入會話代理人的遠端桌面虛擬化主機 (RD 虛擬化主機) 伺服器。</span><span class="sxs-lookup"><span data-stu-id="9f9e6-106">Represents a Remote Desktop Virtualization Host (RD Virtualization Host) server joined to a session broker.</span></span>

<span data-ttu-id="9f9e6-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9f9e6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f9e6-108">語法</span><span class="sxs-lookup"><span data-stu-id="9f9e6-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_SDVirtualDesktopServer_Prov"), AMENDMENT]
class Win32_SessionDirectoryVirtualDesktopServer
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="9f9e6-109">成員</span><span class="sxs-lookup"><span data-stu-id="9f9e6-109">Members</span></span>

<span data-ttu-id="9f9e6-110">**Win32 \_ SessionDirectoryVirtualDesktopServer** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9f9e6-110">The **Win32\_SessionDirectoryVirtualDesktopServer** class has these types of members:</span></span>

-   [<span data-ttu-id="9f9e6-111">屬性</span><span class="sxs-lookup"><span data-stu-id="9f9e6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f9e6-112">屬性</span><span class="sxs-lookup"><span data-stu-id="9f9e6-112">Properties</span></span>

<span data-ttu-id="9f9e6-113">**Win32 \_ SessionDirectoryVirtualDesktopServer** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9f9e6-113">The **Win32\_SessionDirectoryVirtualDesktopServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f9e6-114">**名稱**</span><span class="sxs-lookup"><span data-stu-id="9f9e6-114">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f9e6-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9f9e6-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f9e6-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9f9e6-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f9e6-117">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9f9e6-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9f9e6-118">RD 虛擬主機伺服器的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="9f9e6-118">The DNS name of the RD Virtualization Host server.</span></span> <span data-ttu-id="9f9e6-119">此名稱的格式為「*MachineName*」。*網域*.com」。</span><span class="sxs-lookup"><span data-stu-id="9f9e6-119">This name takes the form "*MachineName*.*Domain*.com".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f9e6-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f9e6-120">Requirements</span></span>



| <span data-ttu-id="9f9e6-121">需求</span><span class="sxs-lookup"><span data-stu-id="9f9e6-121">Requirement</span></span> | <span data-ttu-id="9f9e6-122">值</span><span class="sxs-lookup"><span data-stu-id="9f9e6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f9e6-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f9e6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9f9e6-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="9f9e6-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9f9e6-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f9e6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9f9e6-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f9e6-126">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="9f9e6-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="9f9e6-127">Namespace</span></span><br/>                | <span data-ttu-id="9f9e6-128">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="9f9e6-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="9f9e6-129">MOF</span><span class="sxs-lookup"><span data-stu-id="9f9e6-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f9e6-130"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f9e6-130"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f9e6-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9f9e6-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f9e6-132"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f9e6-132"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

