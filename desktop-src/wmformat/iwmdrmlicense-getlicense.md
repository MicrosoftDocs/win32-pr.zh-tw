---
title: 'IWMDRMLicense GetLicense 方法 (Wmdrmsdk .h) '
description: GetLicense 方法會以 XML 或 XMR 資料的形式來捕獲授權。
ms.assetid: 63317841-fd13-4e83-8b99-e3cab1405050
keywords:
- GetLicense 方法 windows Media 格式
- GetLicense 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，GetLicense 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0692afb2ff127f9456e6da3c7546c67ae22ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977539"
---
# <a name="iwmdrmlicensegetlicense-method"></a><span data-ttu-id="17d76-106">IWMDRMLicense：： GetLicense 方法</span><span class="sxs-lookup"><span data-stu-id="17d76-106">IWMDRMLicense::GetLicense method</span></span>

<span data-ttu-id="17d76-107">**GetLicense** 方法會以 XML 或 XMR 資料的形式來捕獲授權。</span><span class="sxs-lookup"><span data-stu-id="17d76-107">The **GetLicense** method retrieves the license as XML or XMR data.</span></span>

## <a name="syntax"></a><span data-ttu-id="17d76-108">語法</span><span class="sxs-lookup"><span data-stu-id="17d76-108">Syntax</span></span>


```C++
HRESULT GetLicense(
  [out] BYTE  **ppbLicense,
  [out] DWORD *pcbLicense,
  [out] DWORD *pdwLicenseType
);
```



## <a name="parameters"></a><span data-ttu-id="17d76-109">參數</span><span class="sxs-lookup"><span data-stu-id="17d76-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17d76-110">*ppbLicense* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="17d76-110">*ppbLicense* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17d76-111">接收授權。</span><span class="sxs-lookup"><span data-stu-id="17d76-111">Receives the license.</span></span>

</dd> <dt>

<span data-ttu-id="17d76-112">*pcbLicense* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="17d76-112">*pcbLicense* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17d76-113">接收授權的大小。</span><span class="sxs-lookup"><span data-stu-id="17d76-113">Receives the size of the license.</span></span>

</dd> <dt>

<span data-ttu-id="17d76-114">*pdwLicenseType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="17d76-114">*pdwLicenseType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17d76-115">接收傳回的授權類型。</span><span class="sxs-lookup"><span data-stu-id="17d76-115">Receives the type of the license returned.</span></span> <span data-ttu-id="17d76-116">此值會設定為下表中的其中一個常數。</span><span class="sxs-lookup"><span data-stu-id="17d76-116">This value is set to one of the constants in the following table.</span></span>



| <span data-ttu-id="17d76-117">常數</span><span class="sxs-lookup"><span data-stu-id="17d76-117">Constant</span></span>                  | <span data-ttu-id="17d76-118">描述</span><span class="sxs-lookup"><span data-stu-id="17d76-118">Description</span></span>                            |
|---------------------------|----------------------------------------|
| <span data-ttu-id="17d76-119">WMDRM \_ 授權 \_ 類型 \_ XML</span><span class="sxs-lookup"><span data-stu-id="17d76-119">WMDRM\_LICENSE\_TYPE\_XML</span></span> | <span data-ttu-id="17d76-120">取出的授權會格式化為 XML。</span><span class="sxs-lookup"><span data-stu-id="17d76-120">Retrieved license is formatted as XML.</span></span> |
| <span data-ttu-id="17d76-121">WMDRM \_ 授權 \_ 類型 \_ XMR</span><span class="sxs-lookup"><span data-stu-id="17d76-121">WMDRM\_LICENSE\_TYPE\_XMR</span></span> | <span data-ttu-id="17d76-122">已取出的授權格式為 XMR。</span><span class="sxs-lookup"><span data-stu-id="17d76-122">Retrieved license is formatted as XMR.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17d76-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="17d76-123">Return value</span></span>

<span data-ttu-id="17d76-124">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="17d76-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="17d76-125">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="17d76-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="17d76-126">傳回碼</span><span class="sxs-lookup"><span data-stu-id="17d76-126">Return code</span></span>                                                                          | <span data-ttu-id="17d76-127">Description</span><span class="sxs-lookup"><span data-stu-id="17d76-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="17d76-128"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="17d76-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="17d76-129">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="17d76-129">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="17d76-130">備註</span><span class="sxs-lookup"><span data-stu-id="17d76-130">Remarks</span></span>

<span data-ttu-id="17d76-131">無。</span><span class="sxs-lookup"><span data-stu-id="17d76-131">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="17d76-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="17d76-132">Requirements</span></span>



| <span data-ttu-id="17d76-133">需求</span><span class="sxs-lookup"><span data-stu-id="17d76-133">Requirement</span></span> | <span data-ttu-id="17d76-134">值</span><span class="sxs-lookup"><span data-stu-id="17d76-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17d76-135">標頭</span><span class="sxs-lookup"><span data-stu-id="17d76-135">Header</span></span><br/>  | <dl> <span data-ttu-id="17d76-136"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="17d76-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="17d76-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="17d76-137">Library</span></span><br/> | <dl> <span data-ttu-id="17d76-138"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="17d76-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17d76-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17d76-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17d76-140">**GetLicenseProperty**</span><span class="sxs-lookup"><span data-stu-id="17d76-140">**GetLicenseProperty**</span></span>](iwmdrmlicense-getlicenseproperty.md)
</dt> <dt>

[<span data-ttu-id="17d76-141">**IWMDRMLicense 介面**</span><span class="sxs-lookup"><span data-stu-id="17d76-141">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





