---
title: MSAD_NamingCoNtext 類別
description: 代表網域控制站上 (NC) 的特定命名內容。
ms.assetid: 67dd6c68-6c67-40b4-a20a-c6c312d23441
ms.tgt_platform: multiple
keywords:
- MSAD_NamingCoNtext 類別 Active Directory
- MSAD_NamingCoNtext 類別 Active Directory，描述
topic_type:
- apiref
api_name:
- MSAD_NamingContext
- MSAD_NamingContext.DistinguishedName
- MSAD_NamingContext.IsFullReplica
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d68f70c6e40e823df0a6827e1114f40dae7937be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685929"
---
# <a name="msad_namingcontext-class"></a><span data-ttu-id="95d0b-105">MSAD \_ NamingCoNtext 類別</span><span class="sxs-lookup"><span data-stu-id="95d0b-105">MSAD\_NamingContext class</span></span>

<span data-ttu-id="95d0b-106">代表網域控制站上 (NC) 的特定命名內容。</span><span class="sxs-lookup"><span data-stu-id="95d0b-106">Represents a particular naming context (NC) on the domain controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d0b-107">語法</span><span class="sxs-lookup"><span data-stu-id="95d0b-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_NamingContext
{
  String  DistinguishedName;
  boolean IsFullReplica = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="95d0b-108">成員</span><span class="sxs-lookup"><span data-stu-id="95d0b-108">Members</span></span>

<span data-ttu-id="95d0b-109">**MSAD \_ NamingCoNtext** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="95d0b-109">The **MSAD\_NamingContext** class has these types of members:</span></span>

-   [<span data-ttu-id="95d0b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="95d0b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95d0b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="95d0b-111">Properties</span></span>

<span data-ttu-id="95d0b-112">**MSAD \_ NamingCoNtext** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="95d0b-112">The **MSAD\_NamingContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95d0b-113">**DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="95d0b-113">**DistinguishedName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d0b-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="95d0b-114">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="95d0b-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="95d0b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d0b-116">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="95d0b-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="95d0b-117">取得 NC 的 X. 500 路徑。</span><span class="sxs-lookup"><span data-stu-id="95d0b-117">Gets the X.500 path of the NC.</span></span>

</dd> <dt>

<span data-ttu-id="95d0b-118">**IsFullReplica**</span><span class="sxs-lookup"><span data-stu-id="95d0b-118">**IsFullReplica**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d0b-119">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="95d0b-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95d0b-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="95d0b-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95d0b-121">取得值，這個值會指出 NC 是否為讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="95d0b-121">Gets the value that indicates whether the NC is read/write.</span></span> <span data-ttu-id="95d0b-122">如果 NC 為讀取/寫入，則 **為 TRUE** ;如果 NC 是唯讀的，則 **為 FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="95d0b-122">**TRUE** if the NC is read/write; **FALSE** if the NC is read-only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95d0b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="95d0b-123">Requirements</span></span>



| <span data-ttu-id="95d0b-124">需求</span><span class="sxs-lookup"><span data-stu-id="95d0b-124">Requirement</span></span> | <span data-ttu-id="95d0b-125">值</span><span class="sxs-lookup"><span data-stu-id="95d0b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95d0b-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95d0b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="95d0b-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="95d0b-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="95d0b-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95d0b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="95d0b-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95d0b-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95d0b-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="95d0b-130">Namespace</span></span><br/>                | <span data-ttu-id="95d0b-131">根 \\ MicrosoftActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="95d0b-131">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="95d0b-132">MOF</span><span class="sxs-lookup"><span data-stu-id="95d0b-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95d0b-133"><dt>Replprov.dll mof</dt></span><span class="sxs-lookup"><span data-stu-id="95d0b-133"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="95d0b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="95d0b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95d0b-135"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95d0b-135"><dt>Replprov.dll</dt></span></span> </dl> |



 

