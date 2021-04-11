---
description: CIM \_ CollectionSetting 類別代表 cim \_ CollectionOfMSEs 和為其定義的設定類別之間的關聯。
ms.assetid: f09bd656-5fdd-4ab1-8ef9-52d431a5117d
ms.tgt_platform: multiple
title: CIM_CollectionSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionSetting
- CIM_CollectionSetting.Collection
- CIM_CollectionSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c290225ee38008f0345b695af794e57f311f2998
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847402"
---
# <a name="cim_collectionsetting-class"></a><span data-ttu-id="f3c7b-103">CIM \_ CollectionSetting 類別</span><span class="sxs-lookup"><span data-stu-id="f3c7b-103">CIM\_CollectionSetting class</span></span>

<span data-ttu-id="f3c7b-104">**Cim \_ CollectionSetting** 類別代表 [**cim \_ CollectionOfMSEs**](cim-collectionofmses.md)和為其定義的設定類別之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="f3c7b-104">The **CIM\_CollectionSetting** class represents the association between a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) and the setting class defined for them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f3c7b-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="f3c7b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f3c7b-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="f3c7b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f3c7b-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3c7b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f3c7b-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="f3c7b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3c7b-109">語法</span><span class="sxs-lookup"><span data-stu-id="f3c7b-109">Syntax</span></span>

``` syntax
class CIM_CollectionSetting
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="f3c7b-110">成員</span><span class="sxs-lookup"><span data-stu-id="f3c7b-110">Members</span></span>

<span data-ttu-id="f3c7b-111">**CIM \_ CollectionSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f3c7b-111">The **CIM\_CollectionSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="f3c7b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="f3c7b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3c7b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="f3c7b-113">Properties</span></span>

<span data-ttu-id="f3c7b-114">**CIM \_ CollectionSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f3c7b-114">The **CIM\_CollectionSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3c7b-115">**集合**</span><span class="sxs-lookup"><span data-stu-id="f3c7b-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3c7b-116">資料類型： **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="f3c7b-116">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="f3c7b-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3c7b-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3c7b-118">[**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md)類別的參考。</span><span class="sxs-lookup"><span data-stu-id="f3c7b-118">Reference to the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f3c7b-119">**設定**</span><span class="sxs-lookup"><span data-stu-id="f3c7b-119">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3c7b-120">資料類型： **CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="f3c7b-120">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="f3c7b-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3c7b-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3c7b-122">與 **集合** 屬性相關聯之 **設定** 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="f3c7b-122">Reference to the **Setting** object associated with the **Collection** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3c7b-123">備註</span><span class="sxs-lookup"><span data-stu-id="f3c7b-123">Remarks</span></span>

<span data-ttu-id="f3c7b-124">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="f3c7b-124">WMI does not implement this class.</span></span> <span data-ttu-id="f3c7b-125">如需衍生自 **CIM \_ COLLECTIONSETTING** 之 WMI 類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="f3c7b-125">For more information about WMI classes derived from **CIM\_CollectionSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f3c7b-126">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="f3c7b-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f3c7b-127">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f3c7b-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3c7b-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3c7b-128">Requirements</span></span>



| <span data-ttu-id="f3c7b-129">需求</span><span class="sxs-lookup"><span data-stu-id="f3c7b-129">Requirement</span></span> | <span data-ttu-id="f3c7b-130">值</span><span class="sxs-lookup"><span data-stu-id="f3c7b-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c7b-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3c7b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f3c7b-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3c7b-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f3c7b-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3c7b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f3c7b-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3c7b-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f3c7b-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="f3c7b-135">Namespace</span></span><br/>                | <span data-ttu-id="f3c7b-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f3c7b-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f3c7b-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f3c7b-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3c7b-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3c7b-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3c7b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f3c7b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3c7b-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3c7b-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




