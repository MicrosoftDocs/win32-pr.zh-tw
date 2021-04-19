---
title: Win32_TSLicenseReport 類別的 FetchReportPerDeviceEntries 方法
description: 取得 (RDS \ 160; 的每一裝置用戶端存取授權發出遠端桌面服務的資訊。報表) 的每一裝置 Cal。
ms.assetid: 3f632a65-d6e0-4efd-9498-d04a05f9ddec
ms.tgt_platform: multiple
keywords:
- FetchReportPerDeviceEntries 方法遠端桌面服務
- FetchReportPerDeviceEntries 方法遠端桌面服務，Win32_TSLicenseReport 類別
- Win32_TSLicenseReport 類別遠端桌面服務，FetchReportPerDeviceEntries 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportPerDeviceEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce77fce941dd0a24fb6ee17e0aeb67b4e78bdae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969819"
---
# <a name="fetchreportperdeviceentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="e49a9-106">Win32 TSLicenseReport 類別的 FetchReportPerDeviceEntries 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e49a9-106">FetchReportPerDeviceEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="e49a9-107">從報告取得 (RDS 每一裝置的 Cal) 的每一裝置用戶端存取授權發出遠端桌面服務的資訊。</span><span class="sxs-lookup"><span data-stu-id="e49a9-107">Retrieves information of issued Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="e49a9-108">語法</span><span class="sxs-lookup"><span data-stu-id="e49a9-108">Syntax</span></span>


```mof
uint32 FetchReportPerDeviceEntries(
  [in]      uint32                              StartIndex,
  [in, out] uint32                              Count,
  [out]     Win32_TSLicenseReportPerDeviceEntry ReportPerDeviceEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="e49a9-109">參數</span><span class="sxs-lookup"><span data-stu-id="e49a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e49a9-110">*StartIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e49a9-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e49a9-111">要抓取之第一個報表專案的索引。</span><span class="sxs-lookup"><span data-stu-id="e49a9-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="e49a9-112">第一個報表專案的索引為零。</span><span class="sxs-lookup"><span data-stu-id="e49a9-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="e49a9-113">*計數* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="e49a9-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e49a9-114">要從報表物件取出的報表專案數目。</span><span class="sxs-lookup"><span data-stu-id="e49a9-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="e49a9-115">值為零表示要抓取從 *StartIndex* 開始的所有報表專案。</span><span class="sxs-lookup"><span data-stu-id="e49a9-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="e49a9-116">傳回時，包含 *ReportPerDeviceEntries* 陣列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="e49a9-116">On return, contains the number of entries in the *ReportPerDeviceEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="e49a9-117">*ReportPerDeviceEntries* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e49a9-117">*ReportPerDeviceEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e49a9-118">[**Win32 \_ TSLicenseReportPerDeviceEntry**](win32-tslicensereportperdeviceentry.md)類別的陣列，代表已取出的授權專案。</span><span class="sxs-lookup"><span data-stu-id="e49a9-118">An array of [**Win32\_TSLicenseReportPerDeviceEntry**](win32-tslicensereportperdeviceentry.md) classes the represent the license entries retrieved.</span></span> <span data-ttu-id="e49a9-119">*Count* 參數包含這個陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="e49a9-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e49a9-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="e49a9-120">Return value</span></span>

<span data-ttu-id="e49a9-121">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="e49a9-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e49a9-122">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="e49a9-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e49a9-123">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="e49a9-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e49a9-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e49a9-124">Requirements</span></span>



| <span data-ttu-id="e49a9-125">需求</span><span class="sxs-lookup"><span data-stu-id="e49a9-125">Requirement</span></span> | <span data-ttu-id="e49a9-126">值</span><span class="sxs-lookup"><span data-stu-id="e49a9-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e49a9-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e49a9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e49a9-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="e49a9-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e49a9-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e49a9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e49a9-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e49a9-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="e49a9-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="e49a9-131">Namespace</span></span><br/>                | <span data-ttu-id="e49a9-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e49a9-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e49a9-133">MOF</span><span class="sxs-lookup"><span data-stu-id="e49a9-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e49a9-134"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="e49a9-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e49a9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e49a9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e49a9-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e49a9-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e49a9-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e49a9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e49a9-138">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="e49a9-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 





