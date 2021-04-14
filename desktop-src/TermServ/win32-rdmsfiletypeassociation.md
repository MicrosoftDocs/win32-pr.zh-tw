---
title: Win32_RDMSFileTypeAssociation 類別
description: 管理已發行應用程式的檔案類型關聯。
ms.assetid: 22c945cb-4c47-431a-bc9b-d33ba15c8ab3
ms.tgt_platform: multiple
keywords:
- Win32_RDMSFileTypeAssociation 類別遠端桌面服務
- Win32_RDMSFileTypeAssociation 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDMSFileTypeAssociation
- Win32_RDMSFileTypeAssociation.AppAlias
- Win32_RDMSFileTypeAssociation.PoolName
- Win32_RDMSFileTypeAssociation.ExtName
- Win32_RDMSFileTypeAssociation.ProgIdHint
- Win32_RDMSFileTypeAssociation.IconPath
- Win32_RDMSFileTypeAssociation.IconIndex
- Win32_RDMSFileTypeAssociation.IconContents
- Win32_RDMSFileTypeAssociation.IsPrimaryHandler
- Win32_RDMSFileTypeAssociation.IsPublished
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2e569077bf47a2b0eba63db39ae1e86c39feb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383965"
---
# <a name="win32_rdmsfiletypeassociation-class"></a><span data-ttu-id="1db2c-105">Win32 \_ RDMSFileTypeAssociation 類別</span><span class="sxs-lookup"><span data-stu-id="1db2c-105">Win32\_RDMSFileTypeAssociation class</span></span>

<span data-ttu-id="1db2c-106">管理已發行應用程式的檔案類型關聯。</span><span class="sxs-lookup"><span data-stu-id="1db2c-106">Manages a file type association for a published application.</span></span>

<span data-ttu-id="1db2c-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1db2c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1db2c-108">語法</span><span class="sxs-lookup"><span data-stu-id="1db2c-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSFileTypeAssociation
{
  string  AppAlias;
  string  PoolName;
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean IsPrimaryHandler;
  boolean IsPublished;
};
```

## <a name="members"></a><span data-ttu-id="1db2c-109">成員</span><span class="sxs-lookup"><span data-stu-id="1db2c-109">Members</span></span>

<span data-ttu-id="1db2c-110">**Win32 \_ RDMSFileTypeAssociation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1db2c-110">The **Win32\_RDMSFileTypeAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="1db2c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="1db2c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1db2c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="1db2c-112">Properties</span></span>

<span data-ttu-id="1db2c-113">**Win32 \_ RDMSFileTypeAssociation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1db2c-113">The **Win32\_RDMSFileTypeAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1db2c-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="1db2c-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1db2c-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1db2c-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1db2c-116">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1db2c-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1db2c-117">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1db2c-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1db2c-118">取得和設定與檔案類型相關聯之應用程式的別名。</span><span class="sxs-lookup"><span data-stu-id="1db2c-118">Gets and sets the alias of the application that is associated with the file type.</span></span>

</dd> <dt>

<span data-ttu-id="1db2c-119">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="1db2c-119">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1db2c-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1db2c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1db2c-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1db2c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1db2c-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1db2c-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1db2c-123">取得副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="1db2c-123">Gets the name of the file extension.</span></span>

</dd> <dt>

<span data-ttu-id="1db2c-124">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="1db2c-124">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1db2c-125">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="1db2c-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1db2c-126">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1db2c-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1db2c-127">取得和設定檔案類型的圖示內容。</span><span class="sxs-lookup"><span data-stu-id="1db2c-127">Gets and sets the content of the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="1db2c-128">**>iconindex**</span><span class="sxs-lookup"><span data-stu-id="1db2c-128">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1db2c-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="1db2c-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1db2c-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1db2c-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1db2c-131">取得並設定檔案類型圖示的索引。</span><span class="sxs-lookup"><span data-stu-id="1db2c-131">Gets and sets the index to the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="1db2c-132">**>iconpath**</span><span class="sxs-lookup"><span data-stu-id="1db2c-132">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1db2c-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1db2c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1db2c-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1db2c-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1db2c-135">取得和設定檔案類型的圖示路徑。</span><span class="sxs-lookup"><span data-stu-id="1db2c-135">Gets and sets the path to the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="1db2c-136">**IsPrimaryHandler**</span><span class="sxs-lookup"><span data-stu-id="1db2c-136">**IsPrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1db2c-137">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1db2c-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1db2c-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1db2c-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1db2c-139">取得和設定值，這個值會指出檔案類型關聯是否適用于主要處理常式。</span><span class="sxs-lookup"><span data-stu-id="1db2c-139">Gets and sets a value that indicates whether the file type association is for the primary handler.</span></span> <span data-ttu-id="1db2c-140">如果檔案類型關聯適用于主要處理常式，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="1db2c-140">**TRUE** if the file type association is for the primary handler; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1db2c-141">**IsPublished**</span><span class="sxs-lookup"><span data-stu-id="1db2c-141">**IsPublished**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1db2c-142">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1db2c-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1db2c-143">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1db2c-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1db2c-144">是否發佈此 FTA。</span><span class="sxs-lookup"><span data-stu-id="1db2c-144">Whether this FTA is published.</span></span>

<span data-ttu-id="1db2c-145">取得和設定值，這個值會指出是否已發行檔案類型關聯。</span><span class="sxs-lookup"><span data-stu-id="1db2c-145">Gets and sets a value that indicates whether the file type association is published.</span></span> <span data-ttu-id="1db2c-146">如果已發行檔案類型關聯，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="1db2c-146">**TRUE** if the file type association is published; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1db2c-147">**PoolName**</span><span class="sxs-lookup"><span data-stu-id="1db2c-147">**PoolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1db2c-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1db2c-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1db2c-149">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1db2c-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1db2c-150">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1db2c-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1db2c-151">取得和設定檔案類型關聯的應用程式集區名稱。</span><span class="sxs-lookup"><span data-stu-id="1db2c-151">Gets and sets the name of the application pool for the file type association.</span></span>

</dd> <dt>

<span data-ttu-id="1db2c-152">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="1db2c-152">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1db2c-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1db2c-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1db2c-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1db2c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1db2c-155">取得可協助使用者開啟副檔名的提示。</span><span class="sxs-lookup"><span data-stu-id="1db2c-155">Gets a hint to help users open the file extension.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1db2c-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="1db2c-156">Requirements</span></span>



| <span data-ttu-id="1db2c-157">需求</span><span class="sxs-lookup"><span data-stu-id="1db2c-157">Requirement</span></span> | <span data-ttu-id="1db2c-158">值</span><span class="sxs-lookup"><span data-stu-id="1db2c-158">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1db2c-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1db2c-159">Minimum supported client</span></span><br/> | <span data-ttu-id="1db2c-160">都不支援</span><span class="sxs-lookup"><span data-stu-id="1db2c-160">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1db2c-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1db2c-161">Minimum supported server</span></span><br/> | <span data-ttu-id="1db2c-162">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1db2c-162">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="1db2c-163">命名空間</span><span class="sxs-lookup"><span data-stu-id="1db2c-163">Namespace</span></span><br/>                | <span data-ttu-id="1db2c-164">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="1db2c-164">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1db2c-165">MOF</span><span class="sxs-lookup"><span data-stu-id="1db2c-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1db2c-166"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="1db2c-166"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1db2c-167">DLL</span><span class="sxs-lookup"><span data-stu-id="1db2c-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1db2c-168"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1db2c-168"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1db2c-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1db2c-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1db2c-170">遠端桌面管理服務提供者</span><span class="sxs-lookup"><span data-stu-id="1db2c-170">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

