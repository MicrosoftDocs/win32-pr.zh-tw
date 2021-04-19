---
description: 抓取根交易內容中所裝載之交易的隔離等級和超時值。
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: ICoNtextTransactionInfo：： GetTxIsolationLevelAndTimeout 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.GetTxIsolationLevelAndTimeout
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8545a697e672af7206a69ffa19618d5b70e055c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970551"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a><span data-ttu-id="05494-103">ICoNtextTransactionInfo：： GetTxIsolationLevelAndTimeout 方法</span><span class="sxs-lookup"><span data-stu-id="05494-103">IContextTransactionInfo::GetTxIsolationLevelAndTimeout method</span></span>

<span data-ttu-id="05494-104">抓取根交易內容中所裝載之交易的隔離等級和超時值。</span><span class="sxs-lookup"><span data-stu-id="05494-104">Retrieves the isolation level and timeout value of a transaction that is hosted in the root transaction context.</span></span>

## <a name="syntax"></a><span data-ttu-id="05494-105">語法</span><span class="sxs-lookup"><span data-stu-id="05494-105">Syntax</span></span>


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a><span data-ttu-id="05494-106">參數</span><span class="sxs-lookup"><span data-stu-id="05494-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05494-107">*pIsoLevel* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="05494-107">*pIsoLevel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05494-108">交易的 [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) 值。</span><span class="sxs-lookup"><span data-stu-id="05494-108">The [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) value for the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="05494-109">*dwTime* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="05494-109">*dwTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05494-110">交易的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="05494-110">The timeout of the transaction, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05494-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="05494-111">Return value</span></span>

<span data-ttu-id="05494-112">這個方法可以傳回標準傳回值 E \_ INVALIDARG、e \_ OUTOFMEMORY、e 非 \_ 預期和 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="05494-112">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="05494-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="05494-113">Requirements</span></span>



| <span data-ttu-id="05494-114">需求</span><span class="sxs-lookup"><span data-stu-id="05494-114">Requirement</span></span> | <span data-ttu-id="05494-115">值</span><span class="sxs-lookup"><span data-stu-id="05494-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="05494-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05494-116">Minimum supported client</span></span><br/> | <span data-ttu-id="05494-117">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05494-117">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="05494-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05494-118">Minimum supported server</span></span><br/> | <span data-ttu-id="05494-119">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05494-119">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05494-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05494-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05494-121">**ICoNtextTransactionInfo**</span><span class="sxs-lookup"><span data-stu-id="05494-121">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

