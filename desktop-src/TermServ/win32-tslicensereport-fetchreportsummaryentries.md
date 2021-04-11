---
title: Win32_TSLicenseReport 類別的 FetchReportSummaryEntries 方法
description: 抓取遠端桌面服務的每個使用者用戶端存取授權摘要 (RDS \ 160;報表) 的每個使用者 Cal。
ms.assetid: 0312B787-83E9-42FC-B21B-904B804C5C94
ms.tgt_platform: multiple
keywords:
- FetchReportSummaryEntries 方法遠端桌面服務
- FetchReportSummaryEntries 方法遠端桌面服務，Win32_TSLicenseReport 類別
- Win32_TSLicenseReport 類別遠端桌面服務，FetchReportSummaryEntries 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e47100c71e195cacb6a1004975955eae778765a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093959"
---
# <a name="fetchreportsummaryentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="6ead1-106">Win32 TSLicenseReport 類別的 FetchReportSummaryEntries 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6ead1-106">FetchReportSummaryEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="6ead1-107">從報告 (RDS 每個使用者的 Cal) 取得遠端桌面服務的每個使用者用戶端存取授權摘要。</span><span class="sxs-lookup"><span data-stu-id="6ead1-107">Retrieves summaries of Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ead1-108">語法</span><span class="sxs-lookup"><span data-stu-id="6ead1-108">Syntax</span></span>


```mof
uint32 FetchReportSummaryEntries(
  [in]      uint32                            StartIndex,
  [in, out] uint32                            Count,
  [out]     Win32_TSLicenseReportSummaryEntry ReportSummaryEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="6ead1-109">參數</span><span class="sxs-lookup"><span data-stu-id="6ead1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ead1-110">*StartIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ead1-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ead1-111">要接收之第一個報表專案的索引。</span><span class="sxs-lookup"><span data-stu-id="6ead1-111">Index of the first report entry to be received.</span></span> <span data-ttu-id="6ead1-112">第一個報表專案的索引為零。</span><span class="sxs-lookup"><span data-stu-id="6ead1-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="6ead1-113">*計數* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="6ead1-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ead1-114">要從報表物件取出的報表專案數目。</span><span class="sxs-lookup"><span data-stu-id="6ead1-114">Number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="6ead1-115">值為零表示要抓取從 *StartIndex* 開始的所有報表專案。</span><span class="sxs-lookup"><span data-stu-id="6ead1-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="6ead1-116">傳回時，包含 *ReportSummaryEntries* 陣列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="6ead1-116">On return, contains the number of entries in the *ReportSummaryEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="6ead1-117">*ReportSummaryEntries* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6ead1-117">*ReportSummaryEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ead1-118">傳回 [**Win32 \_ TSLicenseReportSummaryEntry**](win32-tslicensereportsummaryentry.md) 類別的陣列。</span><span class="sxs-lookup"><span data-stu-id="6ead1-118">Returns an array of [**Win32\_TSLicenseReportSummaryEntry**](win32-tslicensereportsummaryentry.md) classes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ead1-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ead1-119">Return value</span></span>

<span data-ttu-id="6ead1-120">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="6ead1-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6ead1-121">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="6ead1-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6ead1-122">值為 **LSERVER \_ 我 \_ 沒有 \_ 其他 \_ 資料** (0x4001) 指出沒有其他報表專案。</span><span class="sxs-lookup"><span data-stu-id="6ead1-122">A value of **LSERVER\_I\_NO\_MORE\_DATA** (0x4001) indicates that there are no more report entries.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ead1-123">備註</span><span class="sxs-lookup"><span data-stu-id="6ead1-123">Remarks</span></span>

<span data-ttu-id="6ead1-124">這不是靜態方法。</span><span class="sxs-lookup"><span data-stu-id="6ead1-124">This is not a static method.</span></span> <span data-ttu-id="6ead1-125">您必須從每個使用者授權使用量報表物件呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="6ead1-125">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="6ead1-126">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="6ead1-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6ead1-127">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="6ead1-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6ead1-128">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6ead1-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6ead1-129">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="6ead1-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6ead1-130">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="6ead1-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ead1-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ead1-131">Requirements</span></span>



| <span data-ttu-id="6ead1-132">需求</span><span class="sxs-lookup"><span data-stu-id="6ead1-132">Requirement</span></span> | <span data-ttu-id="6ead1-133">值</span><span class="sxs-lookup"><span data-stu-id="6ead1-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ead1-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ead1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6ead1-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="6ead1-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="6ead1-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ead1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6ead1-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ead1-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="6ead1-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="6ead1-138">Namespace</span></span><br/>                | <span data-ttu-id="6ead1-139">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="6ead1-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="6ead1-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6ead1-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ead1-141"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ead1-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ead1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6ead1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ead1-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ead1-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ead1-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ead1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ead1-145">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="6ead1-145">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="6ead1-146">**Win32 \_ TSLicenseReportSummaryEntry**</span><span class="sxs-lookup"><span data-stu-id="6ead1-146">**Win32\_TSLicenseReportSummaryEntry**</span></span>](win32-tslicensereportsummaryentry.md)
</dt> </dl>

 

