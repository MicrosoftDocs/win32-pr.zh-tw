---
description: 將新的枚舉器加入至 SWbemRefresher 物件。 此列舉值適用于 strClass 參數中指定之類別的所有實例。
ms.assetid: 0fa22a47-4050-43ae-aad3-3a8ebbf5e9b2
ms.tgt_platform: multiple
title: 'SWbemRefresher. AddEnum 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cffa406a3a45869038f5e6fed12b23b6b84fde27
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103696222"
---
# <a name="swbemrefresheraddenum-method"></a><span data-ttu-id="dc230-104">SWbemRefresher. AddEnum 方法</span><span class="sxs-lookup"><span data-stu-id="dc230-104">SWbemRefresher.AddEnum method</span></span>

<span data-ttu-id="dc230-105">**SWbemRefresher. AddEnum** 方法會將新的枚舉器加入至 [**SWbemRefresher**](swbemrefresher.md)物件。</span><span class="sxs-lookup"><span data-stu-id="dc230-105">The **SWbemRefresher.AddEnum** method adds a new enumerator to the [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="dc230-106">此列舉值適用于 *strClass* 參數中指定之類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="dc230-106">This enumerator is for all the instances of the class that is specified in the *strClass* parameter.</span></span>

<span data-ttu-id="dc230-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="dc230-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc230-108">語法</span><span class="sxs-lookup"><span data-stu-id="dc230-108">Syntax</span></span>


```VB
objRefreshEnum = .AddEnum( _
  ByVal objWbemService, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="dc230-109">參數</span><span class="sxs-lookup"><span data-stu-id="dc230-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc230-110">*objWbemService*</span><span class="sxs-lookup"><span data-stu-id="dc230-110">*objWbemService*</span></span> 
</dt> <dd>

<span data-ttu-id="dc230-111">必要。</span><span class="sxs-lookup"><span data-stu-id="dc230-111">Required.</span></span> <span data-ttu-id="dc230-112">代表命名空間之連接的 [**SWbemServices**](swbemservices.md) 物件，在此命名空間中新增到重新整理程式的物件。</span><span class="sxs-lookup"><span data-stu-id="dc230-112">An [**SWbemServices**](swbemservices.md) object that represents a connection to the namespace in which the object that is being added to the refresher resides.</span></span>

</dd> <dt>

<span data-ttu-id="dc230-113">*strClass*</span><span class="sxs-lookup"><span data-stu-id="dc230-113">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="dc230-114">必要。</span><span class="sxs-lookup"><span data-stu-id="dc230-114">Required.</span></span> <span data-ttu-id="dc230-115">字串，其中包含要新增至複習的類別。</span><span class="sxs-lookup"><span data-stu-id="dc230-115">String that contains the class that is being added to the refresher.</span></span> <span data-ttu-id="dc230-116">這個類別是用來做為類別實例的列舉值。</span><span class="sxs-lookup"><span data-stu-id="dc230-116">This class is used as an enumerator of the instances of the class.</span></span> <span data-ttu-id="dc230-117">傳回之 [**SWbemRefreshableItem**](swbemrefreshableitem.md)的 [**index**](swbemrefreshableitem-index.md)屬性代表重新整理程式集合中的列舉值索引。</span><span class="sxs-lookup"><span data-stu-id="dc230-117">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the enumerator in the refresher collection.</span></span>

</dd> <dt>

<span data-ttu-id="dc230-118">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="dc230-118">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dc230-119">字串，包含執行方法之物件的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="dc230-119">String that contains the object path of the object for which the method is executed.</span></span>

</dd> <dt>

<span data-ttu-id="dc230-120">*objWbemNamedvalueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="dc230-120">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dc230-121">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="dc230-121">Typically, this is undefined.</span></span> <span data-ttu-id="dc230-122">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其專案代表服務要求的提供者可使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="dc230-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="dc230-123">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="dc230-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc230-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc230-124">Return value</span></span>

<span data-ttu-id="dc230-125">如果呼叫成功，則會傳回 [**SWbemRefreshableItem**](swbemrefreshableitem.md) 物件，其中包含指定類別的所有實例的列舉值。</span><span class="sxs-lookup"><span data-stu-id="dc230-125">If the call is successful, an [**SWbemRefreshableItem**](swbemrefreshableitem.md) object that contains an enumerator for all the instances for the specified class is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc230-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc230-126">Requirements</span></span>



| <span data-ttu-id="dc230-127">需求</span><span class="sxs-lookup"><span data-stu-id="dc230-127">Requirement</span></span> | <span data-ttu-id="dc230-128">值</span><span class="sxs-lookup"><span data-stu-id="dc230-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc230-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc230-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dc230-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc230-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc230-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc230-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dc230-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc230-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc230-133">標頭</span><span class="sxs-lookup"><span data-stu-id="dc230-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc230-134"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc230-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc230-135">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="dc230-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="dc230-136"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dc230-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dc230-137">DLL</span><span class="sxs-lookup"><span data-stu-id="dc230-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc230-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc230-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dc230-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="dc230-139">CLSID</span></span><br/>                    | <span data-ttu-id="dc230-140">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="dc230-140">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="dc230-141">IID</span><span class="sxs-lookup"><span data-stu-id="dc230-141">IID</span></span><br/>                      | <span data-ttu-id="dc230-142">IID \_ ISWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="dc230-142">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="dc230-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc230-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc230-144">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="dc230-144">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




