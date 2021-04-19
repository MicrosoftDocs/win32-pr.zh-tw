---
title: 'CBCreateClientInstance 函式 (Cbclient) '
description: 建立遠端桌面連線代理人 RPC 用戶端的實例。
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- CBCreateClientInstance 函式遠端桌面服務
topic_type:
- apiref
api_name:
- CBCreateClientInstance
api_location:
- Cbclient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2b30f2d236bcc90dfa4977f54d56a5d1717d18a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001016"
---
# <a name="cbcreateclientinstance-function"></a><span data-ttu-id="56a0c-104">CBCreateClientInstance 函式</span><span class="sxs-lookup"><span data-stu-id="56a0c-104">CBCreateClientInstance function</span></span>

<span data-ttu-id="56a0c-105">建立遠端桌面連線代理人 RPC 用戶端的實例。</span><span class="sxs-lookup"><span data-stu-id="56a0c-105">Creates an instance of the Remote Desktop Connection Broker RPC client.</span></span>

## <a name="syntax"></a><span data-ttu-id="56a0c-106">語法</span><span class="sxs-lookup"><span data-stu-id="56a0c-106">Syntax</span></span>


```C++
HRESULT CBCreateClientInstance(
  _In_  DWORD                   Version,
  _Out_ IConnectionBrokerClient **ppCbClient
);
```



## <a name="parameters"></a><span data-ttu-id="56a0c-107">參數</span><span class="sxs-lookup"><span data-stu-id="56a0c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56a0c-108">*版本* \[在\]</span><span class="sxs-lookup"><span data-stu-id="56a0c-108">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-109">指定所要求遠端桌面連線代理人用戶端介面的版本。</span><span class="sxs-lookup"><span data-stu-id="56a0c-109">Specifies the version of the Remote Desktop Connection Broker client interface being requested.</span></span> <span data-ttu-id="56a0c-110">這必須是下列值。</span><span class="sxs-lookup"><span data-stu-id="56a0c-110">This must be the following value.</span></span>

<dt>

<span data-ttu-id="56a0c-111">1</span><span class="sxs-lookup"><span data-stu-id="56a0c-111">1</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-112">遠端桌面連線代理人用戶端的第1版。</span><span class="sxs-lookup"><span data-stu-id="56a0c-112">Version 1 of the Remote Desktop Connection Broker client.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="56a0c-113">*ppCbClient* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="56a0c-113">*ppCbClient* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56a0c-114">接收遠端桌面連線代理人用戶端物件之 [**IConnectionBrokerClient**](iconnectionbrokerclient.md) 介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="56a0c-114">The address of an [**IConnectionBrokerClient**](iconnectionbrokerclient.md) interface pointer that receives the Remote Desktop Connection Broker client object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56a0c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="56a0c-115">Return value</span></span>

<span data-ttu-id="56a0c-116">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="56a0c-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="56a0c-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="56a0c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="56a0c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="56a0c-118">Requirements</span></span>



| <span data-ttu-id="56a0c-119">需求</span><span class="sxs-lookup"><span data-stu-id="56a0c-119">Requirement</span></span> | <span data-ttu-id="56a0c-120">值</span><span class="sxs-lookup"><span data-stu-id="56a0c-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56a0c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="56a0c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="56a0c-122"><dt>Cbclient。h</dt></span><span class="sxs-lookup"><span data-stu-id="56a0c-122"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="56a0c-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="56a0c-123">Library</span></span><br/> | <dl> <span data-ttu-id="56a0c-124"><dt>Cbclient .lib</dt></span><span class="sxs-lookup"><span data-stu-id="56a0c-124"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="56a0c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="56a0c-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="56a0c-126"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56a0c-126"><dt>Cbclient.dll</dt></span></span> </dl> |



 

 





