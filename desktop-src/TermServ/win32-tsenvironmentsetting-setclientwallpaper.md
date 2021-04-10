---
title: Win32_TSEnvironmentSetting 類別的 SetClientWallPaper 方法
description: SetClientWallPaper 方法會設定 ClientWallPaper 屬性。
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- SetClientWallPaper 方法遠端桌面服務
- SetClientWallPaper 方法遠端桌面服務，Win32_TSEnvironmentSetting 類別
- Win32_TSEnvironmentSetting 類別遠端桌面服務，SetClientWallPaper 方法
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.SetClientWallPaper
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ae476134cf526602a059b4714cded6fd6c990e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685847"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a><span data-ttu-id="0473b-106">Win32 TSEnvironmentSetting 類別的 SetClientWallPaper 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0473b-106">SetClientWallPaper method of the Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="0473b-107">**SetClientWallPaper** 方法會設定 **ClientWallPaper** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0473b-107">The **SetClientWallPaper** method sets the **ClientWallPaper** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0473b-108">語法</span><span class="sxs-lookup"><span data-stu-id="0473b-108">Syntax</span></span>


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a><span data-ttu-id="0473b-109">參數</span><span class="sxs-lookup"><span data-stu-id="0473b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0473b-110">*ClientWallPaper* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0473b-110">*ClientWallPaper* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0473b-111">旗標停用或啟用 **ClientWallPaper** 屬性，指定用戶端上是否顯示背景 (或壁紙) 影像。</span><span class="sxs-lookup"><span data-stu-id="0473b-111">Flag disabling or enabling the **ClientWallPaper** property, which specifies whether the background (or wallpaper) image is displayed on the client.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="0473b-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="0473b-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="0473b-113">用戶端上不會顯示背景 (或壁紙) 影像。</span><span class="sxs-lookup"><span data-stu-id="0473b-113">The background (or wallpaper) image is not displayed on the client.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="0473b-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="0473b-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="0473b-115">背景 (或壁紙) 影像會顯示在用戶端上。</span><span class="sxs-lookup"><span data-stu-id="0473b-115">The background (or wallpaper) image is displayed on the client.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0473b-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="0473b-116">Return value</span></span>

<span data-ttu-id="0473b-117">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0473b-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0473b-118">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="0473b-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="0473b-119">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0473b-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="0473b-120">備註</span><span class="sxs-lookup"><span data-stu-id="0473b-120">Remarks</span></span>

<span data-ttu-id="0473b-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="0473b-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0473b-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="0473b-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0473b-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="0473b-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0473b-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="0473b-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0473b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="0473b-125">Requirements</span></span>



| <span data-ttu-id="0473b-126">需求</span><span class="sxs-lookup"><span data-stu-id="0473b-126">Requirement</span></span> | <span data-ttu-id="0473b-127">值</span><span class="sxs-lookup"><span data-stu-id="0473b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0473b-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0473b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0473b-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0473b-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0473b-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0473b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0473b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0473b-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0473b-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="0473b-132">Namespace</span></span><br/>                | <span data-ttu-id="0473b-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="0473b-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0473b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="0473b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0473b-135"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="0473b-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0473b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0473b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0473b-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0473b-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0473b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0473b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0473b-139">**Win32 \_ TSEnvironmentSetting**</span><span class="sxs-lookup"><span data-stu-id="0473b-139">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> </dl>

 

