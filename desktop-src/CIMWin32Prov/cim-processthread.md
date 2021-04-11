---
description: CIM \_ ProcessThread 類別代表進程與進程內容中執行之執行緒之間的連結。
ms.assetid: e71543c5-d9b3-4f98-93a6-08f977a26305
ms.tgt_platform: multiple
title: CIM_ProcessThread 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessThread
- CIM_ProcessThread.PartComponent
- CIM_ProcessThread.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: afc29d1576355eda1f9e3dfd7ed55d2cca399d5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187650"
---
# <a name="cim_processthread-class"></a><span data-ttu-id="eaf5a-103">CIM \_ ProcessThread 類別</span><span class="sxs-lookup"><span data-stu-id="eaf5a-103">CIM\_ProcessThread class</span></span>

<span data-ttu-id="eaf5a-104">**CIM \_ ProcessThread** 類別代表進程與進程內容中執行之執行緒之間的連結。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-104">The **CIM\_ProcessThread** class represents a link between a process and the threads running in the context of the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eaf5a-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eaf5a-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eaf5a-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="eaf5a-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaf5a-109">語法</span><span class="sxs-lookup"><span data-stu-id="eaf5a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{B7E6042C-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ProcessThread : CIM_Component
{
  CIM_Thread  REF PartComponent;
  CIM_Process REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="eaf5a-110">成員</span><span class="sxs-lookup"><span data-stu-id="eaf5a-110">Members</span></span>

<span data-ttu-id="eaf5a-111">**CIM \_ ProcessThread** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="eaf5a-111">The **CIM\_ProcessThread** class has these types of members:</span></span>

-   [<span data-ttu-id="eaf5a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="eaf5a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eaf5a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="eaf5a-113">Properties</span></span>

<span data-ttu-id="eaf5a-114">**CIM \_ ProcessThread** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-114">The **CIM\_ProcessThread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eaf5a-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="eaf5a-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5a-116">資料類型： **CIM \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="eaf5a-116">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5a-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eaf5a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaf5a-118">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="eaf5a-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="eaf5a-119">描述進程的 [**CIM \_ 處理**](cim-process.md) 程式。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-119">A [**CIM\_Process**](cim-process.md) that describes the process.</span></span>

</dd> <dt>

<span data-ttu-id="eaf5a-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="eaf5a-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaf5a-121">資料類型： **CIM \_ 執行緒**</span><span class="sxs-lookup"><span data-stu-id="eaf5a-121">Data type: **CIM\_Thread**</span></span>
</dt> <dt>

<span data-ttu-id="eaf5a-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eaf5a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaf5a-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) ，[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式</span><span class="sxs-lookup"><span data-stu-id="eaf5a-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="eaf5a-124">[**CIM \_ 執行緒**](cim-thread.md)，描述在進程內容中執行的執行緒。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-124">A [**CIM\_Thread**](cim-thread.md) that describes the thread running in the context of the process.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eaf5a-125">備註</span><span class="sxs-lookup"><span data-stu-id="eaf5a-125">Remarks</span></span>

<span data-ttu-id="eaf5a-126">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-126">WMI does not implement this class.</span></span>

<span data-ttu-id="eaf5a-127">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eaf5a-128">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaf5a-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="eaf5a-129">Requirements</span></span>



| <span data-ttu-id="eaf5a-130">需求</span><span class="sxs-lookup"><span data-stu-id="eaf5a-130">Requirement</span></span> | <span data-ttu-id="eaf5a-131">值</span><span class="sxs-lookup"><span data-stu-id="eaf5a-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf5a-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eaf5a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="eaf5a-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eaf5a-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eaf5a-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eaf5a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="eaf5a-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eaf5a-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eaf5a-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="eaf5a-136">Namespace</span></span><br/>                | <span data-ttu-id="eaf5a-137">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eaf5a-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eaf5a-138">MOF</span><span class="sxs-lookup"><span data-stu-id="eaf5a-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eaf5a-139"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="eaf5a-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eaf5a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="eaf5a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaf5a-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaf5a-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaf5a-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eaf5a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf5a-143">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="eaf5a-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

