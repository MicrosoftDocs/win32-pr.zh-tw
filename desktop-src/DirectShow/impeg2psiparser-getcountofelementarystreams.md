---
description: 此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。 這不是支援的 DirectShow API。
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: IMpeg2PsiParser：： GetCountOfElementaryStreams 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfElementaryStreams
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6593b699592c913940b14c2c26aea42057acfa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973738"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a><span data-ttu-id="add52-104">IMpeg2PsiParser：： GetCountOfElementaryStreams 方法</span><span class="sxs-lookup"><span data-stu-id="add52-104">IMpeg2PsiParser::GetCountOfElementaryStreams method</span></span>

<span data-ttu-id="add52-105">此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。</span><span class="sxs-lookup"><span data-stu-id="add52-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="add52-106">這不是支援的 DirectShow API。</span><span class="sxs-lookup"><span data-stu-id="add52-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="add52-107">方法會抓取 `GetCountOfElementaryStreams` 指定程式中的基本資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="add52-107">The `GetCountOfElementaryStreams` method retrieves the number of elementary streams in a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="add52-108">語法</span><span class="sxs-lookup"><span data-stu-id="add52-108">Syntax</span></span>


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="add52-109">參數</span><span class="sxs-lookup"><span data-stu-id="add52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="add52-110">*wProgramNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="add52-110">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="add52-111">指定程式的 [程式 \_ 代碼] 欄位，如 PAT 所指定。</span><span class="sxs-lookup"><span data-stu-id="add52-111">Specifies the program\_number field for the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="add52-112">*pwVal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="add52-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="add52-113">變數的指標，此變數會接收程式中的基本資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="add52-113">Pointer to a variable that receives the number of elementary streams in the program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="add52-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="add52-114">Return value</span></span>

<span data-ttu-id="add52-115">方法會傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="add52-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="add52-116">可能的值包括（但不限於）下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="add52-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="add52-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="add52-117">Return code</span></span>                                                                          | <span data-ttu-id="add52-118">Description</span><span class="sxs-lookup"><span data-stu-id="add52-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="add52-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="add52-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="add52-120">成功。</span><span class="sxs-lookup"><span data-stu-id="add52-120">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="add52-121">備註</span><span class="sxs-lookup"><span data-stu-id="add52-121">Remarks</span></span>

<span data-ttu-id="add52-122">使用 **GetRecordProgramNumber** 方法來取得程式編號。</span><span class="sxs-lookup"><span data-stu-id="add52-122">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="add52-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="add52-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add52-124">**IMpeg2PsiParser 介面**</span><span class="sxs-lookup"><span data-stu-id="add52-124">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="add52-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="add52-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="add52-126">PSI 剖析器篩選範例</span><span class="sxs-lookup"><span data-stu-id="add52-126">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




