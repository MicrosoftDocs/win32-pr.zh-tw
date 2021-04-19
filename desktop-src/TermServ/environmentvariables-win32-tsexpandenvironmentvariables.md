---
title: Win32_TSExpandEnvironmentVariables 類別的 EnvironmentVariables 方法
description: 展開系統定義的環境變數。 |Win32_TSExpandEnvironmentVariables 類別的 EnvironmentVariables 方法
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- EnvironmentVariables 方法遠端桌面服務
- EnvironmentVariables 方法遠端桌面服務，Win32_TSExpandEnvironmentVariables 類別
- Win32_TSExpandEnvironmentVariables 類別遠端桌面服務，EnvironmentVariables 方法
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables.EnvironmentVariables
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f038ee1d5f93c11336657f9b8c1a80ecc05d6d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976652"
---
# <a name="environmentvariables-method-of-the-win32_tsexpandenvironmentvariables-class"></a><span data-ttu-id="37ed8-107">Win32 TSExpandEnvironmentVariables 類別的 EnvironmentVariables 方法 \_</span><span class="sxs-lookup"><span data-stu-id="37ed8-107">EnvironmentVariables method of the Win32\_TSExpandEnvironmentVariables class</span></span>

<span data-ttu-id="37ed8-108">展開系統定義的環境變數。</span><span class="sxs-lookup"><span data-stu-id="37ed8-108">Expands system-defined environment variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ed8-109">語法</span><span class="sxs-lookup"><span data-stu-id="37ed8-109">Syntax</span></span>


```mof
uint32 EnvironmentVariables(
  [in]  string OriginalString,
  [out] string ExpandedString
);
```



## <a name="parameters"></a><span data-ttu-id="37ed8-110">參數</span><span class="sxs-lookup"><span data-stu-id="37ed8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37ed8-111">*OriginalString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37ed8-111">*OriginalString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ed8-112">包含要展開之環境變數的字串。</span><span class="sxs-lookup"><span data-stu-id="37ed8-112">A string that contains the environment variables to expand.</span></span>

</dd> <dt>

<span data-ttu-id="37ed8-113">*ExpandedString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="37ed8-113">*ExpandedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37ed8-114">已展開環境變數的字串。</span><span class="sxs-lookup"><span data-stu-id="37ed8-114">A string with the environment variables expanded.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37ed8-115">備註</span><span class="sxs-lookup"><span data-stu-id="37ed8-115">Remarks</span></span>

<span data-ttu-id="37ed8-116">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="37ed8-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="37ed8-117">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="37ed8-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="37ed8-118">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="37ed8-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="37ed8-119">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="37ed8-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="37ed8-120">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="37ed8-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="37ed8-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="37ed8-121">Requirements</span></span>



| <span data-ttu-id="37ed8-122">需求</span><span class="sxs-lookup"><span data-stu-id="37ed8-122">Requirement</span></span> | <span data-ttu-id="37ed8-123">值</span><span class="sxs-lookup"><span data-stu-id="37ed8-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37ed8-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37ed8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="37ed8-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="37ed8-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="37ed8-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37ed8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="37ed8-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37ed8-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="37ed8-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="37ed8-128">Namespace</span></span><br/>                | <span data-ttu-id="37ed8-129">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="37ed8-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="37ed8-130">MOF</span><span class="sxs-lookup"><span data-stu-id="37ed8-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37ed8-131"><dt>Tsallow mof</dt></span><span class="sxs-lookup"><span data-stu-id="37ed8-131"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="37ed8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="37ed8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37ed8-133"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37ed8-133"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37ed8-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37ed8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37ed8-135">**Win32 \_ TSExpandEnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="37ed8-135">**Win32\_TSExpandEnvironmentVariables**</span></span>](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

