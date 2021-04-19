---
description: SWbemRefresher 加入方法會將新的 SWbemRefreshableItem 物件加入至 SWbemRefresher 物件中的集合。SWbemRefreshableItem 物件至 SWbemRefresher 物件中的集合。
ms.assetid: 92d11a18-1eed-4958-b74a-2f9de4907dd0
ms.tgt_platform: multiple
title: 'SWbemRefresher： Add 方法 (>wbemdisp.tlb. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Add
- ISWbemRefresher.Add
- ISWbemRefresher.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ebe9da221314252b2b143bf674cd7bb7177329b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981069"
---
# <a name="swbemrefresheradd-method"></a><span data-ttu-id="02147-103">SWbemRefresher 新增方法</span><span class="sxs-lookup"><span data-stu-id="02147-103">SWbemRefresher.Add method</span></span>

<span data-ttu-id="02147-104">**SWbemRefresher 加入** 方法會將新的 [**SWbemRefreshableItem**](swbemrefreshableitem.md)物件加入至 [**SWbemRefresher**](swbemrefresher.md)物件中的集合。</span><span class="sxs-lookup"><span data-stu-id="02147-104">The **SWbemRefresher.Add** method adds a new [**SWbemRefreshableItem**](swbemrefreshableitem.md) object to the collection in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="02147-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="02147-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="02147-106">語法</span><span class="sxs-lookup"><span data-stu-id="02147-106">Syntax</span></span>


```VB
objRefreshItem = .Add( _
  ByVal objWbemService, _
  ByVal strInstancePath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="02147-107">參數</span><span class="sxs-lookup"><span data-stu-id="02147-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02147-108">*objWbemService*</span><span class="sxs-lookup"><span data-stu-id="02147-108">*objWbemService*</span></span> 
</dt> <dd>

<span data-ttu-id="02147-109">必要。</span><span class="sxs-lookup"><span data-stu-id="02147-109">Required.</span></span> <span data-ttu-id="02147-110">代表命名空間之連接的 [**SWbemServices**](swbemservices.md) 物件，在此命名空間中新增到重新整理程式的物件。</span><span class="sxs-lookup"><span data-stu-id="02147-110">An [**SWbemServices**](swbemservices.md) object that represents a connection to the namespace in which the object that is being added to the refresher resides.</span></span>

</dd> <dt>

<span data-ttu-id="02147-111">*strInstancePath*</span><span class="sxs-lookup"><span data-stu-id="02147-111">*strInstancePath*</span></span> 
</dt> <dd>

<span data-ttu-id="02147-112">必要。</span><span class="sxs-lookup"><span data-stu-id="02147-112">Required.</span></span> <span data-ttu-id="02147-113">包含命名空間中物件之相對路徑的字串。</span><span class="sxs-lookup"><span data-stu-id="02147-113">String that contains the relative path of the object in the namespace.</span></span> <span data-ttu-id="02147-114">路徑必須包含實例。</span><span class="sxs-lookup"><span data-stu-id="02147-114">The path must contain an instance.</span></span> <span data-ttu-id="02147-115">傳回之 [**SWbemRefreshableItem**](swbemrefreshableitem.md)的 [**index**](swbemrefreshableitem-index.md)屬性代表重新整理程式集合中的物件索引。</span><span class="sxs-lookup"><span data-stu-id="02147-115">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the object in the refresher collection.</span></span>

</dd> <dt>

<span data-ttu-id="02147-116">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="02147-116">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="02147-117">字串，包含執行方法之物件的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="02147-117">String that contains the object path of the object for which the method is executed.</span></span>

</dd> <dt>

<span data-ttu-id="02147-118">*objWbemNamedvalueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="02147-118">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="02147-119">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="02147-119">Typically, this is undefined.</span></span> <span data-ttu-id="02147-120">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其專案代表服務要求的提供者可使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="02147-120">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="02147-121">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="02147-121">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02147-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="02147-122">Return value</span></span>

<span data-ttu-id="02147-123">如果呼叫成功，則會傳回包含單一可重新整理物件的 [**SWbemRefreshableItem**](swbemrefreshableitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="02147-123">If the call is successful, an [**SWbemRefreshableItem**](swbemrefreshableitem.md) object that contains a single refreshable object is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="02147-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="02147-124">Requirements</span></span>



| <span data-ttu-id="02147-125">需求</span><span class="sxs-lookup"><span data-stu-id="02147-125">Requirement</span></span> | <span data-ttu-id="02147-126">值</span><span class="sxs-lookup"><span data-stu-id="02147-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02147-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02147-127">Minimum supported client</span></span><br/> | <span data-ttu-id="02147-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02147-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02147-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02147-129">Minimum supported server</span></span><br/> | <span data-ttu-id="02147-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02147-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02147-131">標頭</span><span class="sxs-lookup"><span data-stu-id="02147-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="02147-132"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="02147-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="02147-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="02147-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="02147-134"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="02147-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="02147-135">DLL</span><span class="sxs-lookup"><span data-stu-id="02147-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02147-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02147-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="02147-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="02147-137">CLSID</span></span><br/>                    | <span data-ttu-id="02147-138">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="02147-138">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="02147-139">IID</span><span class="sxs-lookup"><span data-stu-id="02147-139">IID</span></span><br/>                      | <span data-ttu-id="02147-140">IID \_ ISWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="02147-140">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="02147-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02147-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02147-142">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="02147-142">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




