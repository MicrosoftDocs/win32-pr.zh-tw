---
description: Merge 物件的 OpenLog 方法會開啟記錄檔，以接收進度和錯誤訊息。 如果記錄檔已經存在，安裝程式會附加新的訊息。 如果記錄檔不存在，安裝程式會建立記錄檔。
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
title: 'OpenLog 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenLog
- IMsmMerge.OpenLog
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 46dc029c88b44540817e93e1e559829d88b9f62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979624"
---
# <a name="mergeopenlog-method"></a><span data-ttu-id="3e187-105">Merge. OpenLog 方法</span><span class="sxs-lookup"><span data-stu-id="3e187-105">Merge.OpenLog method</span></span>

<span data-ttu-id="3e187-106">[**Merge**](merge-object.md)物件的 **OpenLog** 方法會開啟記錄檔，以接收進度和錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="3e187-106">The **OpenLog** method of the [**Merge**](merge-object.md) object opens a log file that receives progress and error messages.</span></span> <span data-ttu-id="3e187-107">如果記錄檔已經存在，安裝程式會附加新的訊息。</span><span class="sxs-lookup"><span data-stu-id="3e187-107">If the log file already exists, the installer appends new messages.</span></span> <span data-ttu-id="3e187-108">如果記錄檔不存在，安裝程式會建立記錄檔。</span><span class="sxs-lookup"><span data-stu-id="3e187-108">If the log file does not exist, the installer creates a log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e187-109">語法</span><span class="sxs-lookup"><span data-stu-id="3e187-109">Syntax</span></span>


```JScript
Merge.OpenLog(
  Filename
)
```



## <a name="parameters"></a><span data-ttu-id="3e187-110">參數</span><span class="sxs-lookup"><span data-stu-id="3e187-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e187-111">*檔案名稱*</span><span class="sxs-lookup"><span data-stu-id="3e187-111">*Filename*</span></span> 
</dt> <dd>

<span data-ttu-id="3e187-112">指向要開啟或建立之檔案的完整檔案名。</span><span class="sxs-lookup"><span data-stu-id="3e187-112">Fully qualified file name pointing to a file to open or create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e187-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e187-113">Return value</span></span>

<span data-ttu-id="3e187-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3e187-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e187-115">備註</span><span class="sxs-lookup"><span data-stu-id="3e187-115">Remarks</span></span>

<span data-ttu-id="3e187-116">用戶端可以透過 [**log**](merge-log.md) 方法將自己的訊息傳送至此記錄檔。</span><span class="sxs-lookup"><span data-stu-id="3e187-116">Clients may send their own messages to this log file through the [**Log**](merge-log.md) method.</span></span>

### <a name="c"></a><span data-ttu-id="3e187-117">C++</span><span class="sxs-lookup"><span data-stu-id="3e187-117">C++</span></span>

<span data-ttu-id="3e187-118">請參閱 [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) 函式。</span><span class="sxs-lookup"><span data-stu-id="3e187-118">See [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e187-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e187-119">Requirements</span></span>



| <span data-ttu-id="3e187-120">需求</span><span class="sxs-lookup"><span data-stu-id="3e187-120">Requirement</span></span> | <span data-ttu-id="3e187-121">值</span><span class="sxs-lookup"><span data-stu-id="3e187-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e187-122">版本</span><span class="sxs-lookup"><span data-stu-id="3e187-122">Version</span></span><br/> | <span data-ttu-id="3e187-123">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="3e187-123">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="3e187-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3e187-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3e187-125"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="3e187-125"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e187-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3e187-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="3e187-127"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e187-127"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
