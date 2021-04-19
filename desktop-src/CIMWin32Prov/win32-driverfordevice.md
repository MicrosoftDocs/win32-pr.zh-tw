---
description: Win32 \_ DriverForDevice 關聯 WMI 類別會建立印表機實例與印表機驅動程式實例的關聯。
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Win32_DriverForDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DriverForDevice
- Win32_DriverForDevice.Antecedent
- Win32_DriverForDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5fb384eed80c6a614af448477c50be3204d3080
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973396"
---
# <a name="win32_driverfordevice-class"></a><span data-ttu-id="acc5c-103">Win32 \_ DriverForDevice 類別</span><span class="sxs-lookup"><span data-stu-id="acc5c-103">Win32\_DriverForDevice class</span></span>

<span data-ttu-id="acc5c-104">**Win32 \_ DriverForDevice** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會建立印表機實例與印表機驅動程式實例的關聯。</span><span class="sxs-lookup"><span data-stu-id="acc5c-104">The **Win32\_DriverForDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a printer instance to a printer driver instance.</span></span>

<span data-ttu-id="acc5c-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="acc5c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="acc5c-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="acc5c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="acc5c-107">語法</span><span class="sxs-lookup"><span data-stu-id="acc5c-107">Syntax</span></span>

``` syntax
class Win32_DriverForDevice : CIM_Dependency
{
  Win32_Printer       REF Antecedent;
  Win32_PrinterDriver REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="acc5c-108">成員</span><span class="sxs-lookup"><span data-stu-id="acc5c-108">Members</span></span>

<span data-ttu-id="acc5c-109">**Win32 \_ DriverForDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="acc5c-109">The **Win32\_DriverForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="acc5c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="acc5c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="acc5c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="acc5c-111">Properties</span></span>

<span data-ttu-id="acc5c-112">**Win32 \_ DriverForDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="acc5c-112">The **Win32\_DriverForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="acc5c-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="acc5c-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acc5c-114">資料類型： **Win32 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="acc5c-114">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="acc5c-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="acc5c-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="acc5c-116">參考代表印表機的 [**Win32 \_ 印表機**](win32-printer.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="acc5c-116">Reference to the [**Win32\_Printer**](win32-printer.md) instance that represents the printer.</span></span>

<span data-ttu-id="acc5c-117">這個屬性繼承自 [**CIM 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="acc5c-117">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="acc5c-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="acc5c-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acc5c-119">資料類型： **Win32 \_ PrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="acc5c-119">Data type: **Win32\_PrinterDriver**</span></span>
</dt> <dt>

<span data-ttu-id="acc5c-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="acc5c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="acc5c-121">參考代表印表機印表機驅動程式的 [**Win32 \_ PrinterDriver**](win32-printerdriver.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="acc5c-121">Reference to the [**Win32\_PrinterDriver**](win32-printerdriver.md) instance that represents the printer driver for the printer.</span></span>

<span data-ttu-id="acc5c-122">這個屬性繼承自 [**CIM 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="acc5c-122">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="acc5c-123">備註</span><span class="sxs-lookup"><span data-stu-id="acc5c-123">Remarks</span></span>

<span data-ttu-id="acc5c-124">**Win32 \_ DriverForDevice** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="acc5c-124">The **Win32\_DriverForDevice** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="acc5c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="acc5c-125">Requirements</span></span>



| <span data-ttu-id="acc5c-126">需求</span><span class="sxs-lookup"><span data-stu-id="acc5c-126">Requirement</span></span> | <span data-ttu-id="acc5c-127">值</span><span class="sxs-lookup"><span data-stu-id="acc5c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="acc5c-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="acc5c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="acc5c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="acc5c-129">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="acc5c-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="acc5c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="acc5c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acc5c-131">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="acc5c-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="acc5c-132">Namespace</span></span><br/>                | <span data-ttu-id="acc5c-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="acc5c-133">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="acc5c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="acc5c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="acc5c-135"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="acc5c-135"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="acc5c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="acc5c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acc5c-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acc5c-137"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="acc5c-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="acc5c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acc5c-139">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="acc5c-139">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

