---
description: Merge 物件的 CloseModule 方法會關閉目前開啟的 Windows Installer Merge 模組。
ms.assetid: a11f72cf-4c4e-4650-95f9-549169452622
title: 'CloseModule 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseModule
- IMsmMerge.CloseModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8688ae06cedca1e3b75290f7831f7d3539e3ec21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981871"
---
# <a name="mergeclosemodule-method"></a><span data-ttu-id="2faf9-103">Merge. CloseModule 方法</span><span class="sxs-lookup"><span data-stu-id="2faf9-103">Merge.CloseModule method</span></span>

<span data-ttu-id="2faf9-104">[**Merge**](merge-object.md)物件的 **CloseModule** 方法會關閉目前開啟的 Windows Installer Merge 模組。</span><span class="sxs-lookup"><span data-stu-id="2faf9-104">The **CloseModule** method of the [**Merge**](merge-object.md) object closes the currently open Windows Installer merge module.</span></span>

## <a name="syntax"></a><span data-ttu-id="2faf9-105">語法</span><span class="sxs-lookup"><span data-stu-id="2faf9-105">Syntax</span></span>


```JScript
Merge.CloseModule()
```



## <a name="parameters"></a><span data-ttu-id="2faf9-106">參數</span><span class="sxs-lookup"><span data-stu-id="2faf9-106">Parameters</span></span>

<span data-ttu-id="2faf9-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2faf9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2faf9-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2faf9-108">Return value</span></span>

<span data-ttu-id="2faf9-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2faf9-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2faf9-110">備註</span><span class="sxs-lookup"><span data-stu-id="2faf9-110">Remarks</span></span>

<span data-ttu-id="2faf9-111">關閉合併模組並不會影響任何未取出的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2faf9-111">Closing a merge module will not affect any errors that have not been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="2faf9-112">C++</span><span class="sxs-lookup"><span data-stu-id="2faf9-112">C++</span></span>

<span data-ttu-id="2faf9-113">請參閱 [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) 函式。</span><span class="sxs-lookup"><span data-stu-id="2faf9-113">See [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2faf9-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2faf9-114">Requirements</span></span>



| <span data-ttu-id="2faf9-115">需求</span><span class="sxs-lookup"><span data-stu-id="2faf9-115">Requirement</span></span> | <span data-ttu-id="2faf9-116">值</span><span class="sxs-lookup"><span data-stu-id="2faf9-116">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2faf9-117">版本</span><span class="sxs-lookup"><span data-stu-id="2faf9-117">Version</span></span><br/> | <span data-ttu-id="2faf9-118">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2faf9-118">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="2faf9-119">標頭</span><span class="sxs-lookup"><span data-stu-id="2faf9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2faf9-120"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="2faf9-120"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="2faf9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="2faf9-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="2faf9-122"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2faf9-122"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
