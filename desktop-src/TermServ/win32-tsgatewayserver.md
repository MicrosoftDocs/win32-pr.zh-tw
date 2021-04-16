---
title: Win32_TSGatewayServer 類別
description: 用於遠端桌面閘道 (RD 閘道) 伺服器特定的作業。
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServer 類別遠端桌面服務
- Win32_TSGatewayServer 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7dee009521c59b606010be085fcb0447558898d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465085"
---
# <a name="win32_tsgatewayserver-class"></a><span data-ttu-id="76999-105">Win32 \_ TSGatewayServer 類別</span><span class="sxs-lookup"><span data-stu-id="76999-105">Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="76999-106">用於遠端桌面閘道 (RD 閘道) 伺服器特定的作業。</span><span class="sxs-lookup"><span data-stu-id="76999-106">Used for Remote Desktop Gateway (RD Gateway) server-specific operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="76999-107">語法</span><span class="sxs-lookup"><span data-stu-id="76999-107">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a><span data-ttu-id="76999-108">成員</span><span class="sxs-lookup"><span data-stu-id="76999-108">Members</span></span>

<span data-ttu-id="76999-109">**Win32 \_ TSGatewayServer** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="76999-109">The **Win32\_TSGatewayServer** class has these types of members:</span></span>

-   [<span data-ttu-id="76999-110">方法</span><span class="sxs-lookup"><span data-stu-id="76999-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="76999-111">方法</span><span class="sxs-lookup"><span data-stu-id="76999-111">Methods</span></span>

<span data-ttu-id="76999-112">**Win32 \_ TSGatewayServer** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="76999-112">The **Win32\_TSGatewayServer** class has these methods.</span></span>



| <span data-ttu-id="76999-113">方法</span><span class="sxs-lookup"><span data-stu-id="76999-113">Method</span></span>                                                                                   | <span data-ttu-id="76999-114">描述</span><span class="sxs-lookup"><span data-stu-id="76999-114">Description</span></span>                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76999-115">**CreateSelfSignedCertificate**</span><span class="sxs-lookup"><span data-stu-id="76999-115">**CreateSelfSignedCertificate**</span></span>](createselfsignedcertificate-win32-tsgatewayserver.md) | <span data-ttu-id="76999-116">使用指定的主體名稱建立自我簽署憑證，並將憑證雜湊傳回為 "out" 參數。</span><span class="sxs-lookup"><span data-stu-id="76999-116">Creates a self-signed certificate with a given subject name and returns the certificate hash as an "out" parameter.</span></span><br/> |
| [<span data-ttu-id="76999-117">**出口**</span><span class="sxs-lookup"><span data-stu-id="76999-117">**Export**</span></span>](export-win32-tsgatewayserver.md)                                           | <span data-ttu-id="76999-118">以 XML 字串形式傳回 RD 閘道伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="76999-118">Returns the RD Gateway server configuration as an XML string.</span></span><br/>                                                       |
| [<span data-ttu-id="76999-119">**匯入**</span><span class="sxs-lookup"><span data-stu-id="76999-119">**Import**</span></span>](import-win32-tsgatewayserver.md)                                           | <span data-ttu-id="76999-120">匯入指定的設定至 RD 閘道伺服器。</span><span class="sxs-lookup"><span data-stu-id="76999-120">Imports a given configuration to the RD Gateway server.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="76999-121">備註</span><span class="sxs-lookup"><span data-stu-id="76999-121">Remarks</span></span>

<span data-ttu-id="76999-122">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="76999-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="76999-123">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="76999-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="76999-124">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="76999-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="76999-125">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="76999-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="76999-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="76999-126">Requirements</span></span>



| <span data-ttu-id="76999-127">需求</span><span class="sxs-lookup"><span data-stu-id="76999-127">Requirement</span></span> | <span data-ttu-id="76999-128">值</span><span class="sxs-lookup"><span data-stu-id="76999-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76999-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="76999-129">Minimum supported client</span></span><br/> | <span data-ttu-id="76999-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="76999-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="76999-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="76999-131">Minimum supported server</span></span><br/> | <span data-ttu-id="76999-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76999-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="76999-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="76999-133">Namespace</span></span><br/>                | <span data-ttu-id="76999-134">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="76999-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="76999-135">MOF</span><span class="sxs-lookup"><span data-stu-id="76999-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76999-136"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="76999-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="76999-137">DLL</span><span class="sxs-lookup"><span data-stu-id="76999-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76999-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76999-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



 

