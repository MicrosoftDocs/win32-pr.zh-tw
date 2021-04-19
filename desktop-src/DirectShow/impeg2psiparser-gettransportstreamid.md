---
description: 此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。 這不是支援的 DirectShow API。
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: IMpeg2PsiParser：： GetTransportStreamId 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetTransportStreamId
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9615c50d8d16aa6d78e3e1b83a3ec0e356c6cb50
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973355"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a><span data-ttu-id="957c3-104">IMpeg2PsiParser：： GetTransportStreamId 方法</span><span class="sxs-lookup"><span data-stu-id="957c3-104">IMpeg2PsiParser::GetTransportStreamId method</span></span>

<span data-ttu-id="957c3-105">此方法的實作為使用 DirectShow SDK 的範例程式碼來提供。</span><span class="sxs-lookup"><span data-stu-id="957c3-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="957c3-106">這不是支援的 DirectShow API。</span><span class="sxs-lookup"><span data-stu-id="957c3-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="957c3-107">`GetTransportStreamId`方法會 \_ 從 PAT 抓取傳輸資料流程 \_ 識別碼欄位。</span><span class="sxs-lookup"><span data-stu-id="957c3-107">The `GetTransportStreamId` method retrieves the transport\_stream\_id field from the PAT.</span></span> <span data-ttu-id="957c3-108">這個值是由使用者定義，可用來區別特定的傳輸資料流程與相同網路上的其他資料流程。</span><span class="sxs-lookup"><span data-stu-id="957c3-108">This value is defined by the user, and can be used to distinguish a particular transport stream from other streams on the same network.</span></span> <span data-ttu-id="957c3-109">傳輸資料流程最多包含一個 PAT。</span><span class="sxs-lookup"><span data-stu-id="957c3-109">A transport stream contains at most one PAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="957c3-110">語法</span><span class="sxs-lookup"><span data-stu-id="957c3-110">Syntax</span></span>


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a><span data-ttu-id="957c3-111">參數</span><span class="sxs-lookup"><span data-stu-id="957c3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="957c3-112">*pStreamId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="957c3-112">*pStreamId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="957c3-113">接收傳輸 \_ 資料流程識別碼欄位之變數的指標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="957c3-113">Pointer to a variable that receives the transport\_stream\_id field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="957c3-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="957c3-114">Return value</span></span>

<span data-ttu-id="957c3-115">方法會傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="957c3-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="957c3-116">可能的值包括（但不限於）下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="957c3-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="957c3-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="957c3-117">Return code</span></span>                                                                          | <span data-ttu-id="957c3-118">Description</span><span class="sxs-lookup"><span data-stu-id="957c3-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="957c3-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="957c3-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="957c3-120">成功。</span><span class="sxs-lookup"><span data-stu-id="957c3-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="957c3-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="957c3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="957c3-122">**IMpeg2PsiParser 介面**</span><span class="sxs-lookup"><span data-stu-id="957c3-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="957c3-123">PSI 剖析器篩選範例</span><span class="sxs-lookup"><span data-stu-id="957c3-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




