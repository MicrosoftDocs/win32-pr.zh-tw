---
title: IWMDRMDevice CleanDataStore 方法
description: CleanDataStore 方法會啟動清除裝置上 DRM 資料存放區的程式。
ms.assetid: aad99137-6d2b-4612-8014-9783035af929
keywords:
- CleanDataStore 方法 windows Media 裝置管理員
- CleanDataStore 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，CleanDataStore 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.CleanDataStore
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5aed9608a7428245edd84602ea5e7252861d938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993942"
---
# <a name="iwmdrmdevicecleandatastore-method"></a><span data-ttu-id="40a62-106">IWMDRMDevice：： CleanDataStore 方法</span><span class="sxs-lookup"><span data-stu-id="40a62-106">IWMDRMDevice::CleanDataStore method</span></span>

<span data-ttu-id="40a62-107">**CleanDataStore** 方法會啟動清除裝置上 DRM 資料存放區的程式。</span><span class="sxs-lookup"><span data-stu-id="40a62-107">The **CleanDataStore** method starts the process of cleaning the DRM data store on the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="40a62-108">語法</span><span class="sxs-lookup"><span data-stu-id="40a62-108">Syntax</span></span>


```C++
HRESULT CleanDataStore(
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="40a62-109">參數</span><span class="sxs-lookup"><span data-stu-id="40a62-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40a62-110">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40a62-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40a62-111">存放區清除準則的旗標。</span><span class="sxs-lookup"><span data-stu-id="40a62-111">Flags for store cleaning criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40a62-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="40a62-112">Return value</span></span>

<span data-ttu-id="40a62-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="40a62-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="40a62-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="40a62-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="40a62-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="40a62-115">Return code</span></span>                                                                          | <span data-ttu-id="40a62-116">Description</span><span class="sxs-lookup"><span data-stu-id="40a62-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="40a62-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="40a62-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="40a62-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="40a62-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="40a62-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="40a62-119">Requirements</span></span>



| <span data-ttu-id="40a62-120">需求</span><span class="sxs-lookup"><span data-stu-id="40a62-120">Requirement</span></span> | <span data-ttu-id="40a62-121">值</span><span class="sxs-lookup"><span data-stu-id="40a62-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40a62-122">標頭</span><span class="sxs-lookup"><span data-stu-id="40a62-122">Header</span></span><br/>  | <dl> <span data-ttu-id="40a62-123"><dt>WMDDRMSP .idl</dt></span><span class="sxs-lookup"><span data-stu-id="40a62-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="40a62-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="40a62-124">Library</span></span><br/> | <dl> <span data-ttu-id="40a62-125"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="40a62-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40a62-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40a62-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40a62-127">**IWMDRMDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="40a62-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





