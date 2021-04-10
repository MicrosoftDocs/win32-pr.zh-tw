---
title: 'IBackgroundCopyFile5 GetProperty 方法 (>deliveryoptimization .h) '
description: 取得傳遞最佳化的泛型屬性 (是否) 檔案傳輸。
ms.assetid: E2E96A0F-5670-4DE7-9DF8-A215AFAD0E8A
keywords:
- GetProperty 方法
- GetProperty 方法，IBackgroundCopyFile5 介面
- IBackgroundCopyFile5 介面，GetProperty 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84c6a9f96fc332bda940573bde78d7dd05efeeb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094456"
---
# <a name="ibackgroundcopyfile5getproperty-method"></a><span data-ttu-id="7187b-106">IBackgroundCopyFile5：： GetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="7187b-106">IBackgroundCopyFile5::GetProperty method</span></span>

<span data-ttu-id="7187b-107">取得傳遞最佳化的泛型屬性 (是否) 檔案傳輸。</span><span class="sxs-lookup"><span data-stu-id="7187b-107">Gets a generic property of a Delivery Optimization (DO) file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7187b-108">語法</span><span class="sxs-lookup"><span data-stu-id="7187b-108">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *PropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="7187b-109">參數</span><span class="sxs-lookup"><span data-stu-id="7187b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7187b-110">*PropertyId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7187b-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7187b-111">指定要抓取其值的檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="7187b-111">Specifies the file property whose value is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="7187b-112">*PropertyValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7187b-112">*PropertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7187b-113">傳回做為 BITS_FILE_PROPERTY_VALUE 聯集之指標的屬性值。</span><span class="sxs-lookup"><span data-stu-id="7187b-113">The property value, returned as a pointer to a BITS_FILE_PROPERTY_VALUE union.</span></span> <span data-ttu-id="7187b-114">使用適用于所傳入屬性識別碼值的聯集欄位。</span><span class="sxs-lookup"><span data-stu-id="7187b-114">Use the union field appropriate for the property ID value passed in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7187b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="7187b-115">Return value</span></span>

<span data-ttu-id="7187b-116">如果這個方法成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="7187b-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="7187b-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7187b-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7187b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7187b-118">Requirements</span></span>



| <span data-ttu-id="7187b-119">需求</span><span class="sxs-lookup"><span data-stu-id="7187b-119">Requirement</span></span> | <span data-ttu-id="7187b-120">值</span><span class="sxs-lookup"><span data-stu-id="7187b-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7187b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7187b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7187b-122">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7187b-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7187b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7187b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7187b-124">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7187b-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7187b-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7187b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7187b-126"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="7187b-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="7187b-127">Idl</span><span class="sxs-lookup"><span data-stu-id="7187b-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7187b-128"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7187b-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="7187b-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="7187b-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="7187b-130"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7187b-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="7187b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7187b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7187b-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7187b-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="7187b-133">IID</span><span class="sxs-lookup"><span data-stu-id="7187b-133">IID</span></span><br/>                      | <span data-ttu-id="7187b-134">IID_IBackgroundCopyFile5 定義為85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="7187b-134">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="7187b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7187b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7187b-136">**IBackgroundCopyFile5**</span><span class="sxs-lookup"><span data-stu-id="7187b-136">**IBackgroundCopyFile5**</span></span>](ibackgroundcopyfile5.md)
</dt> <dt>

[<span data-ttu-id="7187b-137">**IBackgroundCopyFile5**</span><span class="sxs-lookup"><span data-stu-id="7187b-137">**IBackgroundCopyFile5.SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





