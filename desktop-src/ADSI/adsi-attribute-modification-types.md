---
title: 'ADSI 屬性修改類型 (Iads .h) '
description: 與 ADS ATTR INFO 結構的 dwControlCode 成員搭配使用 \_ \_ ，以指定使用 IDirectoryObject SetObjectAttributes 方法修改屬性時所要執行的作業類型。
ms.assetid: e9a454c8-e067-4730-97f4-85c4f5889e05
ms.tgt_platform: multiple
keywords:
- 屬性修改類型 ADSI
topic_type:
- apiref
api_name:
- ADS_ATTR_CLEAR
- ADS_ATTR_UPDATE
- ADS_ATTR_APPEND
- ADS_ATTR_DELETE
api_location:
- Iads.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a739241fd52a7d45d58a1b36bb7de838234d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024808"
---
# <a name="adsi-attribute-modification-types"></a><span data-ttu-id="20cef-104">ADSI 屬性修改類型</span><span class="sxs-lookup"><span data-stu-id="20cef-104">ADSI Attribute Modification Types</span></span>

<span data-ttu-id="20cef-105">下列常數與 [**ADS \_ ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)結構的 **dwControlCode** 成員搭配使用，以指定使用 [**IDirectoryObject：： SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)方法修改屬性時所要執行的作業類型。</span><span class="sxs-lookup"><span data-stu-id="20cef-105">The following constants are used with the **dwControlCode** member of [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure to specify the type of operation to be performed when an attribute is modified with the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span> <span data-ttu-id="20cef-106">如需有關使用這些值的詳細資訊，請參閱使用 [ADSI 修改屬性](modifying-attributes-with-adsi.md)。</span><span class="sxs-lookup"><span data-stu-id="20cef-106">For more information about using these values, see [Modifying Attributes with ADSI](modifying-attributes-with-adsi.md).</span></span>

<dl> <dt>

<span data-ttu-id="20cef-107"><span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**ADS \_ ATTR \_ CLEAR**</span><span class="sxs-lookup"><span data-stu-id="20cef-107"><span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**ADS\_ATTR\_CLEAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20cef-108">1</span><span class="sxs-lookup"><span data-stu-id="20cef-108">1</span></span>
</dt> <dt>



<span data-ttu-id="20cef-109">使所有屬性值從物件中移除。</span><span class="sxs-lookup"><span data-stu-id="20cef-109">Causes all attribute values to be removed from an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20cef-110"><span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**ADS \_ ATTR \_ 更新**</span><span class="sxs-lookup"><span data-stu-id="20cef-110"><span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**ADS\_ATTR\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20cef-111">2</span><span class="sxs-lookup"><span data-stu-id="20cef-111">2</span></span>
</dt> <dt>



<span data-ttu-id="20cef-112">會更新指定的屬性值。</span><span class="sxs-lookup"><span data-stu-id="20cef-112">Causes the specified attribute values to be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20cef-113"><span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**ADS \_ ATTR \_ 附加**</span><span class="sxs-lookup"><span data-stu-id="20cef-113"><span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**ADS\_ATTR\_APPEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20cef-114">3</span><span class="sxs-lookup"><span data-stu-id="20cef-114">3</span></span>
</dt> <dt>



<span data-ttu-id="20cef-115">使指定的屬性值附加至現有的屬性值。</span><span class="sxs-lookup"><span data-stu-id="20cef-115">Causes the specified attribute values to be appended to the existing attribute values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20cef-116"><span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**ADS \_ ATTR \_ 刪除**</span><span class="sxs-lookup"><span data-stu-id="20cef-116"><span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**ADS\_ATTR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20cef-117">4</span><span class="sxs-lookup"><span data-stu-id="20cef-117">4</span></span>
</dt> <dt>



<span data-ttu-id="20cef-118">導致從物件中移除指定的屬性值。</span><span class="sxs-lookup"><span data-stu-id="20cef-118">Causes the specified attribute values to be removed from an object.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20cef-119">備註</span><span class="sxs-lookup"><span data-stu-id="20cef-119">Remarks</span></span>

<span data-ttu-id="20cef-120">這些常數的目的是要搭配 [**IDirectoryObject：： SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)方法中的 [**ADS \_ ATTR \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)結構使用。</span><span class="sxs-lookup"><span data-stu-id="20cef-120">These constants are intended to be used with the [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure in the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span> <span data-ttu-id="20cef-121">這些常數不應與 [**ADS \_ 屬性作業 \_ \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) 列舉的成員混淆，其目的是要搭配 [**IADs：:P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) 方法使用。</span><span class="sxs-lookup"><span data-stu-id="20cef-121">These constants should not be confused with members of the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration, which are intended to be used with the [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="20cef-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="20cef-122">Requirements</span></span>



| <span data-ttu-id="20cef-123">需求</span><span class="sxs-lookup"><span data-stu-id="20cef-123">Requirement</span></span> | <span data-ttu-id="20cef-124">值</span><span class="sxs-lookup"><span data-stu-id="20cef-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="20cef-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20cef-125">Minimum supported client</span></span><br/> | <span data-ttu-id="20cef-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20cef-126">Windows Vista</span></span><br/>                                                          |
| <span data-ttu-id="20cef-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20cef-127">Minimum supported server</span></span><br/> | <span data-ttu-id="20cef-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20cef-128">Windows Server 2008</span></span><br/>                                                    |
| <span data-ttu-id="20cef-129">標頭</span><span class="sxs-lookup"><span data-stu-id="20cef-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="20cef-130"><dt>Iads。h</dt></span><span class="sxs-lookup"><span data-stu-id="20cef-130"><dt>Iads.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20cef-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20cef-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20cef-132">**ADS \_ ATTR \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="20cef-132">**ADS\_ATTR\_INFO**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_attr_info)
</dt> <dt>

[<span data-ttu-id="20cef-133">**IDirectoryObject::SetObjectAttributes**</span><span class="sxs-lookup"><span data-stu-id="20cef-133">**IDirectoryObject::SetObjectAttributes**</span></span>](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)
</dt> <dt>

[<span data-ttu-id="20cef-134">使用 ADSI 修改屬性</span><span class="sxs-lookup"><span data-stu-id="20cef-134">Modifying Attributes with ADSI</span></span>](modifying-attributes-with-adsi.md)
</dt> </dl>

 

 





