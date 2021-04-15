---
description: Win32 \_ >a 關聯會定義會話之間的關聯性，其中一個會話屬於或利用另一個會話，例如，終端機會話使用登入會話。
ms.assetid: 2269de22-b086-4f71-8b19-bc53e1c88dc7
ms.tgt_platform: multiple
title: Win32_SubSession 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubSession
- Win32_SubSession.Antecedent
- Win32_SubSession.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 540cfb4c00b5df64e4ff11a1cc462eaed03be434
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510683"
---
# <a name="win32_subsession-class"></a><span data-ttu-id="93b70-103">Win32 \_ >a 類別</span><span class="sxs-lookup"><span data-stu-id="93b70-103">Win32\_SubSession class</span></span>

<span data-ttu-id="93b70-104">Win32 \_ >a 關聯會定義會話之間的關聯性，其中一個會話屬於或利用另一個會話，例如，終端機會話使用登入會話。</span><span class="sxs-lookup"><span data-stu-id="93b70-104">The Win32\_SubSession association defines relationships between sessions where one session is a part of or utilizes another session for example where a Terminal session uses a Logon Session.</span></span>

<span data-ttu-id="93b70-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="93b70-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="93b70-106">語法</span><span class="sxs-lookup"><span data-stu-id="93b70-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_SubSession : CIM_Dependency
{
  Win32_Session REF Antecedent;
  Win32_Session REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="93b70-107">成員</span><span class="sxs-lookup"><span data-stu-id="93b70-107">Members</span></span>

<span data-ttu-id="93b70-108">**Win32 \_ >a** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="93b70-108">The **Win32\_SubSession** class has these types of members:</span></span>

-   [<span data-ttu-id="93b70-109">屬性</span><span class="sxs-lookup"><span data-stu-id="93b70-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93b70-110">屬性</span><span class="sxs-lookup"><span data-stu-id="93b70-110">Properties</span></span>

<span data-ttu-id="93b70-111">**Win32 \_ >a** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="93b70-111">The **Win32\_SubSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93b70-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="93b70-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93b70-113">資料類型： **Win32 \_ 會話**</span><span class="sxs-lookup"><span data-stu-id="93b70-113">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="93b70-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="93b70-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93b70-115">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) (前) </span><span class="sxs-lookup"><span data-stu-id="93b70-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Antecedent)</span></span>
</dt> </dl>

<span data-ttu-id="93b70-116">描述具有 >a 之會話的 [**Win32 \_ 會話**](win32-session.md) 。</span><span class="sxs-lookup"><span data-stu-id="93b70-116">A [**Win32\_Session**](win32-session.md) that describes the session that has a subsession.</span></span>

</dd> <dt>

<span data-ttu-id="93b70-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="93b70-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93b70-118">資料類型： **Win32 \_ 會話**</span><span class="sxs-lookup"><span data-stu-id="93b70-118">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="93b70-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="93b70-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93b70-120">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) (相依) </span><span class="sxs-lookup"><span data-stu-id="93b70-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Dependent)</span></span>
</dt> </dl>

<span data-ttu-id="93b70-121">描述 >a 之會話的 [**Win32 \_ 會話**](win32-session.md) 。</span><span class="sxs-lookup"><span data-stu-id="93b70-121">A [**Win32\_Session**](win32-session.md) that describes the session that is the subsession.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93b70-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="93b70-122">Requirements</span></span>



| <span data-ttu-id="93b70-123">需求</span><span class="sxs-lookup"><span data-stu-id="93b70-123">Requirement</span></span> | <span data-ttu-id="93b70-124">值</span><span class="sxs-lookup"><span data-stu-id="93b70-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93b70-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93b70-125">Minimum supported client</span></span><br/> | <span data-ttu-id="93b70-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93b70-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93b70-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93b70-127">Minimum supported server</span></span><br/> | <span data-ttu-id="93b70-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93b70-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93b70-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="93b70-129">Namespace</span></span><br/>                | <span data-ttu-id="93b70-130">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="93b70-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="93b70-131">MOF</span><span class="sxs-lookup"><span data-stu-id="93b70-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93b70-132"><dt>CimWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="93b70-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="93b70-133">DLL</span><span class="sxs-lookup"><span data-stu-id="93b70-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93b70-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93b70-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93b70-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93b70-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93b70-136">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="93b70-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

 
