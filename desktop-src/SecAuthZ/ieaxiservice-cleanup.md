---
description: 釋放 IeAxiService 介面使用的資源。
ms.assetid: 11f5cfdc-dcdd-4b41-b02c-b19b9452509e
title: IeAxiService：：清除方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Cleanup
api_type:
- COM
api_location: ''
ms.openlocfilehash: b29784ae360ec78b9f7e01d2045617615333a5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193908"
---
# <a name="ieaxiservicecleanup-method"></a><span data-ttu-id="f7ea8-103">IeAxiService：：清除方法</span><span class="sxs-lookup"><span data-stu-id="f7ea8-103">IeAxiService::Cleanup method</span></span>

<span data-ttu-id="f7ea8-104">**清除** 方法會釋放 [**IeAxiService**](ieaxiservice.md)介面所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="f7ea8-104">The **Cleanup** method frees resources used by the [**IeAxiService**](ieaxiservice.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7ea8-105">語法</span><span class="sxs-lookup"><span data-stu-id="f7ea8-105">Syntax</span></span>


```C++
HRESULT Cleanup();
```



## <a name="parameters"></a><span data-ttu-id="f7ea8-106">參數</span><span class="sxs-lookup"><span data-stu-id="f7ea8-106">Parameters</span></span>

<span data-ttu-id="f7ea8-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f7ea8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f7ea8-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7ea8-108">Return value</span></span>

<span data-ttu-id="f7ea8-109">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="f7ea8-109">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="f7ea8-110">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="f7ea8-110">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="f7ea8-111">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](/windows/desktop/SecCrypto/common-hresult-values)。</span><span class="sxs-lookup"><span data-stu-id="f7ea8-111">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7ea8-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7ea8-112">Requirements</span></span>



| <span data-ttu-id="f7ea8-113">需求</span><span class="sxs-lookup"><span data-stu-id="f7ea8-113">Requirement</span></span> | <span data-ttu-id="f7ea8-114">值</span><span class="sxs-lookup"><span data-stu-id="f7ea8-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ea8-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7ea8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f7ea8-116">Windows Vista Business、Windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7ea8-116">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f7ea8-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7ea8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f7ea8-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="f7ea8-118">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="f7ea8-119">IID</span><span class="sxs-lookup"><span data-stu-id="f7ea8-119">IID</span></span><br/>                      | <span data-ttu-id="f7ea8-120">IID \_ IeAxiService 定義為 E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="f7ea8-120">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="f7ea8-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7ea8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7ea8-122">**IeAxiService**</span><span class="sxs-lookup"><span data-stu-id="f7ea8-122">**IeAxiService**</span></span>](ieaxiservice.md)
</dt> </dl>

 

