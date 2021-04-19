---
title: IConfigAsfWriter2 SetParam 方法
description: SetParam 方法會設定指定之篩選設定參數的值。
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- SetParam 方法 windows Media 格式
- SetParam 方法 windows Media Format，IConfigAsfWriter2 介面
- IConfigAsfWriter2 介面 windows Media Format，SetParam 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f123bf11c8297f3a7ce0d4b0047874d8d7b31b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967908"
---
# <a name="iconfigasfwriter2setparam-method"></a><span data-ttu-id="6628d-106">IConfigAsfWriter2：： SetParam 方法</span><span class="sxs-lookup"><span data-stu-id="6628d-106">IConfigAsfWriter2::SetParam method</span></span>

<span data-ttu-id="6628d-107">**SetParam** 方法會設定指定之篩選設定參數的值。</span><span class="sxs-lookup"><span data-stu-id="6628d-107">The **SetParam** method sets the value of the specified filter configuration parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="6628d-108">語法</span><span class="sxs-lookup"><span data-stu-id="6628d-108">Syntax</span></span>


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a><span data-ttu-id="6628d-109">參數</span><span class="sxs-lookup"><span data-stu-id="6628d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6628d-110">*dwParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6628d-110">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6628d-111">指定要設定的參數。</span><span class="sxs-lookup"><span data-stu-id="6628d-111">Specifies the parameter to set.</span></span> <span data-ttu-id="6628d-112">它必須是[ \_ AM \_ ASFWRITERCONFIG \_ PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))列舉中所定義的值。</span><span class="sxs-lookup"><span data-stu-id="6628d-112">It must be a value defined in the [\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="6628d-113">*dwParam1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6628d-113">*dwParam1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6628d-114">指定要指派給 *dwParam* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="6628d-114">Specifies the value to assign to the *dwParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6628d-115">*dwParam2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6628d-115">*dwParam2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6628d-116">未使用;必須是0。</span><span class="sxs-lookup"><span data-stu-id="6628d-116">Not used; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6628d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="6628d-117">Return value</span></span>

<span data-ttu-id="6628d-118">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="6628d-118">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="6628d-119">如果失敗，則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6628d-119">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="6628d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6628d-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="6628d-121">[**IConfigAsfWriter2 介面**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6628d-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6628d-122">**IConfigAsfWriter2：： GetParam**</span><span class="sxs-lookup"><span data-stu-id="6628d-122">**IConfigAsfWriter2::GetParam**</span></span>](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 