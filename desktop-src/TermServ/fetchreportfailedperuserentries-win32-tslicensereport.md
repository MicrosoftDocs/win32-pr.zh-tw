---
title: Win32_TSLicenseReport 類別的 FetchReportFailedPerUserEntries 方法
description: 取得 (RDS \ 160; 的每個使用者用戶端存取授權失敗遠端桌面服務詳細資料;報表) 的每個使用者 Cal。
ms.assetid: 2c16723c-1755-4ec1-a6db-55d769f8b6fd
ms.tgt_platform: multiple
keywords:
- FetchReportFailedPerUserEntries 方法遠端桌面服務
- FetchReportFailedPerUserEntries 方法遠端桌面服務，Win32_TSLicenseReport 類別
- Win32_TSLicenseReport 類別遠端桌面服務，FetchReportFailedPerUserEntries 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 159f980944c70dbad4c6948a614d0c9964a5f0cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509287"
---
# <a name="fetchreportfailedperuserentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="11add-106">Win32 TSLicenseReport 類別的 FetchReportFailedPerUserEntries 方法 \_</span><span class="sxs-lookup"><span data-stu-id="11add-106">FetchReportFailedPerUserEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="11add-107">抓取每個使用者用戶端存取授權的失敗遠端桌面服務詳細資料 (RDS 每個使用者的 Cal) 從報告。</span><span class="sxs-lookup"><span data-stu-id="11add-107">Retrieves details of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="11add-108">語法</span><span class="sxs-lookup"><span data-stu-id="11add-108">Syntax</span></span>


```mof
uint32 FetchReportFailedPerUserEntries(
  [in]      uint32                                  StartIndex,
  [in, out] uint32                                  Count,
  [out]     Win32_TSLicenseReportFailedPerUserEntry ReportFailedPerUserEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="11add-109">參數</span><span class="sxs-lookup"><span data-stu-id="11add-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11add-110">*StartIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="11add-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11add-111">要抓取之第一個報表專案的索引。</span><span class="sxs-lookup"><span data-stu-id="11add-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="11add-112">第一個報表專案的索引為零。</span><span class="sxs-lookup"><span data-stu-id="11add-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="11add-113">*計數* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="11add-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="11add-114">要從報表物件取出的報表專案數目。</span><span class="sxs-lookup"><span data-stu-id="11add-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="11add-115">值為零表示要抓取從 *StartIndex* 開始的所有報表專案。</span><span class="sxs-lookup"><span data-stu-id="11add-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="11add-116">傳回時，包含 *ReportFailedPerUserEntries* 陣列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="11add-116">On return, contains the number of entries in the *ReportFailedPerUserEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="11add-117">*ReportFailedPerUserEntries* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="11add-117">*ReportFailedPerUserEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11add-118">[**Win32 \_ TSLicenseReportFailedPerUserEntry**](win32-tslicensereportfailedperuserentry.md)類別的陣列，代表已取出的授權專案。</span><span class="sxs-lookup"><span data-stu-id="11add-118">An array of [**Win32\_TSLicenseReportFailedPerUserEntry**](win32-tslicensereportfailedperuserentry.md) classes that represent the license entries retrieved.</span></span> <span data-ttu-id="11add-119">*Count* 參數包含這個陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="11add-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11add-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="11add-120">Return value</span></span>

<span data-ttu-id="11add-121">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="11add-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="11add-122">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="11add-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="11add-123">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="11add-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11add-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="11add-124">Requirements</span></span>



| <span data-ttu-id="11add-125">需求</span><span class="sxs-lookup"><span data-stu-id="11add-125">Requirement</span></span> | <span data-ttu-id="11add-126">值</span><span class="sxs-lookup"><span data-stu-id="11add-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="11add-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11add-127">Minimum supported client</span></span><br/> | <span data-ttu-id="11add-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="11add-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="11add-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11add-129">Minimum supported server</span></span><br/> | <span data-ttu-id="11add-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11add-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="11add-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="11add-131">Namespace</span></span><br/>                | <span data-ttu-id="11add-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="11add-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="11add-133">MOF</span><span class="sxs-lookup"><span data-stu-id="11add-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11add-134"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="11add-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="11add-135">DLL</span><span class="sxs-lookup"><span data-stu-id="11add-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11add-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11add-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11add-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11add-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11add-138">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="11add-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 





