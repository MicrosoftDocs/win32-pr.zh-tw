---
title: Win32_SessionBrokerServiceProperties 類別的 DeleteSBDbConnectionString 方法
description: 從登錄中刪除主要或次要)  (的資料庫連接字串。
ms.assetid: 275dd790-bdc7-46d1-a07d-54ec6fa33e44
ms.tgt_platform: multiple
keywords:
- DeleteSBDbConnectionString 方法遠端桌面服務
- DeleteSBDbConnectionString 方法遠端桌面服務，Win32_SessionBrokerServiceProperties 類別
- Win32_SessionBrokerServiceProperties 類別遠端桌面服務，DeleteSBDbConnectionString 方法
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.DeleteSBDbConnectionString
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a9701afebe150f0c8dc0e4bf437dd23586c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965084"
---
# <a name="deletesbdbconnectionstring-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="13c9b-106">Win32 SessionBrokerServiceProperties 類別的 DeleteSBDbConnectionString 方法 \_</span><span class="sxs-lookup"><span data-stu-id="13c9b-106">DeleteSBDbConnectionString method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="13c9b-107">從登錄中刪除主要或次要)  (的資料庫連接字串。</span><span class="sxs-lookup"><span data-stu-id="13c9b-107">Deletes DB connection strings (primary or secondary) from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="13c9b-108">語法</span><span class="sxs-lookup"><span data-stu-id="13c9b-108">Syntax</span></span>


```mof
uint32 DeleteSBDbConnectionString(
  [in] boolean IsSecondaryConnString
);
```



## <a name="parameters"></a><span data-ttu-id="13c9b-109">參數</span><span class="sxs-lookup"><span data-stu-id="13c9b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13c9b-110">*IsSecondaryConnString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13c9b-110">*IsSecondaryConnString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13c9b-111">若 **為 True**，則會移除次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="13c9b-111">If **True**, secondary connection string is removed.</span></span> <span data-ttu-id="13c9b-112">如果 **為 False**，則會移除主要連接字串。</span><span class="sxs-lookup"><span data-stu-id="13c9b-112">If **False**, primary connection string is removed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13c9b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="13c9b-113">Requirements</span></span>



| <span data-ttu-id="13c9b-114">需求</span><span class="sxs-lookup"><span data-stu-id="13c9b-114">Requirement</span></span> | <span data-ttu-id="13c9b-115">值</span><span class="sxs-lookup"><span data-stu-id="13c9b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13c9b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13c9b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="13c9b-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="13c9b-117">None supported</span></span><br/>                                                              |
| <span data-ttu-id="13c9b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13c9b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="13c9b-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="13c9b-119">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="13c9b-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="13c9b-120">Namespace</span></span><br/>                | <span data-ttu-id="13c9b-121">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="13c9b-121">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="13c9b-122">MOF</span><span class="sxs-lookup"><span data-stu-id="13c9b-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13c9b-123"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="13c9b-123"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="13c9b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="13c9b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13c9b-125"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13c9b-125"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13c9b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13c9b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c9b-127">**Win32 \_ SessionBrokerServiceProperties**</span><span class="sxs-lookup"><span data-stu-id="13c9b-127">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





