---
title: 'IWMSecureBuffer Encrypt 方法 (Wmdrmsdk .h) '
description: Encrypt 方法會加密資料指標。
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- 加密方法 windows Media 格式
- 加密方法 windows Media Format，IWMSecureBuffer 介面
- IWMSecureBuffer 介面 windows 媒體格式，加密方法
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Encrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7758903de5f4a68cddffee982ad457d03ae6094
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983241"
---
# <a name="iwmsecurebufferencrypt-method"></a><span data-ttu-id="418eb-106">IWMSecureBuffer：： Encrypt 方法</span><span class="sxs-lookup"><span data-stu-id="418eb-106">IWMSecureBuffer::Encrypt method</span></span>

<span data-ttu-id="418eb-107">**Encrypt** 方法會加密資料指標。</span><span class="sxs-lookup"><span data-stu-id="418eb-107">The **Encrypt** method encrypts a data pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="418eb-108">語法</span><span class="sxs-lookup"><span data-stu-id="418eb-108">Syntax</span></span>


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a><span data-ttu-id="418eb-109">參數</span><span class="sxs-lookup"><span data-stu-id="418eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="418eb-110">*pSecureChannel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="418eb-110">*pSecureChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="418eb-111">安全通道介面的指標，其中包含要加密的資料指標。</span><span class="sxs-lookup"><span data-stu-id="418eb-111">Pointer to a secure channel interface containing the data pointer to encrypt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="418eb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="418eb-112">Return value</span></span>

<span data-ttu-id="418eb-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="418eb-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="418eb-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="418eb-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="418eb-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="418eb-115">Return code</span></span>                                                                          | <span data-ttu-id="418eb-116">Description</span><span class="sxs-lookup"><span data-stu-id="418eb-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="418eb-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="418eb-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="418eb-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="418eb-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="418eb-119">備註</span><span class="sxs-lookup"><span data-stu-id="418eb-119">Remarks</span></span>

<span data-ttu-id="418eb-120">您可以使用這個方法來加密資料指標，以便跨 DLL 界限傳送。</span><span class="sxs-lookup"><span data-stu-id="418eb-120">Use this method to encrypt data pointers so they can be sent across DLL boundaries.</span></span>

## <a name="requirements"></a><span data-ttu-id="418eb-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="418eb-121">Requirements</span></span>



| <span data-ttu-id="418eb-122">需求</span><span class="sxs-lookup"><span data-stu-id="418eb-122">Requirement</span></span> | <span data-ttu-id="418eb-123">值</span><span class="sxs-lookup"><span data-stu-id="418eb-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="418eb-124">標頭</span><span class="sxs-lookup"><span data-stu-id="418eb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="418eb-125"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="418eb-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="418eb-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="418eb-126">Library</span></span><br/> | <dl> <span data-ttu-id="418eb-127"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="418eb-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="418eb-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="418eb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="418eb-129">**解密**</span><span class="sxs-lookup"><span data-stu-id="418eb-129">**Decrypt**</span></span>](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[<span data-ttu-id="418eb-130">**IWMSecureBuffer 介面**</span><span class="sxs-lookup"><span data-stu-id="418eb-130">**IWMSecureBuffer Interface**</span></span>](iwmsecurebuffer.md)
</dt> </dl>

 

 





