---
title: StreamSelectOperation. GetResults 方法
description: 傳回 SelectBestStreamAsync 啟動的非同步作業結果。
ms.assetid: 2D9887E7-17C8-4161-984F-FA44591D2052
keywords:
- GetResults 方法媒體串流 API
- GetResults 方法媒體串流 API，StreamSelectOperation 介面
- StreamSelectOperation 介面媒體串流 API，GetResults 方法
topic_type:
- apiref
api_name:
- StreamSelectOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c52479949413d32ca54654f355a06a2dee70866e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968088"
---
# <a name="streamselectoperationgetresults-method"></a><span data-ttu-id="55d7c-106">StreamSelectOperation. GetResults 方法</span><span class="sxs-lookup"><span data-stu-id="55d7c-106">StreamSelectOperation.GetResults method</span></span>

<span data-ttu-id="55d7c-107">傳回 [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))啟動的非同步作業結果。</span><span class="sxs-lookup"><span data-stu-id="55d7c-107">Returns the results of the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span>

## <a name="syntax"></a><span data-ttu-id="55d7c-108">語法</span><span class="sxs-lookup"><span data-stu-id="55d7c-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="55d7c-109">參數</span><span class="sxs-lookup"><span data-stu-id="55d7c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55d7c-110">*值* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="55d7c-110">*value* \[out, retval\]</span></span>
<span data-ttu-id="55d7c-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="55d7c-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="55d7c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="55d7c-112">Return value</span></span>

<span data-ttu-id="55d7c-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="55d7c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="55d7c-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="55d7c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="55d7c-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="55d7c-115">Return code</span></span>                                                                          | <span data-ttu-id="55d7c-116">Description</span><span class="sxs-lookup"><span data-stu-id="55d7c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="55d7c-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="55d7c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="55d7c-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="55d7c-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="55d7c-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55d7c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55d7c-120">**StreamSelectOperation**</span><span class="sxs-lookup"><span data-stu-id="55d7c-120">**StreamSelectOperation**</span></span>](streamselectoperation.md)
</dt> </dl>

 

