---
description: ComponentState 屬性是此產品之實例的元件安裝狀態。這個屬性會使用物件的 ProductCode、UserSid 和內容來呼叫 MsiQueryComponentState。
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: ComponentState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.ComponentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 240a854a899f46bf80703bbd6cfb6b1529848586
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000878"
---
# <a name="productcomponentstate-method"></a><span data-ttu-id="b9446-103">ComponentState 方法</span><span class="sxs-lookup"><span data-stu-id="b9446-103">Product.ComponentState method</span></span>

<span data-ttu-id="b9446-104">**ComponentState** 屬性是此產品之實例的元件安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="b9446-104">The **ComponentState** property is the installation state of the component for the instance of this product.</span></span>

<span data-ttu-id="b9446-105">這個屬性會使用物件的 ProductCode、UserSid 和內容來呼叫 [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)。</span><span class="sxs-lookup"><span data-stu-id="b9446-105">This property calls [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea), with the ProductCode, UserSid, and Context of the object.</span></span> <span data-ttu-id="b9446-106">元件識別碼 GUID 會以參數形式提供。</span><span class="sxs-lookup"><span data-stu-id="b9446-106">The component Id GUID is provided as a parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9446-107">語法</span><span class="sxs-lookup"><span data-stu-id="b9446-107">Syntax</span></span>


```JScript
Product.ComponentState(
  ID
)
```



## <a name="parameters"></a><span data-ttu-id="b9446-108">參數</span><span class="sxs-lookup"><span data-stu-id="b9446-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9446-109">*識別碼*</span><span class="sxs-lookup"><span data-stu-id="b9446-109">*ID*</span></span> 
</dt> <dd>

<span data-ttu-id="b9446-110">元件 [資料表](component-table.md)的 [元件 id] 資料行中所找到元件的元件程式碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="b9446-110">Component code GUID of the component as found in the ComponentID column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9446-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9446-111">Return value</span></span>

<span data-ttu-id="b9446-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b9446-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9446-113">備註</span><span class="sxs-lookup"><span data-stu-id="b9446-113">Remarks</span></span>

<span data-ttu-id="b9446-114">如果呼叫成功，屬性會將值包含為 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="b9446-114">If the call succeeds, the property contains the value as a **DWORD**.</span></span>



| <span data-ttu-id="b9446-115">狀態</span><span class="sxs-lookup"><span data-stu-id="b9446-115">State</span></span>                | <span data-ttu-id="b9446-116">意義</span><span class="sxs-lookup"><span data-stu-id="b9446-116">Meaning</span></span>                                            |
|----------------------|----------------------------------------------------|
| <span data-ttu-id="b9446-117">INSTALLSTATE \_ 本機</span><span class="sxs-lookup"><span data-stu-id="b9446-117">INSTALLSTATE\_LOCAL</span></span>  | <span data-ttu-id="b9446-118">元件會安裝在本機。</span><span class="sxs-lookup"><span data-stu-id="b9446-118">The component is installed locally.</span></span>                |
| <span data-ttu-id="b9446-119">INSTALLSTATE \_ 來源</span><span class="sxs-lookup"><span data-stu-id="b9446-119">INSTALLSTATE\_SOURCE</span></span> | <span data-ttu-id="b9446-120">元件會安裝成從來源執行。</span><span class="sxs-lookup"><span data-stu-id="b9446-120">The component is installed to run from the source.</span></span> |



 

<span data-ttu-id="b9446-121">如果呼叫失敗，屬性會包含 [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)中的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b9446-121">If the call fails, the property contains an error code from [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).</span></span>



| <span data-ttu-id="b9446-122">錯誤</span><span class="sxs-lookup"><span data-stu-id="b9446-122">Error</span></span>                     | <span data-ttu-id="b9446-123">意義</span><span class="sxs-lookup"><span data-stu-id="b9446-123">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9446-124">\_拒絕存取 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="b9446-124">ERROR\_ACCESS\_DENIED</span></span>     | <span data-ttu-id="b9446-125">呼叫進程必須具有系統管理許可權，才能取得目前使用者以外的使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="b9446-125">The calling process must have administrative privileges to get information for a user other than the current user.</span></span> |
| <span data-ttu-id="b9446-126">錯誤的設定不 \_ 正確 \_</span><span class="sxs-lookup"><span data-stu-id="b9446-126">ERROR\_BAD\_CONFIGURATION</span></span> | <span data-ttu-id="b9446-127">設定資料已損毀。</span><span class="sxs-lookup"><span data-stu-id="b9446-127">The configuration data is corrupt.</span></span>                                                                                 |
| <span data-ttu-id="b9446-128">錯誤 \_ 不正確 \_ 參數</span><span class="sxs-lookup"><span data-stu-id="b9446-128">ERROR\_INVALID\_PARAMETER</span></span> | <span data-ttu-id="b9446-129">傳遞給函數的參數無效。</span><span class="sxs-lookup"><span data-stu-id="b9446-129">An invalid parameter was passed to the function.</span></span>                                                                   |
| <span data-ttu-id="b9446-130">錯誤 \_ 成功</span><span class="sxs-lookup"><span data-stu-id="b9446-130">ERROR\_SUCCESS</span></span>            | <span data-ttu-id="b9446-131">函數已順利完成。</span><span class="sxs-lookup"><span data-stu-id="b9446-131">The function completed successfully.</span></span>                                                                               |
| <span data-ttu-id="b9446-132">錯誤 \_ 不明的 \_ 元件</span><span class="sxs-lookup"><span data-stu-id="b9446-132">ERROR\_UNKNOWN\_COMPONENT</span></span> | <span data-ttu-id="b9446-133">元件識別碼不會識別已知的元件。</span><span class="sxs-lookup"><span data-stu-id="b9446-133">The component ID does not identify a known component.</span></span>                                                              |
| <span data-ttu-id="b9446-134">錯誤 \_ 未知的 \_ 產品</span><span class="sxs-lookup"><span data-stu-id="b9446-134">ERROR\_UNKNOWN\_PRODUCT</span></span>   | <span data-ttu-id="b9446-135">產品代碼未識別已知的產品。</span><span class="sxs-lookup"><span data-stu-id="b9446-135">The product code does not identify a known product.</span></span>                                                                |
| <span data-ttu-id="b9446-136">錯誤函式 \_ \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="b9446-136">ERROR\_FUNCTION\_FAILED</span></span>   | <span data-ttu-id="b9446-137">未預期的內部失敗。</span><span class="sxs-lookup"><span data-stu-id="b9446-137">An unexpected internal failure.</span></span>                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="b9446-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9446-138">Requirements</span></span>



| <span data-ttu-id="b9446-139">需求</span><span class="sxs-lookup"><span data-stu-id="b9446-139">Requirement</span></span> | <span data-ttu-id="b9446-140">值</span><span class="sxs-lookup"><span data-stu-id="b9446-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9446-141">版本</span><span class="sxs-lookup"><span data-stu-id="b9446-141">Version</span></span><br/> | <span data-ttu-id="b9446-142">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="b9446-142">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b9446-143">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="b9446-143">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b9446-144">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b9446-144">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="b9446-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b9446-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="b9446-146"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9446-146"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="b9446-147">IID</span><span class="sxs-lookup"><span data-stu-id="b9446-147">IID</span></span><br/>     | <span data-ttu-id="b9446-148">IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b9446-148">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="b9446-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9446-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9446-150">**產品**</span><span class="sxs-lookup"><span data-stu-id="b9446-150">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="b9446-151">**MsiQueryComponentState**</span><span class="sxs-lookup"><span data-stu-id="b9446-151">**MsiQueryComponentState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[<span data-ttu-id="b9446-152">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="b9446-152">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




