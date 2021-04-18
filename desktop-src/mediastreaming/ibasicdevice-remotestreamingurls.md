---
title: IBasicDevice RemoteStreamingUrls 方法
description: 傳回遠端串流 Url 的向量。
ms.assetid: 19B4475F-A7E4-4DC4-9C88-68D91D023AF4
keywords:
- RemoteStreamingUrls 方法媒體串流 API
- RemoteStreamingUrls 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，RemoteStreamingUrls 方法
topic_type:
- apiref
api_name:
- IBasicDevice.RemoteStreamingUrls
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdc4bd363096e7b808a51cfbddb764daabe03a55
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373001"
---
# <a name="ibasicdeviceremotestreamingurls-method"></a><span data-ttu-id="297b4-106">IBasicDevice：： RemoteStreamingUrls 方法</span><span class="sxs-lookup"><span data-stu-id="297b4-106">IBasicDevice::RemoteStreamingUrls method</span></span>

<span data-ttu-id="297b4-107">傳回遠端串流 Url 的向量。</span><span class="sxs-lookup"><span data-stu-id="297b4-107">Returns a vector of remote streaming URLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="297b4-108">語法</span><span class="sxs-lookup"><span data-stu-id="297b4-108">Syntax</span></span>


```C++
HRESULT RemoteStreamingUrls(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="297b4-109">參數</span><span class="sxs-lookup"><span data-stu-id="297b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="297b4-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="297b4-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="297b4-111">接收遠端串流 Url 之指標的可列舉集合。</span><span class="sxs-lookup"><span data-stu-id="297b4-111">Receives an enumerable collection of pointers to remote streaming URLs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="297b4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="297b4-112">Return value</span></span>

<span data-ttu-id="297b4-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="297b4-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="297b4-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="297b4-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="297b4-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="297b4-115">Return code</span></span>                                                                          | <span data-ttu-id="297b4-116">Description</span><span class="sxs-lookup"><span data-stu-id="297b4-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="297b4-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="297b4-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="297b4-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="297b4-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="297b4-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="297b4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="297b4-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="297b4-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





