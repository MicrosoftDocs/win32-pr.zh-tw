---
title: Win32_RDMSManagementData 類別
description: 同步處理遠端桌面管理服務 (RDMS) 的發佈資料。
ms.assetid: 17f06294-6580-4297-9301-f88314db7775
ms.tgt_platform: multiple
keywords:
- Win32_RDMSManagementData 類別遠端桌面服務
- Win32_RDMSManagementData 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dddf2a73673e886456eb43bfbd2cefc72250cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024688"
---
# <a name="win32_rdmsmanagementdata-class"></a><span data-ttu-id="10bb8-105">Win32 \_ RDMSManagementData 類別</span><span class="sxs-lookup"><span data-stu-id="10bb8-105">Win32\_RDMSManagementData class</span></span>

<span data-ttu-id="10bb8-106">同步處理遠端桌面管理服務 (RDMS) 的發佈資料。</span><span class="sxs-lookup"><span data-stu-id="10bb8-106">Synchronizes publishing data for Remote Desktop Management Services (RDMS).</span></span>

<span data-ttu-id="10bb8-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="10bb8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="10bb8-108">語法</span><span class="sxs-lookup"><span data-stu-id="10bb8-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSManagementData
{
};
```

## <a name="members"></a><span data-ttu-id="10bb8-109">成員</span><span class="sxs-lookup"><span data-stu-id="10bb8-109">Members</span></span>

<span data-ttu-id="10bb8-110">**Win32 \_ RDMSManagementData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="10bb8-110">The **Win32\_RDMSManagementData** class has these types of members:</span></span>

-   [<span data-ttu-id="10bb8-111">方法</span><span class="sxs-lookup"><span data-stu-id="10bb8-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="10bb8-112">方法</span><span class="sxs-lookup"><span data-stu-id="10bb8-112">Methods</span></span>

<span data-ttu-id="10bb8-113">**Win32 \_ RDMSManagementData** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="10bb8-113">The **Win32\_RDMSManagementData** class has these methods.</span></span>



| <span data-ttu-id="10bb8-114">方法</span><span class="sxs-lookup"><span data-stu-id="10bb8-114">Method</span></span>                                                                                        | <span data-ttu-id="10bb8-115">描述</span><span class="sxs-lookup"><span data-stu-id="10bb8-115">Description</span></span>                                                            |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="10bb8-116">**SynchronizeAllPublishingData**</span><span class="sxs-lookup"><span data-stu-id="10bb8-116">**SynchronizeAllPublishingData**</span></span>](synchronizeallpublishingdata-win32-rdmsmanagementdata.md) | <span data-ttu-id="10bb8-117">同步處理所有 RDM 的發佈資料。</span><span class="sxs-lookup"><span data-stu-id="10bb8-117">Synchronizes all publishing data for RDMS.</span></span><br/>                  |
| [<span data-ttu-id="10bb8-118">**SynchronizePublishingData**</span><span class="sxs-lookup"><span data-stu-id="10bb8-118">**SynchronizePublishingData**</span></span>](synchronizepublishingdata-win32-rdmsmanagementdata.md)       | <span data-ttu-id="10bb8-119">同步處理指定的 RDMS 發行資料集。</span><span class="sxs-lookup"><span data-stu-id="10bb8-119">Synchronizes the specified set of publishing data for RDMS.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="10bb8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="10bb8-120">Requirements</span></span>



| <span data-ttu-id="10bb8-121">需求</span><span class="sxs-lookup"><span data-stu-id="10bb8-121">Requirement</span></span> | <span data-ttu-id="10bb8-122">值</span><span class="sxs-lookup"><span data-stu-id="10bb8-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="10bb8-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10bb8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="10bb8-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="10bb8-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="10bb8-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10bb8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="10bb8-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="10bb8-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="10bb8-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="10bb8-127">Namespace</span></span><br/>                | <span data-ttu-id="10bb8-128">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="10bb8-128">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="10bb8-129">MOF</span><span class="sxs-lookup"><span data-stu-id="10bb8-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10bb8-130"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="10bb8-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="10bb8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="10bb8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10bb8-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10bb8-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="10bb8-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10bb8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10bb8-134">遠端桌面管理服務提供者</span><span class="sxs-lookup"><span data-stu-id="10bb8-134">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





