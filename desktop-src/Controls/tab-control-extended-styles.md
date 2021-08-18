---
title: '索引標籤控制項擴充樣式 (CommCtrl .h) '
description: 索引標籤控制項現在支援擴充樣式。 這些樣式是使用 TCM \_ GETEXTENDEDSTYLE 和 tcm \_ SETEXTENDEDSTYLE 訊息來操作，不應該與傳遞給 CreateWindowEx 的延伸視窗樣式混淆。
ms.assetid: 24294037-598c-4fcd-8a7c-8647ccfb1d81
topic_type:
- apiref
api_name:
- TCS_EX_FLATSEPARATORS
- TCS_EX_REGISTERDROP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd057a1ced7c2f594b9e4a7a2c67abe963caa270e770eebecd2f36b50f309aef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769918"
---
# <a name="tab-control-extended-styles"></a>索引標籤控制項擴充樣式

索引標籤控制項現在支援擴充樣式。 這些樣式是使用 [**tcm \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) 和 [**tcm \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) 訊息來操作，不應該與傳遞給 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的延伸視窗樣式混淆。



| 常數                                                                                                                                                                               | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <dt>**TCS \_ EX \_ FLATSEPARATORS**</dt> </dl> | [版本 4.71](common-control-versions.md)。 索引標籤控制項將會在索引標籤專案之間繪製分隔符號。 此擴充樣式只會影響具有 [TCS] [**\_ 按鈕**](tab-control-styles.md) 和 [**TCS \_ FLATBUTTONS**](tab-control-styles.md) 樣式的索引標籤控制項。 根據預設，建立具有 **TCS \_ FLATBUTTONS** 樣式的索引標籤控制項，會設定此延伸樣式。 如果您不需要分隔符號，則應該在建立控制項之後移除此延伸樣式。<br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <dt>**TCS \_ EX \_ REGISTERDROP**</dt> </dl>       | [版本 4.71](common-control-versions.md)。 當物件拖曳至控制項中的索引標籤專案上方時，此索引標籤控制項會產生 [TCN 的 \_ GETOBJECT](tcn-getobject.md) 通知碼，以要求卸載目標物件。 應用程式必須先呼叫 [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) 或 [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) ，才能設定此樣式。 <br/>                                                                                                                                               |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

