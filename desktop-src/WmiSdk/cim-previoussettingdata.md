---
description: 虛擬系統與快照集（虛擬系統的父系）間的設定資料之間的關聯。
ms.assetid: d11e00e0-a163-49ea-b8ef-e3909a7dc83f
ms.tgt_platform: multiple
title: CIM_PreviousSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PreviousSettingData
- Root\CIMV2.CIM_PreviousSettingData.Target
- Root\CIMV2.CIM_PreviousSettingData.PreviousObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 4422d590714b82120b610dc4eeb9377a385519d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987073"
---
# <a name="cim_previoussettingdata-class"></a><span data-ttu-id="f3bd3-103">CIM \_ PreviousSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="f3bd3-103">CIM\_PreviousSettingData class</span></span>

<span data-ttu-id="f3bd3-104">虛擬系統與快照集（虛擬系統的父系）間的設定資料之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="f3bd3-104">An association between a virtual system and the setting data of the snapshot which is the parent to the virtual system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f3bd3-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="f3bd3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f3bd3-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="f3bd3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f3bd3-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3bd3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3bd3-108">語法</span><span class="sxs-lookup"><span data-stu-id="f3bd3-108">Syntax</span></span>

``` syntax
class CIM_PreviousSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF PreviousObject;
};
```

## <a name="members"></a><span data-ttu-id="f3bd3-109">成員</span><span class="sxs-lookup"><span data-stu-id="f3bd3-109">Members</span></span>

<span data-ttu-id="f3bd3-110">**CIM \_ PreviousSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f3bd3-110">The **CIM\_PreviousSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f3bd3-111">屬性</span><span class="sxs-lookup"><span data-stu-id="f3bd3-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3bd3-112">屬性</span><span class="sxs-lookup"><span data-stu-id="f3bd3-112">Properties</span></span>

<span data-ttu-id="f3bd3-113">**CIM \_ PreviousSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f3bd3-113">The **CIM\_PreviousSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3bd3-114">**PreviousObject**</span><span class="sxs-lookup"><span data-stu-id="f3bd3-114">**PreviousObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3bd3-115">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="f3bd3-115">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="f3bd3-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3bd3-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3bd3-117">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="f3bd3-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f3bd3-118">此電腦系統父系的快照集設定資料。</span><span class="sxs-lookup"><span data-stu-id="f3bd3-118">The snapshot setting data that is the parent of this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="f3bd3-119">**Target**</span><span class="sxs-lookup"><span data-stu-id="f3bd3-119">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3bd3-120">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="f3bd3-120">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="f3bd3-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3bd3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3bd3-122">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="f3bd3-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f3bd3-123">應用程式目標的電腦系統。</span><span class="sxs-lookup"><span data-stu-id="f3bd3-123">The computer system that was the target of the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3bd3-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3bd3-124">Requirements</span></span>



| <span data-ttu-id="f3bd3-125">需求</span><span class="sxs-lookup"><span data-stu-id="f3bd3-125">Requirement</span></span> | <span data-ttu-id="f3bd3-126">值</span><span class="sxs-lookup"><span data-stu-id="f3bd3-126">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="f3bd3-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="f3bd3-127">Namespace</span></span><br/> | <span data-ttu-id="f3bd3-128">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f3bd3-128">Root\\CIMV2</span></span><br/> |



 

 




