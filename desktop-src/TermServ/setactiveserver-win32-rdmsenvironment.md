---
title: Win32_RDMSEnvironment 類別的 SetActiveServer 方法
description: 將遠端桌面管理服務 (RDMS) 環境的 FQDN 設定為目前的節點。
ms.assetid: ed7b71cf-c3a4-4d2f-856a-31332f94fac9
ms.tgt_platform: multiple
keywords:
- SetActiveServer 方法遠端桌面服務
- SetActiveServer 方法遠端桌面服務，Win32_RDMSEnvironment 類別
- Win32_RDMSEnvironment 類別遠端桌面服務，SetActiveServer 方法
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f11b378b15e271200c730691c3654fd10e80f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465109"
---
# <a name="setactiveserver-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="43101-106">Win32 RDMSEnvironment 類別的 SetActiveServer 方法 \_</span><span class="sxs-lookup"><span data-stu-id="43101-106">SetActiveServer method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="43101-107">將遠端桌面管理服務 (RDMS) 環境的 FQDN 設定為目前的節點。</span><span class="sxs-lookup"><span data-stu-id="43101-107">Sets the FQDN of the Remote Desktop Management Services (RDMS) environment to the current node.</span></span>

## <a name="syntax"></a><span data-ttu-id="43101-108">語法</span><span class="sxs-lookup"><span data-stu-id="43101-108">Syntax</span></span>


```mof
uint32 SetActiveServer();
```



## <a name="parameters"></a><span data-ttu-id="43101-109">參數</span><span class="sxs-lookup"><span data-stu-id="43101-109">Parameters</span></span>

<span data-ttu-id="43101-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="43101-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43101-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="43101-111">Return value</span></span>

<span data-ttu-id="43101-112">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="43101-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="43101-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="43101-113">Requirements</span></span>



| <span data-ttu-id="43101-114">需求</span><span class="sxs-lookup"><span data-stu-id="43101-114">Requirement</span></span> | <span data-ttu-id="43101-115">值</span><span class="sxs-lookup"><span data-stu-id="43101-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="43101-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43101-116">Minimum supported client</span></span><br/> | <span data-ttu-id="43101-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="43101-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="43101-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43101-118">Minimum supported server</span></span><br/> | <span data-ttu-id="43101-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="43101-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="43101-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="43101-120">Namespace</span></span><br/>                | <span data-ttu-id="43101-121">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="43101-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="43101-122">MOF</span><span class="sxs-lookup"><span data-stu-id="43101-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43101-123"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="43101-123"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="43101-124">DLL</span><span class="sxs-lookup"><span data-stu-id="43101-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43101-125"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43101-125"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="43101-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43101-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43101-127">**Win32 \_ RDMSEnvironment**</span><span class="sxs-lookup"><span data-stu-id="43101-127">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





