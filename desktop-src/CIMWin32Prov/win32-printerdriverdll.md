---
description: Win32 \_ PrinterDriverDll 關聯 WMI 類別會建立本機印表機及其驅動程式檔案的關聯。
ms.assetid: decbd1de-8091-47f7-94a1-42862070b920
ms.tgt_platform: multiple
title: Win32_PrinterDriverDll 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriverDll
- Win32_PrinterDriverDll.Antecedent
- Win32_PrinterDriverDll.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41484c39d9e1b59efd79d7aee08719b3a241de97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468433"
---
# <a name="win32_printerdriverdll-class"></a><span data-ttu-id="78c74-103">Win32 \_ PrinterDriverDll 類別</span><span class="sxs-lookup"><span data-stu-id="78c74-103">Win32\_PrinterDriverDll class</span></span>

<span data-ttu-id="78c74-104">**Win32 \_ PrinterDriverDll** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會建立本機印表機及其驅動程式檔案的關聯。</span><span class="sxs-lookup"><span data-stu-id="78c74-104">The **Win32\_PrinterDriverDll** association [WMI class](../wmisdk/retrieving-a-class.md) relates a local printer and its driver file.</span></span>

<span data-ttu-id="78c74-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="78c74-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="78c74-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="78c74-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="78c74-107">語法</span><span class="sxs-lookup"><span data-stu-id="78c74-107">Syntax</span></span>

``` syntax
class Win32_PrinterDriverDll : CIM_Dependency
{
  CIM_DataFile  REF Antecedent;
  Win32_Printer REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="78c74-108">成員</span><span class="sxs-lookup"><span data-stu-id="78c74-108">Members</span></span>

<span data-ttu-id="78c74-109">**Win32 \_ PrinterDriverDll** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="78c74-109">The **Win32\_PrinterDriverDll** class has these types of members:</span></span>

-   [<span data-ttu-id="78c74-110">屬性</span><span class="sxs-lookup"><span data-stu-id="78c74-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78c74-111">屬性</span><span class="sxs-lookup"><span data-stu-id="78c74-111">Properties</span></span>

<span data-ttu-id="78c74-112">**Win32 \_ PrinterDriverDll** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="78c74-112">The **Win32\_PrinterDriverDll** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78c74-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="78c74-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c74-114">資料類型： **CIM 資料 \_ 檔**</span><span class="sxs-lookup"><span data-stu-id="78c74-114">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="78c74-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78c74-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78c74-116">限定詞：索引 [**鍵**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="78c74-116">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="78c74-117">參考 [**CIM \_ 資料檔案**](cim-datafile.md) 實例，表示此 Windows 印表機的驅動程式檔案。</span><span class="sxs-lookup"><span data-stu-id="78c74-117">Reference to the [**CIM\_DataFile**](cim-datafile.md) instance representing the driver file for this Windows-based printer.</span></span>

<span data-ttu-id="78c74-118">這個屬性繼承自 [**CIM 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="78c74-118">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="78c74-119">**依賴**</span><span class="sxs-lookup"><span data-stu-id="78c74-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78c74-120">資料類型： **Win32 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="78c74-120">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="78c74-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78c74-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78c74-122">限定詞：索引 [**鍵**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="78c74-122">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="78c74-123">[**Win32 \_ 印表機**](win32-printer.md)實例的參考。</span><span class="sxs-lookup"><span data-stu-id="78c74-123">Reference to the [**Win32\_Printer**](win32-printer.md) instance.</span></span>

<span data-ttu-id="78c74-124">這個屬性繼承自 [**CIM 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="78c74-124">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78c74-125">備註</span><span class="sxs-lookup"><span data-stu-id="78c74-125">Remarks</span></span>

<span data-ttu-id="78c74-126">**Win32 \_ PrinterDriverDll** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="78c74-126">The **Win32\_PrinterDriverDll** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78c74-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="78c74-127">Requirements</span></span>



| <span data-ttu-id="78c74-128">需求</span><span class="sxs-lookup"><span data-stu-id="78c74-128">Requirement</span></span> | <span data-ttu-id="78c74-129">值</span><span class="sxs-lookup"><span data-stu-id="78c74-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="78c74-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78c74-130">Minimum supported client</span></span><br/> | <span data-ttu-id="78c74-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78c74-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="78c74-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78c74-132">Minimum supported server</span></span><br/> | <span data-ttu-id="78c74-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78c74-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="78c74-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="78c74-134">Namespace</span></span><br/>                | <span data-ttu-id="78c74-135">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="78c74-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="78c74-136">MOF</span><span class="sxs-lookup"><span data-stu-id="78c74-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78c74-137"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="78c74-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="78c74-138">DLL</span><span class="sxs-lookup"><span data-stu-id="78c74-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78c74-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78c74-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="78c74-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78c74-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c74-141">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="78c74-141">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="78c74-142">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="78c74-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
