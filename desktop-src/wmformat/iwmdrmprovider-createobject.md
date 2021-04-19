---
title: 'IWMDRMProvider CreateObject 方法 (Wmdrmsdk .h) '
description: CreateObject 方法會抓取指定介面的指標，並視需要建立執行物件。
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- CreateObject 方法 windows Media 格式
- CreateObject 方法 windows Media Format，IWMDRMProvider 介面
- IWMDRMProvider 介面 windows Media Format，CreateObject 方法
topic_type:
- apiref
api_name:
- IWMDRMProvider.CreateObject
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0422138391b0d6f5e38fbc81fd5141bd3d8535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983982"
---
# <a name="iwmdrmprovidercreateobject-method"></a><span data-ttu-id="f0e5d-106">IWMDRMProvider：： CreateObject 方法</span><span class="sxs-lookup"><span data-stu-id="f0e5d-106">IWMDRMProvider::CreateObject method</span></span>

<span data-ttu-id="f0e5d-107">**CreateObject** 方法會抓取指定介面的指標，並視需要建立執行物件。</span><span class="sxs-lookup"><span data-stu-id="f0e5d-107">The **CreateObject** method retrieves a pointer to a specified interface, creating the implementing object if needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0e5d-108">語法</span><span class="sxs-lookup"><span data-stu-id="f0e5d-108">Syntax</span></span>


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a><span data-ttu-id="f0e5d-109">參數</span><span class="sxs-lookup"><span data-stu-id="f0e5d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0e5d-110">*riid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0e5d-110">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0e5d-111">要建立之介面的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0e5d-111">Identifier of the interface to be created.</span></span> <span data-ttu-id="f0e5d-112">設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f0e5d-112">Set to one of the following values.</span></span>

-   <span data-ttu-id="f0e5d-113">IID \_ IWMDRMLicenseManagement</span><span class="sxs-lookup"><span data-stu-id="f0e5d-113">IID\_IWMDRMLicenseManagement</span></span>
-   <span data-ttu-id="f0e5d-114">IID \_ IWMDRMLicenseQuery</span><span class="sxs-lookup"><span data-stu-id="f0e5d-114">IID\_IWMDRMLicenseQuery</span></span>
-   <span data-ttu-id="f0e5d-115">IID \_ IWMDRMNetReceiver</span><span class="sxs-lookup"><span data-stu-id="f0e5d-115">IID\_IWMDRMNetReceiver</span></span>
-   <span data-ttu-id="f0e5d-116">IID \_ IWMDRMNetTransmitter</span><span class="sxs-lookup"><span data-stu-id="f0e5d-116">IID\_IWMDRMNetTransmitter</span></span>
-   <span data-ttu-id="f0e5d-117">IID \_ IWMDRMSecurity</span><span class="sxs-lookup"><span data-stu-id="f0e5d-117">IID\_IWMDRMSecurity</span></span>

</dd> <dt>

<span data-ttu-id="f0e5d-118">*ppvObject* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f0e5d-118">*ppvObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0e5d-119">接收所要求介面位址之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="f0e5d-119">Address of a pointer that receives the address of the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0e5d-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0e5d-120">Return value</span></span>

<span data-ttu-id="f0e5d-121">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="f0e5d-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f0e5d-122">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="f0e5d-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f0e5d-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f0e5d-123">Return code</span></span>                                                                          | <span data-ttu-id="f0e5d-124">Description</span><span class="sxs-lookup"><span data-stu-id="f0e5d-124">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f0e5d-125"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f0e5d-125"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f0e5d-126">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="f0e5d-126">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0e5d-127">備註</span><span class="sxs-lookup"><span data-stu-id="f0e5d-127">Remarks</span></span>

<span data-ttu-id="f0e5d-128">無。</span><span class="sxs-lookup"><span data-stu-id="f0e5d-128">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0e5d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0e5d-129">Requirements</span></span>



| <span data-ttu-id="f0e5d-130">需求</span><span class="sxs-lookup"><span data-stu-id="f0e5d-130">Requirement</span></span> | <span data-ttu-id="f0e5d-131">值</span><span class="sxs-lookup"><span data-stu-id="f0e5d-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e5d-132">標頭</span><span class="sxs-lookup"><span data-stu-id="f0e5d-132">Header</span></span><br/>  | <dl> <span data-ttu-id="f0e5d-133"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0e5d-133"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0e5d-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="f0e5d-134">Library</span></span><br/> | <dl> <span data-ttu-id="f0e5d-135"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0e5d-135"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0e5d-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0e5d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0e5d-137">**IWMDRMProvider 介面**</span><span class="sxs-lookup"><span data-stu-id="f0e5d-137">**IWMDRMProvider Interface**</span></span>](iwmdrmprovider.md)
</dt> <dt>

[<span data-ttu-id="f0e5d-138">**IWMDRMLicenseManagement 介面**</span><span class="sxs-lookup"><span data-stu-id="f0e5d-138">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> <dt>

[<span data-ttu-id="f0e5d-139">**IWMDRMLicenseQuery 介面**</span><span class="sxs-lookup"><span data-stu-id="f0e5d-139">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="f0e5d-140">**IWMDRMNetReceiver 介面**</span><span class="sxs-lookup"><span data-stu-id="f0e5d-140">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="f0e5d-141">**IWMDRMNetTransmitter 介面**</span><span class="sxs-lookup"><span data-stu-id="f0e5d-141">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> <dt>

[<span data-ttu-id="f0e5d-142">**IWMDRMSecurity 介面**</span><span class="sxs-lookup"><span data-stu-id="f0e5d-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





