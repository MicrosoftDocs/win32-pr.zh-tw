---
description: 表示對矩形的存取。
ms.assetid: 78e6c29c-0f43-46a5-9d30-948de5f369c8
title: 'InkRectangle 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRectangle
- InkRectangle.IInkRectangle
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: d643696fe19523bac93ebca71cf885cd93b8570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988475"
---
# <a name="inkrectangle-class"></a>InkRectangle 類別

表示對矩形的存取。

**InkRectangle** 具有下列類型的成員：

-   [介面](#interfaces)
-   [方法](#methods)
-   [屬性](#properties)

### <a name="interfaces"></a>介面

**InkRectangle** 類別會定義這些介面。



| 介面         | 描述                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **IInkRectangle** | 這個物件會實 **IInkRectangle** COM 介面。<br/> |



 

### <a name="methods"></a>方法

**InkRectangle** 類別有這些方法。



| 方法                                            | 描述                                                                        |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**GetRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-getrectangle) | 在單一呼叫中抓取 **InkRectangle** 物件的元素。<br/> |
| [**SetRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-setrectangle) | 在單一呼叫中修改 **InkRectangle** 物件的元素。<br/>  |



 

### <a name="properties"></a>屬性

**InkRectangle** 類別具有這些屬性。



| 屬性                                         | 存取類型           | Description                                                        |
|:-------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**下層**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom)<br/> | 讀取/寫入<br/> | 取得或設定矩形的底部位置。<br/>      |
| [**資料**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_data)<br/>     | 讀取/寫入<br/> | 取得或設定只有)  (c + + 的矩形結構存取權。<br/> |
| [**離開**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left)<br/>     | 讀取/寫入<br/> | 取得或設定矩形的左邊位置。<br/>        |
| [**對**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right)<br/>   | 讀取/寫入<br/> | 取得或設定矩形的右邊位置。<br/>       |
| [**返回頁首**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top)<br/>       | 讀取/寫入<br/> | 取得或設定矩形的上方位置。<br/>         |



 

## <a name="remarks"></a>備註

> [!Note]  
> 如果某個點位於 [**左側**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left)或 [**頂端**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top)，或是在全部四邊內，就會在 **InkRectangle** 中。 [**右邊**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right)或 [**下**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom)一端的點會被視為矩形外部。

 

您可以藉由呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化此物件。

> [!Note]  
> 如果 **InkRectangle** 大於 \_ (2 ^ 31-1 個維度中) 的最大值，則無法使用。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

