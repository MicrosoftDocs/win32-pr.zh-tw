---
description: 此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。 這不是支援的 DirectShow API。
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: IMpeg2PsiParser：： GetPmtVersionNumber 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPmtVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3af4b20067af52216181848f4cc63ac5a7784ba9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106984538"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a><span data-ttu-id="ee778-104">IMpeg2PsiParser：： GetPmtVersionNumber 方法</span><span class="sxs-lookup"><span data-stu-id="ee778-104">IMpeg2PsiParser::GetPmtVersionNumber method</span></span>

<span data-ttu-id="ee778-105">此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。</span><span class="sxs-lookup"><span data-stu-id="ee778-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="ee778-106">這不是支援的 DirectShow API。</span><span class="sxs-lookup"><span data-stu-id="ee778-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="ee778-107">`GetPmtVersionNumber`方法會 \_ 從指定的 PMT 抓取版本號碼欄位。</span><span class="sxs-lookup"><span data-stu-id="ee778-107">The `GetPmtVersionNumber` method retrieves the version\_number field from a specified PMT.</span></span> <span data-ttu-id="ee778-108">當程式的定義變更時，版本號碼就會遞增。</span><span class="sxs-lookup"><span data-stu-id="ee778-108">The version number is incremented whenever the definition of the program changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee778-109">語法</span><span class="sxs-lookup"><span data-stu-id="ee778-109">Syntax</span></span>


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a><span data-ttu-id="ee778-110">參數</span><span class="sxs-lookup"><span data-stu-id="ee778-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee778-111">*wProgramNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee778-111">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee778-112">指定程式的 [程式 \_ 代碼] 欄位，如 PAT 所指定。</span><span class="sxs-lookup"><span data-stu-id="ee778-112">Specifies the program\_number field of the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="ee778-113">*pPmtVersion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ee778-113">*pPmtVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee778-114">接收版本號碼欄位之變數的指標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ee778-114">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee778-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee778-115">Return value</span></span>

<span data-ttu-id="ee778-116">方法會傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="ee778-116">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="ee778-117">可能的值包括（但不限於）下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="ee778-117">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="ee778-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ee778-118">Return code</span></span>                                                                          | <span data-ttu-id="ee778-119">Description</span><span class="sxs-lookup"><span data-stu-id="ee778-119">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="ee778-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ee778-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ee778-121">成功。</span><span class="sxs-lookup"><span data-stu-id="ee778-121">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ee778-122">備註</span><span class="sxs-lookup"><span data-stu-id="ee778-122">Remarks</span></span>

<span data-ttu-id="ee778-123">使用 **GetRecordProgramNumber** 方法來取得程式編號。</span><span class="sxs-lookup"><span data-stu-id="ee778-123">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee778-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee778-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee778-125">**IMpeg2PsiParser 介面**</span><span class="sxs-lookup"><span data-stu-id="ee778-125">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="ee778-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="ee778-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="ee778-127">PSI 剖析器篩選範例</span><span class="sxs-lookup"><span data-stu-id="ee778-127">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




