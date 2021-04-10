---
title: Win32_RDFileAssociation 類別
description: 表示 RemoteApp 的檔案類型關聯。
ms.assetid: 9ecf6fa5-36f0-4b37-9d59-781b41c1d90c
ms.tgt_platform: multiple
keywords:
- Win32_RDFileAssociation 類別遠端桌面服務
- Win32_RDFileAssociation 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDFileAssociation
- Win32_RDFileAssociation.ExtName
- Win32_RDFileAssociation.ProgIdHint
- Win32_RDFileAssociation.IconPath
- Win32_RDFileAssociation.IconIndex
- Win32_RDFileAssociation.IconContents
- Win32_RDFileAssociation.PrimaryHandler
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac64cd38bdad748c64fe6f52cb7a6da8d8220cba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934239"
---
# <a name="win32_rdfileassociation-class"></a><span data-ttu-id="d7366-105">Win32 \_ RDFileAssociation 類別</span><span class="sxs-lookup"><span data-stu-id="d7366-105">Win32\_RDFileAssociation class</span></span>

<span data-ttu-id="d7366-106">表示 RemoteApp 的檔案類型關聯。</span><span class="sxs-lookup"><span data-stu-id="d7366-106">Represents a file type association for a RemoteApp.</span></span>

<span data-ttu-id="d7366-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d7366-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7366-108">語法</span><span class="sxs-lookup"><span data-stu-id="d7366-108">Syntax</span></span>

``` syntax
class Win32_RDFileAssociation
{
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a><span data-ttu-id="d7366-109">成員</span><span class="sxs-lookup"><span data-stu-id="d7366-109">Members</span></span>

<span data-ttu-id="d7366-110">**Win32 \_ RDFileAssociation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d7366-110">The **Win32\_RDFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="d7366-111">屬性</span><span class="sxs-lookup"><span data-stu-id="d7366-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d7366-112">屬性</span><span class="sxs-lookup"><span data-stu-id="d7366-112">Properties</span></span>

<span data-ttu-id="d7366-113">**Win32 \_ RDFileAssociation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d7366-113">The **Win32\_RDFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d7366-114">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="d7366-114">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7366-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7366-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7366-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7366-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7366-117">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="d7366-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d7366-118">副檔名的名稱，例如 .txt。</span><span class="sxs-lookup"><span data-stu-id="d7366-118">The name of the file name extension, for example .txt.</span></span>

</dd> <dt>

<span data-ttu-id="d7366-119">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="d7366-119">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7366-120">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="d7366-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d7366-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7366-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7366-122">此檔案關聯的圖示內容。</span><span class="sxs-lookup"><span data-stu-id="d7366-122">The contents of the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="d7366-123">**>iconindex**</span><span class="sxs-lookup"><span data-stu-id="d7366-123">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7366-124">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="d7366-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d7366-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7366-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7366-126">檔案中的圖示索引。</span><span class="sxs-lookup"><span data-stu-id="d7366-126">The index of the icon in the file.</span></span>

</dd> <dt>

<span data-ttu-id="d7366-127">**>iconpath**</span><span class="sxs-lookup"><span data-stu-id="d7366-127">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7366-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7366-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7366-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7366-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7366-130">這個檔案關聯之圖示的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="d7366-130">The file path to the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="d7366-131">**PrimaryHandler**</span><span class="sxs-lookup"><span data-stu-id="d7366-131">**PrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7366-132">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d7366-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d7366-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7366-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7366-134">指出此關聯是否適用于主要處理常式。</span><span class="sxs-lookup"><span data-stu-id="d7366-134">Indicates whether this association is for a primary handler.</span></span>

</dd> <dt>

<span data-ttu-id="d7366-135">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="d7366-135">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7366-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7366-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7366-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7366-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7366-138">此提示可協助您使用此檔案關聯開啟檔。</span><span class="sxs-lookup"><span data-stu-id="d7366-138">The Hint to help open documents with this file association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7366-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7366-139">Requirements</span></span>



| <span data-ttu-id="d7366-140">需求</span><span class="sxs-lookup"><span data-stu-id="d7366-140">Requirement</span></span> | <span data-ttu-id="d7366-141">值</span><span class="sxs-lookup"><span data-stu-id="d7366-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7366-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7366-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d7366-143">都不支援</span><span class="sxs-lookup"><span data-stu-id="d7366-143">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d7366-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7366-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d7366-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d7366-145">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="d7366-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="d7366-146">Namespace</span></span><br/>                | <span data-ttu-id="d7366-147">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="d7366-147">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d7366-148">MOF</span><span class="sxs-lookup"><span data-stu-id="d7366-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7366-149"><dt>TsAllow mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7366-149"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="d7366-150">DLL</span><span class="sxs-lookup"><span data-stu-id="d7366-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7366-151"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7366-151"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

 





