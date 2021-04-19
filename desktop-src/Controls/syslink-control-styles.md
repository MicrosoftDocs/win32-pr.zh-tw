---
title: 'SysLink 控制項樣式 (CommCtrl) '
description: 建立 SysLink 控制項時，會使用下列樣式常數。
ms.assetid: e9a8c99b-86c4-4385-ae20-b2b78a07b491
topic_type:
- apiref
api_name:
- LWS_TRANSPARENT
- LWS_IGNORERETURN
- LWS_NOPREFIX
- LWS_USEVISUALSTYLE
- LWS_USECUSTOMTEXT
- LWS_RIGHT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 490a64a21ec81c1c91cc34ec8bebd2995476db4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977698"
---
# <a name="syslink-control-styles"></a>SysLink 控制項樣式

建立 SysLink 控制項時，會使用下列樣式常數。



| 常數                                                                                                                                                                        | 描述                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LWS_TRANSPARENT"></span><span id="lws_transparent"></span><dl> <dt>**LWS \_ 透明**</dt> </dl>             | 背景混合模式是透明的。 <br/>                                                                                                                       |
| <span id="LWS_IGNORERETURN_"></span><span id="lws_ignorereturn_"></span><dl> <dt>**LWS \_IGNORERETURN**</dt> </dl>       | 當連結具有鍵盤焦點，且使用者按下 Enter 鍵時，控制項會忽略按鍵，並將其傳遞至主控制項對話方塊。<br/>                        |
| <span id="LWS_NOPREFIX"></span><span id="lws_noprefix"></span><dl> <dt>**LWS \_ NOPREFIX**</dt> </dl>                      | **Windows Vista**。 如果文字包含連字號，則會被視為常值字元，而不是快速鍵的前置詞。<br/>                           |
| <span id="LWS_USEVISUALSTYLE_"></span><span id="lws_usevisualstyle_"></span><dl> <dt>**LWS \_USEVISUALSTYLE**</dt> </dl> | **Windows Vista**。 連結會以目前的視覺效果樣式顯示。<br/>                                                                                          |
| <span id="LWS_USECUSTOMTEXT"></span><span id="lws_usecustomtext"></span><dl> <dt>**LWS \_ USECUSTOMTEXT**</dt> </dl>       | **Windows Vista**。 當繪製控制項時，會傳送 [NM \_ CUSTOMTEXT](nm-customtext.md) 通知，讓應用程式可以動態提供文字。<br/> |
| <span id="LWS_RIGHT"></span><span id="lws_right"></span><dl> <dt>**LWS \_ RIGHT**</dt> </dl>                               | **Windows Vista**。 文字是靠右對齊。<br/>                                                                                                                |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

 





