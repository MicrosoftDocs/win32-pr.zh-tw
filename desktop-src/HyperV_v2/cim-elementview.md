---
description: 表示和相關檢視，以及表示 managed 資源正規化視圖的實例。
ms.assetid: 9c6eb3d5-7366-4954-9e64-12f889c64114
title: CIM_ElementView 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementView
- CIM_ElementView.Antecedent
- CIM_ElementView.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ffc0e4b69667800b1880cae1a992a207cc95a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998506"
---
# <a name="cim_elementview-class"></a><span data-ttu-id="c9051-103">CIM \_ ElementView 類別</span><span class="sxs-lookup"><span data-stu-id="c9051-103">CIM\_ElementView class</span></span>

<span data-ttu-id="c9051-104">表示和相關檢視，以及表示 managed 資源正規化視圖的實例。</span><span class="sxs-lookup"><span data-stu-id="c9051-104">Represents and association between a view, and an instance that represents the normalized view of a managed resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9051-105">語法</span><span class="sxs-lookup"><span data-stu-id="c9051-105">Syntax</span></span>

``` syntax
[Abstract, Association, Experimental, Version("2.21.1"), UMLPackagePath("CIM::Core::CoreElements")]
class CIM_ElementView : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_View           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c9051-106">成員</span><span class="sxs-lookup"><span data-stu-id="c9051-106">Members</span></span>

<span data-ttu-id="c9051-107">**CIM \_ ElementView** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c9051-107">The **CIM\_ElementView** class has these types of members:</span></span>

-   [<span data-ttu-id="c9051-108">屬性</span><span class="sxs-lookup"><span data-stu-id="c9051-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9051-109">屬性</span><span class="sxs-lookup"><span data-stu-id="c9051-109">Properties</span></span>

<span data-ttu-id="c9051-110">**CIM \_ ElementView** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c9051-110">The **CIM\_ElementView** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9051-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="c9051-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9051-112">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="c9051-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="c9051-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c9051-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9051-114">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="c9051-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c9051-115">表示 managed 資源正規化視圖的實例。</span><span class="sxs-lookup"><span data-stu-id="c9051-115">The instance that represents the normalized view of the managed resource.</span></span>

</dd> <dt>

<span data-ttu-id="c9051-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="c9051-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9051-117">資料類型： **CIM \_ View**</span><span class="sxs-lookup"><span data-stu-id="c9051-117">Data type: **CIM\_View**</span></span>
</dt> <dt>

<span data-ttu-id="c9051-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c9051-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9051-119">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="c9051-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c9051-120">代表 managed 資源的已取消正規化或匯總視圖的視圖。</span><span class="sxs-lookup"><span data-stu-id="c9051-120">The view that represents a de-normalized or aggregate view of the managed resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9051-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9051-121">Requirements</span></span>



| <span data-ttu-id="c9051-122">需求</span><span class="sxs-lookup"><span data-stu-id="c9051-122">Requirement</span></span> | <span data-ttu-id="c9051-123">值</span><span class="sxs-lookup"><span data-stu-id="c9051-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9051-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9051-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c9051-125">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9051-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c9051-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9051-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c9051-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c9051-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c9051-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="c9051-128">Namespace</span></span><br/>                | <span data-ttu-id="c9051-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="c9051-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c9051-130">MOF</span><span class="sxs-lookup"><span data-stu-id="c9051-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9051-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c9051-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9051-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c9051-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9051-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c9051-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c9051-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9051-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9051-135">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="c9051-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

