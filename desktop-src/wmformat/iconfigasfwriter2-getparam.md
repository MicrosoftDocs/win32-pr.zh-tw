---
title: IConfigAsfWriter2 GetParam 方法
description: GetParam 方法會抓取指定之篩選準則設定參數的目前值。
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- GetParam 方法 windows Media 格式
- GetParam 方法 windows Media Format，IConfigAsfWriter2 介面
- IConfigAsfWriter2 介面 windows Media Format，GetParam 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d72b8011072424679729686dd5a14c92bae90f66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966471"
---
# <a name="iconfigasfwriter2getparam-method"></a><span data-ttu-id="ad81d-106">IConfigAsfWriter2：： GetParam 方法</span><span class="sxs-lookup"><span data-stu-id="ad81d-106">IConfigAsfWriter2::GetParam method</span></span>

<span data-ttu-id="ad81d-107">**GetParam** 方法會抓取指定之篩選準則設定參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="ad81d-107">The **GetParam** method retrieves the current value of the specified filter configuration parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad81d-108">語法</span><span class="sxs-lookup"><span data-stu-id="ad81d-108">Syntax</span></span>


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a><span data-ttu-id="ad81d-109">參數</span><span class="sxs-lookup"><span data-stu-id="ad81d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad81d-110">*dwParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad81d-110">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad81d-111">指定要取出的參數。</span><span class="sxs-lookup"><span data-stu-id="ad81d-111">Specifies the parameter to retrieve.</span></span> <span data-ttu-id="ad81d-112">它必須是[ \_ AM \_ ASFWRITERCONFIG \_ PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))列舉中所定義的值。</span><span class="sxs-lookup"><span data-stu-id="ad81d-112">It must be a value defined in the [\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="ad81d-113">*pdwParam1* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ad81d-113">*pdwParam1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad81d-114">變數的指標，該變數會抓取 *dwParam* 中指定之參數的值。</span><span class="sxs-lookup"><span data-stu-id="ad81d-114">Pointer to a variable that retrieves the value of the parameter specified in *dwParam*.</span></span>

</dd> <dt>

<span data-ttu-id="ad81d-115">*pdwParam2* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ad81d-115">*pdwParam2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad81d-116">未使用，必須為零。</span><span class="sxs-lookup"><span data-stu-id="ad81d-116">Not used, must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad81d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad81d-117">Return value</span></span>

<span data-ttu-id="ad81d-118">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ad81d-118">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="ad81d-119">如果失敗，則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ad81d-119">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad81d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad81d-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad81d-121">[**IConfigAsfWriter2 介面**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ad81d-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ad81d-122">**IConfigAsfWriter2：： SetParam**</span><span class="sxs-lookup"><span data-stu-id="ad81d-122">**IConfigAsfWriter2::SetParam**</span></span>](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 