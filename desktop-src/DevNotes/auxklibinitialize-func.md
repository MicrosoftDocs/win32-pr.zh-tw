---
description: 初始化 Aux \_ klib 程式庫。
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: 'AuxKlibInitialize function (Aux \_ klib .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibInitialize
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: d16ea418d2012b24ce19ad14afab12e198e7ab2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996029"
---
# <a name="auxklibinitialize-function"></a><span data-ttu-id="566df-103">AuxKlibInitialize 函式</span><span class="sxs-lookup"><span data-stu-id="566df-103">AuxKlibInitialize function</span></span>

<span data-ttu-id="566df-104">初始化 Aux \_ klib 程式庫。</span><span class="sxs-lookup"><span data-stu-id="566df-104">Initializes the Aux\_klib library.</span></span> <span data-ttu-id="566df-105">必須先呼叫此函式，才能呼叫程式庫中的任何其他函式。</span><span class="sxs-lookup"><span data-stu-id="566df-105">This function must be called before any other function in the library can be called.</span></span>

## <a name="syntax"></a><span data-ttu-id="566df-106">語法</span><span class="sxs-lookup"><span data-stu-id="566df-106">Syntax</span></span>


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="566df-107">參數</span><span class="sxs-lookup"><span data-stu-id="566df-107">Parameters</span></span>

<span data-ttu-id="566df-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="566df-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="566df-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="566df-109">Return value</span></span>

<span data-ttu-id="566df-110">如果函式成功，則傳回值為「狀態 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="566df-110">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="566df-111">如果函式失敗，則傳回值可以是在 WDK 中定義的其中一個狀態碼，也就是在 WDK 中可用。</span><span class="sxs-lookup"><span data-stu-id="566df-111">If the function fails, the return value can be one of the status codes defined in Ntstatus.h, which is available in the WDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="566df-112">備註</span><span class="sxs-lookup"><span data-stu-id="566df-112">Remarks</span></span>

<span data-ttu-id="566df-113">您可以從 [這裡](https://www.microsoft.com/?ref=go)下載可執行此 API 的物件程式庫。</span><span class="sxs-lookup"><span data-stu-id="566df-113">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="566df-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="566df-114">Requirements</span></span>



| <span data-ttu-id="566df-115">需求</span><span class="sxs-lookup"><span data-stu-id="566df-115">Requirement</span></span> | <span data-ttu-id="566df-116">值</span><span class="sxs-lookup"><span data-stu-id="566df-116">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="566df-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="566df-117">Redistributable</span></span><br/> | <span data-ttu-id="566df-118">Windows 輔助 API 程式庫1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="566df-118">Windows Auxiliary API library version 1.0 or later</span></span><br/>                            |
| <span data-ttu-id="566df-119">標頭</span><span class="sxs-lookup"><span data-stu-id="566df-119">Header</span></span><br/>          | <dl> <span data-ttu-id="566df-120"><dt>Aux \_ klib。h</dt></span><span class="sxs-lookup"><span data-stu-id="566df-120"><dt>Aux\_klib.h</dt></span></span> </dl>   |
| <span data-ttu-id="566df-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="566df-121">Library</span></span><br/>         | <dl> <span data-ttu-id="566df-122"><dt>Aux \_ klib .lib</dt></span><span class="sxs-lookup"><span data-stu-id="566df-122"><dt>Aux\_klib.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="566df-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="566df-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="566df-124">**AuxKlibQueryModuleInformation**</span><span class="sxs-lookup"><span data-stu-id="566df-124">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




