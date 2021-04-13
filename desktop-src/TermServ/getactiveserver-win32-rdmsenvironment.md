---
title: Win32_RDMSEnvironment 類別的 GetActiveServer 方法
description: 抓取遠端桌面管理服務 (RDMS) 環境 (FQDN) 的完整功能變數名稱。
ms.assetid: 87e25d11-de1d-41d1-974d-2871dde444b5
ms.tgt_platform: multiple
keywords:
- GetActiveServer 方法遠端桌面服務
- GetActiveServer 方法遠端桌面服務，Win32_RDMSEnvironment 類別
- Win32_RDMSEnvironment 類別遠端桌面服務，GetActiveServer 方法
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4265315e3ed2de87e564adab87c023401bbd55e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465801"
---
# <a name="getactiveserver-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="968fb-106">Win32 RDMSEnvironment 類別的 GetActiveServer 方法 \_</span><span class="sxs-lookup"><span data-stu-id="968fb-106">GetActiveServer method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="968fb-107">抓取遠端桌面管理服務 (RDMS) 環境 (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="968fb-107">Retrieves the fully qualified domain name (FQDN) of the Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="968fb-108">語法</span><span class="sxs-lookup"><span data-stu-id="968fb-108">Syntax</span></span>


```mof
uint32 GetActiveServer(
  [out] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="968fb-109">參數</span><span class="sxs-lookup"><span data-stu-id="968fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="968fb-110">*ServerName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="968fb-110">*ServerName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="968fb-111">接收已抓取的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="968fb-111">Receives the retrieved FQDN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="968fb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="968fb-112">Return value</span></span>

<span data-ttu-id="968fb-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="968fb-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="968fb-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="968fb-114">Requirements</span></span>



| <span data-ttu-id="968fb-115">需求</span><span class="sxs-lookup"><span data-stu-id="968fb-115">Requirement</span></span> | <span data-ttu-id="968fb-116">值</span><span class="sxs-lookup"><span data-stu-id="968fb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="968fb-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="968fb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="968fb-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="968fb-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="968fb-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="968fb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="968fb-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="968fb-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="968fb-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="968fb-121">Namespace</span></span><br/>                | <span data-ttu-id="968fb-122">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="968fb-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="968fb-123">MOF</span><span class="sxs-lookup"><span data-stu-id="968fb-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="968fb-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="968fb-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="968fb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="968fb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="968fb-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="968fb-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="968fb-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="968fb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="968fb-128">**Win32 \_ RDMSEnvironment**</span><span class="sxs-lookup"><span data-stu-id="968fb-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





