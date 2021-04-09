---
description: 抓取代表資料區塊的 PROPVARIANT 和輸入字串。 呼叫這個方法與呼叫的方法相同。
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: IRichChunk：： RemoteGetData 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRichChunk.RemoteGetData
api_type:
- COM
api_location: ''
ms.openlocfilehash: 002c85b189a3994b70795c05228ae5331c610284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112389"
---
# <a name="irichchunkremotegetdata-method"></a><span data-ttu-id="f3fea-104">IRichChunk：： RemoteGetData 方法</span><span class="sxs-lookup"><span data-stu-id="f3fea-104">IRichChunk::RemoteGetData method</span></span>

<span data-ttu-id="f3fea-105">抓取代表資料區塊的 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 和輸入字串。</span><span class="sxs-lookup"><span data-stu-id="f3fea-105">Retrieves the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) and input string that represents a chunk of data.</span></span> <span data-ttu-id="f3fea-106">呼叫這個方法與呼叫的方法相同 [**。**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata)</span><span class="sxs-lookup"><span data-stu-id="f3fea-106">Calling this method is the same as calling [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3fea-107">語法</span><span class="sxs-lookup"><span data-stu-id="f3fea-107">Syntax</span></span>


```C++
HRESULT RemoteGetData(
  [out] ULONG       *pFirstPos,
  [out] ULONG       *pLength,
  [out] LPWSTR      *ppsz,
  [out] PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="f3fea-108">參數</span><span class="sxs-lookup"><span data-stu-id="f3fea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3fea-109">*pFirstPos* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f3fea-109">*pFirstPos* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3fea-110">接收範圍的以零為基底的開始位置。</span><span class="sxs-lookup"><span data-stu-id="f3fea-110">Receives the zero-based starting position of the range.</span></span> <span data-ttu-id="f3fea-111">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f3fea-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f3fea-112">*pLength* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f3fea-112">*pLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3fea-113">接收範圍的長度。</span><span class="sxs-lookup"><span data-stu-id="f3fea-113">Receives the length of the range.</span></span> <span data-ttu-id="f3fea-114">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f3fea-114">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f3fea-115">*ppsz* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f3fea-115">*ppsz* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3fea-116">接收相關聯的 Unicode 字串值，如果無法使用，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="f3fea-116">Receives the associated Unicode string value, or **NULL** if not available.</span></span>

</dd> <dt>

<span data-ttu-id="f3fea-117">*pValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f3fea-117">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3fea-118">如果無法使用，則會接收相關聯的 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 值或 **VT \_ 空白** 。</span><span class="sxs-lookup"><span data-stu-id="f3fea-118">Receives the associated [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value, or **VT\_EMPTY** if not available.</span></span> <span data-ttu-id="f3fea-119">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f3fea-119">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3fea-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3fea-120">Return value</span></span>

<span data-ttu-id="f3fea-121">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f3fea-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f3fea-122">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f3fea-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="f3fea-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3fea-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3fea-124">**IRichChunk**</span><span class="sxs-lookup"><span data-stu-id="f3fea-124">**IRichChunk**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
