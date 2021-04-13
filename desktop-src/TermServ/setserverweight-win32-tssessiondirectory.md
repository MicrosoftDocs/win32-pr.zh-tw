---
title: Win32_TSSessionDirectory 類別的 SetServerWeight 方法
description: 設定遠端桌面連線代理人 (RD 連線代理人) 負載平衡的伺服器加權值。
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- SetServerWeight 方法遠端桌面服務
- SetServerWeight 方法遠端桌面服務，Win32_TSSessionDirectory 類別
- Win32_TSSessionDirectory 類別遠端桌面服務，SetServerWeight 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetServerWeight
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e8456fa590de0c9d6236f96f3b09c16087d730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465973"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="e9548-106">Win32 TSSessionDirectory 類別的 SetServerWeight 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e9548-106">SetServerWeight method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="e9548-107">設定遠端桌面連線代理人 (RD 連線代理人) 負載平衡的伺服器加權值。</span><span class="sxs-lookup"><span data-stu-id="e9548-107">Sets the server weight value for Remote Desktop Connection Broker (RD Connection Broker) load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9548-108">語法</span><span class="sxs-lookup"><span data-stu-id="e9548-108">Syntax</span></span>


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a><span data-ttu-id="e9548-109">參數</span><span class="sxs-lookup"><span data-stu-id="e9548-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9548-110">*ServerWeightValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9548-110">*ServerWeightValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9548-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e9548-111">Type: **uint32**</span></span>

<span data-ttu-id="e9548-112">伺服器加權值。</span><span class="sxs-lookup"><span data-stu-id="e9548-112">The server weight value.</span></span> <span data-ttu-id="e9548-113">有效範圍是1至10000。</span><span class="sxs-lookup"><span data-stu-id="e9548-113">The valid range is 1 to 10000.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9548-114">備註</span><span class="sxs-lookup"><span data-stu-id="e9548-114">Remarks</span></span>

<span data-ttu-id="e9548-115">依預設，在遠端桌面服務設定的使用者介面中，伺服器權數值是100。</span><span class="sxs-lookup"><span data-stu-id="e9548-115">By default in the user interface of Remote Desktop Services Configuration, the server weight value is 100.</span></span> <span data-ttu-id="e9548-116">伺服器權數是相對的。</span><span class="sxs-lookup"><span data-stu-id="e9548-116">The server weight is relative.</span></span> <span data-ttu-id="e9548-117">因此，如果您為一部伺服器指派的值為100，而其中一個值為200，則相對權數為200的伺服器將會收到會話數目的兩倍。</span><span class="sxs-lookup"><span data-stu-id="e9548-117">Therefore, if you assign one server a value of 100, and one a value of 200, the server with a relative weight of 200 will receive twice the number of sessions.</span></span>

<span data-ttu-id="e9548-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="e9548-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e9548-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e9548-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e9548-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="e9548-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e9548-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="e9548-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9548-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9548-122">Requirements</span></span>



| <span data-ttu-id="e9548-123">需求</span><span class="sxs-lookup"><span data-stu-id="e9548-123">Requirement</span></span> | <span data-ttu-id="e9548-124">值</span><span class="sxs-lookup"><span data-stu-id="e9548-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9548-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9548-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e9548-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="e9548-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e9548-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9548-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e9548-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9548-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9548-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="e9548-129">Namespace</span></span><br/>                | <span data-ttu-id="e9548-130">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="e9548-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e9548-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e9548-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9548-132"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9548-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9548-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e9548-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9548-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9548-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9548-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9548-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9548-136">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="e9548-136">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

