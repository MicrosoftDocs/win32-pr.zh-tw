---
title: SelectedTaskPane
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 SelectedTaskPane 屬性會指定或抓取目前選取的工作窗格。
ms.assetid: af7b4627-1336-444c-9b4e-5f2e07d9eea7
keywords:
- SelectedTaskPane Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.SelectedTaskPane
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28535e0497362a2153bcaad439425174e9c1bdc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998594"
---
# <a name="externalselectedtaskpane"></a>SelectedTaskPane

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**SelectedTaskPane** 屬性會指定或抓取目前選取的工作窗格。

## <a name="syntax"></a>Syntax

SelectedTaskPane = *servicetask*

## <a name="possible-values"></a>可能的值

這個屬性是讀取/寫入 **字串**。 可能的值為 "ServiceTask1"、"ServiceTask2" 和 "ServiceTask3"。

## <a name="remarks"></a>備註

指定這個屬性的值會反白顯示該窗格的按鈕。 它不會讓指定的工作窗格變成作用中。 當頁面載入時，您應該指定此屬性的值，以設定網頁的目前工作窗格按鈕，以確保正確的工作窗格按鈕處於作用中狀態。

若要讓特定工作窗格成為使用中的工作窗格，請使用 **NavigateTaskPaneURL** 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 10 或更新版本<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型2線上商店的外部物件**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> </dl>

 

 





