---
title: Win32_TSSessionDirectory 類別的 SetSessionDirectoryProperty 方法
description: 設定類別的 SessionDirectoryLocation 屬性或 SessionDirectoryClusterName 屬性。
ms.assetid: 728e1991-294f-4b80-86f8-a0c2cfd10e9c
ms.tgt_platform: multiple
keywords:
- SetSessionDirectoryProperty 方法遠端桌面服務
- SetSessionDirectoryProperty 方法遠端桌面服務，Win32_TSSessionDirectory 類別
- Win32_TSSessionDirectory 類別遠端桌面服務，SetSessionDirectoryProperty 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32357e662ec9b2edb05d75a2814d5215fc9ec7f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464957"
---
# <a name="setsessiondirectoryproperty-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="66d01-106">Win32 TSSessionDirectory 類別的 SetSessionDirectoryProperty 方法 \_</span><span class="sxs-lookup"><span data-stu-id="66d01-106">SetSessionDirectoryProperty method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="66d01-107">設定類別的 **SessionDirectoryLocation** 屬性或 **SessionDirectoryClusterName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="66d01-107">Sets the **SessionDirectoryLocation** property or the **SessionDirectoryClusterName** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="66d01-108">語法</span><span class="sxs-lookup"><span data-stu-id="66d01-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryProperty(
  [in] string PropertyName,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="66d01-109">參數</span><span class="sxs-lookup"><span data-stu-id="66d01-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66d01-110">*PropertyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66d01-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66d01-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="66d01-111">Type: **string**</span></span>

<span data-ttu-id="66d01-112">指定方法設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="66d01-112">Specifies the property that the method is setting.</span></span>

<dt>

<span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>

<span data-ttu-id="66d01-113"><span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**SessionDirectoryLocation**</span><span class="sxs-lookup"><span data-stu-id="66d01-113"><span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**SessionDirectoryLocation**</span></span>


</dt> <dd>

<span data-ttu-id="66d01-114">方法正在設定 **SessionDirectoryLocation** 屬性。</span><span class="sxs-lookup"><span data-stu-id="66d01-114">The method is setting the **SessionDirectoryLocation** property.</span></span>

</dd> <dt>

<span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>

<span data-ttu-id="66d01-115"><span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**SessionDirectoryClusterName**</span><span class="sxs-lookup"><span data-stu-id="66d01-115"><span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**SessionDirectoryClusterName**</span></span>


</dt> <dd>

<span data-ttu-id="66d01-116">方法正在設定 **SessionDirectoryClusterName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="66d01-116">The method is setting the **SessionDirectoryClusterName** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="66d01-117">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66d01-117">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66d01-118">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="66d01-118">Type: **string**</span></span>

<span data-ttu-id="66d01-119">屬性 *名稱* 參數所指定之屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="66d01-119">The new value for the property specified by the *PropertyName* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66d01-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="66d01-120">Return value</span></span>

<span data-ttu-id="66d01-121">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="66d01-121">Type: **uint32**</span></span>

<span data-ttu-id="66d01-122">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="66d01-122">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="66d01-123">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="66d01-123">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="66d01-124">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="66d01-124">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="66d01-125">備註</span><span class="sxs-lookup"><span data-stu-id="66d01-125">Remarks</span></span>

<span data-ttu-id="66d01-126">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="66d01-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="66d01-127">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="66d01-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="66d01-128">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="66d01-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="66d01-129">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="66d01-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="66d01-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="66d01-130">Requirements</span></span>



| <span data-ttu-id="66d01-131">需求</span><span class="sxs-lookup"><span data-stu-id="66d01-131">Requirement</span></span> | <span data-ttu-id="66d01-132">值</span><span class="sxs-lookup"><span data-stu-id="66d01-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66d01-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66d01-133">Minimum supported client</span></span><br/> | <span data-ttu-id="66d01-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="66d01-134">None supported</span></span><br/>                                                               |
| <span data-ttu-id="66d01-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66d01-135">Minimum supported server</span></span><br/> | <span data-ttu-id="66d01-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66d01-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="66d01-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="66d01-137">Namespace</span></span><br/>                | <span data-ttu-id="66d01-138">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="66d01-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="66d01-139">MOF</span><span class="sxs-lookup"><span data-stu-id="66d01-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66d01-140"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="66d01-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="66d01-141">DLL</span><span class="sxs-lookup"><span data-stu-id="66d01-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66d01-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66d01-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66d01-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66d01-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d01-144">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="66d01-144">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

