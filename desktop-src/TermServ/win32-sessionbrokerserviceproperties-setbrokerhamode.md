---
title: Win32_SessionBrokerServiceProperties 類別的 SetBrokerHAMode 方法
description: 將資料從本機 WID 資料庫移轉至新的 SQL server 資料庫。 它也會將訊息代理程式伺服器設定為使用中央 SQL server。
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- SetBrokerHAMode 方法遠端桌面服務
- SetBrokerHAMode 方法遠端桌面服務，Win32_SessionBrokerServiceProperties 類別
- Win32_SessionBrokerServiceProperties 類別遠端桌面服務，SetBrokerHAMode 方法
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4526f8ded96086ccf223b3c8e5aad72d9e0262cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103673"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="633a5-107">Win32 SessionBrokerServiceProperties 類別的 SetBrokerHAMode 方法 \_</span><span class="sxs-lookup"><span data-stu-id="633a5-107">SetBrokerHAMode method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="633a5-108">將資料從本機 WID 資料庫移轉至新的 SQL server 資料庫。</span><span class="sxs-lookup"><span data-stu-id="633a5-108">Migrates data from a local WID database to the new SQL server-based database.</span></span> <span data-ttu-id="633a5-109">它也會將訊息代理程式伺服器設定為使用中央 SQL server。</span><span class="sxs-lookup"><span data-stu-id="633a5-109">It also configures the broker server to use the central SQL server.</span></span>

## <a name="syntax"></a><span data-ttu-id="633a5-110">語法</span><span class="sxs-lookup"><span data-stu-id="633a5-110">Syntax</span></span>


```mof
uint32 SetBrokerHAMode(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms,
  [in] string brokerDnsRRName,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a><span data-ttu-id="633a5-111">參數</span><span class="sxs-lookup"><span data-stu-id="633a5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="633a5-112">*connStringToCentralDBRdcms* \[在\]</span><span class="sxs-lookup"><span data-stu-id="633a5-112">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633a5-113">中央資料庫的連接字串。</span><span class="sxs-lookup"><span data-stu-id="633a5-113">Connection string to the central database.</span></span>

</dd> <dt>

<span data-ttu-id="633a5-114">*secondaryConnStringToCentralDBRdcms* \[在\]</span><span class="sxs-lookup"><span data-stu-id="633a5-114">*secondaryConnStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633a5-115">中央資料庫的次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="633a5-115">Secondary connection string to the central database.</span></span>

<span data-ttu-id="633a5-116">**Windows server 2012 R2 和 Windows server 2012：** 此參數在 Windows Server 2016 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="633a5-116">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="633a5-117">*brokerDnsRRName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="633a5-117">*brokerDnsRRName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633a5-118">訊息代理程式 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="633a5-118">Broker DNS name.</span></span>

</dd> <dt>

<span data-ttu-id="633a5-119">*activeBrokerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="633a5-119">*activeBrokerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633a5-120">Active broker 名稱。</span><span class="sxs-lookup"><span data-stu-id="633a5-120">Active broker name.</span></span>

<span data-ttu-id="633a5-121">**Windows server 2012 R2 和 Windows server 2012：** 此參數在 Windows Server 2016 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="633a5-121">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="633a5-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="633a5-122">Requirements</span></span>



| <span data-ttu-id="633a5-123">需求</span><span class="sxs-lookup"><span data-stu-id="633a5-123">Requirement</span></span> | <span data-ttu-id="633a5-124">值</span><span class="sxs-lookup"><span data-stu-id="633a5-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="633a5-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="633a5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="633a5-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="633a5-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="633a5-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="633a5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="633a5-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="633a5-128">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="633a5-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="633a5-129">Namespace</span></span><br/>                | <span data-ttu-id="633a5-130">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="633a5-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="633a5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="633a5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="633a5-132"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="633a5-132"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="633a5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="633a5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="633a5-134"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="633a5-134"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="633a5-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="633a5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633a5-136">**Win32 \_ SessionBrokerServiceProperties**</span><span class="sxs-lookup"><span data-stu-id="633a5-136">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





