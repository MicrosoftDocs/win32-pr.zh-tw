---
title: Win32_VirtualDesktopSession 類別
description: 管理虛擬桌面會話。
ms.assetid: a5a0d2a4-6e19-42ac-988c-2d3787946325
ms.tgt_platform: multiple
keywords:
- Win32_VirtualDesktopSession 類別遠端桌面服務
- Win32_VirtualDesktopSession 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession.VMHostName
- Win32_VirtualDesktopSession.SessionId
- Win32_VirtualDesktopSession.VMName
- Win32_VirtualDesktopSession.ConnectState
- Win32_VirtualDesktopSession.UserName
- Win32_VirtualDesktopSession.DomainName
- Win32_VirtualDesktopSession.CollectionId
- Win32_VirtualDesktopSession.ClientMachineName
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f343c1dc022dcb4759f813de956ade27e1aff213
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464464"
---
# <a name="win32_virtualdesktopsession-class"></a><span data-ttu-id="74b03-105">Win32 \_ VirtualDesktopSession 類別</span><span class="sxs-lookup"><span data-stu-id="74b03-105">Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="74b03-106">管理虛擬桌面會話。</span><span class="sxs-lookup"><span data-stu-id="74b03-106">Manages a virtual desktop session.</span></span>

<span data-ttu-id="74b03-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="74b03-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="74b03-108">語法</span><span class="sxs-lookup"><span data-stu-id="74b03-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_VirtualDesktopSession
{
  string VMHostName;
  uint32 SessionId;
  string VMName;
  uint32 ConnectState;
  string UserName;
  string DomainName;
  string CollectionId;
  string ClientMachineName;
};
```

## <a name="members"></a><span data-ttu-id="74b03-109">成員</span><span class="sxs-lookup"><span data-stu-id="74b03-109">Members</span></span>

<span data-ttu-id="74b03-110">**Win32 \_ VirtualDesktopSession** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="74b03-110">The **Win32\_VirtualDesktopSession** class has these types of members:</span></span>

-   [<span data-ttu-id="74b03-111">方法</span><span class="sxs-lookup"><span data-stu-id="74b03-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="74b03-112">屬性</span><span class="sxs-lookup"><span data-stu-id="74b03-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="74b03-113">方法</span><span class="sxs-lookup"><span data-stu-id="74b03-113">Methods</span></span>

<span data-ttu-id="74b03-114">**Win32 \_ VirtualDesktopSession** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="74b03-114">The **Win32\_VirtualDesktopSession** class has these methods.</span></span>



| <span data-ttu-id="74b03-115">方法</span><span class="sxs-lookup"><span data-stu-id="74b03-115">Method</span></span>                                                         | <span data-ttu-id="74b03-116">描述</span><span class="sxs-lookup"><span data-stu-id="74b03-116">Description</span></span>                                                                |
|:---------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="74b03-117">**中斷連線**</span><span class="sxs-lookup"><span data-stu-id="74b03-117">**Disconnect**</span></span>](disconnect-win32-virtualdesktopsession.md)   | <span data-ttu-id="74b03-118">中斷虛擬桌面會話的連線。</span><span class="sxs-lookup"><span data-stu-id="74b03-118">Disconnects the virtual desktop session.</span></span><br/>                        |
| [<span data-ttu-id="74b03-119">**登出**</span><span class="sxs-lookup"><span data-stu-id="74b03-119">**Logoff**</span></span>](logoff-win32-virtualdesktopsession.md)           | <span data-ttu-id="74b03-120">登出虛擬桌面會話的使用者。</span><span class="sxs-lookup"><span data-stu-id="74b03-120">Logs off the user from the virtual desktop session.</span></span><br/>             |
| [<span data-ttu-id="74b03-121">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="74b03-121">**SendMessage**</span></span>](sendmessage-win32-virtualdesktopsession.md) | <span data-ttu-id="74b03-122">透過虛擬桌面會話傳送訊息給使用者。</span><span class="sxs-lookup"><span data-stu-id="74b03-122">Send a message to the user through the virtual desktop session.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="74b03-123">屬性</span><span class="sxs-lookup"><span data-stu-id="74b03-123">Properties</span></span>

<span data-ttu-id="74b03-124">**Win32 \_ VirtualDesktopSession** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="74b03-124">The **Win32\_VirtualDesktopSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74b03-125">**ClientMachineName**</span><span class="sxs-lookup"><span data-stu-id="74b03-125">**ClientMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b03-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74b03-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74b03-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74b03-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74b03-128">取得連接到會話的用戶端電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="74b03-128">Gets the name of the client machine that is connected to the session.</span></span>

</dd> <dt>

<span data-ttu-id="74b03-129">**CollectionId**</span><span class="sxs-lookup"><span data-stu-id="74b03-129">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b03-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74b03-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74b03-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74b03-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74b03-132">取得裝載虛擬機器之虛擬桌面集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="74b03-132">Gets the name of the virtual desktop collection that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="74b03-133">**ConnectState**</span><span class="sxs-lookup"><span data-stu-id="74b03-133">**ConnectState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b03-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="74b03-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74b03-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74b03-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74b03-136">取得會話的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="74b03-136">Gets the state of the connection to the session.</span></span>

</dd> <dt>

<span data-ttu-id="74b03-137">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="74b03-137">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b03-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74b03-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74b03-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74b03-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74b03-140">取得使用者的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="74b03-140">Gets the domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="74b03-141">**SessionId**</span><span class="sxs-lookup"><span data-stu-id="74b03-141">**SessionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b03-142">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="74b03-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74b03-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74b03-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74b03-144">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="74b03-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="74b03-145">取得虛擬桌面會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="74b03-145">Gets the ID of the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="74b03-146">**使用者名稱**</span><span class="sxs-lookup"><span data-stu-id="74b03-146">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b03-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74b03-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74b03-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74b03-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74b03-149">取得指派給會話的使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="74b03-149">Gets the name of the user account that is assigned to the session.</span></span>

</dd> <dt>

<span data-ttu-id="74b03-150">**VMHostName**</span><span class="sxs-lookup"><span data-stu-id="74b03-150">**VMHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b03-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74b03-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74b03-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74b03-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74b03-153">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="74b03-153">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="74b03-154">取得裝載虛擬機器之遠端桌面虛擬化主機伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="74b03-154">Gets the name of the Remote Desktop virtualization host server that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="74b03-155">**VMName**</span><span class="sxs-lookup"><span data-stu-id="74b03-155">**VMName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b03-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74b03-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74b03-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74b03-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74b03-158">取得指派給會話的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="74b03-158">Gets the name of the virtual machine that is assigned to the session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74b03-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="74b03-159">Requirements</span></span>



| <span data-ttu-id="74b03-160">需求</span><span class="sxs-lookup"><span data-stu-id="74b03-160">Requirement</span></span> | <span data-ttu-id="74b03-161">值</span><span class="sxs-lookup"><span data-stu-id="74b03-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="74b03-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74b03-162">Minimum supported client</span></span><br/> | <span data-ttu-id="74b03-163">都不支援</span><span class="sxs-lookup"><span data-stu-id="74b03-163">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="74b03-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74b03-164">Minimum supported server</span></span><br/> | <span data-ttu-id="74b03-165">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74b03-165">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="74b03-166">命名空間</span><span class="sxs-lookup"><span data-stu-id="74b03-166">Namespace</span></span><br/>                | <span data-ttu-id="74b03-167">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="74b03-167">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="74b03-168">MOF</span><span class="sxs-lookup"><span data-stu-id="74b03-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74b03-169"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="74b03-169"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="74b03-170">DLL</span><span class="sxs-lookup"><span data-stu-id="74b03-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74b03-171"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74b03-171"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="74b03-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74b03-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74b03-173">遠端桌面管理服務提供者</span><span class="sxs-lookup"><span data-stu-id="74b03-173">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

