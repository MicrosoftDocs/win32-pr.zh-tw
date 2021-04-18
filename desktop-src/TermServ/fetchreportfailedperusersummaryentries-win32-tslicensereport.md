---
title: Win32_TSLicenseReport 類別的 FetchReportFailedPerUserSummaryEntries 方法
description: 取得失敗遠端桌面服務每個使用者用戶端存取授權 (RDS \ 160; 的摘要資訊。報表) 的每個使用者 Cal。
ms.assetid: dc9c4a36-b2a8-407e-b902-ee9d51227909
ms.tgt_platform: multiple
keywords:
- FetchReportFailedPerUserSummaryEntries 方法遠端桌面服務
- FetchReportFailedPerUserSummaryEntries 方法遠端桌面服務，Win32_TSLicenseReport 類別
- Win32_TSLicenseReport 類別遠端桌面服務，FetchReportFailedPerUserSummaryEntries 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5219c2c854e04dabf8b5bfe0b5b70a07bbc3c57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106983318"
---
# <a name="fetchreportfailedperusersummaryentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="c5ff0-106">Win32 TSLicenseReport 類別的 FetchReportFailedPerUserSummaryEntries 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c5ff0-106">FetchReportFailedPerUserSummaryEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="c5ff0-107">抓取每個使用者用戶端存取授權的失敗遠端桌面服務摘要資訊， (RDS 每個使用者的 Cal) 從報告。</span><span class="sxs-lookup"><span data-stu-id="c5ff0-107">Retrieves summary information of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ff0-108">語法</span><span class="sxs-lookup"><span data-stu-id="c5ff0-108">Syntax</span></span>


```mof
uint32 FetchReportFailedPerUserSummaryEntries(
  [in]      uint32                                         StartIndex,
  [in, out] uint32                                         Count,
  [out]     Win32_TSLicenseReportFailedPerUserSummaryEntry ReportFailedPerUserSummaryEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="c5ff0-109">參數</span><span class="sxs-lookup"><span data-stu-id="c5ff0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ff0-110">*StartIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5ff0-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ff0-111">要抓取之第一個報表專案的索引。</span><span class="sxs-lookup"><span data-stu-id="c5ff0-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="c5ff0-112">第一個報表專案的索引為零。</span><span class="sxs-lookup"><span data-stu-id="c5ff0-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="c5ff0-113">*計數* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c5ff0-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ff0-114">要從報表物件取出的報表專案數目。</span><span class="sxs-lookup"><span data-stu-id="c5ff0-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="c5ff0-115">值為零表示要抓取從 *StartIndex* 開始的所有報表專案。</span><span class="sxs-lookup"><span data-stu-id="c5ff0-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="c5ff0-116">傳回時，包含 *ReportFailedPerUserSummaryEntries* 陣列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="c5ff0-116">On return, contains the number of entries in the *ReportFailedPerUserSummaryEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="c5ff0-117">*ReportFailedPerUserSummaryEntries* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c5ff0-117">*ReportFailedPerUserSummaryEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ff0-118">[**Win32 \_ TSLicenseReportFailedPerUserSummaryEntry**](win32-tslicensereportfailedperusersummaryentry.md)類別的陣列，代表已取出的授權專案。</span><span class="sxs-lookup"><span data-stu-id="c5ff0-118">An array of [**Win32\_TSLicenseReportFailedPerUserSummaryEntry**](win32-tslicensereportfailedperusersummaryentry.md) classes that represent the license entries retrieved.</span></span> <span data-ttu-id="c5ff0-119">*Count* 參數包含這個陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="c5ff0-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ff0-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5ff0-120">Return value</span></span>

<span data-ttu-id="c5ff0-121">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="c5ff0-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c5ff0-122">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="c5ff0-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c5ff0-123">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="c5ff0-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ff0-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5ff0-124">Requirements</span></span>



| <span data-ttu-id="c5ff0-125">需求</span><span class="sxs-lookup"><span data-stu-id="c5ff0-125">Requirement</span></span> | <span data-ttu-id="c5ff0-126">值</span><span class="sxs-lookup"><span data-stu-id="c5ff0-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ff0-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5ff0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ff0-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="c5ff0-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c5ff0-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5ff0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ff0-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c5ff0-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="c5ff0-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="c5ff0-131">Namespace</span></span><br/>                | <span data-ttu-id="c5ff0-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c5ff0-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="c5ff0-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c5ff0-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5ff0-134"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5ff0-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5ff0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c5ff0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5ff0-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5ff0-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ff0-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5ff0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ff0-138">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="c5ff0-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 





