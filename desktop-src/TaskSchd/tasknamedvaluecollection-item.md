---
title: TaskNamedValueCollection 專案屬性
description: 針對腳本，從集合取得指定的名稱/值組。
ms.assetid: 89c87b22-e459-435d-8c15-69907e9b1329
keywords:
- Item 屬性工作排程器
- 專案屬性工作排程器，TaskNamedValueCollection 物件
- TaskNamedValueCollection 物件工作排程器，Item 屬性
topic_type:
- apiref
api_name:
- TaskNamedValueCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd0abff47d699fd6d85f04745f28e2feb31c6a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965746"
---
# <a name="tasknamedvaluecollectionitem-property"></a><span data-ttu-id="e9d46-106">TaskNamedValueCollection 專案屬性</span><span class="sxs-lookup"><span data-stu-id="e9d46-106">TaskNamedValueCollection.Item property</span></span>

<span data-ttu-id="e9d46-107">針對腳本，從集合取得指定的名稱/值組。</span><span class="sxs-lookup"><span data-stu-id="e9d46-107">For scripting, gets the specified name-value pair from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9d46-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9d46-108">Syntax</span></span>


```VB
TaskNamedValueCollection.Item( _
  ByVal index, _
  ByRef pair _
) As long
```



## <a name="property-value"></a><span data-ttu-id="e9d46-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="e9d46-109">Property value</span></span>

<span data-ttu-id="e9d46-110">代表所要求之配對的 [**TaskNamedValuePair**](tasknamedvaluepair.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e9d46-110">A [**TaskNamedValuePair**](tasknamedvaluepair.md) object that represents the requested pair.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9d46-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9d46-111">Requirements</span></span>



| <span data-ttu-id="e9d46-112">需求</span><span class="sxs-lookup"><span data-stu-id="e9d46-112">Requirement</span></span> | <span data-ttu-id="e9d46-113">值</span><span class="sxs-lookup"><span data-stu-id="e9d46-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d46-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9d46-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e9d46-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9d46-115">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e9d46-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9d46-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e9d46-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9d46-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e9d46-118">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e9d46-118">Type library</span></span><br/>             | <dl> <span data-ttu-id="e9d46-119"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e9d46-119"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e9d46-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e9d46-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9d46-121"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9d46-121"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





