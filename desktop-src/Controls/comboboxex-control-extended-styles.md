---
title: 'ComboBoxEx 控制項擴充樣式 (CommCtrl .h) '
description: 支援本節中所列的延伸樣式，以及大部分標準的下拉式方塊控制項樣式。
ms.assetid: 4741ac5e-1c46-4fd3-9174-b4ceb479261f
topic_type:
- apiref
api_name:
- CBES_EX_CASESENSITIVE
- CBES_EX_NOEDITIMAGE
- CBES_EX_NOEDITIMAGEINDENT
- CBES_EX_NOSIZELIMIT
- CBES_EX_PATHWORDBREAKPROC
- CBES_EX_TEXTENDELLIPSIS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71dc92264dbd1bd2f5a4b1136d9a6138e1fcffa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992577"
---
# <a name="comboboxex-control-extended-styles"></a>ComboBoxEx 控制項擴充樣式

支援本節中所列的延伸樣式，以及大部分標準的下拉式方塊控制項樣式。



| 常數                                                                                                                                                                                           | 描述                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <dt>**CBES \_ EX \_ CASESENSITIVE**</dt> </dl>             | 清單中的 **BSTR** 搜尋會區分大小寫。 這包括在編輯方塊中輸入文字的結果，以及 CB FINDSTRINGEXACT 訊息中的搜尋結果 \_ 。<br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <dt>**CBES \_ EX \_ NOEDITIMAGE**</dt> </dl>                   | 編輯方塊和下拉式清單不會顯示專案影像。 <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <dt>**CBES \_ EX \_ NOEDITIMAGEINDENT**</dt> </dl> | 編輯方塊和下拉式清單不會顯示專案影像。 <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <dt>**CBES \_ EX \_ NOSIZELIMIT**</dt> </dl>                   | 允許 ComboBoxEx 控制項的垂直大小小於其包含的下拉式方塊控制項。 如果 ComboBoxEx 的大小小於下拉式方塊，則會裁剪下拉式方塊。 <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <dt>**CBES \_ EX \_ PATHWORDBREAKPROC**</dt> </dl> | 僅 Windows NT。 編輯方塊會使用斜線 (/) 、反斜線 (\) 和句號 (. ) 字元作為文字分隔符號。 這可讓鍵盤快速鍵在路徑名稱和 Url 中有效地移動單字游標。<br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <dt>**CBES \_ EX \_ TEXTENDELLIPSIS**</dt> </dl>       | **Windows Vista （含）以後版本。** 當編輯方塊為唯讀時，會導致下拉式清單和編輯方塊中的專案 () 要以省略號 ( "... ) " 來截斷，而不是只由控制項邊緣裁剪。 當控制項必須設定為固定寬度，但清單中的專案可能很長時，這非常有用。<br/> |



## <a name="remarks"></a>備註

您可以使用 [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) 和 [**CBEM \_ GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) 訊息來設定和取出 combobox 擴充樣式。

> [!Note]  
> 如果您嘗試為以 [**CBS \_ 簡單**](combo-box-styles.md) 樣式建立的 ComboBoxEx 控制項設定擴充樣式，則可能無法正確地重新繪製。 **CBS \_ 簡單** 樣式也無法與 CBES \_ EX \_ PATHWORDBREAKPROC 擴充樣式一起正常運作。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

 





