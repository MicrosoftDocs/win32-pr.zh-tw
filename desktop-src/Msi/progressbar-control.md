---
description: ProgressBar 控制項會顯示在接收進度訊息時變更長度的橫條圖。 此控制項會訂閱 SetProgress ControlEvent。 它可以訂閱在受監視的動作之後所命名的 ControlEvent。
ms.assetid: 0d366a1b-3c7e-4590-8557-c6a7d1fcd426
title: ProgressBar 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c531a0edcf822c3a4cc75ec6516f1b871e2db6cb7122bb74178d59850710843
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913178"
---
# <a name="progressbar-control"></a>ProgressBar 控制項

ProgressBar 控制項會顯示在接收進度訊息時變更長度的橫條圖。 此控制項會訂閱 [SetProgress](setprogress-controlevent.md) ControlEvent。 它可以訂閱在受監視的動作之後所命名的 ControlEvent。

如需相關資訊，請參閱 [撰寫 ProgressBar 控制項](authoring-a-progressbar-control.md)，以及 [將自訂動作新增至 ProgressBar](adding-custom-actions-to-the-progressbar.md)。

## <a name="control-attributes"></a>控制項屬性

您可以將下列屬性與這個控制項搭配使用。 若要使用事件來變更屬性的值，請將控制項訂閱至 [EventMapping 資料表](eventmapping-table.md) 中的 ControlEvent，並在 [屬性] 資料行中列出屬性的識別碼。 在 [事件] 資料行中輸入 ControlEvent 的識別碼。



| 屬性識別碼                           | 十六進位位                  | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [位置](position-control-attribute.md)     |                                  | 對話方塊中控制項的位置。 將控制項左上角的控制項寬度、高度和座標，輸入控制項 [資料表](control-table.md)的 Width、Height、X 和 Y 資料行中。 使用 [安裝程式單位](installer-units.md) 來表示長度和距離。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [Progress](progress-control-attribute.md)     |                                  | 這個屬性會指定 ProgressBar 的填滿程度。 此屬性是由兩個整數和一個字串所組成。 第一個整數位段是目前的進度刻度數目，而第二個整數位段是預設的進度刻度 (1024) 的最大數目。 第三個欄位是字串，它是正在進行中的動作名稱。 如果目前的進度刻度數目大於最大值，則安裝程式會將它變更為最大值。 這個屬性是由 [SetProgress ControlEvent](setprogress-controlevent.md)設定和變更。 您必須在 [事件] 資料行中輸入 SetProgress，然後在 [屬性] 資料行中輸入進度，以在 [EventMapping 資料表](eventmapping-table.md) 中訂閱此事件的控制項。<br/> |
| [Text](text-control-attribute.md)             |                                  | 控制項所顯示的文字。 若要設定文字字串的字型與字型樣式，請在顯示的字元字串前面加上 { \\ style} 或 {&*style*}。 其中 style 是在 [資料行] 資料表的 [樣式 [表單](textstyle-table.md)] 資料行中所列的識別碼。 如果這兩個都不存在，但 [**DefaultUIFont**](defaultuifont.md) 屬性定義為有效的文字樣式，則會使用該字型。<br/>                                                                                                                                                                                                                                                                                                                                       |
| [Visible](visible-control-attribute.md)       | 0x00000000 0x00000001<br/> | 隱藏的控制項。 可見的控制項。<br/> 在 [控制資料表](control-table.md) 中的 [屬性] 資料行的位字組中包含這個位，讓控制項在建立時顯示或隱藏。<br/> 您也可以使用 [ControlCondition 資料表](controlcondition-table.md)來隱藏或顯示控制項。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [沉沒](sunken-control-attribute.md)         | 0x00000000 0x00000004<br/> | 顯示預設的視覺化樣式。 顯示具有凹陷、立體、外觀的控制項。<br/> 在 [控制項資料表](control-table.md)的 [屬性] 資料行中，將這些位包含在位字中。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [RTLRO](rtlro-control-attribute.md)           | 0x00000000 0x00000020<br/> | 控制項中的文字會以從左至右的讀取順序顯示。 控制項中的文字會以由右至左的讀取順序顯示。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [Progress95](progress95-control-attribute.md) | 0x00000000 0x00010000<br/> | 以連續橫條圖形式繪製的進度列。 繪製成一系列矩形的進度列。<br/> 在 [控制項資料表](control-table.md)的 [屬性] 資料行中，將這些位包含在位字中。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="remarks"></a>備註

您可以使用 CreateWindowEx 函數，從進度 \_ 類別類別建立這個控制項[](/windows/win32/api/winuser/nf-winuser-createwindowexa) 。 它具有 **ws \_ 子** 系和 **ws \_ 群組** 樣式。

 

 
