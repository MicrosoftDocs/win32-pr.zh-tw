---
description: 此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。 這不是支援的 DirectShow API。
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: IMpeg2PsiParser：： GetPatVersionNumber 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPatVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6117060cf0c8d3c56d03e5838376485244fde8d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385619"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a><span data-ttu-id="94bd0-104">IMpeg2PsiParser：： GetPatVersionNumber 方法</span><span class="sxs-lookup"><span data-stu-id="94bd0-104">IMpeg2PsiParser::GetPatVersionNumber method</span></span>

<span data-ttu-id="94bd0-105">此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。</span><span class="sxs-lookup"><span data-stu-id="94bd0-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="94bd0-106">這不是支援的 DirectShow API。</span><span class="sxs-lookup"><span data-stu-id="94bd0-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="94bd0-107">`GetPatVersionNumber`方法會 \_ 從 PAT 抓取版本號碼欄位。</span><span class="sxs-lookup"><span data-stu-id="94bd0-107">The `GetPatVersionNumber` method retrieves the version\_number field from the PAT.</span></span> <span data-ttu-id="94bd0-108">傳輸資料流程最多包含一個 PAT。</span><span class="sxs-lookup"><span data-stu-id="94bd0-108">A transport stream contains at most one PAT.</span></span> <span data-ttu-id="94bd0-109">當資料表中的資訊變更時，版本號碼就會遞增。</span><span class="sxs-lookup"><span data-stu-id="94bd0-109">The version number is incremented whenever the information in the table changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="94bd0-110">語法</span><span class="sxs-lookup"><span data-stu-id="94bd0-110">Syntax</span></span>


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a><span data-ttu-id="94bd0-111">參數</span><span class="sxs-lookup"><span data-stu-id="94bd0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94bd0-112">*pPatVersion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="94bd0-112">*pPatVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94bd0-113">接收版本號碼欄位之變數的指標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="94bd0-113">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94bd0-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="94bd0-114">Return value</span></span>

<span data-ttu-id="94bd0-115">方法會傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="94bd0-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="94bd0-116">可能的值包括（但不限於）下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="94bd0-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="94bd0-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="94bd0-117">Return code</span></span>                                                                          | <span data-ttu-id="94bd0-118">Description</span><span class="sxs-lookup"><span data-stu-id="94bd0-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="94bd0-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="94bd0-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="94bd0-120">成功。</span><span class="sxs-lookup"><span data-stu-id="94bd0-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="94bd0-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94bd0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94bd0-122">**IMpeg2PsiParser 介面**</span><span class="sxs-lookup"><span data-stu-id="94bd0-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="94bd0-123">PSI 剖析器篩選範例</span><span class="sxs-lookup"><span data-stu-id="94bd0-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




