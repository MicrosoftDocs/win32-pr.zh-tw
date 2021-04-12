---
title: 'IADsBackLink 屬性方法 (Iads .h) '
description: IADsBackLink 介面的 property 方法會設定下表所述的屬性。 如需詳細資訊，請參閱介面屬性方法。
ms.assetid: 0a66fa6d-1bf5-4ff0-8bbd-625a69cf9594
ms.tgt_platform: multiple
keywords:
- IADsBackLink 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsBackLink Property Methods
- IADsBackLink.RemoteID
- IADsBackLink.get_RemoteID
- IADsBackLink.put_RemoteID
- IADsBackLink.ObjectName
- IADsBackLink.get_ObjectName
- IADsBackLink.put_ObjectName
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2220fff3a18b0822c0167b387ec10c324d95aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105156"
---
# <a name="iadsbacklink-property-methods"></a><span data-ttu-id="8d86d-105">IADsBackLink 屬性方法</span><span class="sxs-lookup"><span data-stu-id="8d86d-105">IADsBackLink Property Methods</span></span>

<span data-ttu-id="8d86d-106">[**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink)介面的 property 方法會設定下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="8d86d-106">The property method of the [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) interface sets the property described in the following table.</span></span> <span data-ttu-id="8d86d-107">如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="8d86d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="8d86d-108">屬性</span><span class="sxs-lookup"><span data-stu-id="8d86d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="8d86d-109">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="8d86d-109">**ObjectName**</span></span>
<span data-ttu-id="8d86d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8d86d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="8d86d-111">**後置連結** 屬性所附加的物件名稱。</span><span class="sxs-lookup"><span data-stu-id="8d86d-111">The name of an object the **Back Link** attribute is attached to.</span></span>

<dt>

<span data-ttu-id="8d86d-112">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d86d-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8d86d-113">腳本資料類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8d86d-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retval
);
HRESULT put_ObjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d86d-114">**RemoteID**</span><span class="sxs-lookup"><span data-stu-id="8d86d-114">**RemoteID**</span></span>
<span data-ttu-id="8d86d-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8d86d-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="8d86d-116">遠端伺服器的識別碼，需要 **ObjectName** 所指定之物件的外部參考。</span><span class="sxs-lookup"><span data-stu-id="8d86d-116">The identifier of the remote server that requires an external reference of the object specified by **ObjectName**.</span></span>

<dt>

<span data-ttu-id="8d86d-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8d86d-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8d86d-118">編寫資料類型的腳本： **LONG**</span><span class="sxs-lookup"><span data-stu-id="8d86d-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_RemoteID(
  [out] LONG* retVal
);
HRESULT put_RemoteID(
  [in] LONG bstrProtectedAttrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="8d86d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d86d-119">Requirements</span></span>



| <span data-ttu-id="8d86d-120">需求</span><span class="sxs-lookup"><span data-stu-id="8d86d-120">Requirement</span></span> | <span data-ttu-id="8d86d-121">值</span><span class="sxs-lookup"><span data-stu-id="8d86d-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d86d-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d86d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8d86d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d86d-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d86d-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d86d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8d86d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d86d-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d86d-126">標頭</span><span class="sxs-lookup"><span data-stu-id="8d86d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d86d-127"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="8d86d-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="8d86d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8d86d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d86d-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d86d-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="8d86d-130">IID</span><span class="sxs-lookup"><span data-stu-id="8d86d-130">IID</span></span><br/>                      | <span data-ttu-id="8d86d-131">IID \_ IADsBackLink 定義為 FD1302BD-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="8d86d-131">IID\_IADsBackLink is defined as FD1302BD-4080-11D1-A3AC-00C04FB950DC</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="8d86d-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d86d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d86d-133">**IADsBackLink**</span><span class="sxs-lookup"><span data-stu-id="8d86d-133">**IADsBackLink**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsbacklink)
</dt> <dt>

[<span data-ttu-id="8d86d-134">**ADS \_ BACKLINK**</span><span class="sxs-lookup"><span data-stu-id="8d86d-134">**ADS\_BACKLINK**</span></span>](/windows/win32/api/iads/ns-iads-ads_backlink)
</dt> </dl>

 

 





