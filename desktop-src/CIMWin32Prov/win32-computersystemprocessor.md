---
description: Win32 \_ ComputerSystemProcessor 關聯 WMI 類別會關聯電腦系統和在該系統上執行的處理器。
ms.assetid: e630ebea-19bf-43c7-a8a0-7acfda3a752b
ms.tgt_platform: multiple
title: Win32_ComputerSystemProcessor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProcessor
- Win32_ComputerSystemProcessor.PartComponent
- Win32_ComputerSystemProcessor.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2f836d8f5e9053029763c38d2c4f2116987b08fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110348"
---
# <a name="win32_computersystemprocessor-class"></a><span data-ttu-id="99130-103">Win32 \_ ComputerSystemProcessor 類別</span><span class="sxs-lookup"><span data-stu-id="99130-103">Win32\_ComputerSystemProcessor class</span></span>

<span data-ttu-id="99130-104">**Win32 \_ ComputerSystemProcessor** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會關聯電腦系統和在該系統上執行的處理器。</span><span class="sxs-lookup"><span data-stu-id="99130-104">The **Win32\_ComputerSystemProcessor** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a computer system and a processor running on that system.</span></span>

<span data-ttu-id="99130-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="99130-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="99130-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="99130-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="99130-107">語法</span><span class="sxs-lookup"><span data-stu-id="99130-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{719A6839-C124-11d2-85E8-0000F8102E5F}"), AMENDMENT]
class Win32_ComputerSystemProcessor : Win32_SystemDevices
{
  Win32_Processor      REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="99130-108">成員</span><span class="sxs-lookup"><span data-stu-id="99130-108">Members</span></span>

<span data-ttu-id="99130-109">**Win32 \_ ComputerSystemProcessor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="99130-109">The **Win32\_ComputerSystemProcessor** class has these types of members:</span></span>

-   [<span data-ttu-id="99130-110">屬性</span><span class="sxs-lookup"><span data-stu-id="99130-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="99130-111">屬性</span><span class="sxs-lookup"><span data-stu-id="99130-111">Properties</span></span>

<span data-ttu-id="99130-112">**Win32 \_ ComputerSystemProcessor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="99130-112">The **Win32\_ComputerSystemProcessor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="99130-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="99130-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99130-114">資料類型： **Win32 \_** 未執行</span><span class="sxs-lookup"><span data-stu-id="99130-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="99130-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="99130-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99130-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI Win32 \| \_ " ) </span><span class="sxs-lookup"><span data-stu-id="99130-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="99130-117">**Win32 執行 \_** 程式描述處理器執行所在電腦系統的屬性。</span><span class="sxs-lookup"><span data-stu-id="99130-117">A **Win32\_ComputerSystem** that describes the properties of the computer system on which the processor is running.</span></span>

</dd> <dt>

<span data-ttu-id="99130-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="99130-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99130-119">資料類型： **Win32 \_ 處理器**</span><span class="sxs-lookup"><span data-stu-id="99130-119">Data type: **Win32\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="99130-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="99130-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99130-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「PartComponent」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「WMI \| Win32 處理器」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="99130-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Processor")</span></span>
</dt> </dl>

<span data-ttu-id="99130-122">[**Win32 \_ 處理器**](win32-processor.md)，描述正在執行電腦系統的處理器屬性。</span><span class="sxs-lookup"><span data-stu-id="99130-122">A [**Win32\_Processor**](win32-processor.md) that describes the properties of a processor which is running the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99130-123">備註</span><span class="sxs-lookup"><span data-stu-id="99130-123">Remarks</span></span>

<span data-ttu-id="99130-124">**Win32 \_ ComputerSystemProcessor** 類別衍生自 [**win32 \_ SystemDevices**](win32-systemdevices.md)。</span><span class="sxs-lookup"><span data-stu-id="99130-124">The **Win32\_ComputerSystemProcessor** class is derived from [**Win32\_SystemDevices**](win32-systemdevices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99130-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="99130-125">Requirements</span></span>



| <span data-ttu-id="99130-126">需求</span><span class="sxs-lookup"><span data-stu-id="99130-126">Requirement</span></span> | <span data-ttu-id="99130-127">值</span><span class="sxs-lookup"><span data-stu-id="99130-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99130-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99130-128">Minimum supported client</span></span><br/> | <span data-ttu-id="99130-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99130-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="99130-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99130-130">Minimum supported server</span></span><br/> | <span data-ttu-id="99130-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99130-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="99130-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="99130-132">Namespace</span></span><br/>                | <span data-ttu-id="99130-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="99130-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="99130-134">MOF</span><span class="sxs-lookup"><span data-stu-id="99130-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99130-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="99130-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="99130-136">DLL</span><span class="sxs-lookup"><span data-stu-id="99130-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99130-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99130-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99130-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99130-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99130-139">**Win32 \_ SystemDevices**</span><span class="sxs-lookup"><span data-stu-id="99130-139">**Win32\_SystemDevices**</span></span>](win32-systemdevices.md)
</dt> <dt>

<span data-ttu-id="99130-140">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99130-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

