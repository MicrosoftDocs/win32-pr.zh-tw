---
description: Merge 物件的 CloseDatabase 方法會關閉目前開啟的 Windows Installer 資料庫。
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: 'CloseDatabase 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseDatabase
- IMsmMerge.CloseDatabase
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5df72b9423ad212264736d16db0ae73ded9afef5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106974907"
---
# <a name="mergeclosedatabase-method"></a><span data-ttu-id="ad375-103">Merge. CloseDatabase 方法</span><span class="sxs-lookup"><span data-stu-id="ad375-103">Merge.CloseDatabase method</span></span>

<span data-ttu-id="ad375-104">[**Merge**](merge-object.md)物件的 **CloseDatabase** 方法會關閉目前開啟的 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ad375-104">The **CloseDatabase** method of the [**Merge**](merge-object.md) object closes the currently open Windows Installer database.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad375-105">語法</span><span class="sxs-lookup"><span data-stu-id="ad375-105">Syntax</span></span>


```JScript
Merge.CloseDatabase(
  bCommit
)
```



## <a name="parameters"></a><span data-ttu-id="ad375-106">參數</span><span class="sxs-lookup"><span data-stu-id="ad375-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad375-107">*bCommit*</span><span class="sxs-lookup"><span data-stu-id="ad375-107">*bCommit*</span></span> 
</dt> <dd>

<span data-ttu-id="ad375-108">若應儲存變更，**則為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ad375-108">**TRUE** if changes should be saved, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad375-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad375-109">Return value</span></span>

<span data-ttu-id="ad375-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ad375-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad375-111">備註</span><span class="sxs-lookup"><span data-stu-id="ad375-111">Remarks</span></span>

<span data-ttu-id="ad375-112">關閉資料庫會清除所有相依性資訊，但不會影響任何未取出的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ad375-112">Closing a database clears all dependency information but does not affect any errors that have not been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="ad375-113">C++</span><span class="sxs-lookup"><span data-stu-id="ad375-113">C++</span></span>

<span data-ttu-id="ad375-114">請參閱 [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) 函式。</span><span class="sxs-lookup"><span data-stu-id="ad375-114">See [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad375-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad375-115">Requirements</span></span>



| <span data-ttu-id="ad375-116">需求</span><span class="sxs-lookup"><span data-stu-id="ad375-116">Requirement</span></span> | <span data-ttu-id="ad375-117">值</span><span class="sxs-lookup"><span data-stu-id="ad375-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad375-118">版本</span><span class="sxs-lookup"><span data-stu-id="ad375-118">Version</span></span><br/> | <span data-ttu-id="ad375-119">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ad375-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="ad375-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ad375-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ad375-121"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="ad375-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad375-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ad375-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="ad375-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad375-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
