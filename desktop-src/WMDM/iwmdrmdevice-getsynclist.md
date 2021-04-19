---
title: IWMDRMDevice GetSyncList 方法
description: GetSyncList 方法會抓取裝置上的授權同步處理清單。 授權同步處理可讓主機電腦根據指定的準則，將更新的授權傳送至裝置。
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- GetSyncList 方法 windows Media 裝置管理員
- GetSyncList 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，GetSyncList 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381d410bd938cb90855b182e62354d48e72f16d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995712"
---
# <a name="iwmdrmdevicegetsynclist-method"></a><span data-ttu-id="d8a85-107">IWMDRMDevice：： GetSyncList 方法</span><span class="sxs-lookup"><span data-stu-id="d8a85-107">IWMDRMDevice::GetSyncList method</span></span>

<span data-ttu-id="d8a85-108">**GetSyncList** 方法會抓取裝置上的授權同步處理清單。</span><span class="sxs-lookup"><span data-stu-id="d8a85-108">The **GetSyncList** method retrieves the license synchronization list on the device.</span></span> <span data-ttu-id="d8a85-109">授權同步處理可讓主機電腦根據指定的準則，將更新的授權傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="d8a85-109">License synchronization allows the host computer to transfer updated licenses to a device according to the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8a85-110">語法</span><span class="sxs-lookup"><span data-stu-id="d8a85-110">Syntax</span></span>


```C++
HRESULT GetSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList
);
```



## <a name="parameters"></a><span data-ttu-id="d8a85-111">參數</span><span class="sxs-lookup"><span data-stu-id="d8a85-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8a85-112">*cMinCountThreshold* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d8a85-112">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8a85-113">最小計數閾值。</span><span class="sxs-lookup"><span data-stu-id="d8a85-113">Minimum count threshold.</span></span>

</dd> <dt>

<span data-ttu-id="d8a85-114">*cMinHoursThreshold* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d8a85-114">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8a85-115">最小時間閾值。</span><span class="sxs-lookup"><span data-stu-id="d8a85-115">Minimum hours threshold.</span></span>

</dd> <dt>

<span data-ttu-id="d8a85-116">*ppbSyncList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d8a85-116">*ppbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8a85-117">已取出授權同步處理清單。</span><span class="sxs-lookup"><span data-stu-id="d8a85-117">Retrieved license synchronization list.</span></span>

</dd> <dt>

<span data-ttu-id="d8a85-118">*pcbSyncList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d8a85-118">*pcbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8a85-119">授權同步清單的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8a85-119">Size of the license synchronization list, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8a85-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8a85-120">Return value</span></span>

<span data-ttu-id="d8a85-121">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="d8a85-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d8a85-122">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="d8a85-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d8a85-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d8a85-123">Return code</span></span>                                                                          | <span data-ttu-id="d8a85-124">Description</span><span class="sxs-lookup"><span data-stu-id="d8a85-124">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d8a85-125"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d8a85-125"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d8a85-126">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="d8a85-126">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d8a85-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8a85-127">Requirements</span></span>



| <span data-ttu-id="d8a85-128">需求</span><span class="sxs-lookup"><span data-stu-id="d8a85-128">Requirement</span></span> | <span data-ttu-id="d8a85-129">值</span><span class="sxs-lookup"><span data-stu-id="d8a85-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8a85-130">標頭</span><span class="sxs-lookup"><span data-stu-id="d8a85-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d8a85-131"><dt>WMDDRMSP .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d8a85-131"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="d8a85-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="d8a85-132">Library</span></span><br/> | <dl> <span data-ttu-id="d8a85-133"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8a85-133"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8a85-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8a85-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8a85-135">**IWMDRMDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="d8a85-135">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





