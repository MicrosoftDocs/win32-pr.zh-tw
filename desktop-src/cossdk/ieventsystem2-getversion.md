---
description: 捕獲事件系統的版本號碼。
ms.assetid: 6355f1b3-e1e7-435f-9795-d92464e004ae
title: IEventSystem2：： GetVersion 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.GetVersion
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2c75538d9fd71cb8ee81e454249fd5116ccd090c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468521"
---
# <a name="ieventsystem2getversion-method"></a><span data-ttu-id="0a3f7-103">IEventSystem2：： GetVersion 方法</span><span class="sxs-lookup"><span data-stu-id="0a3f7-103">IEventSystem2::GetVersion method</span></span>

<span data-ttu-id="0a3f7-104">捕獲事件系統的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="0a3f7-104">Retrieves the version number of the event system.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a3f7-105">語法</span><span class="sxs-lookup"><span data-stu-id="0a3f7-105">Syntax</span></span>


```C++
HRESULT GetVersion(
  [out] int *pnVersion
);
```



## <a name="parameters"></a><span data-ttu-id="0a3f7-106">參數</span><span class="sxs-lookup"><span data-stu-id="0a3f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a3f7-107">*pnVersion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0a3f7-107">*pnVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a3f7-108">事件系統的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="0a3f7-108">The version number of the event system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a3f7-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a3f7-109">Return value</span></span>

<span data-ttu-id="0a3f7-110">這個方法可以傳回標準傳回值 E \_ INVALIDARG、e \_ OUTOFMEMORY、e 非 \_ 預期、e \_ 失敗和 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="0a3f7-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a3f7-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a3f7-111">Requirements</span></span>



| <span data-ttu-id="0a3f7-112">需求</span><span class="sxs-lookup"><span data-stu-id="0a3f7-112">Requirement</span></span> | <span data-ttu-id="0a3f7-113">值</span><span class="sxs-lookup"><span data-stu-id="0a3f7-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0a3f7-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a3f7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0a3f7-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a3f7-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0a3f7-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a3f7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0a3f7-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a3f7-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0a3f7-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a3f7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a3f7-119">**IEventSystem2**</span><span class="sxs-lookup"><span data-stu-id="0a3f7-119">**IEventSystem2**</span></span>](ieventsystem2.md)
</dt> </dl>

 

 




