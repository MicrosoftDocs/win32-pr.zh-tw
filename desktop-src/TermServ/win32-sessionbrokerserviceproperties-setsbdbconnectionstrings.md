---
title: Win32_SessionBrokerServiceProperties 類別的 SetSBDbConnectionStrings 方法
description: 將主要和次要資料庫的資料庫連接字串儲存在登錄中。
ms.assetid: a9a20eca-22d9-495c-b976-2952c97be67e
ms.tgt_platform: multiple
keywords:
- SetSBDbConnectionStrings 方法遠端桌面服務
- SetSBDbConnectionStrings 方法遠端桌面服務，Win32_SessionBrokerServiceProperties 類別
- Win32_SessionBrokerServiceProperties 類別遠端桌面服務，SetSBDbConnectionStrings 方法
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetSBDbConnectionStrings
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4aa02cabe89e434fb8b24b308bbe2ec51fa5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465288"
---
# <a name="setsbdbconnectionstrings-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="80565-106">Win32 SessionBrokerServiceProperties 類別的 SetSBDbConnectionStrings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="80565-106">SetSBDbConnectionStrings method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="80565-107">將主要和次要資料庫的資料庫連接字串儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="80565-107">Saves DB connection strings, both primary and secondary, in the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="80565-108">語法</span><span class="sxs-lookup"><span data-stu-id="80565-108">Syntax</span></span>


```mof
uint32 SetSBDbConnectionStrings(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms
);
```



## <a name="parameters"></a><span data-ttu-id="80565-109">參數</span><span class="sxs-lookup"><span data-stu-id="80565-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80565-110">*connStringToCentralDBRdcms* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80565-110">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80565-111">主要連接字串。</span><span class="sxs-lookup"><span data-stu-id="80565-111">The primary connection string.</span></span>

</dd> <dt>

<span data-ttu-id="80565-112">*secondaryConnStringToCentralDBRdcms* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80565-112">*secondaryConnStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80565-113">次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="80565-113">The secondary connection string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80565-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="80565-114">Requirements</span></span>



| <span data-ttu-id="80565-115">需求</span><span class="sxs-lookup"><span data-stu-id="80565-115">Requirement</span></span> | <span data-ttu-id="80565-116">值</span><span class="sxs-lookup"><span data-stu-id="80565-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80565-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80565-117">Minimum supported client</span></span><br/> | <span data-ttu-id="80565-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="80565-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="80565-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80565-119">Minimum supported server</span></span><br/> | <span data-ttu-id="80565-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="80565-120">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="80565-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="80565-121">Namespace</span></span><br/>                | <span data-ttu-id="80565-122">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="80565-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="80565-123">MOF</span><span class="sxs-lookup"><span data-stu-id="80565-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80565-124"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="80565-124"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="80565-125">DLL</span><span class="sxs-lookup"><span data-stu-id="80565-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80565-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80565-126"><dt>RDMS.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="80565-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80565-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80565-128">**Win32 \_ SessionBrokerServiceProperties**</span><span class="sxs-lookup"><span data-stu-id="80565-128">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





