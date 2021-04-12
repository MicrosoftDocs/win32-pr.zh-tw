---
title: Win32_RDAllowListFileAssociation 類別
description: 描述已發行的檔案類型與 RemoteApp 的關聯。
ms.assetid: 80cc8f5e-a7f0-458c-b05b-7822306f839a
ms.tgt_platform: multiple
keywords:
- Win32_RDAllowListFileAssociation 類別遠端桌面服務
- Win32_RDAllowListFileAssociation 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDAllowListFileAssociation
- Win32_RDAllowListFileAssociation.ExtName
- Win32_RDAllowListFileAssociation.AppAlias
- Win32_RDAllowListFileAssociation.ProgIdHint
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acbc74b5b0dab228a5c625863b4fcd0574b5f96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465296"
---
# <a name="win32_rdallowlistfileassociation-class"></a><span data-ttu-id="cdb06-105">Win32 \_ RDAllowListFileAssociation 類別</span><span class="sxs-lookup"><span data-stu-id="cdb06-105">Win32\_RDAllowListFileAssociation class</span></span>

<span data-ttu-id="cdb06-106">描述已發行的檔案類型與 RemoteApp 的關聯。</span><span class="sxs-lookup"><span data-stu-id="cdb06-106">Describes a published file type association with a RemoteApp.</span></span>

<span data-ttu-id="cdb06-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="cdb06-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdb06-108">語法</span><span class="sxs-lookup"><span data-stu-id="cdb06-108">Syntax</span></span>

``` syntax
class Win32_RDAllowListFileAssociation
{
  string ExtName;
  string AppAlias;
  string ProgIdHint;
};
```

## <a name="members"></a><span data-ttu-id="cdb06-109">成員</span><span class="sxs-lookup"><span data-stu-id="cdb06-109">Members</span></span>

<span data-ttu-id="cdb06-110">**Win32 \_ RDAllowListFileAssociation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cdb06-110">The **Win32\_RDAllowListFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="cdb06-111">屬性</span><span class="sxs-lookup"><span data-stu-id="cdb06-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cdb06-112">屬性</span><span class="sxs-lookup"><span data-stu-id="cdb06-112">Properties</span></span>

<span data-ttu-id="cdb06-113">**Win32 \_ RDAllowListFileAssociation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cdb06-113">The **Win32\_RDAllowListFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cdb06-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="cdb06-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb06-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cdb06-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdb06-116">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cdb06-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cdb06-117">與延伸模組相關聯的 RemoteApp 別名。</span><span class="sxs-lookup"><span data-stu-id="cdb06-117">Alias of the RemoteApp associated with the extension.</span></span>

</dd> <dt>

<span data-ttu-id="cdb06-118">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="cdb06-118">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb06-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cdb06-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdb06-120">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cdb06-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cdb06-121">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="cdb06-121">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="cdb06-122">延伸模組的名稱，例如 .txt。</span><span class="sxs-lookup"><span data-stu-id="cdb06-122">Name of the extension, for example .txt.</span></span>

</dd> <dt>

<span data-ttu-id="cdb06-123">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="cdb06-123">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdb06-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cdb06-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdb06-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cdb06-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cdb06-126">使用此檔案關聯協助開啟檔的提示</span><span class="sxs-lookup"><span data-stu-id="cdb06-126">Hint to help open documents with this file association</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cdb06-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="cdb06-127">Requirements</span></span>



| <span data-ttu-id="cdb06-128">需求</span><span class="sxs-lookup"><span data-stu-id="cdb06-128">Requirement</span></span> | <span data-ttu-id="cdb06-129">值</span><span class="sxs-lookup"><span data-stu-id="cdb06-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb06-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cdb06-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cdb06-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="cdb06-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="cdb06-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cdb06-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cdb06-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cdb06-133">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="cdb06-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="cdb06-134">Namespace</span></span><br/>                | <span data-ttu-id="cdb06-135">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="cdb06-135">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="cdb06-136">MOF</span><span class="sxs-lookup"><span data-stu-id="cdb06-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdb06-137"><dt>TsAllow mof</dt></span><span class="sxs-lookup"><span data-stu-id="cdb06-137"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="cdb06-138">DLL</span><span class="sxs-lookup"><span data-stu-id="cdb06-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdb06-139"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdb06-139"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

 





