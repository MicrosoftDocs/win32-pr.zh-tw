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
ms.openlocfilehash: 06d057f1a67fb6e18be0b0ed7e3fc21e1276a4068017c44c4e28d125fe271046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181143"
---
# <a name="adsi-attribute-modification-types"></a>ADSI 屬性修改類型

下列常數與 [**ADS \_ ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)結構的 **dwControlCode** 成員搭配使用，以指定使用 [**IDirectoryObject：： SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)方法修改屬性時所要執行的作業類型。 如需有關使用這些值的詳細資訊，請參閱使用 [ADSI 修改屬性](modifying-attributes-with-adsi.md)。

<dl> <dt>

<span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**ADS \_ ATTR \_ CLEAR**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



使所有屬性值從物件中移除。


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**ADS \_ ATTR \_ 更新**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



會更新指定的屬性值。


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**ADS \_ ATTR \_ 附加**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



使指定的屬性值附加至現有的屬性值。


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**ADS \_ ATTR \_ 刪除**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



導致從物件中移除指定的屬性值。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

這些常數的目的是要搭配 [**IDirectoryObject：： SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)方法中的 [**ADS \_ ATTR \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)結構使用。 這些常數不應與 [**ADS \_ 屬性作業 \_ \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) 列舉的成員混淆，其目的是要搭配 [**IADs：:P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) 方法使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                          |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                    |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ADS \_ ATTR \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)
</dt> <dt>

[**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)
</dt> <dt>

[使用 ADSI 修改屬性](modifying-attributes-with-adsi.md)
</dt> </dl>

 

 





