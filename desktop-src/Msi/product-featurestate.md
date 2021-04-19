---
description: FeatureState 屬性是此產品實例之功能的安裝狀態。這個屬性會使用物件的 ProductCode、UserSid 和內容來呼叫 MsiQueryFeatureStateEx。 功能識別碼會以參數形式提供。
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: FeatureState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f7e602ce5d5b0a8e524f76144c7f1eff8876bb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995692"
---
# <a name="productfeaturestate-method"></a><span data-ttu-id="6d019-104">FeatureState 方法</span><span class="sxs-lookup"><span data-stu-id="6d019-104">Product.FeatureState method</span></span>

<span data-ttu-id="6d019-105">**FeatureState** 屬性是此產品實例之功能的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="6d019-105">The **FeatureState** property is the installation state of the feature for the instance of this product.</span></span>

<span data-ttu-id="6d019-106">這個屬性會使用物件的 *ProductCode*、 *UserSid* 和 *內容* 來呼叫 [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)。</span><span class="sxs-lookup"><span data-stu-id="6d019-106">This property calls [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa), with the *ProductCode*, *UserSid* and *Context* of the object.</span></span> <span data-ttu-id="6d019-107">功能識別碼會以參數形式提供。</span><span class="sxs-lookup"><span data-stu-id="6d019-107">The feature Id is provided as a parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d019-108">語法</span><span class="sxs-lookup"><span data-stu-id="6d019-108">Syntax</span></span>


```JScript
Product.FeatureState(
  FeatureId
)
```



## <a name="parameters"></a><span data-ttu-id="6d019-109">參數</span><span class="sxs-lookup"><span data-stu-id="6d019-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d019-110">*FeatureId*</span><span class="sxs-lookup"><span data-stu-id="6d019-110">*FeatureId*</span></span> 
</dt> <dd>

<span data-ttu-id="6d019-111">功能識別碼出現在 [功能資料表](feature-table.md)的功能資料行中。</span><span class="sxs-lookup"><span data-stu-id="6d019-111">Feature Id appearing in the Feature column of the [Feature Table](feature-table.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d019-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d019-112">Return value</span></span>

<span data-ttu-id="6d019-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6d019-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d019-114">備註</span><span class="sxs-lookup"><span data-stu-id="6d019-114">Remarks</span></span>

<span data-ttu-id="6d019-115">如果呼叫成功，屬性會將值包含為 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="6d019-115">If the call succeeds, the property contains the value as a **DWORD**.</span></span>



| <span data-ttu-id="6d019-116">狀態</span><span class="sxs-lookup"><span data-stu-id="6d019-116">State</span></span>                    | <span data-ttu-id="6d019-117">意義</span><span class="sxs-lookup"><span data-stu-id="6d019-117">Meaning</span></span>                                      |
|--------------------------|----------------------------------------------|
| <span data-ttu-id="6d019-118">INSTALLSTATE \_ 公告</span><span class="sxs-lookup"><span data-stu-id="6d019-118">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="6d019-119">這項功能已公告。</span><span class="sxs-lookup"><span data-stu-id="6d019-119">This feature is advertised.</span></span>                  |
| <span data-ttu-id="6d019-120">INSTALLSTATE \_ 本機</span><span class="sxs-lookup"><span data-stu-id="6d019-120">INSTALLSTATE\_LOCAL</span></span>      | <span data-ttu-id="6d019-121">這項功能會安裝在本機。</span><span class="sxs-lookup"><span data-stu-id="6d019-121">The feature is installed locally.</span></span>            |
| <span data-ttu-id="6d019-122">INSTALLSTATE \_ 來源</span><span class="sxs-lookup"><span data-stu-id="6d019-122">INSTALLSTATE\_SOURCE</span></span>     | <span data-ttu-id="6d019-123">這項功能已安裝成從來源執行。</span><span class="sxs-lookup"><span data-stu-id="6d019-123">The feature is installed to run from source.</span></span> |



 

<span data-ttu-id="6d019-124">如果呼叫失敗，屬性會包含 [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)中的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6d019-124">If the call fails, the property contains an error code from [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).</span></span>



| <span data-ttu-id="6d019-125">錯誤</span><span class="sxs-lookup"><span data-stu-id="6d019-125">Error</span></span>                     | <span data-ttu-id="6d019-126">意義</span><span class="sxs-lookup"><span data-stu-id="6d019-126">Meaning</span></span>                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d019-127">\_拒絕存取 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="6d019-127">ERROR\_ACCESS\_DENIED</span></span>     | <span data-ttu-id="6d019-128">呼叫進程必須具有系統管理許可權，才能取得針對目前使用者以外的使用者所安裝之產品的資訊。</span><span class="sxs-lookup"><span data-stu-id="6d019-128">The calling process must have administrative privileges to get information for a product installed for a user other than the current user.</span></span> |
| <span data-ttu-id="6d019-129">錯誤的設定不 \_ 正確 \_</span><span class="sxs-lookup"><span data-stu-id="6d019-129">ERROR\_BAD\_CONFIGURATION</span></span> | <span data-ttu-id="6d019-130">設定資料已損毀。</span><span class="sxs-lookup"><span data-stu-id="6d019-130">The configuration data is corrupt.</span></span>                                                                                                         |
| <span data-ttu-id="6d019-131">錯誤 \_ 不正確 \_ 參數</span><span class="sxs-lookup"><span data-stu-id="6d019-131">ERROR\_INVALID\_PARAMETER</span></span> | <span data-ttu-id="6d019-132">傳遞給函數的參數無效。</span><span class="sxs-lookup"><span data-stu-id="6d019-132">An invalid parameter was passed to the function.</span></span>                                                                                           |
| <span data-ttu-id="6d019-133">錯誤 \_ 成功</span><span class="sxs-lookup"><span data-stu-id="6d019-133">ERROR\_SUCCESS</span></span>            | <span data-ttu-id="6d019-134">函數已順利完成。</span><span class="sxs-lookup"><span data-stu-id="6d019-134">The function completed successfully.</span></span>                                                                                                       |
| <span data-ttu-id="6d019-135">錯誤 \_ 未知的 \_ 功能</span><span class="sxs-lookup"><span data-stu-id="6d019-135">ERROR\_UNKNOWN\_FEATURE</span></span>   | <span data-ttu-id="6d019-136">功能識別碼不會識別已知的功能。</span><span class="sxs-lookup"><span data-stu-id="6d019-136">The feature ID does not identify a known feature.</span></span>                                                                                          |
| <span data-ttu-id="6d019-137">錯誤 \_ 未知的 \_ 產品</span><span class="sxs-lookup"><span data-stu-id="6d019-137">ERROR\_UNKNOWN\_PRODUCT</span></span>   | <span data-ttu-id="6d019-138">產品代碼未識別已知的產品。</span><span class="sxs-lookup"><span data-stu-id="6d019-138">The product code does not identify a known product.</span></span>                                                                                        |
| <span data-ttu-id="6d019-139">錯誤函式 \_ \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="6d019-139">ERROR\_FUNCTION\_FAILED</span></span>   | <span data-ttu-id="6d019-140">未預期的內部失敗。</span><span class="sxs-lookup"><span data-stu-id="6d019-140">An unexpected internal failure.</span></span>                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="6d019-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d019-141">Requirements</span></span>



| <span data-ttu-id="6d019-142">需求</span><span class="sxs-lookup"><span data-stu-id="6d019-142">Requirement</span></span> | <span data-ttu-id="6d019-143">值</span><span class="sxs-lookup"><span data-stu-id="6d019-143">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d019-144">版本</span><span class="sxs-lookup"><span data-stu-id="6d019-144">Version</span></span><br/> | <span data-ttu-id="6d019-145">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="6d019-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6d019-146">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="6d019-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6d019-147">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6d019-147">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="6d019-148">DLL</span><span class="sxs-lookup"><span data-stu-id="6d019-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="6d019-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d019-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="6d019-150">IID</span><span class="sxs-lookup"><span data-stu-id="6d019-150">IID</span></span><br/>     | <span data-ttu-id="6d019-151">IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6d019-151">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="6d019-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d019-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d019-153">**產品**</span><span class="sxs-lookup"><span data-stu-id="6d019-153">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="6d019-154">**MsiQueryFeatureStateEx**</span><span class="sxs-lookup"><span data-stu-id="6d019-154">**MsiQueryFeatureStateEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[<span data-ttu-id="6d019-155">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="6d019-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




