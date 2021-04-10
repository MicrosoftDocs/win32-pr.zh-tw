---
title: Win32_TSLicenseReportFailedPerUserSummaryEntry 類別
description: 提供每個使用者發行失敗的網域詳細資料。
ms.assetid: f7265734-ac4d-439f-ae8b-3694e6f81f2a
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportFailedPerUserSummaryEntry 類別遠端桌面服務
- Win32_TSLicenseReportFailedPerUserSummaryEntry 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserSummaryEntry
- Win32_TSLicenseReportFailedPerUserSummaryEntry.DomainName
- Win32_TSLicenseReportFailedPerUserSummaryEntry.FailedIssuanceCount
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f086d275c064f5df18ee01a3a38639a40913f3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933975"
---
# <a name="win32_tslicensereportfailedperusersummaryentry-class"></a><span data-ttu-id="538ea-105">Win32 \_ TSLicenseReportFailedPerUserSummaryEntry 類別</span><span class="sxs-lookup"><span data-stu-id="538ea-105">Win32\_TSLicenseReportFailedPerUserSummaryEntry class</span></span>

<span data-ttu-id="538ea-106">提供每個使用者發行失敗的網域詳細資料。</span><span class="sxs-lookup"><span data-stu-id="538ea-106">Provides details of the domains to which Per User Issuance was failed.</span></span>

<span data-ttu-id="538ea-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="538ea-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="538ea-108">語法</span><span class="sxs-lookup"><span data-stu-id="538ea-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserSummaryEntry
{
  string DomainName;
  uint32 FailedIssuanceCount;
};
```

## <a name="members"></a><span data-ttu-id="538ea-109">成員</span><span class="sxs-lookup"><span data-stu-id="538ea-109">Members</span></span>

<span data-ttu-id="538ea-110">**Win32 \_ TSLicenseReportFailedPerUserSummaryEntry** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="538ea-110">The **Win32\_TSLicenseReportFailedPerUserSummaryEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="538ea-111">屬性</span><span class="sxs-lookup"><span data-stu-id="538ea-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="538ea-112">屬性</span><span class="sxs-lookup"><span data-stu-id="538ea-112">Properties</span></span>

<span data-ttu-id="538ea-113">**Win32 \_ TSLicenseReportFailedPerUserSummaryEntry** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="538ea-113">The **Win32\_TSLicenseReportFailedPerUserSummaryEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="538ea-114">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="538ea-114">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="538ea-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="538ea-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="538ea-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="538ea-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="538ea-117">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="538ea-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="538ea-118">指定授權發行失敗的網功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="538ea-118">Specifies the domain name to which the license issuance failed.</span></span>

</dd> <dt>

<span data-ttu-id="538ea-119">**FailedIssuanceCount**</span><span class="sxs-lookup"><span data-stu-id="538ea-119">**FailedIssuanceCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="538ea-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="538ea-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="538ea-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="538ea-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="538ea-122">失敗的 issuances 數目。</span><span class="sxs-lookup"><span data-stu-id="538ea-122">The number of failed issuances.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="538ea-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="538ea-123">Requirements</span></span>



| <span data-ttu-id="538ea-124">需求</span><span class="sxs-lookup"><span data-stu-id="538ea-124">Requirement</span></span> | <span data-ttu-id="538ea-125">值</span><span class="sxs-lookup"><span data-stu-id="538ea-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="538ea-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="538ea-126">Minimum supported client</span></span><br/> | <span data-ttu-id="538ea-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="538ea-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="538ea-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="538ea-128">Minimum supported server</span></span><br/> | <span data-ttu-id="538ea-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="538ea-129">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="538ea-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="538ea-130">Namespace</span></span><br/>                | <span data-ttu-id="538ea-131">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="538ea-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="538ea-132">MOF</span><span class="sxs-lookup"><span data-stu-id="538ea-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="538ea-133"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="538ea-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="538ea-134">DLL</span><span class="sxs-lookup"><span data-stu-id="538ea-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="538ea-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="538ea-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="538ea-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="538ea-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="538ea-137">**FetchReportFailedPerUserSummaryEntries**</span><span class="sxs-lookup"><span data-stu-id="538ea-137">**FetchReportFailedPerUserSummaryEntries**</span></span>](fetchreportfailedperusersummaryentries-win32-tslicensereport.md)
</dt> </dl>

 

