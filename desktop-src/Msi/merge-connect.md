---
description: Merge 物件的 Connect 方法會將模組連接到其他功能。 模組必須已經合併到資料庫中，或合併到資料庫中。 在呼叫此函式之前，此功能必須存在。
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: 'Merge. Connect 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Connect
- IMsmMerge.Connect
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: da66f7dfe4203e80d4778ae9b39c665a66164384
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989580"
---
# <a name="mergeconnect-method"></a><span data-ttu-id="ae8ed-105">Merge. Connect 方法</span><span class="sxs-lookup"><span data-stu-id="ae8ed-105">Merge.Connect method</span></span>

<span data-ttu-id="ae8ed-106">[**Merge**](merge-object.md)物件的 **Connect** 方法會將模組連接到其他功能。</span><span class="sxs-lookup"><span data-stu-id="ae8ed-106">The **Connect** method of the [**Merge**](merge-object.md) object connects a module to an additional feature.</span></span> <span data-ttu-id="ae8ed-107">模組必須已經合併到資料庫中，或合併到資料庫中。</span><span class="sxs-lookup"><span data-stu-id="ae8ed-107">The module must have already been merged into the database or will be merged into the database.</span></span> <span data-ttu-id="ae8ed-108">在呼叫此函式之前，此功能必須存在。</span><span class="sxs-lookup"><span data-stu-id="ae8ed-108">The feature must exist before calling this function.</span></span>

<span data-ttu-id="ae8ed-109">除非呼叫 [**CloseDatabase**](merge-closedatabase.md) 方法，並將 *BCommit* 設定為 **TRUE**，否則對資料庫所做的變更不會儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="ae8ed-109">Changes made to the database are not saved to disk unless the [**CloseDatabase**](merge-closedatabase.md) method is called with *bCommit* set to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae8ed-110">語法</span><span class="sxs-lookup"><span data-stu-id="ae8ed-110">Syntax</span></span>


```JScript
Merge.Connect(
  Feature
)
```



## <a name="parameters"></a><span data-ttu-id="ae8ed-111">參數</span><span class="sxs-lookup"><span data-stu-id="ae8ed-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae8ed-112">*功能*</span><span class="sxs-lookup"><span data-stu-id="ae8ed-112">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="ae8ed-113">存在於資料庫中的功能名稱。</span><span class="sxs-lookup"><span data-stu-id="ae8ed-113">The name of a feature already existing in the database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae8ed-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae8ed-114">Return value</span></span>

<span data-ttu-id="ae8ed-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ae8ed-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae8ed-116">備註</span><span class="sxs-lookup"><span data-stu-id="ae8ed-116">Remarks</span></span>

<span data-ttu-id="ae8ed-117">錯誤可能會透過 [ [**錯誤**](merge-errors.md) ] 屬性來抓取。</span><span class="sxs-lookup"><span data-stu-id="ae8ed-117">Errors may be retrieved through the [**Errors**](merge-errors.md) property.</span></span> <span data-ttu-id="ae8ed-118">錯誤和參考用訊息會張貼至目前的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="ae8ed-118">Errors and informational messages are posted to the current log file.</span></span>

### <a name="c"></a><span data-ttu-id="ae8ed-119">C++</span><span class="sxs-lookup"><span data-stu-id="ae8ed-119">C++</span></span>

<span data-ttu-id="ae8ed-120">請參閱 [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) 函數。</span><span class="sxs-lookup"><span data-stu-id="ae8ed-120">See [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae8ed-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae8ed-121">Requirements</span></span>



| <span data-ttu-id="ae8ed-122">需求</span><span class="sxs-lookup"><span data-stu-id="ae8ed-122">Requirement</span></span> | <span data-ttu-id="ae8ed-123">值</span><span class="sxs-lookup"><span data-stu-id="ae8ed-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae8ed-124">版本</span><span class="sxs-lookup"><span data-stu-id="ae8ed-124">Version</span></span><br/> | <span data-ttu-id="ae8ed-125">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ae8ed-125">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="ae8ed-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ae8ed-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ae8ed-127"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="ae8ed-127"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="ae8ed-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ae8ed-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="ae8ed-129"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae8ed-129"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
