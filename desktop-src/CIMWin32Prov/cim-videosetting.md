---
description: CIM \_ VideoSetting 類別會將 CIM \_ VideoControllerResolution 設定物件與其套用的控制器產生關聯。
ms.assetid: 1f6742ad-ab92-4723-b691-0c3e6c0d82fa
ms.tgt_platform: multiple
title: CIM_VideoSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoSetting
- CIM_VideoSetting.Setting
- CIM_VideoSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a37fe8dd03738ae93f391a754caca84564dc6f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970344"
---
# <a name="cim_videosetting-class"></a><span data-ttu-id="96200-103">CIM \_ VideoSetting 類別</span><span class="sxs-lookup"><span data-stu-id="96200-103">CIM\_VideoSetting class</span></span>

<span data-ttu-id="96200-104">**Cim \_ VideoSetting** 類別會將 [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)設定物件與其套用的控制器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="96200-104">The **CIM\_VideoSetting** class associates the [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) setting object with the controller to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="96200-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="96200-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="96200-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="96200-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="96200-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="96200-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="96200-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="96200-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="96200-109">語法</span><span class="sxs-lookup"><span data-stu-id="96200-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCEB-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoSetting : CIM_ElementSetting
{
  CIM_VideoControllerResolution REF Setting;
  CIM_VideoController           REF Element;
};
```

## <a name="members"></a><span data-ttu-id="96200-110">成員</span><span class="sxs-lookup"><span data-stu-id="96200-110">Members</span></span>

<span data-ttu-id="96200-111">**CIM \_ VideoSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="96200-111">The **CIM\_VideoSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="96200-112">屬性</span><span class="sxs-lookup"><span data-stu-id="96200-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96200-113">屬性</span><span class="sxs-lookup"><span data-stu-id="96200-113">Properties</span></span>

<span data-ttu-id="96200-114">**CIM \_ VideoSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="96200-114">The **CIM\_VideoSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96200-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="96200-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96200-116">資料類型： **CIM \_ VideoController**</span><span class="sxs-lookup"><span data-stu-id="96200-116">Data type: **CIM\_VideoController**</span></span>
</dt> <dt>

<span data-ttu-id="96200-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="96200-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96200-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Element" ) </span><span class="sxs-lookup"><span data-stu-id="96200-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span></span>
</dt> </dl>

<span data-ttu-id="96200-119">描述影片控制器的 [**CIM \_ VideoController**](cim-videocontroller.md) 。</span><span class="sxs-lookup"><span data-stu-id="96200-119">A [**CIM\_VideoController**](cim-videocontroller.md) that describes the video controller.</span></span>

</dd> <dt>

<span data-ttu-id="96200-120">**設定**</span><span class="sxs-lookup"><span data-stu-id="96200-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96200-121">資料類型： **CIM \_ VideoControllerResolution**</span><span class="sxs-lookup"><span data-stu-id="96200-121">Data type: **CIM\_VideoControllerResolution**</span></span>
</dt> <dt>

<span data-ttu-id="96200-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="96200-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96200-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "設定" ) </span><span class="sxs-lookup"><span data-stu-id="96200-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span></span>
</dt> </dl>

<span data-ttu-id="96200-124">[**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) ，描述可為控制器設定的解析度、重新整理速率、掃描模式和色彩數目。</span><span class="sxs-lookup"><span data-stu-id="96200-124">A [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) that describes the resolutions, refresh rates, scan mode and number of colors that can be set for the Controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96200-125">備註</span><span class="sxs-lookup"><span data-stu-id="96200-125">Remarks</span></span>

<span data-ttu-id="96200-126">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="96200-126">WMI does not implement this class.</span></span> <span data-ttu-id="96200-127">針對衍生自 **CIM \_ VIDEOSETTING** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="96200-127">For WMI classes derived from **CIM\_VideoSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="96200-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="96200-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="96200-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="96200-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="96200-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="96200-130">Requirements</span></span>



| <span data-ttu-id="96200-131">需求</span><span class="sxs-lookup"><span data-stu-id="96200-131">Requirement</span></span> | <span data-ttu-id="96200-132">值</span><span class="sxs-lookup"><span data-stu-id="96200-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96200-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96200-133">Minimum supported client</span></span><br/> | <span data-ttu-id="96200-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96200-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="96200-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96200-135">Minimum supported server</span></span><br/> | <span data-ttu-id="96200-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96200-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="96200-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="96200-137">Namespace</span></span><br/>                | <span data-ttu-id="96200-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="96200-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="96200-139">MOF</span><span class="sxs-lookup"><span data-stu-id="96200-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96200-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="96200-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="96200-141">DLL</span><span class="sxs-lookup"><span data-stu-id="96200-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96200-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96200-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96200-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96200-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96200-144">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="96200-144">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

