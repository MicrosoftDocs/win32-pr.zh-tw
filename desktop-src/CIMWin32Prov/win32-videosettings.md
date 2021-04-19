---
description: Win32 \_ VideoSettings 關聯 WMI 類別會將可以套用的影片控制器和影片設定產生關聯。
ms.assetid: 0cc42352-0a89-434d-a8b6-230c677de49c
ms.tgt_platform: multiple
title: Win32_VideoSettings 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoSettings
- Win32_VideoSettings.Setting
- Win32_VideoSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 38e949b6b6501dc51b39448d72e6bf61f37fbecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970713"
---
# <a name="win32_videosettings-class"></a><span data-ttu-id="7663b-103">Win32 \_ VideoSettings 類別</span><span class="sxs-lookup"><span data-stu-id="7663b-103">Win32\_VideoSettings class</span></span>

<span data-ttu-id="7663b-104">**Win32 \_ VideoSettings** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將可以套用的影片控制器和影片設定產生關聯。</span><span class="sxs-lookup"><span data-stu-id="7663b-104">The **Win32\_VideoSettings** association [WMI class](../wmisdk/retrieving-a-class.md) relates a video controller and video settings that can be applied to it.</span></span>

<span data-ttu-id="7663b-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7663b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7663b-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="7663b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7663b-107">語法</span><span class="sxs-lookup"><span data-stu-id="7663b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEE-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoSettings : CIM_VideoSetting
{
  CIM_VideoControllerResolution REF Setting;
  Win32_VideoController         REF Element;
};
```

## <a name="members"></a><span data-ttu-id="7663b-108">成員</span><span class="sxs-lookup"><span data-stu-id="7663b-108">Members</span></span>

<span data-ttu-id="7663b-109">**Win32 \_ VideoSettings** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7663b-109">The **Win32\_VideoSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="7663b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7663b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7663b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="7663b-111">Properties</span></span>

<span data-ttu-id="7663b-112">**Win32 \_ VideoSettings** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7663b-112">The **Win32\_VideoSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7663b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7663b-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7663b-114">資料類型： **Win32 \_ VideoController**</span><span class="sxs-lookup"><span data-stu-id="7663b-114">Data type: **Win32\_VideoController**</span></span>
</dt> <dt>

<span data-ttu-id="7663b-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7663b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7663b-116">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Element" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ VideoController" ) </span><span class="sxs-lookup"><span data-stu-id="7663b-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_VideoController")</span></span>
</dt> </dl>

<span data-ttu-id="7663b-117">[**Win32 \_ VideoController**](win32-videocontroller.md) ，其中包含可用於影片設定的影片控制器屬性。</span><span class="sxs-lookup"><span data-stu-id="7663b-117">A [**Win32\_VideoController**](win32-videocontroller.md) containing the properties of the video controller that a video setting can be used on.</span></span>

</dd> <dt>

<span data-ttu-id="7663b-118">**設定**</span><span class="sxs-lookup"><span data-stu-id="7663b-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7663b-119">資料類型： **CIM \_ VideoControllerResolution**</span><span class="sxs-lookup"><span data-stu-id="7663b-119">Data type: **CIM\_VideoControllerResolution**</span></span>
</dt> <dt>

<span data-ttu-id="7663b-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7663b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7663b-121">限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "設定" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "cim \| CIM \_ VideoControllerResolution" ) </span><span class="sxs-lookup"><span data-stu-id="7663b-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_VideoControllerResolution")</span></span>
</dt> </dl>

<span data-ttu-id="7663b-122">[**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) ，包含可套用至視訊控制器的設定。</span><span class="sxs-lookup"><span data-stu-id="7663b-122">A [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) containing settings that can be applied to the video controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7663b-123">備註</span><span class="sxs-lookup"><span data-stu-id="7663b-123">Remarks</span></span>

<span data-ttu-id="7663b-124">**Win32 \_ VideoSettings** 類別衍生自 [**CIM \_ VideoSetting**](cim-videosetting.md)。</span><span class="sxs-lookup"><span data-stu-id="7663b-124">The **Win32\_VideoSettings** class is derived from [**CIM\_VideoSetting**](cim-videosetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7663b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="7663b-125">Requirements</span></span>



| <span data-ttu-id="7663b-126">需求</span><span class="sxs-lookup"><span data-stu-id="7663b-126">Requirement</span></span> | <span data-ttu-id="7663b-127">值</span><span class="sxs-lookup"><span data-stu-id="7663b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7663b-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7663b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7663b-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7663b-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7663b-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7663b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7663b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7663b-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7663b-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="7663b-132">Namespace</span></span><br/>                | <span data-ttu-id="7663b-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7663b-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7663b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7663b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7663b-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7663b-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7663b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7663b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7663b-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7663b-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7663b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7663b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7663b-139">**CIM \_ VideoSetting**</span><span class="sxs-lookup"><span data-stu-id="7663b-139">**CIM\_VideoSetting**</span></span>](cim-videosetting.md)
</dt> <dt>

[<span data-ttu-id="7663b-140">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="7663b-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
