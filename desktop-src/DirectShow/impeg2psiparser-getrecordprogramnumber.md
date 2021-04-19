---
description: 此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。 這不是支援的 DirectShow API。
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: IMpeg2PsiParser：： GetRecordProgramNumber 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetRecordProgramNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2bedc5922ce90fa2fda612f30571f884e75841d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971097"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a><span data-ttu-id="deb21-104">IMpeg2PsiParser：： GetRecordProgramNumber 方法</span><span class="sxs-lookup"><span data-stu-id="deb21-104">IMpeg2PsiParser::GetRecordProgramNumber method</span></span>

<span data-ttu-id="deb21-105">此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。</span><span class="sxs-lookup"><span data-stu-id="deb21-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="deb21-106">這不是支援的 DirectShow API。</span><span class="sxs-lookup"><span data-stu-id="deb21-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="deb21-107">方法會抓取 `GetRecordProgramNumber` 指定程式的程式編號。</span><span class="sxs-lookup"><span data-stu-id="deb21-107">The `GetRecordProgramNumber` method retrieves the program number for a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="deb21-108">語法</span><span class="sxs-lookup"><span data-stu-id="deb21-108">Syntax</span></span>


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="deb21-109">參數</span><span class="sxs-lookup"><span data-stu-id="deb21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deb21-110">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="deb21-110">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deb21-111">指定定義程式的 PAT 中的專案，從零編制索引。</span><span class="sxs-lookup"><span data-stu-id="deb21-111">Specifies the entry in the PAT that defines the program, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="deb21-112">*pwVal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="deb21-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="deb21-113">\_從 PAT 接收程式編號欄位之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="deb21-113">Pointer to a variable that receives the program\_number field from the PAT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deb21-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="deb21-114">Return value</span></span>

<span data-ttu-id="deb21-115">方法會傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="deb21-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="deb21-116">可能的值包括（但不限於）下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="deb21-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="deb21-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="deb21-117">Return code</span></span>                                                                          | <span data-ttu-id="deb21-118">Description</span><span class="sxs-lookup"><span data-stu-id="deb21-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="deb21-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="deb21-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="deb21-120">成功。</span><span class="sxs-lookup"><span data-stu-id="deb21-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="deb21-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="deb21-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deb21-122">**IMpeg2PsiParser 介面**</span><span class="sxs-lookup"><span data-stu-id="deb21-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="deb21-123">PSI 剖析器篩選範例</span><span class="sxs-lookup"><span data-stu-id="deb21-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




