---
title: Win32_SessionBrokerServiceProperties 類別的 InstallBrokerDatabase 方法
description: 在中央 SQL server 上安裝 RD 連線代理人資料庫。
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- InstallBrokerDatabase 方法遠端桌面服務
- InstallBrokerDatabase 方法遠端桌面服務，Win32_SessionBrokerServiceProperties 類別
- Win32_SessionBrokerServiceProperties 類別遠端桌面服務，InstallBrokerDatabase 方法
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.InstallBrokerDatabase
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da560bd4746c41864b3c56438f841efebe71ecd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685582"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="78671-106">Win32 SessionBrokerServiceProperties 類別的 InstallBrokerDatabase 方法 \_</span><span class="sxs-lookup"><span data-stu-id="78671-106">InstallBrokerDatabase method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="78671-107">在中央 SQL server 上安裝 RD 連線代理人資料庫。</span><span class="sxs-lookup"><span data-stu-id="78671-107">Installs an RD connection broker database on a central SQL server.</span></span>

## <a name="syntax"></a><span data-ttu-id="78671-108">語法</span><span class="sxs-lookup"><span data-stu-id="78671-108">Syntax</span></span>


```mof
uint32 InstallBrokerDatabase(
  [in] string newDbFilePath,
  [in] string connStringToCentralDBMaster,
  [in] string centralRdcmsDbName
);
```



## <a name="parameters"></a><span data-ttu-id="78671-109">參數</span><span class="sxs-lookup"><span data-stu-id="78671-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78671-110">*newDbFilePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="78671-110">*newDbFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78671-111">新的資料庫檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="78671-111">new database file path.</span></span>

</dd> <dt>

<span data-ttu-id="78671-112">*connStringToCentralDBMaster* \[在\]</span><span class="sxs-lookup"><span data-stu-id="78671-112">*connStringToCentralDBMaster* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78671-113">中央資料庫主資料庫的連接字串。</span><span class="sxs-lookup"><span data-stu-id="78671-113">Connection string to the central database master.</span></span>

</dd> <dt>

<span data-ttu-id="78671-114">*centralRdcmsDbName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="78671-114">*centralRdcmsDbName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78671-115">中央資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="78671-115">Name of the central database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78671-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="78671-116">Requirements</span></span>



| <span data-ttu-id="78671-117">需求</span><span class="sxs-lookup"><span data-stu-id="78671-117">Requirement</span></span> | <span data-ttu-id="78671-118">值</span><span class="sxs-lookup"><span data-stu-id="78671-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78671-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78671-119">Minimum supported client</span></span><br/> | <span data-ttu-id="78671-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="78671-120">None supported</span></span><br/>                                                              |
| <span data-ttu-id="78671-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78671-121">Minimum supported server</span></span><br/> | <span data-ttu-id="78671-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78671-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="78671-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="78671-123">Namespace</span></span><br/>                | <span data-ttu-id="78671-124">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="78671-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="78671-125">MOF</span><span class="sxs-lookup"><span data-stu-id="78671-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78671-126"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="78671-126"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="78671-127">DLL</span><span class="sxs-lookup"><span data-stu-id="78671-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78671-128"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78671-128"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78671-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78671-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78671-130">**Win32 \_ SessionBrokerServiceProperties**</span><span class="sxs-lookup"><span data-stu-id="78671-130">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





