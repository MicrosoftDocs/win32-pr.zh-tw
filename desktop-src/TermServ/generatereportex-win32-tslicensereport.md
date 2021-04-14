---
title: Win32_TSLicenseReport 類別的 GenerateReportEx 方法
description: 針對每位使用者和每一裝置授權產生目前的授權使用量報表。
ms.assetid: c454e0c5-ca1c-41c7-86b2-1e52c414aeb5
ms.tgt_platform: multiple
keywords:
- GenerateReportEx 方法遠端桌面服務
- GenerateReportEx 方法遠端桌面服務，Win32_TSLicenseReport 類別
- Win32_TSLicenseReport 類別遠端桌面服務，GenerateReportEx 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReportEx
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893e6e29d1e4716560b0f0f6b41e6109c89e2f5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384057"
---
# <a name="generatereportex-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="d02bb-106">Win32 TSLicenseReport 類別的 GenerateReportEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d02bb-106">GenerateReportEx method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="d02bb-107">針對每位使用者和每一裝置授權產生目前的授權使用量報表。</span><span class="sxs-lookup"><span data-stu-id="d02bb-107">Generates a current license usage report for both Per User and Per Device licenses.</span></span>

## <a name="syntax"></a><span data-ttu-id="d02bb-108">語法</span><span class="sxs-lookup"><span data-stu-id="d02bb-108">Syntax</span></span>


```mof
uint32 GenerateReportEx(
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="d02bb-109">參數</span><span class="sxs-lookup"><span data-stu-id="d02bb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d02bb-110">*檔案名* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d02bb-110">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d02bb-111">產生之報表的檔案名。</span><span class="sxs-lookup"><span data-stu-id="d02bb-111">The file name of the generated report.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d02bb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d02bb-112">Return value</span></span>

<span data-ttu-id="d02bb-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="d02bb-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d02bb-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="d02bb-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d02bb-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="d02bb-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d02bb-116">備註</span><span class="sxs-lookup"><span data-stu-id="d02bb-116">Remarks</span></span>

<span data-ttu-id="d02bb-117">此為靜態方法。</span><span class="sxs-lookup"><span data-stu-id="d02bb-117">This is a static method.</span></span>

<span data-ttu-id="d02bb-118">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="d02bb-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d02bb-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="d02bb-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d02bb-120">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="d02bb-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d02bb-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="d02bb-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d02bb-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="d02bb-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d02bb-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d02bb-123">Requirements</span></span>



| <span data-ttu-id="d02bb-124">需求</span><span class="sxs-lookup"><span data-stu-id="d02bb-124">Requirement</span></span> | <span data-ttu-id="d02bb-125">值</span><span class="sxs-lookup"><span data-stu-id="d02bb-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d02bb-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d02bb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d02bb-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="d02bb-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="d02bb-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d02bb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d02bb-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d02bb-129">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="d02bb-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="d02bb-130">Namespace</span></span><br/>                | <span data-ttu-id="d02bb-131">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="d02bb-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="d02bb-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d02bb-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d02bb-133"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="d02bb-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d02bb-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d02bb-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d02bb-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d02bb-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d02bb-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d02bb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d02bb-137">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="d02bb-137">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

