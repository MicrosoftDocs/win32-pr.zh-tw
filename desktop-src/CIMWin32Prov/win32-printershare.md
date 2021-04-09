---
description: Win32 \_ PrinterShare 關聯 WMI 類別會建立本機印表機和共用的關聯，因為它是透過網路來查看。
ms.assetid: 9ac99e52-5e8f-4329-960f-7bd1fd229e37
ms.tgt_platform: multiple
title: Win32_PrinterShare 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterShare
- Win32_PrinterShare.Antecedent
- Win32_PrinterShare.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57bc15fc5d3db78179335b039851d7d3b7cbf8a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847480"
---
# <a name="win32_printershare-class"></a><span data-ttu-id="dcdaa-103">Win32 \_ PrinterShare 類別</span><span class="sxs-lookup"><span data-stu-id="dcdaa-103">Win32\_PrinterShare class</span></span>

<span data-ttu-id="dcdaa-104">**Win32 \_ PrinterShare** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會建立本機印表機和共用的關聯，因為它是透過網路來查看。</span><span class="sxs-lookup"><span data-stu-id="dcdaa-104">The **Win32\_PrinterShare** association [WMI class](../wmisdk/retrieving-a-class.md) relates a local printer and the share that represents it as it is viewed over a network.</span></span>

<span data-ttu-id="dcdaa-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="dcdaa-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dcdaa-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="dcdaa-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcdaa-107">語法</span><span class="sxs-lookup"><span data-stu-id="dcdaa-107">Syntax</span></span>

``` syntax
class Win32_PrinterShare : CIM_Dependency
{
  Win32_Printer REF Antecedent;
  Win32_Share   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="dcdaa-108">成員</span><span class="sxs-lookup"><span data-stu-id="dcdaa-108">Members</span></span>

<span data-ttu-id="dcdaa-109">**Win32 \_ PrinterShare** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dcdaa-109">The **Win32\_PrinterShare** class has these types of members:</span></span>

-   [<span data-ttu-id="dcdaa-110">屬性</span><span class="sxs-lookup"><span data-stu-id="dcdaa-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dcdaa-111">屬性</span><span class="sxs-lookup"><span data-stu-id="dcdaa-111">Properties</span></span>

<span data-ttu-id="dcdaa-112">**Win32 \_ PrinterShare** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="dcdaa-112">The **Win32\_PrinterShare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dcdaa-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="dcdaa-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcdaa-114">資料類型： **Win32 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="dcdaa-114">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="dcdaa-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dcdaa-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dcdaa-116">限定詞：索引 [**鍵**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dcdaa-116">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dcdaa-117">代表此關聯中共用之本機印表機的實例參考。</span><span class="sxs-lookup"><span data-stu-id="dcdaa-117">Reference to the instance representing the local printer shared in this association.</span></span>

</dd> <dt>

<span data-ttu-id="dcdaa-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="dcdaa-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcdaa-119">資料類型： **Win32 \_ 共用**</span><span class="sxs-lookup"><span data-stu-id="dcdaa-119">Data type: **Win32\_Share**</span></span>
</dt> <dt>

<span data-ttu-id="dcdaa-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dcdaa-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dcdaa-121">限定詞：索引 [**鍵**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dcdaa-121">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dcdaa-122">代表此關聯中的印表機共用之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="dcdaa-122">Reference to the instance representing the share of the printer in this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dcdaa-123">備註</span><span class="sxs-lookup"><span data-stu-id="dcdaa-123">Remarks</span></span>

<span data-ttu-id="dcdaa-124">**Win32 \_ PrinterShare** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="dcdaa-124">The **Win32\_PrinterShare** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dcdaa-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcdaa-125">Requirements</span></span>



| <span data-ttu-id="dcdaa-126">需求</span><span class="sxs-lookup"><span data-stu-id="dcdaa-126">Requirement</span></span> | <span data-ttu-id="dcdaa-127">值</span><span class="sxs-lookup"><span data-stu-id="dcdaa-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcdaa-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dcdaa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dcdaa-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dcdaa-129">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="dcdaa-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dcdaa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dcdaa-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dcdaa-131">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="dcdaa-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="dcdaa-132">Namespace</span></span><br/>                | <span data-ttu-id="dcdaa-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dcdaa-133">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="dcdaa-134">MOF</span><span class="sxs-lookup"><span data-stu-id="dcdaa-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcdaa-135"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="dcdaa-135"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="dcdaa-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dcdaa-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcdaa-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcdaa-137"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="dcdaa-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dcdaa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcdaa-139">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="dcdaa-139">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
