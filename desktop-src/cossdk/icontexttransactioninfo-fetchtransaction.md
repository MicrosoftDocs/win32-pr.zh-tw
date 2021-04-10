---
description: 抓取與目前內容相關聯的交易或交易 proxy （如果有的話）。
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: ICoNtextTransactionInfo：： FetchTransaction 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.FetchTransaction
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0e753974f93539f051465f13a1ea92d7e0e3bfa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110916"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a><span data-ttu-id="fb801-103">ICoNtextTransactionInfo：： FetchTransaction 方法</span><span class="sxs-lookup"><span data-stu-id="fb801-103">IContextTransactionInfo::FetchTransaction method</span></span>

<span data-ttu-id="fb801-104">抓取與目前內容相關聯的交易或交易 proxy （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="fb801-104">Retrieves the transaction or transaction proxy that is associated with the current context, if any.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb801-105">語法</span><span class="sxs-lookup"><span data-stu-id="fb801-105">Syntax</span></span>


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="fb801-106">參數</span><span class="sxs-lookup"><span data-stu-id="fb801-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb801-107">*pUnk* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="fb801-107">*pUnk* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fb801-108">與目前內容相關聯的交易或交易 proxy;否則 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="fb801-108">The transaction or transaction proxy that is associated with the current context; otherwise, **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb801-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb801-109">Return value</span></span>

<span data-ttu-id="fb801-110">這個方法可以傳回標準傳回值 E \_ INVALIDARG、e \_ OUTOFMEMORY、e 非 \_ 預期和 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="fb801-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb801-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb801-111">Requirements</span></span>



| <span data-ttu-id="fb801-112">需求</span><span class="sxs-lookup"><span data-stu-id="fb801-112">Requirement</span></span> | <span data-ttu-id="fb801-113">值</span><span class="sxs-lookup"><span data-stu-id="fb801-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="fb801-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb801-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fb801-115">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb801-115">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="fb801-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb801-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fb801-117">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb801-117">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fb801-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb801-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb801-119">**ICoNtextTransactionInfo**</span><span class="sxs-lookup"><span data-stu-id="fb801-119">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

 




