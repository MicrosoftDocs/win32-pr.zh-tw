---
description: 函式方法。
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: CPosPassThru. CPosPassThru 函數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CPosPassThru
api_type:
- COM
api_location: ''
ms.openlocfilehash: ba49bd1e2f65cf0d2a8a398ecab167e74dc35ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973736"
---
# <a name="cpospassthrucpospassthru-constructor"></a><span data-ttu-id="cc20e-103">CPosPassThru. CPosPassThru 函數</span><span class="sxs-lookup"><span data-stu-id="cc20e-103">CPosPassThru.CPosPassThru constructor</span></span>

<span data-ttu-id="cc20e-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="cc20e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc20e-105">語法</span><span class="sxs-lookup"><span data-stu-id="cc20e-105">Syntax</span></span>


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a><span data-ttu-id="cc20e-106">參數</span><span class="sxs-lookup"><span data-stu-id="cc20e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc20e-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="cc20e-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="cc20e-108">物件名稱的指標，用於偵測用途。</span><span class="sxs-lookup"><span data-stu-id="cc20e-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="cc20e-109">在靜態記憶體中配置此參數。</span><span class="sxs-lookup"><span data-stu-id="cc20e-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="cc20e-110">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="cc20e-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="cc20e-111">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="cc20e-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="cc20e-112">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="cc20e-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="cc20e-113">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="cc20e-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cc20e-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="cc20e-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="cc20e-115">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="cc20e-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="cc20e-116">忽略。</span><span class="sxs-lookup"><span data-stu-id="cc20e-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="cc20e-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="cc20e-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="cc20e-118">篩選器輸入釘選的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="cc20e-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



