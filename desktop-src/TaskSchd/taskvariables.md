---
title: TaskVariables 物件
description: 腳本物件，定義可作為參數傳遞給工作處理常式的工作變數，以及工作所啟動的外部可執行檔。
ms.assetid: 194babe0-16bd-4a78-af45-139c9c7eacbe
keywords:
- TaskVariables 物件工作排程器
- TaskVariables 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TaskVariables
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fe20153b0d6d66ca6c7f263a8e76d5a4d480b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466397"
---
# <a name="taskvariables-object"></a><span data-ttu-id="b29fa-105">TaskVariables 物件</span><span class="sxs-lookup"><span data-stu-id="b29fa-105">TaskVariables object</span></span>

<span data-ttu-id="b29fa-106">腳本物件，定義可作為參數傳遞給工作處理常式的工作變數，以及工作所啟動的外部可執行檔。</span><span class="sxs-lookup"><span data-stu-id="b29fa-106">Scripting object that defines task variables that can be passed as parameters to task handlers and external executables that are launched by tasks.</span></span>

## <a name="members"></a><span data-ttu-id="b29fa-107">成員</span><span class="sxs-lookup"><span data-stu-id="b29fa-107">Members</span></span>

<span data-ttu-id="b29fa-108">**TaskVariables** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b29fa-108">The **TaskVariables** object has these types of members:</span></span>

-   [<span data-ttu-id="b29fa-109">方法</span><span class="sxs-lookup"><span data-stu-id="b29fa-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b29fa-110">方法</span><span class="sxs-lookup"><span data-stu-id="b29fa-110">Methods</span></span>

<span data-ttu-id="b29fa-111">**TaskVariables** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b29fa-111">The **TaskVariables** object has these methods.</span></span>



| <span data-ttu-id="b29fa-112">方法</span><span class="sxs-lookup"><span data-stu-id="b29fa-112">Method</span></span>                                         | <span data-ttu-id="b29fa-113">描述</span><span class="sxs-lookup"><span data-stu-id="b29fa-113">Description</span></span>                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b29fa-114">**GetCoNtext**</span><span class="sxs-lookup"><span data-stu-id="b29fa-114">**GetContext**</span></span>](taskvariables-getcontext.md) | <span data-ttu-id="b29fa-115">用來在不同的步驟與相同作業實例中的工作之間共用內容。</span><span class="sxs-lookup"><span data-stu-id="b29fa-115">Used to share the context between different steps and tasks that are in the same job instance.</span></span><br/> |
| [<span data-ttu-id="b29fa-116">**>getinput**</span><span class="sxs-lookup"><span data-stu-id="b29fa-116">**GetInput**</span></span>](taskvariables-getinput.md)     | <span data-ttu-id="b29fa-117">取得工作的輸入變數。</span><span class="sxs-lookup"><span data-stu-id="b29fa-117">Gets the input variables for a task.</span></span><br/>                                                           |
| [<span data-ttu-id="b29fa-118">**SetOutput**</span><span class="sxs-lookup"><span data-stu-id="b29fa-118">**SetOutput**</span></span>](taskvariables-setoutput.md)   | <span data-ttu-id="b29fa-119">設定工作的輸出變數。</span><span class="sxs-lookup"><span data-stu-id="b29fa-119">Sets the output variables for a task.</span></span><br/>                                                          |



 

## <a name="requirements"></a><span data-ttu-id="b29fa-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b29fa-120">Requirements</span></span>



| <span data-ttu-id="b29fa-121">需求</span><span class="sxs-lookup"><span data-stu-id="b29fa-121">Requirement</span></span> | <span data-ttu-id="b29fa-122">值</span><span class="sxs-lookup"><span data-stu-id="b29fa-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b29fa-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b29fa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b29fa-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b29fa-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b29fa-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b29fa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b29fa-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b29fa-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b29fa-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b29fa-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="b29fa-128"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b29fa-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b29fa-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b29fa-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b29fa-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b29fa-130"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





