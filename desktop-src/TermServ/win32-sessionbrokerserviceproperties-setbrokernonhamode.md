---
title: Win32_SessionBrokerServiceProperties 類別的 SetBrokerNonHAMode 方法
description: 將資料從中央 SQL Server 遷移至本機資料庫。 它也會將訊息代理程式伺服器設定為使用本機資料庫。
ms.assetid: a73908be-0cc8-4512-842c-439d5cf18ed4
ms.tgt_platform: multiple
keywords:
- SetBrokerNonHAMode 方法遠端桌面服務
- SetBrokerNonHAMode 方法遠端桌面服務，Win32_SessionBrokerServiceProperties 類別
- Win32_SessionBrokerServiceProperties 類別遠端桌面服務，SetBrokerNonHAMode 方法
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerNonHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef811bf8024f8e89f9739461dfa8499891077f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966926"
---
# <a name="setbrokernonhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="37267-107">Win32 SessionBrokerServiceProperties 類別的 SetBrokerNonHAMode 方法 \_</span><span class="sxs-lookup"><span data-stu-id="37267-107">SetBrokerNonHAMode method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="37267-108">將資料從中央 SQL Server 遷移至本機資料庫。</span><span class="sxs-lookup"><span data-stu-id="37267-108">Migrates data from central SQL Server to a local database.</span></span> <span data-ttu-id="37267-109">它也會將訊息代理程式伺服器設定為使用本機資料庫。</span><span class="sxs-lookup"><span data-stu-id="37267-109">It also configures the broker server to use the local database.</span></span>

## <a name="syntax"></a><span data-ttu-id="37267-110">語法</span><span class="sxs-lookup"><span data-stu-id="37267-110">Syntax</span></span>


```mof
uint32 SetBrokerNonHAMode(
  [in] string connStringToCentralDBRdcms
);
```



## <a name="parameters"></a><span data-ttu-id="37267-111">參數</span><span class="sxs-lookup"><span data-stu-id="37267-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37267-112">*connStringToCentralDBRdcms* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37267-112">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37267-113">中央資料庫的連接字串。</span><span class="sxs-lookup"><span data-stu-id="37267-113">Connection string to the central database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37267-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="37267-114">Requirements</span></span>



| <span data-ttu-id="37267-115">需求</span><span class="sxs-lookup"><span data-stu-id="37267-115">Requirement</span></span> | <span data-ttu-id="37267-116">值</span><span class="sxs-lookup"><span data-stu-id="37267-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37267-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37267-117">Minimum supported client</span></span><br/> | <span data-ttu-id="37267-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="37267-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="37267-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37267-119">Minimum supported server</span></span><br/> | <span data-ttu-id="37267-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37267-120">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="37267-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="37267-121">Namespace</span></span><br/>                | <span data-ttu-id="37267-122">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="37267-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="37267-123">MOF</span><span class="sxs-lookup"><span data-stu-id="37267-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37267-124"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="37267-124"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="37267-125">DLL</span><span class="sxs-lookup"><span data-stu-id="37267-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37267-126"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37267-126"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37267-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37267-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37267-128">**Win32 \_ SessionBrokerServiceProperties**</span><span class="sxs-lookup"><span data-stu-id="37267-128">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





