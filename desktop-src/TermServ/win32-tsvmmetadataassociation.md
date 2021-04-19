---
title: Win32_TSVmMetadataAssociation 類別
description: 代表遠端桌面虛擬機器與其中繼資料屬性之間的關聯。
ms.assetid: 374b1a29-78de-45fd-97b3-c5a5b724e66b
ms.tgt_platform: multiple
keywords:
- Win32_TSVmMetadataAssociation 類別遠端桌面服務
- Win32_TSVmMetadataAssociation 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataAssociation
- Win32_TSVmMetadataAssociation.TSVm
- Win32_TSVmMetadataAssociation.MetadataItem
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db3a68c20553eaf52903471d19df9df169ecde21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966086"
---
# <a name="win32_tsvmmetadataassociation-class"></a><span data-ttu-id="88d7b-105">Win32 \_ TSVmMetadataAssociation 類別</span><span class="sxs-lookup"><span data-stu-id="88d7b-105">Win32\_TSVmMetadataAssociation class</span></span>

<span data-ttu-id="88d7b-106">代表遠端桌面虛擬機器與其中繼資料屬性之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="88d7b-106">Represents an association between a Remote Desktop virtual machine and its metadata properties.</span></span>

<span data-ttu-id="88d7b-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="88d7b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="88d7b-108">語法</span><span class="sxs-lookup"><span data-stu-id="88d7b-108">Syntax</span></span>

``` syntax
[dynamic, Association, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataAssociation
{
  Win32_TSVm             REF TSVm;
  Win32_TSVmMetadataItem REF MetadataItem;
};
```

## <a name="members"></a><span data-ttu-id="88d7b-109">成員</span><span class="sxs-lookup"><span data-stu-id="88d7b-109">Members</span></span>

<span data-ttu-id="88d7b-110">**Win32 \_ TSVmMetadataAssociation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="88d7b-110">The **Win32\_TSVmMetadataAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="88d7b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="88d7b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88d7b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="88d7b-112">Properties</span></span>

<span data-ttu-id="88d7b-113">**Win32 \_ TSVmMetadataAssociation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="88d7b-113">The **Win32\_TSVmMetadataAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88d7b-114">**MetadataItem**</span><span class="sxs-lookup"><span data-stu-id="88d7b-114">**MetadataItem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88d7b-115">資料類型： **[ **Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md)**</span><span class="sxs-lookup"><span data-stu-id="88d7b-115">Data type: **[**Win32\_TSVmMetadataItem**](win32-tsvmmetadataitem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="88d7b-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88d7b-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88d7b-117">[**Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md)類別的實例，表示虛擬機器的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="88d7b-117">An instance of the [**Win32\_TSVmMetadataItem**](win32-tsvmmetadataitem.md) class that represents the metadata for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="88d7b-118">**TSVm**</span><span class="sxs-lookup"><span data-stu-id="88d7b-118">**TSVm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88d7b-119">資料類型： **[ **Win32 \_ TSVm**](win32-tsvm.md)**</span><span class="sxs-lookup"><span data-stu-id="88d7b-119">Data type: **[**Win32\_TSVm**](win32-tsvm.md)**</span></span>
</dt> <dt>

<span data-ttu-id="88d7b-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88d7b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88d7b-121">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="88d7b-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="88d7b-122">代表虛擬機器之 [**Win32 \_ TSVm**](win32-tsvm.md) 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="88d7b-122">An instance of the [**Win32\_TSVm**](win32-tsvm.md) class that represents the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88d7b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="88d7b-123">Requirements</span></span>



| <span data-ttu-id="88d7b-124">需求</span><span class="sxs-lookup"><span data-stu-id="88d7b-124">Requirement</span></span> | <span data-ttu-id="88d7b-125">值</span><span class="sxs-lookup"><span data-stu-id="88d7b-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="88d7b-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88d7b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="88d7b-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="88d7b-127">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="88d7b-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88d7b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="88d7b-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88d7b-129">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="88d7b-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="88d7b-130">Namespace</span></span><br/>                | <span data-ttu-id="88d7b-131">根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="88d7b-131">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="88d7b-132">MOF</span><span class="sxs-lookup"><span data-stu-id="88d7b-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88d7b-133"><dt>TSVmHost mof</dt></span><span class="sxs-lookup"><span data-stu-id="88d7b-133"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="88d7b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="88d7b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88d7b-135"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88d7b-135"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

