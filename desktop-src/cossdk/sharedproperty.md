---
description: 設定或抓取共用屬性的值。
ms.assetid: 19ed8d50-3ac1-408e-9f25-09f284d025f1
title: 'SharedProperty 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedProperty
api_type:
- COM
ms.openlocfilehash: a7a7857ad280ad722601bdced6c25d04b03dc0b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110553"
---
# <a name="sharedproperty-class"></a>SharedProperty 類別

設定或抓取共用屬性的值。

如需有關在 COM + 中使用共用屬性管理員的一般資訊，請參閱 [Com + 共用屬性管理員](com--shared-property-manager.md)。

## <a name="when-to-implement"></a>執行時機

這個類別是由 COM + 所執行。



| 需求 | 值 |
|------------|--------------------------------------------|
| 介面 | [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) |



 

## <a name="when-to-use"></a>使用時機

您可以使用這個類別來存取 [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)的方法。

## <a name="remarks"></a>備註

您可以使用 [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)的 [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty)或 [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition)方法來建立 **SharedProperty** 物件。

若要從 Microsoft Visual Basic 使用這個類別，請新增 COM + 服務類型程式庫的參考。 SharedProperty 物件是藉由呼叫 [**SharedPropertyGroup**](sharedpropertygroup.md)物件的 [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty)或 [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition)方法來建立。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>ComSvcs。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)
</dt> <dt>

[**SharedPropertyGroup**](sharedpropertygroup.md)
</dt> <dt>

[**SharedPropertyGroupManager**](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




