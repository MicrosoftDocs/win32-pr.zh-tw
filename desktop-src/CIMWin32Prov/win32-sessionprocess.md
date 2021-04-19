---
description: Win32 \_ SessionProcess 關聯 WMI 類別代表登入會話與與該會話相關聯之進程之間的關聯。
ms.assetid: 19d4ecf9-27b5-4a0b-9c76-7d10679aaf5e
ms.tgt_platform: multiple
title: Win32_SessionProcess 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionProcess
- Win32_SessionProcess.Antecedent
- Win32_SessionProcess.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f4090da88e8f5d31b0940b0c7d217a930a364b63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986245"
---
# <a name="win32_sessionprocess-class"></a><span data-ttu-id="8e475-103">Win32 \_ SessionProcess 類別</span><span class="sxs-lookup"><span data-stu-id="8e475-103">Win32\_SessionProcess class</span></span>

<span data-ttu-id="8e475-104">**Win32 \_ SessionProcess** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)代表登入會話與與該會話相關聯之進程之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="8e475-104">The **Win32\_SessionProcess** association [WMI class](../wmisdk/retrieving-a-class.md) represents an association between a logon session and the processes associated with that session.</span></span>

<span data-ttu-id="8e475-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8e475-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8e475-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="8e475-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e475-107">語法</span><span class="sxs-lookup"><span data-stu-id="8e475-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("9CD8E1CE-0D27-4a41-AADE-F8D200230FF4"), AMENDMENT]
class Win32_SessionProcess : Win32_SessionResource
{
  Win32_LogonSession REF Antecedent;
  Win32_Process      REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="8e475-108">成員</span><span class="sxs-lookup"><span data-stu-id="8e475-108">Members</span></span>

<span data-ttu-id="8e475-109">**Win32 \_ SessionProcess** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8e475-109">The **Win32\_SessionProcess** class has these types of members:</span></span>

-   [<span data-ttu-id="8e475-110">屬性</span><span class="sxs-lookup"><span data-stu-id="8e475-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e475-111">屬性</span><span class="sxs-lookup"><span data-stu-id="8e475-111">Properties</span></span>

<span data-ttu-id="8e475-112">**Win32 \_ SessionProcess** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8e475-112">The **Win32\_SessionProcess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e475-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="8e475-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e475-114">資料類型： **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="8e475-114">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="8e475-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e475-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e475-116">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Antecedent" ) ， [**Key**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="8e475-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="8e475-117">[**Win32 \_ LogonSession**](win32-logonsessionmappeddisk.md) ，表示與進程相關的會話。</span><span class="sxs-lookup"><span data-stu-id="8e475-117">A [**Win32\_LogonSession**](win32-logonsessionmappeddisk.md) that represents the session which is related to the process.</span></span>

</dd> <dt>

<span data-ttu-id="8e475-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="8e475-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e475-119">資料類型： **Win32 \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="8e475-119">Data type: **Win32\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="8e475-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e475-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e475-121">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( 「相依」 ) ，索引 [**鍵**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="8e475-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="8e475-122">[**Win32 \_ 進程**](win32-processor.md)，表示與會話相關聯的進程。</span><span class="sxs-lookup"><span data-stu-id="8e475-122">A [**Win32\_Process**](win32-processor.md) that represents the process associated with the session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e475-123">備註</span><span class="sxs-lookup"><span data-stu-id="8e475-123">Remarks</span></span>

<span data-ttu-id="8e475-124">**Win32 \_** 當系統管理員已提高許可權或從遠端執行時，SessionProcess 會傳回系統管理員的所有會話。</span><span class="sxs-lookup"><span data-stu-id="8e475-124">**Win32\_SessionProcess** returns all session for the administrator when logged in elevated or when run remotely.</span></span> <span data-ttu-id="8e475-125">這是類別行為的延伸。</span><span class="sxs-lookup"><span data-stu-id="8e475-125">This is an extension to the behavior of the class.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e475-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e475-126">Requirements</span></span>



| <span data-ttu-id="8e475-127">需求</span><span class="sxs-lookup"><span data-stu-id="8e475-127">Requirement</span></span> | <span data-ttu-id="8e475-128">值</span><span class="sxs-lookup"><span data-stu-id="8e475-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e475-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e475-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8e475-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e475-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e475-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e475-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8e475-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e475-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e475-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="8e475-133">Namespace</span></span><br/>                | <span data-ttu-id="8e475-134">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8e475-134">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e475-135">MOF</span><span class="sxs-lookup"><span data-stu-id="8e475-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e475-136"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e475-136"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e475-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8e475-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e475-138"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e475-138"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e475-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e475-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e475-140">**Win32 \_ SessionResource**</span><span class="sxs-lookup"><span data-stu-id="8e475-140">**Win32\_SessionResource**</span></span>](win32-sessionresource.md)
</dt> <dt>

[<span data-ttu-id="8e475-141">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="8e475-141">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
