---
title: Win32_TerminalServiceSetting 類別的 GetTSLanaIds 方法
description: 取得 NetBIOS 局域網路介面卡 (LANA) 識別碼和遠端桌面服務網路介面卡的描述。
ms.assetid: 3f42e5da-c52b-4500-8cd0-52088dca544a
ms.tgt_platform: multiple
keywords:
- GetTSLanaIds 方法遠端桌面服務
- GetTSLanaIds 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，GetTSLanaIds 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTSLanaIds
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a66d2b2357df7e6d7ccc2cb8a774ba34c50cb46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467036"
---
# <a name="gettslanaids-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="b566c-106">Win32 TerminalServiceSetting 類別的 GetTSLanaIds 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b566c-106">GetTSLanaIds method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="b566c-107">**GetTSLanaIds** 方法會取得 NetBIOS 局域網路介面卡 (LANA) 識別碼和遠端桌面服務網路介面卡的描述。</span><span class="sxs-lookup"><span data-stu-id="b566c-107">The **GetTSLanaIds** method gets the NetBIOS Local Area Network Adapter (LANA) IDs and descriptions of Remote Desktop Services network adapters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b566c-108">語法</span><span class="sxs-lookup"><span data-stu-id="b566c-108">Syntax</span></span>


```mof
uint32 GetTSLanaIds(
  [out] uint32 LanaIdList[],
  [out] string LanaIdDescriptions[]
);
```



## <a name="parameters"></a><span data-ttu-id="b566c-109">參數</span><span class="sxs-lookup"><span data-stu-id="b566c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b566c-110">*LanaIdList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b566c-110">*LanaIdList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b566c-111">LANA 編號的陣列。</span><span class="sxs-lookup"><span data-stu-id="b566c-111">Array of LANA numbers.</span></span>

</dd> <dt>

<span data-ttu-id="b566c-112">*LanaIdDescriptions* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b566c-112">*LanaIdDescriptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b566c-113">對應于 *LanaIdList* 陣列的 LANA 描述陣列。</span><span class="sxs-lookup"><span data-stu-id="b566c-113">Array of LANA descriptions corresponding to the *LanaIdList* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b566c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b566c-114">Return value</span></span>

<span data-ttu-id="b566c-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b566c-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="b566c-116">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="b566c-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="b566c-117">備註</span><span class="sxs-lookup"><span data-stu-id="b566c-117">Remarks</span></span>

<span data-ttu-id="b566c-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="b566c-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b566c-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b566c-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b566c-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="b566c-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b566c-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="b566c-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b566c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="b566c-122">Requirements</span></span>



| <span data-ttu-id="b566c-123">需求</span><span class="sxs-lookup"><span data-stu-id="b566c-123">Requirement</span></span> | <span data-ttu-id="b566c-124">值</span><span class="sxs-lookup"><span data-stu-id="b566c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b566c-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b566c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b566c-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b566c-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b566c-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b566c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b566c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b566c-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b566c-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="b566c-129">Namespace</span></span><br/>                | <span data-ttu-id="b566c-130">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="b566c-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b566c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b566c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b566c-132"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="b566c-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b566c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b566c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b566c-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b566c-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b566c-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b566c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b566c-136">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="b566c-136">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

