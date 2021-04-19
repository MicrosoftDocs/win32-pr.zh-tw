---
title: Win32_RDMSEnvironment 類別的 SetClientAccessName 方法
description: 將網域名稱系統 (DNS) 資源記錄 (RR) 遠端桌面管理服務 (的) 環境的名稱。
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- SetClientAccessName 方法遠端桌面服務
- SetClientAccessName 方法遠端桌面服務，Win32_RDMSEnvironment 類別
- Win32_RDMSEnvironment 類別遠端桌面服務，SetClientAccessName 方法
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13f9087fe2c2139833baeb21bc62da508c6e5989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966540"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="81ea5-106">Win32 RDMSEnvironment 類別的 SetClientAccessName 方法 \_</span><span class="sxs-lookup"><span data-stu-id="81ea5-106">SetClientAccessName method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="81ea5-107">將網域名稱系統 (DNS) 資源記錄 (RR) 遠端桌面管理服務 (的) 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="81ea5-107">Updates the Domain Name System (DNS) resource record (RR) name of an Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="81ea5-108">語法</span><span class="sxs-lookup"><span data-stu-id="81ea5-108">Syntax</span></span>


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a><span data-ttu-id="81ea5-109">參數</span><span class="sxs-lookup"><span data-stu-id="81ea5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81ea5-110">*ClientAccessName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81ea5-110">*ClientAccessName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81ea5-111">新的 RR 名稱。</span><span class="sxs-lookup"><span data-stu-id="81ea5-111">The new RR name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81ea5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="81ea5-112">Return value</span></span>

<span data-ttu-id="81ea5-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="81ea5-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="81ea5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="81ea5-114">Requirements</span></span>



| <span data-ttu-id="81ea5-115">需求</span><span class="sxs-lookup"><span data-stu-id="81ea5-115">Requirement</span></span> | <span data-ttu-id="81ea5-116">值</span><span class="sxs-lookup"><span data-stu-id="81ea5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="81ea5-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="81ea5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="81ea5-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="81ea5-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="81ea5-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="81ea5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="81ea5-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81ea5-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="81ea5-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="81ea5-121">Namespace</span></span><br/>                | <span data-ttu-id="81ea5-122">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="81ea5-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="81ea5-123">MOF</span><span class="sxs-lookup"><span data-stu-id="81ea5-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81ea5-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="81ea5-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="81ea5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="81ea5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81ea5-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81ea5-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="81ea5-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81ea5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81ea5-128">**Win32 \_ RDMSEnvironment**</span><span class="sxs-lookup"><span data-stu-id="81ea5-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





