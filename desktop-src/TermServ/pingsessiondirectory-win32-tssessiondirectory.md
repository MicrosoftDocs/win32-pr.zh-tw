---
title: Win32_TSSessionDirectory 類別的 PingSessionDirectory 方法
description: 檢查遠端桌面連線代理人 (RD 連線代理人) 伺服器是否可供使用。
ms.assetid: 89243998-5ab2-4ea6-aa31-95ec63289055
ms.tgt_platform: multiple
keywords:
- PingSessionDirectory 方法遠端桌面服務
- PingSessionDirectory 方法遠端桌面服務，Win32_TSSessionDirectory 類別
- Win32_TSSessionDirectory 類別遠端桌面服務，PingSessionDirectory 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.PingSessionDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4022a0c34094a19651522c3f8153038c6d9df503
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508751"
---
# <a name="pingsessiondirectory-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="345c3-106">Win32 TSSessionDirectory 類別的 PingSessionDirectory 方法 \_</span><span class="sxs-lookup"><span data-stu-id="345c3-106">PingSessionDirectory method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="345c3-107">檢查遠端桌面連線代理人 (RD 連線代理人) 伺服器是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="345c3-107">Checks whether the Remote Desktop Connection Broker (RD Connection Broker) server is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="345c3-108">語法</span><span class="sxs-lookup"><span data-stu-id="345c3-108">Syntax</span></span>


```mof
uint32 PingSessionDirectory(
  [in] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="345c3-109">參數</span><span class="sxs-lookup"><span data-stu-id="345c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="345c3-110">*ServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="345c3-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="345c3-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="345c3-111">Type: **string**</span></span>

<span data-ttu-id="345c3-112">RD 連線代理人伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="345c3-112">Name of the RD Connection Broker server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="345c3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="345c3-113">Return value</span></span>

<span data-ttu-id="345c3-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="345c3-114">Type: **uint32**</span></span>

<span data-ttu-id="345c3-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="345c3-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="345c3-116">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="345c3-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="345c3-117">備註</span><span class="sxs-lookup"><span data-stu-id="345c3-117">Remarks</span></span>

<span data-ttu-id="345c3-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="345c3-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="345c3-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="345c3-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="345c3-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="345c3-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="345c3-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="345c3-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="345c3-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="345c3-122">Requirements</span></span>



| <span data-ttu-id="345c3-123">需求</span><span class="sxs-lookup"><span data-stu-id="345c3-123">Requirement</span></span> | <span data-ttu-id="345c3-124">值</span><span class="sxs-lookup"><span data-stu-id="345c3-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="345c3-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="345c3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="345c3-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="345c3-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="345c3-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="345c3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="345c3-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="345c3-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="345c3-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="345c3-129">Namespace</span></span><br/>                | <span data-ttu-id="345c3-130">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="345c3-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="345c3-131">MOF</span><span class="sxs-lookup"><span data-stu-id="345c3-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="345c3-132"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="345c3-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="345c3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="345c3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="345c3-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="345c3-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="345c3-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="345c3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="345c3-136">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="345c3-136">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

