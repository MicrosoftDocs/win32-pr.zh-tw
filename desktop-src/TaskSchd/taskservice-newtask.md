---
title: TaskService. NewTask 方法
description: 針對腳本，會傳回空的工作定義物件，以使用設定和屬性填入，然後使用 TaskFolder. RegisterTaskDefinition 方法進行註冊。
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- NewTask 方法工作排程器
- NewTask 方法工作排程器，TaskService 物件
- TaskService 物件工作排程器，NewTask 方法
topic_type:
- apiref
api_name:
- TaskService.NewTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f5f10ce90861c76d0a751c54e8282269b7a8986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966153"
---
# <a name="taskservicenewtask-method"></a><span data-ttu-id="9a2d7-106">TaskService. NewTask 方法</span><span class="sxs-lookup"><span data-stu-id="9a2d7-106">TaskService.NewTask method</span></span>

<span data-ttu-id="9a2d7-107">針對腳本，會傳回空的工作定義物件，以使用設定和屬性填入，然後使用 [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) 方法進行註冊。</span><span class="sxs-lookup"><span data-stu-id="9a2d7-107">For scripting, returns an empty task definition object to be filled in with settings and properties and then registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a2d7-108">語法</span><span class="sxs-lookup"><span data-stu-id="9a2d7-108">Syntax</span></span>


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="9a2d7-109">參數</span><span class="sxs-lookup"><span data-stu-id="9a2d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a2d7-110">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a2d7-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a2d7-111">此參數會保留供日後使用，且必須設定為0。</span><span class="sxs-lookup"><span data-stu-id="9a2d7-111">This parameter is reserved for future use and must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a2d7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a2d7-112">Return value</span></span>

<span data-ttu-id="9a2d7-113">指定建立新工作所需之所有資訊的工作定義。</span><span class="sxs-lookup"><span data-stu-id="9a2d7-113">The task definition that specifies all the information required to create a new task.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a2d7-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a2d7-114">Requirements</span></span>



| <span data-ttu-id="9a2d7-115">需求</span><span class="sxs-lookup"><span data-stu-id="9a2d7-115">Requirement</span></span> | <span data-ttu-id="9a2d7-116">值</span><span class="sxs-lookup"><span data-stu-id="9a2d7-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a2d7-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a2d7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9a2d7-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a2d7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9a2d7-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a2d7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9a2d7-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a2d7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9a2d7-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9a2d7-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="9a2d7-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9a2d7-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9a2d7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9a2d7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a2d7-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a2d7-124"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





