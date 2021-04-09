---
description: Win32 \_ SessionResource 關聯表示會話與會話提供存取權的資源之間的關聯性。
ms.assetid: 39c195cf-e70b-4e93-b46b-61ed4f08f57e
ms.tgt_platform: multiple
title: Win32_SessionResource 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionResource
- Win32_SessionResource.Antecedent
- Win32_SessionResource.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 3962c8523863bb97710bf21be38906d3897beea3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689071"
---
# <a name="win32_sessionresource-class"></a><span data-ttu-id="31cae-103">Win32 \_ SessionResource 類別</span><span class="sxs-lookup"><span data-stu-id="31cae-103">Win32\_SessionResource class</span></span>

<span data-ttu-id="31cae-104">Win32 \_ SessionResource 關聯表示會話與會話提供存取權的資源之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="31cae-104">The Win32\_SessionResource association represents the relationship between a session and the resources that the session provides access to.</span></span>

<span data-ttu-id="31cae-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="31cae-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="31cae-106">語法</span><span class="sxs-lookup"><span data-stu-id="31cae-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_SessionResource : CIM_Dependency
{
  Win32_LogicalElement REF Antecedent;
  Win32_Session        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="31cae-107">成員</span><span class="sxs-lookup"><span data-stu-id="31cae-107">Members</span></span>

<span data-ttu-id="31cae-108">**Win32 \_ SessionResource** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="31cae-108">The **Win32\_SessionResource** class has these types of members:</span></span>

-   [<span data-ttu-id="31cae-109">屬性</span><span class="sxs-lookup"><span data-stu-id="31cae-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31cae-110">屬性</span><span class="sxs-lookup"><span data-stu-id="31cae-110">Properties</span></span>

<span data-ttu-id="31cae-111">**Win32 \_ SessionResource** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="31cae-111">The **Win32\_SessionResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31cae-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="31cae-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31cae-113">資料類型： **Win32 \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="31cae-113">Data type: **Win32\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="31cae-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31cae-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31cae-115">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="31cae-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="31cae-116">前面的參考代表此會話所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="31cae-116">The Antecedent reference represents resources used by this session.</span></span>

</dd> <dt>

<span data-ttu-id="31cae-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="31cae-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31cae-118">資料類型： **Win32 \_ 會話**</span><span class="sxs-lookup"><span data-stu-id="31cae-118">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="31cae-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31cae-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31cae-120">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="31cae-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="31cae-121">相依參考代表使用資源的會話。</span><span class="sxs-lookup"><span data-stu-id="31cae-121">The Dependent reference represents the session using the resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31cae-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="31cae-122">Requirements</span></span>



| <span data-ttu-id="31cae-123">需求</span><span class="sxs-lookup"><span data-stu-id="31cae-123">Requirement</span></span> | <span data-ttu-id="31cae-124">值</span><span class="sxs-lookup"><span data-stu-id="31cae-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31cae-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31cae-125">Minimum supported client</span></span><br/> | <span data-ttu-id="31cae-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31cae-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31cae-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31cae-127">Minimum supported server</span></span><br/> | <span data-ttu-id="31cae-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31cae-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31cae-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="31cae-129">Namespace</span></span><br/>                | <span data-ttu-id="31cae-130">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="31cae-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="31cae-131">MOF</span><span class="sxs-lookup"><span data-stu-id="31cae-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31cae-132"><dt>CimWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="31cae-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="31cae-133">DLL</span><span class="sxs-lookup"><span data-stu-id="31cae-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31cae-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31cae-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31cae-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31cae-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31cae-136">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="31cae-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

 
