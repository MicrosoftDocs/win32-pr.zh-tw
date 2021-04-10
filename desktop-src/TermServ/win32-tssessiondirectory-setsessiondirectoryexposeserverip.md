---
title: Win32_TSSessionDirectory 類別的 SetSessionDirectoryExposeServerIP 方法
description: 設定 SessionDirectoryExposeServerIP 屬性。
ms.assetid: ae9a0c72-0a0a-42a0-a233-13da1efe60ef
ms.tgt_platform: multiple
keywords:
- SetSessionDirectoryExposeServerIP 方法遠端桌面服務
- SetSessionDirectoryExposeServerIP 方法遠端桌面服務，Win32_TSSessionDirectory 類別
- Win32_TSSessionDirectory 類別遠端桌面服務，SetSessionDirectoryExposeServerIP 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryExposeServerIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f175e780d63eed3881b9146116702a30a02a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934230"
---
# <a name="setsessiondirectoryexposeserverip-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="c7a1d-106">Win32 TSSessionDirectory 類別的 SetSessionDirectoryExposeServerIP 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c7a1d-106">SetSessionDirectoryExposeServerIP method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="c7a1d-107">設定 **SessionDirectoryExposeServerIP** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c7a1d-107">Sets the **SessionDirectoryExposeServerIP** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7a1d-108">語法</span><span class="sxs-lookup"><span data-stu-id="c7a1d-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryExposeServerIP(
  [in] uint32 SessionDirectoryExposeServerIP
);
```



## <a name="parameters"></a><span data-ttu-id="c7a1d-109">參數</span><span class="sxs-lookup"><span data-stu-id="c7a1d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7a1d-110">*SessionDirectoryExposeServerIP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7a1d-110">*SessionDirectoryExposeServerIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7a1d-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c7a1d-111">Type: **uint32**</span></span>

<span data-ttu-id="c7a1d-112">旗標停用或啟用 **SessionDirectoryExposeServerIP** 屬性，以允許或拒絕抓取會話目錄的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c7a1d-112">Flag disabling or enabling the **SessionDirectoryExposeServerIP** property which allows or denies retrieval of the IP address for the session directory.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="c7a1d-113"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="c7a1d-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="c7a1d-114">停用屬性。</span><span class="sxs-lookup"><span data-stu-id="c7a1d-114">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="c7a1d-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="c7a1d-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="c7a1d-116">啟用屬性。</span><span class="sxs-lookup"><span data-stu-id="c7a1d-116">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7a1d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7a1d-117">Return value</span></span>

<span data-ttu-id="c7a1d-118">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c7a1d-118">Type: **uint32**</span></span>

<span data-ttu-id="c7a1d-119">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c7a1d-119">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c7a1d-120">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="c7a1d-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="c7a1d-121">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c7a1d-121">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7a1d-122">備註</span><span class="sxs-lookup"><span data-stu-id="c7a1d-122">Remarks</span></span>

<span data-ttu-id="c7a1d-123">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="c7a1d-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c7a1d-124">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c7a1d-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c7a1d-125">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="c7a1d-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c7a1d-126">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="c7a1d-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7a1d-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7a1d-127">Requirements</span></span>



| <span data-ttu-id="c7a1d-128">需求</span><span class="sxs-lookup"><span data-stu-id="c7a1d-128">Requirement</span></span> | <span data-ttu-id="c7a1d-129">值</span><span class="sxs-lookup"><span data-stu-id="c7a1d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7a1d-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7a1d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c7a1d-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="c7a1d-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c7a1d-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7a1d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c7a1d-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7a1d-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7a1d-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="c7a1d-134">Namespace</span></span><br/>                | <span data-ttu-id="c7a1d-135">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="c7a1d-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c7a1d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c7a1d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7a1d-137"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7a1d-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7a1d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c7a1d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7a1d-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7a1d-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7a1d-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7a1d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7a1d-141">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="c7a1d-141">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

