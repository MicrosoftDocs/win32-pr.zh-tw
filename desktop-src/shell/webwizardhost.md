---
description: 公開方法，這些方法可讓您在 wizard 擴充功能中裝載的 HTML 網頁與 wizard 進行通訊。
ms.assetid: 7b3690dc-2007-43a0-80a3-4a68e3c8464d
title: 'WebWizardHost 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: c5bcf40a77c2f464d5277ac4823ed74a3f3c2bdd6a2114d2431684cc8b319f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967746"
---
# <a name="webwizardhost-object"></a>WebWizardHost 物件

公開方法，這些方法可讓您在 wizard 擴充功能中裝載的 HTML 網頁與 wizard 進行通訊。

## <a name="members"></a>成員

**WebWizardHost** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**WebWizardHost** 物件有這些方法。



| 方法                                                      | 描述                                                                                                                                                                        |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取消**](iwebwizardhost-cancel.md)                     | 模擬 [ **取消** ] 按鈕的按一下。<br/>                                                                                                                                    |
| [**FinalBack**](iwebwizardhost-finalback.md)               | 在主控伺服器端 HTML 頁面的頁面上，直接流覽至用戶端頁面。<br/>                                                                    |
| [**FinalNext**](iwebwizardhost-finalnext.md)               | 流覽至裝載伺服器端 HTML 頁面的頁面下的用戶端 wizard 頁面，或者，如果沒有進一步的用戶端頁面，則完成 wizard。<br/> |
| [**SetHeaderText**](iwebwizardhost-setheadertext.md)       | 設定出現在 wizard 標頭中的標題和副標題。 一般而言，用戶端會將標頭顯示在 HTML 和標題列下方。<br/>                    |
| [**SetWizardButtons**](iwebwizardhost-setwizardbuttons.md) | 更新用戶端的 wizard 框架中的 [ **上一頁**]、 **[下一頁**] 和 **[完成]** 按鈕。<br/>                                                                                    |



 

### <a name="properties"></a>屬性

**WebWizardHost** 物件具有這些屬性。



| 屬性                                               | 存取類型           | 描述                                              |
|:-------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [**標題**](iwebwizardhost-caption.md)<br/>   | 讀取/寫入<br/> | 未實作。<br/>                              |
| [**屬性**](iwebwizardhost-property.md)<br/> | 讀取/寫入<br/> | 設定或抓取屬性的目前值。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl> |
| IID<br/>                      | CLSID \_ WebWizardHost<br/>                                                        |



 

 




