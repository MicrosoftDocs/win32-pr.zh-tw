---
title: Win32_SessionBrokerServiceProperties 類別的 IsDbReachable 方法
description: 檢查資料庫是否可連線。
ms.assetid: c9774d6d-1b78-4ec1-bae2-80d41d4c9b06
ms.tgt_platform: multiple
keywords:
- IsDbReachable 方法遠端桌面服務
- IsDbReachable 方法遠端桌面服務，Win32_SessionBrokerServiceProperties 類別
- Win32_SessionBrokerServiceProperties 類別遠端桌面服務，IsDbReachable 方法
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.IsDbReachable
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a59b8b0eba80dd832b3967b5e626642684f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465289"
---
# <a name="isdbreachable-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="61259-106">Win32 SessionBrokerServiceProperties 類別的 IsDbReachable 方法 \_</span><span class="sxs-lookup"><span data-stu-id="61259-106">IsDbReachable method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="61259-107">檢查資料庫是否可連線。</span><span class="sxs-lookup"><span data-stu-id="61259-107">Checks if the database is reachable.</span></span>

## <a name="syntax"></a><span data-ttu-id="61259-108">語法</span><span class="sxs-lookup"><span data-stu-id="61259-108">Syntax</span></span>


```mof
uint32 IsDbReachable(
  [in] string connStringToDb,
  [in] string connSecondaryStringToDb,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a><span data-ttu-id="61259-109">參數</span><span class="sxs-lookup"><span data-stu-id="61259-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61259-110">*connStringToDb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61259-110">*connStringToDb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61259-111">資料庫的連接字串。</span><span class="sxs-lookup"><span data-stu-id="61259-111">The connection string to the database.</span></span>

</dd> <dt>

<span data-ttu-id="61259-112">*connSecondaryStringToDb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61259-112">*connSecondaryStringToDb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61259-113">中央資料庫的次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="61259-113">Secondary connection string to the central database.</span></span>

<span data-ttu-id="61259-114">**Windows server 2012 R2 和 Windows server 2012：** 此參數在 Windows Server 2016 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="61259-114">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="61259-115">*activeBrokerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61259-115">*activeBrokerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61259-116">Active broker 名稱。</span><span class="sxs-lookup"><span data-stu-id="61259-116">Active broker name.</span></span>

<span data-ttu-id="61259-117">**Windows server 2012 R2 和 Windows server 2012：** 此參數在 Windows Server 2016 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="61259-117">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61259-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="61259-118">Requirements</span></span>



| <span data-ttu-id="61259-119">需求</span><span class="sxs-lookup"><span data-stu-id="61259-119">Requirement</span></span> | <span data-ttu-id="61259-120">值</span><span class="sxs-lookup"><span data-stu-id="61259-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="61259-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61259-121">Minimum supported client</span></span><br/> | <span data-ttu-id="61259-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="61259-122">None supported</span></span><br/>                                                              |
| <span data-ttu-id="61259-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61259-123">Minimum supported server</span></span><br/> | <span data-ttu-id="61259-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61259-124">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="61259-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="61259-125">Namespace</span></span><br/>                | <span data-ttu-id="61259-126">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="61259-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="61259-127">MOF</span><span class="sxs-lookup"><span data-stu-id="61259-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61259-128"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="61259-128"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="61259-129">DLL</span><span class="sxs-lookup"><span data-stu-id="61259-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61259-130"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61259-130"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61259-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61259-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61259-132">**Win32 \_ SessionBrokerServiceProperties**</span><span class="sxs-lookup"><span data-stu-id="61259-132">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





