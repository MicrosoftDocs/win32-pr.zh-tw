---
title: LSLicense 結構
description: 包含特定遠端桌面服務授權的相關資訊。
ms.assetid: 2c7f7b7a-e3b5-4f84-b49f-5f1d6960652d
ms.tgt_platform: multiple
keywords:
- LSLicense 結構遠端桌面服務
- LPLSLicense 結構指標遠端桌面服務
topic_type:
- apiref
api_name:
- LSLicense
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dcb8551c1d1edfd9486d42df63de9a76fab38433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465124"
---
# <a name="lslicense-structure"></a><span data-ttu-id="94618-105">LSLicense 結構</span><span class="sxs-lookup"><span data-stu-id="94618-105">LSLicense structure</span></span>

<span data-ttu-id="94618-106">包含特定遠端桌面服務授權的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="94618-106">Contains information about a specific Remote Desktop Services license.</span></span>

> [!Note]  
> <span data-ttu-id="94618-107">此結構未定義于任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="94618-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="94618-108">若要使用這個結構，您必須自行定義，如本主題所示。</span><span class="sxs-lookup"><span data-stu-id="94618-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="94618-109">語法</span><span class="sxs-lookup"><span data-stu-id="94618-109">Syntax</span></span>


```C++
typedef struct _LSLicense {
  DWORD dwVersion;
  DWORD dwLicenseId;
  DWORD dwKeyPackId;
  TCHAR szHWID[GUID_MAX_SIZE];
  TCHAR szMachineName[MAXCOMPUTERNAMELENGTH];
  TCHAR szUserName[MAXUSERNAMELENGTH];
  DWORD dwCertSerialLicense;
  DWORD dwLicenseSerialNumber;
  DWORD ftIssueDate;
  DWORD ftExpireDate;
  UCHAR ucLicenseStatus;
} LSLicense, *LPLSLicense;
```



## <a name="members"></a><span data-ttu-id="94618-110">成員</span><span class="sxs-lookup"><span data-stu-id="94618-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="94618-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="94618-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="94618-112">授權版本。</span><span class="sxs-lookup"><span data-stu-id="94618-112">Version of the license.</span></span>

</dd> <dt>

<span data-ttu-id="94618-113">**dwLicenseId**</span><span class="sxs-lookup"><span data-stu-id="94618-113">**dwLicenseId**</span></span>
</dt> <dd>

<span data-ttu-id="94618-114">授權的識別碼。</span><span class="sxs-lookup"><span data-stu-id="94618-114">ID of the license.</span></span>

</dd> <dt>

<span data-ttu-id="94618-115">**dwKeyPackId**</span><span class="sxs-lookup"><span data-stu-id="94618-115">**dwKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="94618-116">包含授權的 [**LSKEYPACK**](lskeypack.md) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="94618-116">ID of the [**LSKeyPack**](lskeypack.md) that contains the license.</span></span>

</dd> <dt>

<span data-ttu-id="94618-117">**szHWID**</span><span class="sxs-lookup"><span data-stu-id="94618-117">**szHWID**</span></span>
</dt> <dd>

<span data-ttu-id="94618-118">發出授權的遠端桌面連線 (RDC) 用戶端的硬體識別碼。</span><span class="sxs-lookup"><span data-stu-id="94618-118">Hardware ID of the Remote Desktop Connection (RDC) client that was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="94618-119">**szMachineName**</span><span class="sxs-lookup"><span data-stu-id="94618-119">**szMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="94618-120">已發出授權之遠端桌面連線 (RDC) 用戶端的名稱。</span><span class="sxs-lookup"><span data-stu-id="94618-120">Name of the Remote Desktop Connection (RDC) client that was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="94618-121">**szUserName**</span><span class="sxs-lookup"><span data-stu-id="94618-121">**szUserName**</span></span>
</dt> <dd>

<span data-ttu-id="94618-122">已發出授權之使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="94618-122">Name of the user who was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="94618-123">**dwCertSerialLicense**</span><span class="sxs-lookup"><span data-stu-id="94618-123">**dwCertSerialLicense**</span></span>
</dt> <dd>

<span data-ttu-id="94618-124">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="94618-124">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="94618-125">**dwLicenseSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="94618-125">**dwLicenseSerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="94618-126">授權的序號。</span><span class="sxs-lookup"><span data-stu-id="94618-126">Serial number of the license.</span></span>

</dd> <dt>

<span data-ttu-id="94618-127">**ftIssueDate**</span><span class="sxs-lookup"><span data-stu-id="94618-127">**ftIssueDate**</span></span>
</dt> <dd>

<span data-ttu-id="94618-128">授權的發出日期。</span><span class="sxs-lookup"><span data-stu-id="94618-128">Date that the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="94618-129">**ftExpireDate**</span><span class="sxs-lookup"><span data-stu-id="94618-129">**ftExpireDate**</span></span>
</dt> <dd>

<span data-ttu-id="94618-130">授權將到期的日期。</span><span class="sxs-lookup"><span data-stu-id="94618-130">Date that the license will expire.</span></span>

</dd> <dt>

<span data-ttu-id="94618-131">**ucLicenseStatus**</span><span class="sxs-lookup"><span data-stu-id="94618-131">**ucLicenseStatus**</span></span>
</dt> <dd>

<span data-ttu-id="94618-132">授權的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="94618-132">Current status of the license.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94618-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="94618-133">Requirements</span></span>



| <span data-ttu-id="94618-134">需求</span><span class="sxs-lookup"><span data-stu-id="94618-134">Requirement</span></span> | <span data-ttu-id="94618-135">值</span><span class="sxs-lookup"><span data-stu-id="94618-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="94618-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94618-136">Minimum supported client</span></span><br/> | <span data-ttu-id="94618-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94618-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="94618-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94618-138">Minimum supported server</span></span><br/> | <span data-ttu-id="94618-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94618-139">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94618-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94618-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94618-141">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="94618-141">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="94618-142">**TLSLicenseEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="94618-142">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="94618-143">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="94618-143">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dt>

[<span data-ttu-id="94618-144">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="94618-144">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

 





