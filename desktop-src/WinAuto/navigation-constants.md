---
title: '流覽常數 (Oleacc .h) '
description: 本主題說明 oleacc 中定義的常數值，指出當用戶端使用 IAccessible accNavigate 在相同容器內的某個使用者介面專案之間流覽時，所觀察到的空間 (向上、向下、左方和右邊) 或邏輯 (第一個子系、最後一個、下一個和先前的) 方向。
ms.assetid: 5859a7a3-bcd3-443e-8ff0-4952f4639517
topic_type:
- apiref
api_name:
- NAVDIR_DOWN
- NAVDIR_FIRSTCHILD
- NAVDIR_LASTCHILD
- NAVDIR_LEFT
- NAVDIR_NEXT
- NAVDIR_PREVIOUS
- NAVDIR_RIGHT
- NAVDIR_UP
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8de5f4eaa3fc7fb24583e49bdd14acb9633b2bd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983015"
---
# <a name="navigation-constants"></a>導覽常數

本主題說明在 oleacc 中定義的常數值，指出 *空間* (向上、向下、向左和向右) 或 *邏輯* (第一個子系、最後一個、下一個，以及當用戶端使用 [**IAccessible：： accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) 從某個使用者介面專案流覽至相同容器內的另一個使用者介面專案時所觀察到的) 方向。 如需詳細資訊，請參閱 [物件導覽屬性和方法](object-navigation-properties-and-methods.md)。

Microsoft Active Accessibility 的導覽常數如下所示：



| 常數                                                                                                                                                                  | 描述                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NAVDIR_DOWN"></span><span id="navdir_down"></span><dl> <dt>**\_向下 NAVDIR**</dt> </dl>                   | 流覽至位於起始物件下方的同級物件。<br/>                                                                  |
| <span id="NAVDIR_FIRSTCHILD"></span><span id="navdir_firstchild"></span><dl> <dt>**NAVDIR \_ FIRSTCHILD**</dt> </dl> | 流覽至這個物件的第一個子系。 使用這個旗標時， *varStart* 參數的 **lVal** 成員必須是 CHILDID \_ SELF。<br/> |
| <span id="NAVDIR_LASTCHILD"></span><span id="navdir_lastchild"></span><dl> <dt>**NAVDIR \_ LASTCHILD**</dt> </dl>    | 流覽至這個物件的最後一個子系。 使用這個旗標時， *varStart* 參數的 **lVal** 成員必須是 CHILDID \_ SELF。<br/>    |
| <span id="NAVDIR_LEFT"></span><span id="navdir_left"></span><dl> <dt>**\_左 NAVDIR**</dt> </dl>                   | 流覽至位於起始物件左邊的同級物件。<br/>                                                                 |
| <span id="NAVDIR_NEXT"></span><span id="navdir_next"></span><dl> <dt>**NAVDIR \_ 下一步**</dt> </dl>                   | 流覽至下一個邏輯物件;一般而言，它是起始物件的同級。<br/>                                                    |
| <span id="NAVDIR_PREVIOUS"></span><span id="navdir_previous"></span><dl> <dt>**NAVDIR \_ 上一步**</dt> </dl>       | 流覽至先前的邏輯物件;一般而言，它是起始物件的同級。<br/>                                                |
| <span id="NAVDIR_RIGHT"></span><span id="navdir_right"></span><dl> <dt>**NAVDIR \_ RIGHT**</dt> </dl>                | 流覽至位於起始物件右邊的同級物件。<br/>                                                        |
| <span id="NAVDIR_UP"></span><span id="navdir_up"></span><dl> <dt>**\_向上 NAVDIR**</dt> </dl>                         | 流覽至位於起始物件上方的同級物件。<br/>                                                                  |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Oleacc。h</dt> </dl> |



 

 





