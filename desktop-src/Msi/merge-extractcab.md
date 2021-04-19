---
description: Merge 物件的 ExtractCAB 方法會從模組中解壓縮內嵌的 .cab 檔案，並將它儲存為指定的檔案。 如果此檔案不存在，安裝程式會建立此檔案，如果存在，則會覆寫該檔案。
ms.assetid: a6fe8b69-8f4a-45f7-b7e6-7620a00500bb
title: 'ExtractCAB 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractCAB
- IMsmMerge.ExtractCAB
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d0bdc79fb0087456d035bf732faca384b35b2a9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997631"
---
# <a name="mergeextractcab-method"></a><span data-ttu-id="5fec2-104">Merge. ExtractCAB 方法</span><span class="sxs-lookup"><span data-stu-id="5fec2-104">Merge.ExtractCAB method</span></span>

<span data-ttu-id="5fec2-105">[**Merge**](merge-object.md)物件的 **ExtractCAB** 方法會從模組中解壓縮內嵌的 .cab 檔案，並將它儲存為指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="5fec2-105">The **ExtractCAB** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and saves it as the specified file.</span></span> <span data-ttu-id="5fec2-106">如果此檔案不存在，安裝程式會建立此檔案，如果存在，則會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="5fec2-106">The installer creates this file if it does not already exist and overwritten if it does exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fec2-107">語法</span><span class="sxs-lookup"><span data-stu-id="5fec2-107">Syntax</span></span>


```JScript
Merge.ExtractCAB(
  FileName
)
```



## <a name="parameters"></a><span data-ttu-id="5fec2-108">參數</span><span class="sxs-lookup"><span data-stu-id="5fec2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fec2-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="5fec2-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="5fec2-110">完整的目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="5fec2-110">The fully qualified destination file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fec2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5fec2-111">Return value</span></span>

<span data-ttu-id="5fec2-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5fec2-112">This method does not return a value.</span></span>

## <a name="c"></a><span data-ttu-id="5fec2-113">C++</span><span class="sxs-lookup"><span data-stu-id="5fec2-113">C++</span></span>

<span data-ttu-id="5fec2-114">請參閱 [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) 函式。</span><span class="sxs-lookup"><span data-stu-id="5fec2-114">See [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fec2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5fec2-115">Requirements</span></span>



| <span data-ttu-id="5fec2-116">需求</span><span class="sxs-lookup"><span data-stu-id="5fec2-116">Requirement</span></span> | <span data-ttu-id="5fec2-117">值</span><span class="sxs-lookup"><span data-stu-id="5fec2-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fec2-118">版本</span><span class="sxs-lookup"><span data-stu-id="5fec2-118">Version</span></span><br/> | <span data-ttu-id="5fec2-119">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5fec2-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="5fec2-120">標頭</span><span class="sxs-lookup"><span data-stu-id="5fec2-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5fec2-121"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="5fec2-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="5fec2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5fec2-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="5fec2-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fec2-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
