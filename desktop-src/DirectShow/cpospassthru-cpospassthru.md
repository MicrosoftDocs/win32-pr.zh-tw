---
description: CPosPassThru。 CPosPassThru 函式-函數方法。
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
ms.openlocfilehash: 2a6c49b305b3c6638aeaaee1480d0b561fd8c99a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085596"
---
# <a name="cpospassthrucpospassthru-constructor"></a><span data-ttu-id="30081-103">CPosPassThru. CPosPassThru 函數</span><span class="sxs-lookup"><span data-stu-id="30081-103">CPosPassThru.CPosPassThru constructor</span></span>

<span data-ttu-id="30081-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="30081-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="30081-105">語法</span><span class="sxs-lookup"><span data-stu-id="30081-105">Syntax</span></span>


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a><span data-ttu-id="30081-106">參數</span><span class="sxs-lookup"><span data-stu-id="30081-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30081-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="30081-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="30081-108">物件名稱的指標，用於偵測用途。</span><span class="sxs-lookup"><span data-stu-id="30081-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="30081-109">在靜態記憶體中配置此參數。</span><span class="sxs-lookup"><span data-stu-id="30081-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="30081-110">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="30081-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="30081-111">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="30081-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="30081-112">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="30081-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="30081-113">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="30081-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="30081-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="30081-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="30081-115">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="30081-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="30081-116">忽略。</span><span class="sxs-lookup"><span data-stu-id="30081-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="30081-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="30081-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="30081-118">篩選器輸入釘選的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="30081-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



