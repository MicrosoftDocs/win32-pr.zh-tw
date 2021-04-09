---
description: 包含有關指定之虛擬電腦系統的資訊摘要。
ms.assetid: ab31d5db-a8d3-47bc-a024-0f4c4b93a34b
title: Msvm_ComputerSystemSummaryInformation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystemSummaryInformation
- Msvm_ComputerSystemSummaryInformation.Antecedent
- Msvm_ComputerSystemSummaryInformation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35248bcfa14609e8db25b148088b6feb8d161116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848058"
---
# <a name="msvm_computersystemsummaryinformation-class"></a><span data-ttu-id="fe0af-103">Msvm \_ ComputerSystemSummaryInformation 類別</span><span class="sxs-lookup"><span data-stu-id="fe0af-103">Msvm\_ComputerSystemSummaryInformation class</span></span>

<span data-ttu-id="fe0af-104">包含有關指定之虛擬電腦系統的資訊摘要。</span><span class="sxs-lookup"><span data-stu-id="fe0af-104">Contains an information summary about the specified virtual computer system.</span></span>

<span data-ttu-id="fe0af-105">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fe0af-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe0af-106">語法</span><span class="sxs-lookup"><span data-stu-id="fe0af-106">Syntax</span></span>

``` syntax
[Dynamic, Association, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ComputerSystemSummaryInformation : CIM_ElementView
{
  CIM_ComputerSystem          REF Antecedent;
  Msvm_SummaryInformationBase REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="fe0af-107">成員</span><span class="sxs-lookup"><span data-stu-id="fe0af-107">Members</span></span>

<span data-ttu-id="fe0af-108">**Msvm \_ ComputerSystemSummaryInformation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fe0af-108">The **Msvm\_ComputerSystemSummaryInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="fe0af-109">屬性</span><span class="sxs-lookup"><span data-stu-id="fe0af-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fe0af-110">屬性</span><span class="sxs-lookup"><span data-stu-id="fe0af-110">Properties</span></span>

<span data-ttu-id="fe0af-111">**Msvm \_ ComputerSystemSummaryInformation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fe0af-111">The **Msvm\_ComputerSystemSummaryInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe0af-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="fe0af-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe0af-113">資料類型： **CIM \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="fe0af-113">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="fe0af-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe0af-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe0af-115">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="fe0af-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="fe0af-116">[**CIM 系統 \_**](cim-computersystem.md)管理物件，此物件是 managed 資源正規化標記法中的實例。</span><span class="sxs-lookup"><span data-stu-id="fe0af-116">A [**CIM\_ComputerSystem**](cim-computersystem.md) object that is an instance in the normalized representation of the managed resource.</span></span>

> [!Note]
>
> <span data-ttu-id="fe0af-117">Msvm 中的 [**資料 \_**](msvm-computersystem.md) 類型從 Windows 10 的版本1703進行升級。</span><span class="sxs-lookup"><span data-stu-id="fe0af-117">Datatype upgraded from [**Msvm\_ComputerSystem**](msvm-computersystem.md) in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="fe0af-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="fe0af-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe0af-119">資料類型： **Msvm \_ SummaryInformationBase**</span><span class="sxs-lookup"><span data-stu-id="fe0af-119">Data type: **Msvm\_SummaryInformationBase**</span></span>
</dt> <dt>

<span data-ttu-id="fe0af-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe0af-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe0af-121">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="fe0af-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fe0af-122">[**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)的實例，代表由前一個屬性所參考的 [**Msvm \_**](msvm-computersystem.md)宏所代表之 managed 資源的反正規化或匯總視圖。</span><span class="sxs-lookup"><span data-stu-id="fe0af-122">An instance of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) that represents a de-normalized or aggregate view of the managed resource that is represented by the [**Msvm\_ComputerSystem**](msvm-computersystem.md) referenced by the Antecedent property.</span></span>

> [!Note]
>
> <span data-ttu-id="fe0af-123">在 Windows 10 1703 版中，從 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) 更新的資料類型。</span><span class="sxs-lookup"><span data-stu-id="fe0af-123">Datatype updated from [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) in Windows 10, version 1703.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe0af-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe0af-124">Requirements</span></span>



| <span data-ttu-id="fe0af-125">需求</span><span class="sxs-lookup"><span data-stu-id="fe0af-125">Requirement</span></span> | <span data-ttu-id="fe0af-126">值</span><span class="sxs-lookup"><span data-stu-id="fe0af-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe0af-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe0af-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fe0af-128">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe0af-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="fe0af-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe0af-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fe0af-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fe0af-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fe0af-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="fe0af-131">Namespace</span></span><br/>                | <span data-ttu-id="fe0af-132">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="fe0af-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fe0af-133">MOF</span><span class="sxs-lookup"><span data-stu-id="fe0af-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe0af-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="fe0af-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe0af-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fe0af-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe0af-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fe0af-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fe0af-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe0af-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe0af-138">**CIM \_ ElementView**</span><span class="sxs-lookup"><span data-stu-id="fe0af-138">**CIM\_ElementView**</span></span>](cim-elementview.md)
</dt> </dl>

 

