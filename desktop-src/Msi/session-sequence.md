---
description: Session 物件的 Sequence 方法會在指定的資料表上開啟查詢，並依 [順序] 資料行中的數位排序動作。
ms.assetid: cde735b0-0b97-4c4f-adfc-f0321aafb012
title: Session. Sequence 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Sequence
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18708b79bdce73b29f46b4d62a15ceb8003d9c9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976254"
---
# <a name="sessionsequence-method"></a><span data-ttu-id="9f344-103">Session. Sequence 方法</span><span class="sxs-lookup"><span data-stu-id="9f344-103">Session.Sequence method</span></span>

<span data-ttu-id="9f344-104">[**Session**](session-object.md)物件的 **Sequence** 方法會在指定的資料表上開啟查詢，並依 [順序] 資料行中的數位排序動作。</span><span class="sxs-lookup"><span data-stu-id="9f344-104">The **Sequence** method of the [**Session**](session-object.md) object opens a query on the specified table, ordering the actions by the numbers in the Sequence column.</span></span> <span data-ttu-id="9f344-105">針對每個提取的資料列，如果任何提供的條件運算式未評估為 False，則會呼叫 [**dataadapter.doaction**](session-doaction.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="9f344-105">For each row fetched, the [**DoAction**](session-doaction.md) method is called, provided that any supplied condition expression does not evaluate to False.</span></span> <span data-ttu-id="9f344-106">傳回列舉 msiDoActionStatusEnum，如 [**dataadapter.doaction**](session-doaction.md) 方法中所述。</span><span class="sxs-lookup"><span data-stu-id="9f344-106">Returns an enumeration msiDoActionStatusEnum, as described in the [**DoAction**](session-doaction.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f344-107">語法</span><span class="sxs-lookup"><span data-stu-id="9f344-107">Syntax</span></span>


```JScript
Session.Sequence(
  table
)
```



## <a name="parameters"></a><span data-ttu-id="9f344-108">參數</span><span class="sxs-lookup"><span data-stu-id="9f344-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f344-109">*table*</span><span class="sxs-lookup"><span data-stu-id="9f344-109">*table*</span></span> 
</dt> <dd>

<span data-ttu-id="9f344-110">要用於排序的資料表所需的字串名稱。</span><span class="sxs-lookup"><span data-stu-id="9f344-110">Required string name of the table to use for sequencing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f344-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f344-111">Return value</span></span>

<span data-ttu-id="9f344-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9f344-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f344-113">備註</span><span class="sxs-lookup"><span data-stu-id="9f344-113">Remarks</span></span>

<span data-ttu-id="9f344-114">通常會由最上層動作在內部呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="9f344-114">This method is normally called internally by top-level actions.</span></span>

<span data-ttu-id="9f344-115">藉由呼叫 **sequence** 方法，無法執行包含更新系統之動作的動作序列，例如 [InstallFiles](installfiles-action.md)和 [WriteRegistryValues](writeregistryvalues-action.md)動作。</span><span class="sxs-lookup"><span data-stu-id="9f344-115">An action sequence containing actions that update the system, such as the [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions, cannot be run by calling the **Sequence** method.</span></span> <span data-ttu-id="9f344-116">這項規則的例外狀況是從 [InstallInitialize](installinitialize-action.md)和 [InstallFinalize 動作](installfinalize-action.md)之間的 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中排程的自訂動作呼叫 **順序** 方法。</span><span class="sxs-lookup"><span data-stu-id="9f344-116">The exception to this rule is if the **Sequence** method is called from a custom action that is scheduled in the [InstallExecuteSequence table](installexecutesequence-table.md) between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize actions](installfinalize-action.md).</span></span> <span data-ttu-id="9f344-117">您可以呼叫不會更新系統的動作，例如 [AppSearch](appsearch-action.md) 或 [CostInitialize](costinitialize-action.md)。</span><span class="sxs-lookup"><span data-stu-id="9f344-117">Actions that do not update the system, such as [AppSearch](appsearch-action.md) or [CostInitialize](costinitialize-action.md), can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f344-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f344-118">Requirements</span></span>



| <span data-ttu-id="9f344-119">需求</span><span class="sxs-lookup"><span data-stu-id="9f344-119">Requirement</span></span> | <span data-ttu-id="9f344-120">值</span><span class="sxs-lookup"><span data-stu-id="9f344-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f344-121">版本</span><span class="sxs-lookup"><span data-stu-id="9f344-121">Version</span></span><br/> | <span data-ttu-id="9f344-122">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="9f344-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9f344-123">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="9f344-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9f344-124">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="9f344-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="9f344-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9f344-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="9f344-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f344-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="9f344-127">IID</span><span class="sxs-lookup"><span data-stu-id="9f344-127">IID</span></span><br/>     | <span data-ttu-id="9f344-128">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9f344-128">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




