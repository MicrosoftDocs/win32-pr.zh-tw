---
description: 此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。 這不是支援的 DirectShow API。
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: IMpeg2PsiParser：： GetCountOfPrograms 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfPrograms
api_type:
- COM
api_location: ''
ms.openlocfilehash: e4f01b2a360465b9670b52547cff1ff4c312a705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846500"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a><span data-ttu-id="94dfe-104">IMpeg2PsiParser：： GetCountOfPrograms 方法</span><span class="sxs-lookup"><span data-stu-id="94dfe-104">IMpeg2PsiParser::GetCountOfPrograms method</span></span>

<span data-ttu-id="94dfe-105">此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。</span><span class="sxs-lookup"><span data-stu-id="94dfe-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="94dfe-106">這不是支援的 DirectShow API。</span><span class="sxs-lookup"><span data-stu-id="94dfe-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="94dfe-107">`GetCountOfPrograms`方法會捕獲傳輸資料流程中的程式數目。</span><span class="sxs-lookup"><span data-stu-id="94dfe-107">The `GetCountOfPrograms` method retrieves the number of programs in the transport stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="94dfe-108">語法</span><span class="sxs-lookup"><span data-stu-id="94dfe-108">Syntax</span></span>


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a><span data-ttu-id="94dfe-109">參數</span><span class="sxs-lookup"><span data-stu-id="94dfe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94dfe-110">*pNumOfPrograms* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="94dfe-110">*pNumOfPrograms* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94dfe-111">接收程式數目之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="94dfe-111">Pointer to a variable that receives the number of programs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94dfe-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="94dfe-112">Return value</span></span>

<span data-ttu-id="94dfe-113">方法會傳回 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="94dfe-113">The method returns an HRESULT value.</span></span> <span data-ttu-id="94dfe-114">可能的值包括（但不限於）下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="94dfe-114">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="94dfe-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="94dfe-115">Return code</span></span>                                                                          | <span data-ttu-id="94dfe-116">Description</span><span class="sxs-lookup"><span data-stu-id="94dfe-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="94dfe-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="94dfe-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="94dfe-118">成功。</span><span class="sxs-lookup"><span data-stu-id="94dfe-118">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="94dfe-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94dfe-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94dfe-120">**IMpeg2PsiParser 介面**</span><span class="sxs-lookup"><span data-stu-id="94dfe-120">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="94dfe-121">PSI 剖析器篩選範例</span><span class="sxs-lookup"><span data-stu-id="94dfe-121">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




