---
title: 'IWMSecureBuffer 解密方法 (Wmdrmsdk .h) '
description: 解密方法會解密透過呼叫 Encrypt 方法加密的資料指標。
ms.assetid: 15cedb56-686a-4a3c-81a5-b1797cfe0838
keywords:
- 解密方法 windows 媒體格式
- 解密方法 windows Media Format，IWMSecureBuffer 介面
- IWMSecureBuffer 介面 windows 媒體格式，解密方法
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Decrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6f48ae389090840e085c90b0bc5444e7cd6784e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001222"
---
# <a name="iwmsecurebufferdecrypt-method"></a><span data-ttu-id="d4729-106">IWMSecureBuffer：:D ecrypt 方法</span><span class="sxs-lookup"><span data-stu-id="d4729-106">IWMSecureBuffer::Decrypt method</span></span>

<span data-ttu-id="d4729-107">**解密** 方法會解密透過呼叫 [**Encrypt**](iwmsecurebuffer-encrypt.md)方法加密的資料指標。</span><span class="sxs-lookup"><span data-stu-id="d4729-107">The **Decrypt** method decrypts a data pointer that was encrypted by calling the [**Encrypt**](iwmsecurebuffer-encrypt.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4729-108">語法</span><span class="sxs-lookup"><span data-stu-id="d4729-108">Syntax</span></span>


```C++
HRESULT Decrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a><span data-ttu-id="d4729-109">參數</span><span class="sxs-lookup"><span data-stu-id="d4729-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4729-110">*pSecureChannel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4729-110">*pSecureChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4729-111">安全通道介面的指標，其中包含加密的資料指標。</span><span class="sxs-lookup"><span data-stu-id="d4729-111">Pointer to a secure channel interface containing the encrypted data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4729-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4729-112">Return value</span></span>

<span data-ttu-id="d4729-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="d4729-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d4729-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="d4729-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d4729-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d4729-115">Return code</span></span>                                                                          | <span data-ttu-id="d4729-116">Description</span><span class="sxs-lookup"><span data-stu-id="d4729-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d4729-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d4729-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d4729-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="d4729-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d4729-119">備註</span><span class="sxs-lookup"><span data-stu-id="d4729-119">Remarks</span></span>

<span data-ttu-id="d4729-120">無。</span><span class="sxs-lookup"><span data-stu-id="d4729-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4729-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4729-121">Requirements</span></span>



| <span data-ttu-id="d4729-122">需求</span><span class="sxs-lookup"><span data-stu-id="d4729-122">Requirement</span></span> | <span data-ttu-id="d4729-123">值</span><span class="sxs-lookup"><span data-stu-id="d4729-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4729-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d4729-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d4729-125"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4729-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4729-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="d4729-126">Library</span></span><br/> | <dl> <span data-ttu-id="d4729-127"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4729-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4729-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4729-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4729-129">**加密**</span><span class="sxs-lookup"><span data-stu-id="d4729-129">**Encrypt**</span></span>](iwmsecurebuffer-encrypt.md)
</dt> <dt>

[<span data-ttu-id="d4729-130">**IWMSecureBuffer 介面**</span><span class="sxs-lookup"><span data-stu-id="d4729-130">**IWMSecureBuffer Interface**</span></span>](iwmsecurebuffer.md)
</dt> </dl>

 

 





