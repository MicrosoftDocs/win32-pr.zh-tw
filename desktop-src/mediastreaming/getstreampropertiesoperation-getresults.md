---
title: GetStreamPropertiesOperation. GetResults 方法
description: 傳回 GetStreamPropertiesAsync 啟動的非同步作業結果。
ms.assetid: D09DCDF5-2B9E-4E03-908B-AEEC7DC228C1
keywords:
- GetResults 方法媒體串流 API
- GetResults 方法媒體串流 API，GetStreamPropertiesOperation 介面
- GetStreamPropertiesOperation 介面媒體串流 API，GetResults 方法
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 312703c28f5cdbb888b46d6ccd312dd358aa6b6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375152"
---
# <a name="getstreampropertiesoperationgetresults-method"></a><span data-ttu-id="edf98-106">GetStreamPropertiesOperation. GetResults 方法</span><span class="sxs-lookup"><span data-stu-id="edf98-106">GetStreamPropertiesOperation.GetResults method</span></span>

<span data-ttu-id="edf98-107">傳回 [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))啟動的非同步作業結果。</span><span class="sxs-lookup"><span data-stu-id="edf98-107">Returns the results of the asynchronous operation started by [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span>

## <a name="syntax"></a><span data-ttu-id="edf98-108">語法</span><span class="sxs-lookup"><span data-stu-id="edf98-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="edf98-109">參數</span><span class="sxs-lookup"><span data-stu-id="edf98-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edf98-110">*值* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="edf98-110">*value* \[out, retval\]</span></span>
<span data-ttu-id="edf98-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="edf98-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="edf98-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="edf98-112">Return value</span></span>

<span data-ttu-id="edf98-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="edf98-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="edf98-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="edf98-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="edf98-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="edf98-115">Return code</span></span>                                                                          | <span data-ttu-id="edf98-116">Description</span><span class="sxs-lookup"><span data-stu-id="edf98-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="edf98-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="edf98-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="edf98-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="edf98-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="edf98-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edf98-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edf98-120">**GetStreamPropertiesOperation**</span><span class="sxs-lookup"><span data-stu-id="edf98-120">**GetStreamPropertiesOperation**</span></span>](getstreampropertiesoperation.md)
</dt> </dl>

 

