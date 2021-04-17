---
title: Win32_RDCentralPublishedFileAssociation 類別
description: 與應用程式相關聯的副檔名資訊。
ms.assetid: ba12d933-572c-48d3-bf0f-1c99de61457d
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedFileAssociation 類別遠端桌面服務
- Win32_RDCentralPublishedFileAssociation 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFileAssociation
- Win32_RDCentralPublishedFileAssociation.ExtName
- Win32_RDCentralPublishedFileAssociation.AppAlias
- Win32_RDCentralPublishedFileAssociation.FarmAlias
- Win32_RDCentralPublishedFileAssociation.ProgIdHint
- Win32_RDCentralPublishedFileAssociation.IconContents
- Win32_RDCentralPublishedFileAssociation.PrimaryHandler
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a0f1c9bf7905504ee3aa2ba6fff7e9804f4747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466729"
---
# <a name="win32_rdcentralpublishedfileassociation-class"></a><span data-ttu-id="23386-105">Win32 \_ RDCentralPublishedFileAssociation 類別</span><span class="sxs-lookup"><span data-stu-id="23386-105">Win32\_RDCentralPublishedFileAssociation class</span></span>

<span data-ttu-id="23386-106">與應用程式相關聯的副檔名資訊</span><span class="sxs-lookup"><span data-stu-id="23386-106">Info for a file extension associated with an application</span></span>

<span data-ttu-id="23386-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="23386-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="23386-108">語法</span><span class="sxs-lookup"><span data-stu-id="23386-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedFileAssociation
{
  string  ExtName;
  string  AppAlias;
  string  FarmAlias;
  string  ProgIdHint;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a><span data-ttu-id="23386-109">成員</span><span class="sxs-lookup"><span data-stu-id="23386-109">Members</span></span>

<span data-ttu-id="23386-110">**Win32 \_ RDCentralPublishedFileAssociation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="23386-110">The **Win32\_RDCentralPublishedFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="23386-111">屬性</span><span class="sxs-lookup"><span data-stu-id="23386-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23386-112">屬性</span><span class="sxs-lookup"><span data-stu-id="23386-112">Properties</span></span>

<span data-ttu-id="23386-113">**Win32 \_ RDCentralPublishedFileAssociation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="23386-113">The **Win32\_RDCentralPublishedFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23386-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="23386-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23386-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="23386-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23386-116">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="23386-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="23386-117">檔案關聯的 RemoteApp 別名。</span><span class="sxs-lookup"><span data-stu-id="23386-117">Alias of the file association's RemoteApp.</span></span>

</dd> <dt>

<span data-ttu-id="23386-118">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="23386-118">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23386-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="23386-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23386-120">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="23386-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="23386-121">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="23386-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="23386-122">延伸 (的名稱，例如 .txt) 。</span><span class="sxs-lookup"><span data-stu-id="23386-122">Name of the extension (e.g. .txt).</span></span>

</dd> <dt>

<span data-ttu-id="23386-123">**FarmAlias**</span><span class="sxs-lookup"><span data-stu-id="23386-123">**FarmAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23386-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="23386-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23386-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="23386-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="23386-126">檔案關聯之 RemoteApp's 伺服器陣列的別名</span><span class="sxs-lookup"><span data-stu-id="23386-126">Alias of the file association's RemoteApp's Farm</span></span>

</dd> <dt>

<span data-ttu-id="23386-127">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="23386-127">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23386-128">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="23386-128">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="23386-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="23386-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="23386-130">此檔案關聯的圖示內容。</span><span class="sxs-lookup"><span data-stu-id="23386-130">Contents of the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="23386-131">**PrimaryHandler**</span><span class="sxs-lookup"><span data-stu-id="23386-131">**PrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23386-132">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="23386-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23386-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="23386-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23386-134">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="23386-134">Reserved for future use.</span></span> <span data-ttu-id="23386-135">一律會是 **true**。</span><span class="sxs-lookup"><span data-stu-id="23386-135">Will always be **true**.</span></span>

</dd> <dt>

<span data-ttu-id="23386-136">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="23386-136">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23386-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="23386-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23386-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="23386-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="23386-139">提示，協助您使用此檔案關聯開啟檔。</span><span class="sxs-lookup"><span data-stu-id="23386-139">Hint to help open documents with this file association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23386-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="23386-140">Requirements</span></span>



| <span data-ttu-id="23386-141">需求</span><span class="sxs-lookup"><span data-stu-id="23386-141">Requirement</span></span> | <span data-ttu-id="23386-142">值</span><span class="sxs-lookup"><span data-stu-id="23386-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="23386-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23386-143">Minimum supported client</span></span><br/> | <span data-ttu-id="23386-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="23386-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="23386-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23386-145">Minimum supported server</span></span><br/> | <span data-ttu-id="23386-146">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="23386-146">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="23386-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="23386-147">Namespace</span></span><br/>                | <span data-ttu-id="23386-148">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="23386-148">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="23386-149">MOF</span><span class="sxs-lookup"><span data-stu-id="23386-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23386-150"><dt>Tscpub mof</dt></span><span class="sxs-lookup"><span data-stu-id="23386-150"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="23386-151">DLL</span><span class="sxs-lookup"><span data-stu-id="23386-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23386-152"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23386-152"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

