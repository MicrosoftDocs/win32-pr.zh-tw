---
description: 物件與另一個已套用至它的物件之間的關聯。
ms.assetid: ee6b17b7-4f01-4731-8d6b-a3421621a75a
ms.tgt_platform: multiple
title: CIM_LastAppliedSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSettingData
- Root\CIMV2.CIM_LastAppliedSettingData.Target
- Root\CIMV2.CIM_LastAppliedSettingData.AppliedObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: fbad71cd88992673af5dd60c04b92dd3c833e5b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989268"
---
# <a name="cim_lastappliedsettingdata-class"></a><span data-ttu-id="16cf1-103">CIM \_ LastAppliedSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="16cf1-103">CIM\_LastAppliedSettingData class</span></span>

<span data-ttu-id="16cf1-104">物件與另一個已套用至它的物件之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="16cf1-104">An association between an object and another object which has been applied to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="16cf1-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="16cf1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="16cf1-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="16cf1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="16cf1-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="16cf1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="16cf1-108">語法</span><span class="sxs-lookup"><span data-stu-id="16cf1-108">Syntax</span></span>

``` syntax
class CIM_LastAppliedSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF AppliedObject;
};
```

## <a name="members"></a><span data-ttu-id="16cf1-109">成員</span><span class="sxs-lookup"><span data-stu-id="16cf1-109">Members</span></span>

<span data-ttu-id="16cf1-110">**CIM \_ LastAppliedSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="16cf1-110">The **CIM\_LastAppliedSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="16cf1-111">屬性</span><span class="sxs-lookup"><span data-stu-id="16cf1-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16cf1-112">屬性</span><span class="sxs-lookup"><span data-stu-id="16cf1-112">Properties</span></span>

<span data-ttu-id="16cf1-113">**CIM \_ LastAppliedSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="16cf1-113">The **CIM\_LastAppliedSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16cf1-114">**AppliedObject**</span><span class="sxs-lookup"><span data-stu-id="16cf1-114">**AppliedObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16cf1-115">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="16cf1-115">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="16cf1-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16cf1-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16cf1-117">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="16cf1-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="16cf1-118">套用至目標物件的物件。</span><span class="sxs-lookup"><span data-stu-id="16cf1-118">The object that was applied to the target object.</span></span>

</dd> <dt>

<span data-ttu-id="16cf1-119">**Target**</span><span class="sxs-lookup"><span data-stu-id="16cf1-119">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16cf1-120">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="16cf1-120">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="16cf1-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16cf1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16cf1-122">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="16cf1-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="16cf1-123">物件，該物件為物件之應用程式的目標。</span><span class="sxs-lookup"><span data-stu-id="16cf1-123">The object that was the target of the object's application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16cf1-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="16cf1-124">Requirements</span></span>



| <span data-ttu-id="16cf1-125">需求</span><span class="sxs-lookup"><span data-stu-id="16cf1-125">Requirement</span></span> | <span data-ttu-id="16cf1-126">值</span><span class="sxs-lookup"><span data-stu-id="16cf1-126">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="16cf1-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="16cf1-127">Namespace</span></span><br/> | <span data-ttu-id="16cf1-128">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="16cf1-128">Root\\CIMV2</span></span><br/> |



 

 




