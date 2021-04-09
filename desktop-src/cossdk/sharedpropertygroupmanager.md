---
description: 建立共用屬性群組，並取得現有共用屬性群組的存取權。
ms.assetid: 4ba05806-afda-4926-8ca4-abbf15ed8278
title: 'SharedPropertyGroupManager 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroupManager
api_type:
- COM
ms.openlocfilehash: 680c5caef996d329e18192193f30841f61f02f27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847220"
---
# <a name="sharedpropertygroupmanager-class"></a>SharedPropertyGroupManager 類別

建立共用屬性群組，並取得現有共用屬性群組的存取權。

如需有關在 COM + 中使用共用屬性管理員的詳細資訊，請參閱 [Com + 共用屬性管理員](com--shared-property-manager.md)。

## <a name="when-to-implement"></a>執行時機

這個類別是由 COM + 所執行。



| 需求 | 值 |
|------------|--------------------------------------------------------------------|
| CLSID      | CLSID \_ SharedPropertyGroupManager                                  |
| ProgID     | L "MTxSpm. SharedPropertyGroupManager"                               |
| 介面 | [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) |



 

## <a name="when-to-use"></a>使用時機

您可以使用這個類別來存取 [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)的方法。

## <a name="remarks"></a>備註

若要建立這個物件，請呼叫 [**IObjectCoNtext：： CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)。

若要從 Microsoft Visual Basic 使用這個類別，請新增 COM + 服務類型程式庫的參考。 您可以使用 "COMSVCSLib. SharedPropertyGroupManager" 將 SharedPropertyGroupManager 物件宣告為類別名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>ComSvcs。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[**SharedProperty**](sharedproperty.md)
</dt> <dt>

[**SharedPropertyGroup**](sharedpropertygroup.md)
</dt> </dl>

 

 




