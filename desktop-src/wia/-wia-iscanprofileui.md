---
description: IScanProfileUI 介面可讓應用程式顯示對話方塊，讓使用者可以建立、修改和刪除掃描設定檔。
ms.assetid: d0c7edcc-00d8-49b2-a0f7-fe4bbba90bfb
title: 'IScanProfileUI 介面 (Scanprofileui .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: 9afc030c485b1c4a873416c22217ce159601aad5e619f16ff799dcc68d5375e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706338"
---
# <a name="iscanprofileui-interface"></a>IScanProfileUI 介面

**IScanProfileUI** 介面可讓應用程式顯示對話方塊，讓使用者可以建立、修改和刪除掃描設定檔。

## <a name="members"></a>成員

**IScanProfileUI** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IScanProfileUI** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IScanProfileUI** 介面具有這些方法。



| 方法                                                             | 描述                                                                                      |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) | 顯示對話方塊，讓使用者可以建立、修改和刪除掃描設定檔。<br/> |



 

## <a name="remarks"></a>備註

對話方塊為強制回應;在對話方塊關閉之前，使用者無法切換至父視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Scanprofileui。h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Scanprofiles .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[掃描設定檔架構](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
