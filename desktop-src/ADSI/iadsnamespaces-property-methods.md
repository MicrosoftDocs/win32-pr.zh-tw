---
title: 'IADsNamespaces 屬性方法 (Iads .h) '
description: IADsNamespaces 介面屬性方法會取得並設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: fe959741-429e-480a-8111-3ebadaf55f77
ms.tgt_platform: multiple
keywords:
- IADsNamespaces 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsNamespaces Property Methods
- IADsNamespaces.DefaultContainer
- IADsNamespaces.get_DefaultContainer
- IADsNamespaces.put_DefaultContainer
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b30467e931d7e8790f9a17542d5da2070525fe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686206"
---
# <a name="iadsnamespaces-property-methods"></a><span data-ttu-id="9b247-105">IADsNamespaces 屬性方法</span><span class="sxs-lookup"><span data-stu-id="9b247-105">IADsNamespaces Property Methods</span></span>

<span data-ttu-id="9b247-106">[**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)介面屬性方法會取得並設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="9b247-106">The [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) interface property methods get and set the properties described in the following table.</span></span> <span data-ttu-id="9b247-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="9b247-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="9b247-108">屬性</span><span class="sxs-lookup"><span data-stu-id="9b247-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="9b247-109">**DefaultContainer**</span><span class="sxs-lookup"><span data-stu-id="9b247-109">**DefaultContainer**</span></span>
<span data-ttu-id="9b247-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9b247-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="9b247-111">**DefaultContainer** 屬性會識別基底容器物件，您可以在流覽時將其系結至起點作為起點。</span><span class="sxs-lookup"><span data-stu-id="9b247-111">The **DefaultContainer** property identifies a base container object to which you can bind and use as a starting point when browsing.</span></span> <span data-ttu-id="9b247-112">這項資料會從下列登錄值儲存和取出。</span><span class="sxs-lookup"><span data-stu-id="9b247-112">This data is stored and retrieved from the following registry value.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         ADs
            DefaultContainer
```

<span data-ttu-id="9b247-113">ADSI 定義了 **DefaultContainer** 屬性，以提供快速的方式來取得先前定義之 ADSI 容器物件的指標。</span><span class="sxs-lookup"><span data-stu-id="9b247-113">ADSI defines the **DefaultContainer** property to provide a quick way of getting a pointer to a previously defined ADSI container object.</span></span>

<dt>

<span data-ttu-id="9b247-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9b247-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9b247-115">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9b247-115">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultContainer(
  [out] BSTR* pbstrDefault
);
HRESULT put_DefaultContainer(
  [in] BSTR bstrDefault
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="9b247-116">備註</span><span class="sxs-lookup"><span data-stu-id="9b247-116">Remarks</span></span>

<span data-ttu-id="9b247-117">提供者必須以每個使用者為基礎來提供此屬性。</span><span class="sxs-lookup"><span data-stu-id="9b247-117">Providers must supply this property on a per-user basis.</span></span> <span data-ttu-id="9b247-118">預設容器會在 IADsNamespaces 的調用之後立即設定 **：:p 的 \_ DefaultContainer**。</span><span class="sxs-lookup"><span data-stu-id="9b247-118">The default container is set immediately after the invocation of **IADsNamespaces::put\_DefaultContainer**.</span></span> <span data-ttu-id="9b247-119">不需要呼叫 [**IADs。 SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 。</span><span class="sxs-lookup"><span data-stu-id="9b247-119">Calling [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) is not required.</span></span> <span data-ttu-id="9b247-120">事實上，系統提供的命名空間物件會傳回這個物件上所呼叫之 **IADs. SetInfo** 方法的 **E \_ >notimpl** 。</span><span class="sxs-lookup"><span data-stu-id="9b247-120">In fact, the system-supplied namespaces object returns **E\_NOTIMPL** for the **IADs.SetInfo** method called on this object.</span></span> <span data-ttu-id="9b247-121">當容器是命名空間物件時，列舉作業一律會產生提供者專屬命名空間物件的清單。</span><span class="sxs-lookup"><span data-stu-id="9b247-121">When a container is the namespaces object, an enumeration operation always results in a list of provider-specific namespace objects.</span></span> <span data-ttu-id="9b247-122">當使用 [**IADsContainer**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) 來取得 namespace 物件時，會忽略 *bstrClass* 參數。</span><span class="sxs-lookup"><span data-stu-id="9b247-122">When [**IADsContainer.GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) is used to obtain a namespace object, the *bstrClass* parameter is ignored.</span></span> <span data-ttu-id="9b247-123">這是因為容器（也就是命名空間物件）只包含一種類型的物件，也就是提供者特定的命名空間物件。</span><span class="sxs-lookup"><span data-stu-id="9b247-123">This is because the container, that is, the namespaces object, contains only one type of object, namely, provider-specific namespace objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b247-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b247-124">Requirements</span></span>



| <span data-ttu-id="9b247-125">需求</span><span class="sxs-lookup"><span data-stu-id="9b247-125">Requirement</span></span> | <span data-ttu-id="9b247-126">值</span><span class="sxs-lookup"><span data-stu-id="9b247-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b247-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b247-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9b247-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b247-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b247-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b247-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9b247-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b247-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b247-131">標頭</span><span class="sxs-lookup"><span data-stu-id="9b247-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b247-132"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="9b247-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="9b247-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9b247-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b247-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b247-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="9b247-135">IID</span><span class="sxs-lookup"><span data-stu-id="9b247-135">IID</span></span><br/>                      | <span data-ttu-id="9b247-136">IID \_ IADsNamespaces 定義為28B96BA0-B330-11CF-A9AD-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="9b247-136">IID\_IADsNamespaces is defined as 28B96BA0-B330-11CF-A9AD-00AA006BC149</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9b247-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b247-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b247-138">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="9b247-138">**IADsContainer.GetObject**</span></span>](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)
</dt> <dt>

[<span data-ttu-id="9b247-139">**IADsNamespaces**</span><span class="sxs-lookup"><span data-stu-id="9b247-139">**IADsNamespaces**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)
</dt> <dt>

[<span data-ttu-id="9b247-140">介面屬性方法</span><span class="sxs-lookup"><span data-stu-id="9b247-140">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





