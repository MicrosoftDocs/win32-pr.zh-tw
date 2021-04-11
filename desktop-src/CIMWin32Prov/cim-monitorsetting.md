---
description: CIM \_ MonitorSetting 類別會將監視器解析度與其套用的桌面監視器產生關聯。
ms.assetid: 4bf0b2d5-b901-4294-a33b-9c8a87785af0
ms.tgt_platform: multiple
title: CIM_MonitorSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorSetting
- CIM_MonitorSetting.Setting
- CIM_MonitorSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc947f4bb484ec5392204747e583fbf80bbf88cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847394"
---
# <a name="cim_monitorsetting-class"></a><span data-ttu-id="3e4b5-103">CIM \_ MonitorSetting 類別</span><span class="sxs-lookup"><span data-stu-id="3e4b5-103">CIM\_MonitorSetting class</span></span>

<span data-ttu-id="3e4b5-104">**CIM \_ MonitorSetting** 類別會將監視器解析度與其套用的桌面監視器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="3e4b5-104">The **CIM\_MonitorSetting** class associates the monitor resolution with the desktop monitor to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e4b5-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="3e4b5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3e4b5-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="3e4b5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3e4b5-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3e4b5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3e4b5-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="3e4b5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e4b5-109">語法</span><span class="sxs-lookup"><span data-stu-id="3e4b5-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCED-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorSetting : CIM_ElementSetting
{
  CIM_MonitorResolution REF Setting;
  CIM_DesktopMonitor    REF Element;
};
```

## <a name="members"></a><span data-ttu-id="3e4b5-110">成員</span><span class="sxs-lookup"><span data-stu-id="3e4b5-110">Members</span></span>

<span data-ttu-id="3e4b5-111">**CIM \_ MonitorSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3e4b5-111">The **CIM\_MonitorSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="3e4b5-112">屬性</span><span class="sxs-lookup"><span data-stu-id="3e4b5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e4b5-113">屬性</span><span class="sxs-lookup"><span data-stu-id="3e4b5-113">Properties</span></span>

<span data-ttu-id="3e4b5-114">**CIM \_ MonitorSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3e4b5-114">The **CIM\_MonitorSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e4b5-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="3e4b5-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e4b5-116">資料類型： **CIM \_ DesktopMonitor**</span><span class="sxs-lookup"><span data-stu-id="3e4b5-116">Data type: **CIM\_DesktopMonitor**</span></span>
</dt> <dt>

<span data-ttu-id="3e4b5-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e4b5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e4b5-118">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Element" ) </span><span class="sxs-lookup"><span data-stu-id="3e4b5-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span></span>
</dt> </dl>

<span data-ttu-id="3e4b5-119">描述桌面監視器的 [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md) 。</span><span class="sxs-lookup"><span data-stu-id="3e4b5-119">A [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) describing the desktop monitor.</span></span>

</dd> <dt>

<span data-ttu-id="3e4b5-120">**設定**</span><span class="sxs-lookup"><span data-stu-id="3e4b5-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e4b5-121">資料類型： **CIM \_ MonitorResolution**</span><span class="sxs-lookup"><span data-stu-id="3e4b5-121">Data type: **CIM\_MonitorResolution**</span></span>
</dt> <dt>

<span data-ttu-id="3e4b5-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e4b5-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e4b5-123">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "設定" ) </span><span class="sxs-lookup"><span data-stu-id="3e4b5-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span></span>
</dt> </dl>

<span data-ttu-id="3e4b5-124">[**CIM \_ MonitorResolution**](cim-monitorresolution.md) ，描述與桌面監視器相關聯的監視器解析度。</span><span class="sxs-lookup"><span data-stu-id="3e4b5-124">A [**CIM\_MonitorResolution**](cim-monitorresolution.md) describing the monitor resolution associated with the desktop monitor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e4b5-125">備註</span><span class="sxs-lookup"><span data-stu-id="3e4b5-125">Remarks</span></span>

<span data-ttu-id="3e4b5-126">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="3e4b5-126">WMI does not implement this class.</span></span>

<span data-ttu-id="3e4b5-127">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="3e4b5-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3e4b5-128">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3e4b5-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e4b5-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e4b5-129">Requirements</span></span>



| <span data-ttu-id="3e4b5-130">需求</span><span class="sxs-lookup"><span data-stu-id="3e4b5-130">Requirement</span></span> | <span data-ttu-id="3e4b5-131">值</span><span class="sxs-lookup"><span data-stu-id="3e4b5-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e4b5-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e4b5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3e4b5-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e4b5-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e4b5-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e4b5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3e4b5-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e4b5-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e4b5-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="3e4b5-136">Namespace</span></span><br/>                | <span data-ttu-id="3e4b5-137">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3e4b5-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3e4b5-138">MOF</span><span class="sxs-lookup"><span data-stu-id="3e4b5-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e4b5-139"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e4b5-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e4b5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3e4b5-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e4b5-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e4b5-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e4b5-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e4b5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e4b5-143">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="3e4b5-143">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

