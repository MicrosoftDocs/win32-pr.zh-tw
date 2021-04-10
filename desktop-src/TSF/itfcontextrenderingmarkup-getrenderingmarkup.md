---
title: ITfCoNtextRenderingMarkup GetRenderingMarkup 方法
description: ITfCoNtextRenderingMarkup GetRenderingMarkup 方法會抓取指定範圍之轉譯標記的列舉值。
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- GetRenderingMarkup 方法文字服務架構
- GetRenderingMarkup 方法文字服務架構，ITfCoNtextRenderingMarkup 介面
- ITfCoNtextRenderingMarkup 介面文字服務架構，GetRenderingMarkup 方法
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f3ccfb97af6a6657c33982359640a2a924cad2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682671"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a><span data-ttu-id="8c481-106">ITfCoNtextRenderingMarkup：： GetRenderingMarkup 方法</span><span class="sxs-lookup"><span data-stu-id="8c481-106">ITfContextRenderingMarkup::GetRenderingMarkup method</span></span>

<span data-ttu-id="8c481-107">**ITfCoNtextRenderingMarkup：： GetRenderingMarkup** 方法會抓取指定範圍之轉譯標記的列舉值。</span><span class="sxs-lookup"><span data-stu-id="8c481-107">The **ITfContextRenderingMarkup::GetRenderingMarkup** method retrieves an enumerator of the rendering markups for the given range.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c481-108">語法</span><span class="sxs-lookup"><span data-stu-id="8c481-108">Syntax</span></span>


```C++
HRESULT GetRenderingMarkup(
  [in]  TfEditCookie           ec,
  [in]  DWORD                  dwFlags,
  [in]  ITfRange               *pRangeCover,
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="8c481-109">參數</span><span class="sxs-lookup"><span data-stu-id="8c481-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c481-110">*ec* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c481-110">*ec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c481-111">\[\]以唯讀的編輯 cookie 來存取內容。</span><span class="sxs-lookup"><span data-stu-id="8c481-111">\[in\] A read only edit cookie to access the context.</span></span>

</dd> <dt>

<span data-ttu-id="8c481-112">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c481-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c481-113">\[in\]</span><span class="sxs-lookup"><span data-stu-id="8c481-113">\[in\]</span></span>



| <span data-ttu-id="8c481-114">值</span><span class="sxs-lookup"><span data-stu-id="8c481-114">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="8c481-115">意義</span><span class="sxs-lookup"><span data-stu-id="8c481-115">Meaning</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <span data-ttu-id="8c481-116"><dt>**TF \_ GRM \_ INCLUDE \_ 屬性**</dt></span><span class="sxs-lookup"><span data-stu-id="8c481-116"><dt>**TF\_GRM\_INCLUDE\_PROPERTY**</dt></span></span> </dl> | <span data-ttu-id="8c481-117">如果這個位為1，則列舉值將包含 GUID 屬性屬性（ \_ \_ property）。</span><span class="sxs-lookup"><span data-stu-id="8c481-117">If this bit is 1, the enumerator will include the GUID\_PROP\_ATTRIBUTE property.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8c481-118">*pRangeCover* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c481-118">*pRangeCover* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c481-119">\[在指向 \] 範圍之 [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) 介面的指標中，以列舉呈現標記。</span><span class="sxs-lookup"><span data-stu-id="8c481-119">\[in\] A pointer to an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) interface of the range to enumerate the rendering markups.</span></span>

</dd> <dt>

<span data-ttu-id="8c481-120">*ppEnum* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8c481-120">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c481-121">\[取出 \] 指標以取得 [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="8c481-121">\[out\] A pointer to retrieve [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c481-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c481-122">Return value</span></span>

<span data-ttu-id="8c481-123">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8c481-123">This method can return one of these values.</span></span>



| <span data-ttu-id="8c481-124">值</span><span class="sxs-lookup"><span data-stu-id="8c481-124">Value</span></span>                                                                                | <span data-ttu-id="8c481-125">描述</span><span class="sxs-lookup"><span data-stu-id="8c481-125">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="8c481-126"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8c481-126"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8c481-127">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="8c481-127">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8c481-128">備註</span><span class="sxs-lookup"><span data-stu-id="8c481-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8c481-129">這個方法目前不在公用標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="8c481-129">This method is not currently in the public header files.</span></span> <span data-ttu-id="8c481-130">若要使用此 API，您必須 MIDL 編譯 [原型](prototypes.md)。</span><span class="sxs-lookup"><span data-stu-id="8c481-130">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

