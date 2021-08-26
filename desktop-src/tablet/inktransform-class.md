---
description: 代表3x3 矩陣，後者又表示仿射轉換。
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: 'InkTransform 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkTransform
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 4bdc93e2c80f1a7ef4a8eacf1a58288c008e1354cda702e492deb2990e8938d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938658"
---
# <a name="inktransform-class"></a>InkTransform 類別

代表3x3 矩陣，後者又表示仿射轉換。

**InkTransform** 具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**InkTransform** 類別有這些方法。



| 方法                                                  | 描述                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**GetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | 將 **InkTransform** 抓取為6個浮點數。<br/>                                                                      |
| [**反映**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | 以水準或垂直方向反映轉換。<br/>                                          |
| [**重設**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | 將轉換重設為其原始狀態。<br/>                                                                      |
| [**旋轉**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | 以度為單位的角度旋轉轉換，並選擇性地指定旋轉的中心點。<br/> |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | 依 X 和 Y 因數調整轉換。<br/>                                                                         |
| [**SetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | 使用6個浮點數修改 **InkTransform** 。<br/>                                                                    |
| [**剪切**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | 套用具有指定水準和垂直因數的切變。<br/>                                              |
| [**翻譯**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | 依指定的水準和垂直元件移動轉換。<br/>                                         |



 

### <a name="properties"></a>屬性

**InkTransform** 類別具有這些屬性。



| 屬性                                     | 存取類型           | 描述                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**資料**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | 讀取/寫入<br/> | 取得或設定 WIN32 XFORM 結構的自動化版本。<br/>                            |
| [**eDx**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | 讀取/寫入<br/> | 取得或設定指定第三列第一個資料行中之元素的實數。<br/>   |
| [**艾迪**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | 讀取/寫入<br/> | 取得或設定指定第三列第二個數據行中之元素的實數。<br/>  |
| [**eM11**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | 讀取/寫入<br/> | 取得或設定指定第一個資料列第一個資料行中之元素的實數。<br/>   |
| [**eM12**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | 讀取/寫入<br/> | 取得或設定指定第一個資料列第二個數據行中之元素的實數。<br/>  |
| [**eM21**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | 讀取/寫入<br/> | 取得或設定指定第二個數據列第一個資料行中之元素的實數。<br/>  |
| [**eM22**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | 讀取/寫入<br/> | 取得或設定指定第二個數據列第二個數據行中之元素的實數。<br/> |



 

## <a name="remarks"></a>備註

此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。

此物件在3x3 矩陣中只會儲存九個數字的六個，因為表示仿射轉換的所有3x3 矩陣都有相同的第三個數據行 (0、0、1) 。 接著，這個物件會用來描述轉換作業，例如移動、剪下、縮放或旋轉 [**InkRenderer**](inkrenderer-class.md) 物件、 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件或 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合。

> [!Note]  
> **InkTransform** 物件與 [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform)結構相互關聯。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

